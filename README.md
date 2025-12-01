<html lang="en"><head>
    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <title>Home | Homicide</title>
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    
    <meta name="title" content="Homicide">
    <meta name="description" content="Homicide is a document sharing and publishing website for text-based information such as dox, code-snippets and other stuff.">

    <meta property="og:title" content="Homicide">
    <meta property="og:description" content="Homicide is a document sharing and publishing website for text-based information such as dox, code-snippets and other stuff.">
    <meta property="og:site_name" content="Homicide">
    <meta property="og:type" content="website">
    <meta property="og:url" content="/">
    <meta property="twitter:title" content="Homicide">
    <meta property="twitter:description" content="Homicide is a document sharing and publishing website for text-based information such as dox, code-snippets and other stuff.">
    <meta name="keywords" content="Homicide, Homicide, Vilebin, vilebin, Darkbin, darkbin, даркбин, вилебин, вил, гостбин, doxbin, доксбин, dox, doxed, ghost, гост">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&amp;display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
<style>
    .search-container {
        text-align: center;
        margin: 10px 0 0 0;
    }
    .search-label {
        color: #888888;
        font-weight: bold;
        display: block;
        margin-bottom: 5px;
        font-size: 14px;
    }
    .search-form {
        display: flex;
        justify-content: center;
        gap: 5px;
    }
    .search-box {
        background: #282828;
        border: none;
        outline: none;
        color: white;
        padding: 5px 10px;
        width: 240px;
        height: 32px;
        box-sizing: border-box;
    }
    .search-box::placeholder {
        color: #878787;
    }
    .search-box:focus {
        outline: none;
    }
    .search-button {
        background: #282828;
        color: white;
        border: none;
        padding: 5px 15px;
        cursor: pointer;
        height: 32px;
        box-sizing: border-box;
        font-size: 13px;
    }
    .pagination {
        text-align: center;
        margin: 10px 0;
        color: white;
        display: inline-flex;
        justify-content: center;
        position: relative;
        left: 50%;
        transform: translateX(-50%);
        font-size: 13px;
    }
    .pagination a {
        color: #FFFFFF;
        text-decoration: none;
        padding: 3px 8px;
        min-width: 15px;
        display: inline-block;
        transition: all 0.2s ease;
        border: 1px solid #878787;
        margin-left: -1px;
    }
    .pagination a:first-child {
        border-radius: 3px 0 0 3px;
        margin-left: 0;
    }
    .pagination a:last-child {
        border-radius: 0 3px 3px 0;
    }
    .pagination a:hover {
        color: white;
    }
    .pagination a.active {
        color: white;
        background: #181818;
        border: 1px solid #878787;
        position: relative;
    }
    .pinned-pastes {
        width: 75%;
        max-width: 1100px;
        margin: 10px auto 25px;
        color: white;
    }
    .pinned-pastes h2 {
        color: white;
        margin: 10px 0;
        padding: 0;
        font-weight: normal;
        font-size: 16px;
    }
    .pinned-pastes table {
        width: 100%;
        border-collapse: collapse;
        background: #080808;
        font-size: 14px;
    }
    .pinned-pastes th {
        padding: 8px;
        text-align: left;
        background: #181818;
        font-weight: bold;
        border: none;
        border-bottom: 1px solid #333;
    }
    .pinned-pastes th:not(:first-child) {
        text-align: center;
    }
    .pinned-pastes td {
        padding: 9px;
        border: none;
        border-bottom: 1px solid #333;
    }
    .pinned-pastes td:not(:first-child) {
        text-align: center;
    }
    .pinned-pastes tr {
        background: #080808;
    }
    .pinned-pastes tr[data-highlight] {
        background: attr(data-highlight);
    }
    .pinned-pastes a {
        color: inherit;
        text-decoration: none;
    }
    .pinned-pastes a:hover {
        text-decoration: underline;
    }
    .all-pastes {
        width: 75%;
        max-width: 1100px;
        margin: 0 auto 20px;
        color: white;
    }
    .all-pastes table {
        width: 100%;
        border-collapse: collapse;
        font-size: 14px;
    }
    .all-pastes th {
        padding: 8px;
        text-align: left;
        background: #181818;
        font-weight: bold;
        border: none;
        border-bottom: 1px solid #333;
    }
    .all-pastes th:not(:first-child) {
        text-align: center;
    }
    .all-pastes td {
        padding: 9px;
        border: none;
        border-bottom: 1px solid #333;
    }
    .all-pastes td:not(:first-child) {
        text-align: center;
    }
    .all-pastes tr {
        background: #181818;
    }
    .all-pastes tr:nth-child(even) {
        background: #080808;
    }
    .all-pastes a {
        color: inherit;
        text-decoration: none;
    }
    .all-pastes a:hover {
        text-decoration: underline;
    }
    .pinned-pastes td:first-child,
    .pinned-pastes th:first-child,
    .all-pastes td:first-child,
    .all-pastes th:first-child {
        width: 35%;
    }
    .pinned-pastes td:nth-child(2),
    .pinned-pastes th:nth-child(2),
    .all-pastes td:nth-child(2),
    .all-pastes th:nth-child(2) {
        width: 10%;
    }
    .pinned-pastes td:nth-child(3),
    .pinned-pastes th:nth-child(3),
    .all-pastes td:nth-child(3),
    .all-pastes th:nth-child(3) {
        width: 10%;
    }
    .pinned-pastes td:nth-child(4),
    .pinned-pastes th:nth-child(4),
    .all-pastes td:nth-child(4),
    .all-pastes th:nth-child(4) {
        width: 20%;
    }
    .pinned-pastes td:nth-child(5),
    .pinned-pastes th:nth-child(5),
    .all-pastes td:nth-child(5),
    .all-pastes th:nth-child(5) {
        width: 15%;
    }
    .pinned-pastes td:nth-child(6),
    .pinned-pastes th:nth-child(6),
    .all-pastes td:nth-child(6),
    .all-pastes th:nth-child(6) {
        width: 10%;
        color: #ff0000;
    }
    .showing-text {
        color: #888888;
        text-align: center;
        font-size: 14px;
        margin: 10px 0;
    }
    .showing-text span {
        color: #666;
    }
    .logo-container {
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    .logo-container img {
        max-width: 300px;
        height: auto;
    }
    @media screen and (max-width: 480px) {
        .logo-container img {
            max-width: 200px;
        }
    }
    .announcements {
        text-align: center;
        margin: 10px 0;
    }
    .announcement {
        margin: 10px 0;
        font-size: 17px;
        font-weight: bold;
    }
    @media screen and (max-width: 1024px) {
        .pinned-pastes {
            width: 90%;
        }
        .all-pastes {
            width: 90%;
        }
    }
    @media screen and (max-width: 768px) {
        .pinned-pastes {
            width: 95%;
        }
        .pinned-pastes table {
            font-size: 13px;
        }
        .all-pastes {
            width: 95%;
        }
        .all-pastes table {
            font-size: 13px;
        }
        .pinned-pastes td:nth-child(2),
        .pinned-pastes th:nth-child(2),
        .all-pastes td:nth-child(2),
        .all-pastes th:nth-child(2),
        .pinned-pastes td:nth-child(3),
        .pinned-pastes th:nth-child(3),
        .all-pastes td:nth-child(3),
        .all-pastes th:nth-child(3),
        .pinned-pastes td:nth-child(6),
        .pinned-pastes th:nth-child(6),
        .all-pastes td:nth-child(6),
        .all-pastes th:nth-child(6) {
            display: none;
        }
        .pinned-pastes td:first-child,
        .pinned-pastes th:first-child,
        .all-pastes td:first-child,
        .all-pastes th:first-child {
            width: 45%;
        }
        .pinned-pastes td:nth-child(4),
        .pinned-pastes th:nth-child(4),
        .all-pastes td:nth-child(4),
        .all-pastes th:nth-child(4) {
            width: 30%;
        }
        .pinned-pastes td:nth-child(5),
        .pinned-pastes th:nth-child(5),
        .all-pastes td:nth-child(5),
        .all-pastes th:nth-child(5) {
            width: 25%;
        }
    }
    @media screen and (max-width: 480px) {
        .pinned-pastes {
            width: 100%;
            margin: 20px 5px;
        }
        .pinned-pastes table {
            font-size: 12px;
            table-layout: fixed;
        }
        .all-pastes {
            width: 100%;
            margin: 20px 5px;
        }
        .all-pastes table {
            font-size: 12px;
            table-layout: fixed;
        }
        .search-box {
            width: 180px;
        }
        .pinned-pastes td,
        .pinned-pastes th,
        .all-pastes td,
        .all-pastes th {
            padding: 6px 4px;
        }
        .pinned-pastes td:first-child,
        .pinned-pastes th:first-child,
        .all-pastes td:first-child,
        .all-pastes th:first-child {
            width: 45%;
            max-width: 120px;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        .pinned-pastes td:first-child a,
        .all-pastes td:first-child a {
            display: block;
            width: 100%;
            white-space: nowrap;
            overflow: hidden;
            text-overflow: ellipsis;
        }
        .pinned-pastes td:nth-child(4),
        .pinned-pastes th:nth-child(4),
        .all-pastes td:nth-child(4),
        .all-pastes th:nth-child(4) {
            width: 30%;
        }
        .pinned-pastes td:nth-child(5),
        .pinned-pastes th:nth-child(5),
        .all-pastes td:nth-child(5),
        .all-pastes th:nth-child(5) {
            width: 25%;
        }
    }
    .loading {
        text-align: center;
        padding: 20px;
        color: #888888;
        font-style: italic;
    }
    .modal {
        display: none;
        position: fixed;
        z-index: 1000;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0, 0, 0, 0.7);
    }
    .modal.show {
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .modal-content {
        background-color: #111;
        padding: 20px;
        border: 1px solid #333;
        width: 80%;
        max-width: 500px;
        position: relative;
        color: #fff;
    }
    .modal-close {
        color: #666;
        float: right;
        font-size: 28px;
        font-weight: bold;
        cursor: pointer;
    }
    .modal-close:hover {
        color: #999;
    }
    input[type="checkbox"]:checked {
        accent-color: #ff0000;
    }
    /* NEW YEAR */
    #logo-site {
        animation: floatUpDown 3s ease-in-out infinite;
    }
    @keyframes floatUpDown {
        0% {
            transform: translateY(0);
        }
        50% {
            transform: translateY(-10px);a
        }
        100% {
            transform: translateY(0);
        }
    }
    .snowflake {
        user-select: none !important;
        pointer-events: none !important;
    }
</style></head>

<body>
    
    
    <div class="logo-container">
        <img id="logo-site" src="/static/logo2025.png" alt="Ghostbin Logo">
        <img src="/static/podlogo.png" alt="Ghostbin PodLogo">
    </div>

    <div class="announcements">
        <div id="telegram-site" class="announcement" style="color: #ffffff">
            <a href="https://t.me/ghostbin_news" target="_blank" style="font-size: 23px; color: #25ABEE; text-decoration: underline;">Join <span id="site-name">Ghostbin</span> Telegram</a>
        </div>
        <div class="announcement" style="color: #ffffff">
            <span style="font-size: 16px; color: #CC0000;">Mirrors: ghostbin.fun | doxbin.online</span>
        </div>
        <div class="announcement" style="color: #ffffff">
            <a href="https://t.me/ghostbin_news/4" target="_blank" style="font-size: 16px; color: #9b1616; text-decoration: none;" onmouseover="this.style.textDecoration='underline'" onmouseout="this.style.textDecoration='none'">All Mirrors</a>
        </div>
        
            <div class="announcement" style="color: #ffffff">
                
                    <a href="/mailer" target="_blank" style="font-size: 23px; color: #5cb9b0; text-decoration: underline;">
                        Free Mailer
                    </a>
                
            </div>
        
            <div class="announcement" style="color: #ffffff">
                
                    <a href="https://t.me/HideMessagesRobot" target="_blank" style="font-size: 23px; color: red; text-decoration: underline;">
                        Hide Messages
                    </a>
                
            </div>
        
    </div>

    <div class="search-container">
        <label class="search-label">Search for a paste</label>
        
        <div style="margin-bottom: 8px; font-size: 13px;">
            <input type="radio" id="searchTitle" name="searchType" value="title" checked="" style="accent-color: #ff0000;" onchange="updateSearchOption('title')">
            <label for="searchTitle" style="color: #888888;">Search in title</label><br>
            <input type="radio" id="searchContent" name="searchType" value="content" style="accent-color: #ff0000;" onchange="updateSearchOption('content')">
            <label for="searchContent" style="color: #888888;">Search in paste</label>
        </div>
        
        <form class="search-form" action="/searchp" method="GET">
            <input name="search_query" type="text" class="search-box" placeholder="Search for...">
            <input type="hidden" id="searchOption" name="search_option" value="title">
            <button type="submit" class="search-button">Search</button>
        </form>
    </div>
    
    <div class="showing-text">
        Showing 25 (of 4214 total) pastes
    </div>
    
    <div class="pagination">
        
            <a class="disabled">&lt;</a>
        
    
        
            
                <a href="javascript:void(0)" class="active">1</a>
            
        
            
                <a href="/home?page=2">2</a>
            
        
            
                <a href="/home?page=3">3</a>
            
        
            
                <a href="/home?page=4">4</a>
            
        
            
                <a href="/home?page=5">5</a>
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
    
        
            <a href="/home?page=2" class="next">&gt;</a>
        
    </div>

    <div class="pinned-pastes">
        <h2>Pinned Pastes</h2>
        <table id="pinnedTable">
            <thead>
                <tr>
                    <th>Title</th>
                    <th>Comments</th>
                    <th>Views</th>
                    <th>Created by</th>
                    <th>Added</th>
                    
                </tr>
            </thead>
            <tbody>
                
                <tr style="background-color: #3D0606;" data-rank-color="#3D0606">
                    <td><a href="/upload/InformativeToSforPastes" title="Informative ToS for Pastes">
                        
                        
                        
                        Informative ToS for Pastes
                    </a></td>
                    <td>—</td>
                    <td>3858</td>
                    <td>
                        
                        
                            <a href="/user/Admin" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');">
                                <span style="color: #FFFFFF;">Admin</span>
                                 [Admin]
                            </a>
                        
                    </td>                    
                    <td>Apr 06, 2025</td>
                    
                </tr>
                
                <tr style="background-color: #3D0606;" data-rank-color="#3D0606">
                    <td><a href="/upload/TransparencyReport" title="Transparency Report">
                        
                        
                        
                        Transparency Report
                    </a></td>
                    <td>—</td>
                    <td>4528</td>
                    <td>
                        
                        
                            <a href="/user/Admin" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');">
                                <span style="color: #FFFFFF;">Admin</span>
                                 [Admin]
                            </a>
                        
                    </td>                    
                    <td>Apr 06, 2025</td>
                    
                </tr>
                
            </tbody>
        </table>
    </div>
    
    <div class="all-pastes">
        <table id="allPastesTable">
            <thead>
                <tr>
                    <th>Title</th>
                    <th>Comments</th>
                    <th>Views</th>
                    <th>Created by</th>
                    <th>Added</th>
                    
                </tr>
            </thead>
            <tbody>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/LisaSophieTripp" title="Lisa Sophie Tripp">
                        
                        

                        Lisa Sophie Tripp
                    </a></td>
                    <td>0</td>
                    <td>41</td>
                    <td>
                        
                        
                            <a href="/user/D3v1lHub" style="color: #2a9fd6;">
                                <span style="color: None;">D3v1lHub</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 02, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/OwnerFlysky1" title="Owner Flysky 1">
                        
                        

                        Owner Flysky 1
                    </a></td>
                    <td>0</td>
                    <td>57</td>
                    <td>
                        
                        
                            <a href="/user/colins" style="color: #2a9fd6;">
                                <span style="color: None;">colins</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/filchenkosergeyakafckingdog" title="filchenko sergey aka fcking dog">
                        
                        

                        filchenko sergey aka fcking dog
                    </a></td>
                    <td>0</td>
                    <td>58</td>
                    <td>
                        
                        
                            <a href="/user/unity" style="color: #2a9fd6;">
                                <span style="color: None;">unity</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: #1A3D5D;" data-rank-color="#1A3D5D">
                    <td><a href="/upload/leackowner" title="leackowner">
                        
                        

                        leackowner
                    </a></td>
                    <td>0</td>
                    <td>66</td>
                    <td>
                        
                        
                            <a href="/user/Kiroshin" style="color: #87cefa; font-weight: bold;">
                                <span style="color: #FFFFFF;">Kiroshin</span>
                                 [Council]
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/VanessaMarianovaAnonov" title="Vanessa Marianova Anonov">
                        
                        

                        Vanessa Marianova Anonov
                    </a></td>
                    <td>0</td>
                    <td>90</td>
                    <td>
                        
                        
                            <a href="/user/colins" style="color: #2a9fd6;">
                                <span style="color: None;">colins</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/Pokrovitelnica" title="Pokrovitelnica">
                        
                        

                        Pokrovitelnica
                    </a></td>
                    <td>0</td>
                    <td>62</td>
                    <td>
                        
                        
                            <a href="/user/colins" style="color: #2a9fd6;">
                                <span style="color: None;">colins</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/fuckshzx" title="fuckshzx">
                        
                        

                        fuckshzx
                    </a></td>
                    <td>0</td>
                    <td>83</td>
                    <td>
                        
                        
                            <span style="color: ;">Anonymous</span>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/886994649917583390" title="886994649917583390">
                        
                        

                        886994649917583390
                    </a></td>
                    <td>0</td>
                    <td>92</td>
                    <td>
                        
                        
                            <a href="/user/Crowned" style="color: #2a9fd6;">
                                <span style="color: #BB1E64;">Crowned</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/Liam" title="Liam">
                        
                        

                        Liam
                    </a></td>
                    <td>0</td>
                    <td>91</td>
                    <td>
                        
                        
                            <a href="/user/Crowned" style="color: #2a9fd6;">
                                <span style="color: #BB1E64;">Crowned</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/1211915203382607903" title="1211915203382607903">
                        
                        

                        1211915203382607903
                    </a></td>
                    <td>0</td>
                    <td>86</td>
                    <td>
                        
                        
                            <a href="/user/Crowned" style="color: #2a9fd6;">
                                <span style="color: #BB1E64;">Crowned</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/1235792434596810832" title="1235792434596810832">
                        
                        

                        1235792434596810832
                    </a></td>
                    <td>0</td>
                    <td>63</td>
                    <td>
                        
                        
                            <a href="/user/Crowned" style="color: #2a9fd6;">
                                <span style="color: #BB1E64;">Crowned</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/1364634377425911899" title="1364634377425911899">
                        
                        

                        1364634377425911899
                    </a></td>
                    <td>0</td>
                    <td>57</td>
                    <td>
                        
                        
                            <a href="/user/Crowned" style="color: #2a9fd6;">
                                <span style="color: #BB1E64;">Crowned</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/1352001108486127738" title="1352001108486127738">
                        
                        

                        1352001108486127738
                    </a></td>
                    <td>0</td>
                    <td>49</td>
                    <td>
                        
                        
                            <a href="/user/Crowned" style="color: #2a9fd6;">
                                <span style="color: #BB1E64;">Crowned</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/1007203953219485706" title="1007203953219485706">
                        
                        

                        1007203953219485706
                    </a></td>
                    <td>0</td>
                    <td>52</td>
                    <td>
                        
                        
                            <a href="/user/Crowned" style="color: #2a9fd6;">
                                <span style="color: #BB1E64;">Crowned</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/huriccan" title="huriccan">
                        
                        

                        huriccan
                    </a></td>
                    <td>0</td>
                    <td>60</td>
                    <td>
                        
                        
                            <a href="/user/byebardexsa" style="color: #2a9fd6;">
                                <span style="color: None;">byebardexsa</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/MikeDavidRedbar" title="Mike David Redbar">
                        
                        

                        Mike David Redbar
                    </a></td>
                    <td>0</td>
                    <td>59</td>
                    <td>
                        
                        
                            <a href="/user/PizzaHutLegion" style="color: #2a9fd6;">
                                <span style="color: None;">PizzaHutLegion</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/Memberofthe764group" title="Member of the 764 group">
                        
                        

                        Member of the 764 group
                    </a></td>
                    <td>1</td>
                    <td>77</td>
                    <td>
                        
                        
                            <a href="/user/Sern" style="color: #2a9fd6;">
                                <span style="color: None;">Sern</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: #2D0A21;" data-rank-color="#2D0A21">
                    <td><a href="/upload/spector" title="spector">
                        
                        

                        spector
                    </a></td>
                    <td>0</td>
                    <td>53</td>
                    <td>
                        
                        
                            <a href="/user/antagonist" style="color: #9B318E; font-weight: bold;">
                                <span style="color: #FFFFFF;">antagonist</span>
                                 [VIP]
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/239077751825367040" title="239077751825367040">
                        
                        

                        239077751825367040
                    </a></td>
                    <td>0</td>
                    <td>55</td>
                    <td>
                        
                        
                            <a href="/user/dizoff" style="color: #2a9fd6;">
                                <span style="color: None;">dizoff</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Dec 01, 2025</td>
                    
                </tr>
                
                <tr style="background-color: #2B021B;" data-rank-color="#2B021B">
                    <td><a href="/upload/na2eb3upd2" title="na2eb3 upd2">
                        
                        

                        na2eb3 upd2
                    </a></td>
                    <td>0</td>
                    <td>58</td>
                    <td>
                        
                        
                            <a href="/user/nespal5let" style="color: #780A48; font-weight: bold;">
                                <span style="color: None;">nespal5let</span>
                                 [Criminal]
                            </a>
                        
                    </td>                    
                    <td>Nov 30, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/aspalovnepogreshimyestrastnye" title="aspalov nepogreshimye strastnye">
                        
                        

                        aspalov nepogreshimye strastnye
                    </a></td>
                    <td>0</td>
                    <td>80</td>
                    <td>
                        
                        
                            <a href="/user/nub" style="color: #2a9fd6;">
                                <span style="color: None;">nub</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Nov 30, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/loxssy" title="loxssy">
                        
                        

                        loxssy
                    </a></td>
                    <td>0</td>
                    <td>143</td>
                    <td>
                        
                        
                            <a href="/user/wasted" style="color: #2a9fd6;">
                                <span style="color: None;">wasted</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Nov 30, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/sonnnadapter" title="sonnnadapter">
                        
                        

                        sonnnadapter
                    </a></td>
                    <td>0</td>
                    <td>75</td>
                    <td>
                        
                        
                            <a href="/user/wasted" style="color: #2a9fd6;">
                                <span style="color: None;">wasted</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Nov 30, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/macheta" title="macheta">
                        
                        

                        macheta
                    </a></td>
                    <td>0</td>
                    <td>85</td>
                    <td>
                        
                        
                            <a href="/user/wasted" style="color: #2a9fd6;">
                                <span style="color: None;">wasted</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Nov 30, 2025</td>
                    
                </tr>
                
                <tr style="background-color: ;" data-rank-color="">
                    <td><a href="/upload/doxykill" title="doxykill">
                        
                        

                        doxykill
                    </a></td>
                    <td>0</td>
                    <td>84</td>
                    <td>
                        
                        
                            <a href="/user/wasted" style="color: #2a9fd6;">
                                <span style="color: None;">wasted</span>
                                
                            </a>
                        
                    </td>                    
                    <td>Nov 30, 2025</td>
                    
                </tr>
                
            </tbody>
        </table>
    </div>
    
    <div class="pagination">
        
            <a class="disabled">&lt;</a>
        
    
        
            
                <a href="javascript:void(0)" class="active">1</a>
            
        
            
                <a href="/home?page=2">2</a>
            
        
            
                <a href="/home?page=3">3</a>
            
        
            
                <a href="/home?page=4">4</a>
            
        
            
                <a href="/home?page=5">5</a>
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
            
        
    
        
            <a href="/home?page=2" class="next">&gt;</a>
        
    </div>

    <div class="showing-text">
        Showing 25 (of 2101 total) pastes
    </div>
    
    
    <script>
        function updateSearchOption(option) {
            document.getElementById('searchOption').value = option;
        }
    </script>
    

        
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            if (window.location.hostname === "vilebin.net") {
                document.getElementById("logo-site").src = "/static/logo.jpg";
            }
        });
    </script>
<script defer="" src="https://static.cloudflareinsights.com/beacon.min.js/vcd15cbe7772f49c399c6a5babf22c1241717689176015" integrity="sha512-ZpsOmlRQV6y907TI0dKBHq9Md29nnaEIPlkf84rnaERnq6zvWvPUqr2ft8M1aS28oN72PdrCzSjY4U6VaAw1EQ==" data-cf-beacon="{&quot;rayId&quot;:&quot;9a765081fba8078c&quot;,&quot;version&quot;:&quot;2025.9.1&quot;,&quot;r&quot;:1,&quot;token&quot;:&quot;33347883c6ee4801a813a6d1921fd91e&quot;,&quot;serverTiming&quot;:{&quot;name&quot;:{&quot;cfExtPri&quot;:true,&quot;cfEdge&quot;:true,&quot;cfOrigin&quot;:true,&quot;cfL4&quot;:true,&quot;cfSpeedBrain&quot;:true,&quot;cfCacheStatus&quot;:true}}}" crossorigin="anonymous"></script>



<script src="/static/scripts/snow.js"></script>
<link rel="stylesheet" href="/static/nav.css">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&amp;display=swap" rel="stylesheet">
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
<script src="https://cdnjs.cloudflare.com/ajax/libs/socket.io/4.7.4/socket.io.min.js"></script>
<link rel="icon" href="data:,">

<style>
    input {
        outline: none !important;
        box-shadow: none !important;
    }

    input:focus {
        outline: none !important;
        box-shadow: none !important;
    }

    *:focus {
        outline: none !important;
        box-shadow: none !important;
    }

    input, textarea, select {
        font-size: 16px !important;
    }

    ::-webkit-scrollbar {
        display: none;
    }

    html {
        -ms-overflow-style: none;
        scrollbar-width: none;
    }
    body {
        font-family: 'Inter', -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Arial, sans-serif;
    }

    .verification-modal {
        position: fixed;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.5);
        display: none;
        justify-content: center;
        align-items: center;
        z-index: 9999;
    }

    body.modal-open {
        overflow: hidden;
        pointer-events: none;
    }

    body.modal-open .verification-modal {
        pointer-events: all;
    }

    .verification-content {
        background: #1a1a1a;
        color: #fff;
        padding: 2rem;
        border-radius: 0;
        text-align: center;
        max-width: 400px;
        width: 90%;
    }

    .verification-buttons {
        display: flex;
        justify-content: center;
        gap: 1rem;
        margin-top: 1.5rem;
    }

    .verification-buttons button {
        padding: 0.5rem 1.5rem;
        border: none;
        border-radius: 0;
        cursor: pointer;
        font-weight: 500;
    }

    .verification-buttons button:hover {
        opacity: 1;
    }

    .approve-btn {
        background: #4CAF50;
        color: white;
    }

    .deny-btn {
        background: #f44336;
        color: white;
    }
</style>

<script>
    document.addEventListener("DOMContentLoaded", function() {
        const protocol = window.location.protocol === "https:" ? "wss" : "ws";
        const host = window.location.host;
    
        function generateClientId() {
            return 'xxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g, function(c) {
                const r = Math.random() * 16 | 0,
                    v = c === 'x' ? r : (r & 0x3 | 0x8);
                return v.toString(16);
            });
        }
    
        const clientId = localStorage.getItem("client_id") || generateClientId();
        localStorage.setItem("client_id", clientId);
    
        const socketUrl = `${protocol}://${host}/ws/${clientId}?username=None`;
        const socket = new WebSocket(socketUrl);
    
        socket.onmessage = function(event) {
            const data = JSON.parse(event.data);

            if (data.event === 'online') {
                const onlineCounts = document.querySelectorAll('.online-count');
                onlineCounts.forEach(count => {
                    count.textContent = data.data;
                    count.style.display = 'flex';
                });
            }

            if (data.event === 'refresh') {
                location.reload();
            }

            if (data.event === 'clear_chat') {
                const messages = document.querySelectorAll('[data-message-id]');
                messages.forEach(messageElement => {
                    messageElement.remove();
                });
            }

            if (data.event === 'send_message') {
                addMessageToChat(data.data);
            }

            if (data.event === 'delete_message') {
                const messageElement = document.querySelector(`[data-message-id="${data.data.messageID}"]`);
                if (messageElement) {
                    messageElement.remove();
                }
            }
        };
    
        window.socket = socket;
    });
</script>

<style>
    #notifications-container {
        max-height: 400px;
        overflow-y: auto;
        background: #000000;
    }
    #notifications-container > div {
        padding: 4px 15px;
        border-bottom: 1px solid #282828;
        background: #000000;
    }
    .notification-message {
        white-space: normal;
        word-break: break-word;
        display: block;
        font-size: 13px;
        line-height: 16px;
    }
    .notification-message a {
        color: #2A9FD6 !important;
        text-decoration: none !important;
        display: inline;
    }
    .notification-message a:hover {
        color: #2A9FD6 !important;
        text-decoration: underline !important;
    }
    #notifications-container::-webkit-scrollbar {
        width: 8px !important;
    }
    #notifications-container::-webkit-scrollbar-track {
        background: #060606 !important;
    }
    #notifications-container::-webkit-scrollbar-thumb {
        background: #282828 !important;
        border-radius: 4px !important;
    }
    #notifications-container::-webkit-scrollbar-thumb:hover {
        background: #333 !important;
    }
    #notification-dropdown {
        border-radius: 4px;
    }
    #notification-dropdown::before {
        display: none;
    }
    .notification-highlight {
        background: rgba(255, 255, 0, 0.1) !important;
    }
    .online-count {
        display: flex;
        align-items: center;
        color: #00ff00;
        font-size: 12px;
    }
    .online-count::before {
        content: '';
        display: inline-block;
        width: 6px;
        height: 6px;
        background: #00ff00;
        border-radius: 50%;
        margin-right: 6px;
        animation: pulse 2s infinite;
        box-shadow: 0 0 0 0 rgba(0, 255, 0, 0.7);
    }
    @keyframes pulse {
        0% {
            box-shadow: 0 0 0 0 rgba(0, 255, 0, 0.7);
        }
        70% {
            box-shadow: 0 0 0 6px rgba(0, 255, 0, 0);
        }
        100% {
            box-shadow: 0 0 0 0 rgba(0, 255, 0, 0);
        }
    }
    .mobile-only {
        display: none !important;
    }
    @media (max-width: 1000px) {
        .nav-brand {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .mobile-only.online-count {
            display: flex !important;
            margin-left: 0px;
            font-size: 12px;
        }
        .mobile-only.online-count::before {
            width: 6px;
            height: 6px;
            margin-right: 6px;
        }
        .desktop-only {
            display: none !important;
        }
    }

    .notification-container {
        visibility: hidden;
        pointer-events: none;
        position: fixed;
        bottom: 30px;
        right: 30px;
        z-index: 9999;
        max-width: 350px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5);
        background-color: #111;
        border: 1px solid #333;
        color: #fff;
        border-radius: 3px;
        opacity: 0;
        transform: translateY(20px);
        transition: opacity 0.3s ease, transform 0.3s ease, visibility 0.3s;
        font-family: 'Inter', sans-serif;
        display: block;
    }

    .notification-container.show {
        visibility: visible;
        pointer-events: auto;
        opacity: 1;
        transform: translateY(0);
    }
    
    .notification-header {
        background-color: #181818;
        padding: 10px 15px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        border-bottom: 1px solid #333;
    }
    
    .notification-title {
        font-weight: 600;
        font-size: 14px;
    }
    
    .notification-close {
        color: #666;
        cursor: pointer;
        font-size: 18px;
        transition: color 0.2s;
        padding: 0 5px;
    }
    
    .notification-close:hover {
        color: #999;
    }
    
    .notification-body {
        padding: 15px;
        font-size: 13px;
        line-height: 1.5;
    }
    
    .notification-footer {
        padding: 0 15px 15px;
        display: flex;
        justify-content: flex-end;
        gap: 10px;
    }
    
    .notification-btn {
        background: #222;
        color: #fff;
        border: 1px solid #333;
        padding: 6px 14px;
        border-radius: 3px;
        cursor: pointer;
        font-size: 13px;
        transition: background-color 0.2s;
        outline: none;
    }
    
    .notification-btn:hover {
        background: #282828;
    }
    
    .notification-btn.primary {
        background: rgb(17, 17, 17);
        border: 1px solid #312f2f;
    }
    
    .notification-btn.primary:hover {
        background: #312f2f;
    }
</style>

<!-- CHAT -->

<style>
    .chat-container {
        position: fixed !important;
        bottom: 0 !important;
        left: 20px !important;
        width: 600px !important;
        height: 400px !important;
        background: #1a1a1a !important;
        border: 1px solid #333 !important;
        display: flex !important;
        flex-direction: column !important;
        z-index: 1000 !important;
        isolation: isolate !important;
    }
    .chat-header {
        padding: 4px 8px !important;
        background: #222 !important;
        border-bottom: 1px solid #333 !important;
        display: flex !important;
        justify-content: space-between !important;
        align-items: center !important;
        color: #fff !important;
        font-size: 12px !important;
    }
    .chat-messages {
        flex: 1 !important;
        overflow-y: scroll !important;
        padding: 8px 8px 8px 8px !important;
        font-size: 12px !important;
        overscroll-behavior: contain !important;
        -ms-overflow-style: none !important;
    }
    .chat-input-container {
        padding: 8px !important;
        border-top: 1px solid #333 !important;
        display: flex !important;
        gap: 8px !important;
    }
    .chat-input {
        flex: 1 !important;
        padding: 6px !important;
        border: 1px solid #333 !important;
        background: #222 !important;
        color: #fff !important;
        font-size: 12px !important;
    }
    .chat-send-btn {
        padding: 6px 12px !important;
        background: #333 !important;
        border: none !important;
        color: #fff !important;
        cursor: pointer !important;
        font-size: 12px !important;
        border-radius: 0 !important;
    }
    .message {
        margin: 2px 0 !important;
        padding: 2px 2px 2px 0 !important;
        word-wrap: break-word !important;
        cursor: pointer !important;
        display: block !important;
    }
    .message .author {
        white-space: nowrap !important;
        display: inline !important;
    }
    .message .content {
        color: #fff !important;
        display: inline !important;
    }
    .message .content span {
        display: inline !important;
    }
    .message .chat-timestamp {
        color: #888 !important;
        font-size: 11px !important;
        white-space: nowrap !important;
        display: inline !important;
    }
    .chat-toggle {
        position: fixed !important;
        bottom: 20px !important;
        left: 20px !important;
        padding: 8px 16px !important;
        background: #333 !important;
        color: #fff !important;
        border: none !important;
        cursor: pointer !important;
        z-index: 999 !important;
        font-size: 12px !important;
        border-radius: 0 !important;
    }
    .chat-container.hidden {
        display: none !important;
    }
    .chat-msg-modal {
        display: none !important;
        position: fixed !important;
        top: 0 !important;
        left: 0 !important;
        width: 100% !important;
        height: 100% !important;
        background: rgba(0, 0, 0, 0.85) !important;
        z-index: 1001 !important;
    }

    .chat-msg-modal.show {
        display: flex !important;
        align-items: center !important;
        justify-content: center !important;
    }

    .chat-msg-modal-content {
        background: #141414 !important;
        padding: 24px !important;
        width: 90% !important;
        max-width: 400px !important;
        color: #fff !important;
        border: 1px solid #333 !important;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.5) !important;
    }

    #chat-msg-info {
        color: #fff !important;
        margin-bottom: 24px !important;
        font-size: 14px !important;
        line-height: 1.5 !important;
        padding: 10px;
        word-break: break-word;
    }

    #chat-msg-info a:hover {
        text-decoration: underline !important;
    }

    .chat-msg-info-header {
        color: #888 !important;
        font-size: 12px !important;
        margin-bottom: 4px !important;
    }

    .chat-msg-button-container {
        display: flex !important;
        flex-direction: column !important;
        gap: 8px !important;
    }

    .chat-msg-button {
        background: #1E1E1E !important;
        border: 1px solid #333 !important;
        color: #fff !important;
        padding: 8px 16px !important;
        font-size: 13px !important;
        cursor: pointer !important;
        width: 100% !important;
        text-align: center !important;
        border-radius: 0 !important;
    }

    .chat-close {
        background: none !important;
        border: none !important;
        color: #fff !important;
        font-size: 20px !important;
        line-height: 1 !important;
        padding: 0 !important;
        cursor: pointer !important;
        margin: 0 !important;
    }

    .chat-close:hover {
        color: #ff0000 !important;
    }

    @media (max-width: 768px) {
        .chat-container {
            width: 100% !important;
            left: 0 !important;
            bottom: 0 !important;
            border: none !important;
            border-top: 1px solid #333 !important;
        }

        .chat-toggle {
            left: 10px !important;
        }

        .chat-input {
            font-size: 16px !important;
        }
    }

    .message a:hover {
        text-decoration: underline !important;
    }

    .switch {
        position: relative;
        display: inline-block;
        width: 40px;
        height: 20px;
    }

    .switch input {
        opacity: 0;
        width: 0;
        height: 0;
    }

    .slider {
        position: absolute;
        cursor: pointer;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
        background-color: #333;
    }

    .slider:before {
        position: absolute;
        content: "";
        height: 16px;
        width: 16px;
        left: 2px;
        bottom: 2px;
        background-color: #fff;
    }

    input:checked + .slider {
        background-color: #ff0000;
    }

    input:checked + .slider:before {
        transform: translateX(20px);
    }

    /* NEW YEAR */
    .snowflake {
        user-select: none !important;
        pointer-events: none !important;
    }
</style>

<button class="chat-toggle" onclick="toggleChat()">Chat</button>

<div class="chat-container hidden">
    <div class="chat-header">
        <span id="chatTitle" style="cursor: default">Chat</span>
        <button class="chat-close" onclick="toggleChat()">×</button>
    </div>
    <div class="chat-messages" id="chatMessages"><div class="message" data-message-id="1">
                <span class="chat-timestamp">12:35 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #ff0000">Admin</span> cleared it chat.</span></span>
            </div><div class="message" data-message-id="2">
                <span class="chat-timestamp">18:19 UTC</span>
                <span class="author" style="color: #5555FF; font-weight: bold;">shell [Helper]:</span>
                <span class="content"><span>васап</span></span>
            </div><div class="message" data-message-id="3">
                <span class="chat-timestamp">18:30 UTC</span>
                <span class="author" style="color: #5555FF; font-weight: bold;">kiroshin [Helper]:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="4">
                <span class="chat-timestamp">03:16 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">wtf [Mod]:</span>
                <span class="content"><span>qq all</span></span>
            </div><div class="message" data-message-id="5">
                <span class="chat-timestamp">03:16 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">wtf [Mod]:</span>
                <span class="content"><span>qq all</span></span>
            </div><div class="message" data-message-id="6">
                <span class="chat-timestamp">09:38 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">mvdmail</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="7">
                <span class="chat-timestamp">19:11 UTC</span>
                <span class="author" style="color: #2A9FD6">Filk673:</span>
                <span class="content"><span>Всем здарова</span></span>
            </div><div class="message" data-message-id="10">
                <span class="chat-timestamp">19:14 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');">spyder [Admin]:</span>
                <span class="content"><span>И что</span></span>
            </div><div class="message" data-message-id="11">
                <span class="chat-timestamp">19:14 UTC</span>
                <span class="author" style="color: #2A9FD6">Filk673:</span>
                <span class="content"><span>Не чо</span></span>
            </div><div class="message" data-message-id="12">
                <span class="chat-timestamp">19:14 UTC</span>
                <span class="author" style="color: #2A9FD6">Filk673:</span>
                <span class="content"><span>Лоникс я</span></span>
            </div><div class="message" data-message-id="12">
                <span class="chat-timestamp">15:10 UTC</span>
                <span class="author" style="color: #2A9FD6">Wolldysss:</span>
                <span class="content"><span>Блин</span></span>
            </div><div class="message" data-message-id="13">
                <span class="chat-timestamp">15:10 UTC</span>
                <span class="author" style="color: #2A9FD6">Wolldysss:</span>
                <span class="content"><span>Сука нахуй я сюдаа зашел</span></span>
            </div><div class="message" data-message-id="22">
                <span class="chat-timestamp">05:18 UTC</span>
                <span class="author" style="color: #2A9FD6">Filk673:</span>
                <span class="content"><span>Так и уж быть</span></span>
            </div><div class="message" data-message-id="19">
                <span class="chat-timestamp">07:19 UTC</span>
                <span class="author" style="color: #2A9FD6">Filk673:</span>
                <span class="content"><span>Бл лак</span></span>
            </div><div class="message" data-message-id="17">
                <span class="chat-timestamp">08:43 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>да блять че мои пасты удаляют</span></span>
            </div><div class="message" data-message-id="19">
                <span class="chat-timestamp">08:53 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>та я вчера 2 пасты залил и 2 удалили</span></span>
            </div><div class="message" data-message-id="20">
                <span class="chat-timestamp">08:57 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">shell [Council]:</span>
                <span class="content"><span>если снесли - значит вы нарушили правила TOS.Прочтите их перед выкладкой пасты</span></span>
            </div><div class="message" data-message-id="19">
                <span class="chat-timestamp">11:33 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>бля если мне и ща пасту удалят я ваще ахуею</span></span>
            </div><div class="message" data-message-id="20">
                <span class="chat-timestamp">11:33 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>я щас все по TOS сделал</span></span>
            </div><div class="message" data-message-id="21">
                <span class="chat-timestamp">11:33 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>ну типо +- так же</span></span>
            </div><div class="message" data-message-id="22">
                <span class="chat-timestamp">11:59 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');">spyder [Admin]:</span>
                <span class="content"><span>не повезло</span></span>
            </div><div class="message" data-message-id="23">
                <span class="chat-timestamp">12:10 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">shell [Council]:</span>
                <span class="content"><span>найс трай</span></span>
            </div><div class="message" data-message-id="24">
                <span class="chat-timestamp">12:20 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>пиздец блять</span></span>
            </div><div class="message" data-message-id="25">
                <span class="chat-timestamp">12:20 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>блять а че не так то там было</span></span>
            </div><div class="message" data-message-id="26">
                <span class="chat-timestamp">12:20 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>бля</span></span>
            </div><div class="message" data-message-id="27">
                <span class="chat-timestamp">12:23 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>пиздец сидел ебашил 30 минут искал инфу и тут вот блять</span></span>
            </div><div class="message" data-message-id="28">
                <span class="chat-timestamp">12:23 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>бля обьясните дауну а че там было не так</span></span>
            </div><div class="message" data-message-id="29">
                <span class="chat-timestamp">12:23 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>я не понял просто</span></span>
            </div><div class="message" data-message-id="30">
                <span class="chat-timestamp">12:23 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">shell [Council]:</span>
                <span class="content"><span>меньше 15 лет людям в пасте удаляем</span></span>
            </div><div class="message" data-message-id="31">
                <span class="chat-timestamp">12:27 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>пупупупу</span></span>
            </div><div class="message" data-message-id="32">
                <span class="chat-timestamp">12:28 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>а если почти 15?</span></span>
            </div><div class="message" data-message-id="33">
                <span class="chat-timestamp">12:28 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>или все равно не7</span></span>
            </div><div class="message" data-message-id="34">
                <span class="chat-timestamp">12:31 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">shell [Council]:</span>
                <span class="content"><span>именно 15,если вчера др было,то не удалим,а если не было,и человеку 14,не смотря на то,что 15 - удалим</span></span>
            </div><div class="message" data-message-id="35">
                <span class="chat-timestamp">12:31 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">shell [Council]:</span>
                <span class="content"><span>не смотря на то что почти 15*</span></span>
            </div><div class="message" data-message-id="36">
                <span class="chat-timestamp">12:33 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>бля пон</span></span>
            </div><div class="message" data-message-id="37">
                <span class="chat-timestamp">12:33 UTC</span>
                <span class="author" style="color: #2A9FD6">16opgNAKAJET:</span>
                <span class="content"><span>ну все зря ебашил пасту</span></span>
            </div><div class="message" data-message-id="38">
                <span class="chat-timestamp">12:34 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');">spyder [Admin]:</span>
                <span class="content"><span>шелл</span></span>
            </div><div class="message" data-message-id="39">
                <span class="chat-timestamp">12:34 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');">spyder [Admin]:</span>
                <span class="content"><span>тут?</span></span>
            </div><div class="message" data-message-id="39">
                <span class="chat-timestamp">18:54 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6">Ueushw</span> was temporarily muted for 1 hour.</span></span>
            </div><div class="message" data-message-id="40">
                <span class="chat-timestamp">19:45 UTC</span>
                <span class="author" style="color: #2A9FD6">f1oxustraxaetworld:</span>
                <span class="content"><span>пацеки что делать если хотят сватуть?</span></span>
            </div><div class="message" data-message-id="41">
                <span class="chat-timestamp">19:46 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">shell [Council]:</span>
                <span class="content"><span>Купить у кого-то дефф</span></span>
            </div><div class="message" data-message-id="42">
                <span class="chat-timestamp">09:27 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">nespal5let</span> has redeemed <span style="color: #780A48; font-weight: bold;">criminal</span> rank!</span></span>
            </div><div class="message" data-message-id="43">
                <span class="chat-timestamp">09:27 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #9B318E; font-weight: bold;">cvv</span> has redeemed <span style="color: #780A48; font-weight: bold;">criminal</span> rank!</span></span>
            </div><div class="message" data-message-id="44">
                <span class="chat-timestamp">09:27 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">brundukplatina</span> has redeemed <span style="color: #780A48; font-weight: bold;">criminal</span> rank!</span></span>
            </div><div class="message" data-message-id="45">
                <span class="chat-timestamp">09:28 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">me</span> has redeemed <span style="color: #780A48; font-weight: bold;">criminal</span> rank!</span></span>
            </div><div class="message" data-message-id="46">
                <span class="chat-timestamp">09:29 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">7Spirit</span> has redeemed <span style="color: #780A48; font-weight: bold;">criminal</span> rank!</span></span>
            </div><div class="message" data-message-id="47">
                <span class="chat-timestamp">09:29 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #FFD700; font-weight: bold;">akimera</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="48">
                <span class="chat-timestamp">09:29 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">avdgrief</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="49">
                <span class="chat-timestamp">09:29 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #FFD700; font-weight: bold;">Balenciagov</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="50">
                <span class="chat-timestamp">09:30 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #bb71e4; font-weight: bold;">cataract</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="52">
                <span class="chat-timestamp">09:42 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">zvtychka</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="53">
                <span class="chat-timestamp">09:45 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">oxicrise</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="54">
                <span class="chat-timestamp">09:46 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">xel</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="55">
                <span class="chat-timestamp">09:56 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #780A48; font-weight: bold;">cvv</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="56">
                <span class="chat-timestamp">09:58 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">razterzatel</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="57">
                <span class="chat-timestamp">10:18 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">yaw</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="58">
                <span class="chat-timestamp">19:58 UTC</span>
                <span class="author" style="color: #2A9FD6">stgdgdhdsueue:</span>
                <span class="content"><span>А</span></span>
            </div><div class="message" data-message-id="58">
                <span class="chat-timestamp">09:11 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6">Blake</span> was temporarily muted for 1 hour.</span></span>
            </div><div class="message" data-message-id="59">
                <span class="chat-timestamp">16:16 UTC</span>
                <span class="author" style="color: #2A9FD6">Spaced0xs:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="60">
                <span class="chat-timestamp">16:17 UTC</span>
                <span class="author" style="color: #2A9FD6">Spaced0xs:</span>
                <span class="content"><span>is TS just d0xbin renamed?</span></span>
            </div><div class="message" data-message-id="61">
                <span class="chat-timestamp">16:28 UTC</span>
                <span class="author" style="color: #2A9FD6">Spaced0xs:</span>
                <span class="content"><span>I made some like tos type things for you guys</span></span>
            </div><div class="message" data-message-id="62">
                <span class="chat-timestamp">16:28 UTC</span>
                <span class="author" style="color: #2A9FD6">Spaced0xs:</span>
                <span class="content"><span>I wont!</span></span>
            </div><div class="message" data-message-id="63">
                <span class="chat-timestamp">21:52 UTC</span>
                <span class="author" style="color: #9B318E; font-weight: bold;">xive [VIP]:</span>
                <span class="content"><span>qq everyone</span></span>
            </div><div class="message" data-message-id="64">
                <span class="chat-timestamp">21:52 UTC</span>
                <span class="author" style="color: #9B318E; font-weight: bold;">xive [VIP]:</span>
                <span class="content"><span>у меня чат не грузит!!!! бляха</span></span>
            </div><div class="message" data-message-id="65">
                <span class="chat-timestamp">21:52 UTC</span>
                <span class="author" style="color: #9B318E; font-weight: bold;">xive [VIP]:</span>
                <span class="content"><span>во загрузило</span></span>
            </div><div class="message" data-message-id="66">
                <span class="chat-timestamp">21:52 UTC</span>
                <span class="author" style="color: #9B318E; font-weight: bold;">xive [VIP]:</span>
                <span class="content"><span>во загрузило</span></span>
            </div><div class="message" data-message-id="67">
                <span class="chat-timestamp">02:02 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>всем салямчик общий</span></span>
            </div><div class="message" data-message-id="68">
                <span class="chat-timestamp">09:52 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6">generalpechenka</span> was unmuted.</span></span>
            </div><div class="message" data-message-id="69">
                <span class="chat-timestamp">09:52 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6">Ueushw</span> was unmuted.</span></span>
            </div><div class="message" data-message-id="70">
                <span class="chat-timestamp">09:52 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">wtf [Mod]:</span>
                <span class="content"><span>qq</span></span>
            </div><div class="message" data-message-id="71">
                <span class="chat-timestamp">12:51 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>qq</span></span>
            </div><div class="message" data-message-id="72">
                <span class="chat-timestamp">14:03 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hello</span></span>
            </div><div class="message" data-message-id="73">
                <span class="chat-timestamp">04:07 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');">Lucifer [Admin]:</span>
                <span class="content"><span>are people active in here</span></span>
            </div><div class="message" data-message-id="74">
                <span class="chat-timestamp">14:32 UTC</span>
                <span class="author" style="color: #5555FF; font-weight: bold;">kiroshin [Helper]:</span>
                <span class="content"><span>здаров всем</span></span>
            </div><div class="message" data-message-id="75">
                <span class="chat-timestamp">14:32 UTC</span>
                <span class="author" style="color: #5555FF; font-weight: bold;">kiroshin [Helper]:</span>
                <span class="content"><span>толстопузики</span></span>
            </div><div class="message" data-message-id="76">
                <span class="chat-timestamp">14:32 UTC</span>
                <span class="author" style="color: #5555FF; font-weight: bold;">kiroshin [Helper]:</span>
                <span class="content"><span>толстопузики</span></span>
            </div><div class="message" data-message-id="77">
                <span class="chat-timestamp">17:44 UTC</span>
                <span class="author" style="color: #2A9FD6">emaol:</span>
                <span class="content"><span>привет всем!</span></span>
            </div><div class="message" data-message-id="78">
                <span class="chat-timestamp">17:44 UTC</span>
                <span class="author" style="color: #2A9FD6">emaol:</span>
                <span class="content"><span>если кому надо</span></span>
            </div><div class="message" data-message-id="79">
                <span class="chat-timestamp">20:52 UTC</span>
                <span class="author" style="color: #2A9FD6">scelty:</span>
                <span class="content"><span>qq all</span></span>
            </div><div class="message" data-message-id="80">
                <span class="chat-timestamp">16:24 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">Sihdndsj</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="81">
                <span class="chat-timestamp">16:25 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">fierysky</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="82">
                <span class="chat-timestamp">16:25 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">soundcloud</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="83">
                <span class="chat-timestamp">16:26 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">monikoshisten</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="84">
                <span class="chat-timestamp">16:35 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">family</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="85">
                <span class="chat-timestamp">16:57 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">xSlattz</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="86">
                <span class="chat-timestamp">16:57 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">shwt1me</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="87">
                <span class="chat-timestamp">16:58 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">KURRION</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="88">
                <span class="chat-timestamp">17:02 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">xxqv</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="89">
                <span class="chat-timestamp">02:10 UTC</span>
                <span class="author" style="color: #9B318E; font-weight: bold;">family [VIP]:</span>
                <span class="content"><span>Hello, guys.</span></span>
            </div><div class="message" data-message-id="90">
                <span class="chat-timestamp">02:11 UTC</span>
                <span class="author" style="color: #9B318E; font-weight: bold;">family [VIP]:</span>
                <span class="content"><span>Is there an active/temporary recruitment in the helper at the moment?</span></span>
            </div><div class="message" data-message-id="91">
                <span class="chat-timestamp">02:12 UTC</span>
                <span class="author" style="color: #9B318E; font-weight: bold;">family [VIP]:</span>
                <span class="content"><span>Is there an active/temporary recruitment in the helper at the moment?</span></span>
            </div><div class="message" data-message-id="92">
                <span class="chat-timestamp">02:12 UTC</span>
                <span class="author" style="color: #9B318E; font-weight: bold;">family [VIP]:</span>
                <span class="content"><span>Is there an active/temporary recruitment in the helper at the moment?</span></span>
            </div><div class="message" data-message-id="93">
                <span class="chat-timestamp">02:14 UTC</span>
                <span class="author" style="color: #9B318E; font-weight: bold;">family [VIP]:</span>
                <span class="content"><span>I apologize for the spam, alas, it sent 3 messages in a row.</span></span>
            </div><div class="message" data-message-id="94">
                <span class="chat-timestamp">04:17 UTC</span>
                <span class="author" style="color: #bb71e4; font-weight: bold; background-image: url('/static/purple.gif');">kolsfed [Manager]:</span>
                <span class="content"><span>Hello</span></span>
            </div><div class="message" data-message-id="95">
                <span class="chat-timestamp">04:17 UTC</span>
                <span class="author" style="color: #bb71e4; font-weight: bold; background-image: url('/static/purple.gif');">kolsfed [Manager]:</span>
                <span class="content"><span>No, we don't need a helper.</span></span>
            </div><div class="message" data-message-id="96">
                <span class="chat-timestamp">12:44 UTC</span>
                <span class="author" style="color: #9B318E; font-weight: bold;">family [VIP]:</span>
                <span class="content"><span>Thanks)</span></span>
            </div><div class="message" data-message-id="97">
                <span class="chat-timestamp">16:34 UTC</span>
                <span class="author" style="color: #5555FF; font-weight: bold;">kiroshin [Helper]:</span>
                <span class="content"><span>qq</span></span>
            </div><div class="message" data-message-id="98">
                <span class="chat-timestamp">14:40 UTC</span>
                <span class="author" style="color: #2A9FD6">brainishee:</span>
                <span class="content"><span>ы</span></span>
            </div><div class="message" data-message-id="99">
                <span class="chat-timestamp">14:40 UTC</span>
                <span class="author" style="color: #2A9FD6">brainishee:</span>
                <span class="content"><span>здарова</span></span>
            </div><div class="message" data-message-id="100">
                <span class="chat-timestamp">05:31 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>всем здаров пацанчики</span></span>
            </div><div class="message" data-message-id="101">
                <span class="chat-timestamp">15:54 UTC</span>
                <span class="author" style="color: #5555FF; font-weight: bold;">kiroshin [Helper]:</span>
                <span class="content"><span>шо</span></span>
            </div><div class="message" data-message-id="102">
                <span class="chat-timestamp">15:54 UTC</span>
                <span class="author" style="color: #5555FF; font-weight: bold;">kiroshin [Helper]:</span>
                <span class="content"><span>вы</span></span>
            </div><div class="message" data-message-id="103">
                <span class="chat-timestamp">15:54 UTC</span>
                <span class="author" style="color: #5555FF; font-weight: bold;">kiroshin [Helper]:</span>
                <span class="content"><span>нубасики</span></span>
            </div><div class="message" data-message-id="104">
                <span class="chat-timestamp">19:15 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">alexandercruel</span> has redeemed <span style="color: #780A48; font-weight: bold;">criminal</span> rank!</span></span>
            </div><div class="message" data-message-id="105">
                <span class="chat-timestamp">07:46 UTC</span>
                <span class="author" style="color: #2A9FD6">CIA:</span>
                <span class="content"><span>W Name?</span></span>
            </div><div class="message" data-message-id="106">
                <span class="chat-timestamp">05:16 UTC</span>
                <span class="author" style="color: #2A9FD6">asey:</span>
                <span class="content"><span>xxx</span></span>
            </div><div class="message" data-message-id="107">
                <span class="chat-timestamp">07:50 UTC</span>
                <span class="author" style="color: #2A9FD6">asey:</span>
                <span class="content"><span>rate my bio</span></span>
            </div><div class="message" data-message-id="108">
                <span class="chat-timestamp">16:41 UTC</span>
                <span class="author" style="color: #2A9FD6">TWOESS:</span>
                <span class="content"><span>Greetings, dear</span></span>
            </div><div class="message" data-message-id="109">
                <span class="chat-timestamp">16:42 UTC</span>
                <span class="author" style="color: #2A9FD6">TWOESS:</span>
                <span class="content"><span>Нормально ты «kiroshin»</span></span>
            </div><div class="message" data-message-id="110">
                <span class="chat-timestamp">16:42 UTC</span>
                <span class="author" style="color: #2A9FD6">TWOESS:</span>
                <span class="content"><span>Нормально ты «kiroshin»</span></span>
            </div><div class="message" data-message-id="111">
                <span class="chat-timestamp">09:42 UTC</span>
                <span class="author" style="color: #2A9FD6">Danya:</span>
                <span class="content"><span>Всем привет</span></span>
            </div><div class="message" data-message-id="112">
                <span class="chat-timestamp">09:42 UTC</span>
                <span class="author" style="color: #2A9FD6">Danya:</span>
                <span class="content"><span>У меня украли крупную сумму денег</span></span>
            </div><div class="message" data-message-id="113">
                <span class="chat-timestamp">09:42 UTC</span>
                <span class="author" style="color: #2A9FD6">Danya:</span>
                <span class="content"><span>У меня украли деньги и кто поможет мне получит все деньги</span></span>
            </div><div class="message" data-message-id="114">
                <span class="chat-timestamp">01:29 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>дарова пацунчики вы как</span></span>
            </div><div class="message" data-message-id="115">
                <span class="chat-timestamp">01:29 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>дарова пацунчики вы как</span></span>
            </div><div class="message" data-message-id="116">
                <span class="chat-timestamp">11:16 UTC</span>
                <span class="author" style="color: #2A9FD6">Youkazzov:</span>
                <span class="content"><span>Только не щокс</span></span>
            </div><div class="message" data-message-id="117">
                <span class="chat-timestamp">11:17 UTC</span>
                <span class="author" style="color: #2A9FD6">Youkazzov:</span>
                <span class="content"><span>Докс не</span></span>
            </div><div class="message" data-message-id="118">
                <span class="chat-timestamp">11:17 UTC</span>
                <span class="author" style="color: #2A9FD6">Youkazzov:</span>
                <span class="content"><span>Не докс</span></span>
            </div><div class="message" data-message-id="120">
                <span class="chat-timestamp">12:23 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">Nicotine [Mod]:</span>
                <span class="content"><span>hi chat</span></span>
            </div><div class="message" data-message-id="121">
                <span class="chat-timestamp">12:24 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>helo</span></span>
            </div><div class="message" data-message-id="122">
                <span class="chat-timestamp">12:25 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>how r u mr mod</span></span>
            </div><div class="message" data-message-id="123">
                <span class="chat-timestamp">12:25 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">Nicotine [Mod]:</span>
                <span class="content"><span>great, thanks for checkin</span></span>
            </div><div class="message" data-message-id="124">
                <span class="chat-timestamp">12:25 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">Nicotine [Mod]:</span>
                <span class="content"><span>hub?</span></span>
            </div><div class="message" data-message-id="125">
                <span class="chat-timestamp">12:26 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">Nicotine [Mod]:</span>
                <span class="content"><span>*hbu</span></span>
            </div><div class="message" data-message-id="126">
                <span class="chat-timestamp">12:27 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>:)</span></span>
            </div><div class="message" data-message-id="127">
                <span class="chat-timestamp">12:27 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>wdym hub</span></span>
            </div><div class="message" data-message-id="128">
                <span class="chat-timestamp">12:27 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">Nicotine [Mod]:</span>
                <span class="content"><span>i mean how about u..?</span></span>
            </div><div class="message" data-message-id="129">
                <span class="chat-timestamp">12:27 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>oh im gud ty for askin</span></span>
            </div><div class="message" data-message-id="130">
                <span class="chat-timestamp">12:28 UTC</span>
                <span class="author" style="color: #2A9FD6">fwddasdsadsaads:</span>
                <span class="content"><span>nigga</span></span>
            </div><div class="message" data-message-id="132">
                <span class="chat-timestamp">15:51 UTC</span>
                <span class="author" style="color: #2A9FD6">Doffy:</span>
                <span class="content"><span>Yo</span></span>
            </div><div class="message" data-message-id="133">
                <span class="chat-timestamp">15:52 UTC</span>
                <span class="author" style="color: #2A9FD6">Doffy:</span>
                <span class="content"><span>Guys who can help to delete account to one girl who said bad things about Jesus</span></span>
            </div><div class="message" data-message-id="133">
                <span class="chat-timestamp">19:13 UTC</span>
                <span class="author" style="color: #2A9FD6">Pigeon:</span>
                <span class="content"><span>you dont</span></span>
            </div><div class="message" data-message-id="134">
                <span class="chat-timestamp">00:14 UTC</span>
                <span class="author" style="color: #FFD700; font-weight: bold; background-image: url('/static/gold.gif');">root [Rich]:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="135">
                <span class="chat-timestamp">15:28 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>hey guys!</span></span>
            </div><div class="message" data-message-id="136">
                <span class="chat-timestamp">15:37 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #BB1E64">xxqv</span> [Council]:</span>
                <span class="content"><span>yo guys</span></span>
            </div><div class="message" data-message-id="137">
                <span class="chat-timestamp">15:51 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>meow</span></span>
            </div><div class="message" data-message-id="137">
                <span class="chat-timestamp">03:12 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>hello guys</span></span>
            </div><div class="message" data-message-id="138">
                <span class="chat-timestamp">03:12 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>buh</span></span>
            </div><div class="message" data-message-id="139">
                <span class="chat-timestamp">12:33 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Is this just doxbin? I feel like it</span></span>
            </div><div class="message" data-message-id="140">
                <span class="chat-timestamp">12:33 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Like did you guys atop doxbin to put up ghostbin</span></span>
            </div><div class="message" data-message-id="141">
                <span class="chat-timestamp">21:59 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>we are ghostbin</span></span>
            </div><div class="message" data-message-id="142">
                <span class="chat-timestamp">22:03 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Like also doxbin???</span></span>
            </div><div class="message" data-message-id="143">
                <span class="chat-timestamp">00:47 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Yo can you delete my dox of the CIA please someone who can</span></span>
            </div><div class="message" data-message-id="144">
                <span class="chat-timestamp">00:48 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Can some one take down my dox CIA one</span></span>
            </div><div class="message" data-message-id="145">
                <span class="chat-timestamp">00:48 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Can some one take down my dox of the CIA</span></span>
            </div><div class="message" data-message-id="146">
                <span class="chat-timestamp">00:48 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="147">
                <span class="chat-timestamp">00:48 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>qq</span></span>
            </div><div class="message" data-message-id="148">
                <span class="chat-timestamp">00:49 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>HElp</span></span>
            </div><div class="message" data-message-id="149">
                <span class="chat-timestamp">00:49 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>why lmao</span></span>
            </div><div class="message" data-message-id="150">
                <span class="chat-timestamp">00:50 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I feel bad for doxxing them</span></span>
            </div><div class="message" data-message-id="151">
                <span class="chat-timestamp">00:50 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I don't want to go to jail</span></span>
            </div><div class="message" data-message-id="152">
                <span class="chat-timestamp">00:50 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>TAKE IT DOWN</span></span>
            </div><div class="message" data-message-id="153">
                <span class="chat-timestamp">00:50 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>you can't go to jail for doxxing someone who's above 18</span></span>
            </div><div class="message" data-message-id="154">
                <span class="chat-timestamp">00:51 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>this entire site is protected under the 1st amendment</span></span>
            </div><div class="message" data-message-id="155">
                <span class="chat-timestamp">00:51 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>What?</span></span>
            </div><div class="message" data-message-id="156">
                <span class="chat-timestamp">00:51 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>your fine homie</span></span>
            </div><div class="message" data-message-id="157">
                <span class="chat-timestamp">00:51 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>In the us</span></span>
            </div><div class="message" data-message-id="158">
                <span class="chat-timestamp">00:51 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>+they can't even find you here</span></span>
            </div><div class="message" data-message-id="159">
                <span class="chat-timestamp">00:51 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I am fu*king dumb</span></span>
            </div><div class="message" data-message-id="160">
                <span class="chat-timestamp">00:51 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I am fu*king dumb</span></span>
            </div><div class="message" data-message-id="161">
                <span class="chat-timestamp">00:51 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>We don't comply with the feds</span></span>
            </div><div class="message" data-message-id="162">
                <span class="chat-timestamp">00:51 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I can tell</span></span>
            </div><div class="message" data-message-id="163">
                <span class="chat-timestamp">00:52 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I applyed for councli</span></span>
            </div><div class="message" data-message-id="164">
                <span class="chat-timestamp">00:52 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>Yeah we don't give your info out to the feds</span></span>
            </div><div class="message" data-message-id="165">
                <span class="chat-timestamp">00:52 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>We tell them to fuck off</span></span>
            </div><div class="message" data-message-id="166">
                <span class="chat-timestamp">00:52 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>This is just doxbin?</span></span>
            </div><div class="message" data-message-id="167">
                <span class="chat-timestamp">00:52 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>In a diff name?</span></span>
            </div><div class="message" data-message-id="168">
                <span class="chat-timestamp">00:52 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>pretty much yeah</span></span>
            </div><div class="message" data-message-id="169">
                <span class="chat-timestamp">00:52 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>mb</span></span>
            </div><div class="message" data-message-id="170">
                <span class="chat-timestamp">00:52 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>we have the same policies</span></span>
            </div><div class="message" data-message-id="171">
                <span class="chat-timestamp">00:52 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Same owners?</span></span>
            </div><div class="message" data-message-id="172">
                <span class="chat-timestamp">00:52 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>no</span></span>
            </div><div class="message" data-message-id="173">
                <span class="chat-timestamp">00:52 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Because Doxbin I cant find</span></span>
            </div><div class="message" data-message-id="174">
                <span class="chat-timestamp">00:53 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>on the web</span></span>
            </div><div class="message" data-message-id="175">
                <span class="chat-timestamp">00:54 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>why don't you paste?</span></span>
            </div><div class="message" data-message-id="176">
                <span class="chat-timestamp">00:54 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>just haven't made any recently to post on here</span></span>
            </div><div class="message" data-message-id="177">
                <span class="chat-timestamp">00:55 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Ok</span></span>
            </div><div class="message" data-message-id="178">
                <span class="chat-timestamp">00:55 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Ok</span></span>
            </div><div class="message" data-message-id="179">
                <span class="chat-timestamp">00:56 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>The CIA was hunting out for ghostbin</span></span>
            </div><div class="message" data-message-id="180">
                <span class="chat-timestamp">00:56 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>and doxbin</span></span>
            </div><div class="message" data-message-id="181">
                <span class="chat-timestamp">00:56 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>so I doxxed</span></span>
            </div><div class="message" data-message-id="182">
                <span class="chat-timestamp">00:57 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>your a good boy</span></span>
            </div><div class="message" data-message-id="183">
                <span class="chat-timestamp">00:59 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>thank you</span></span>
            </div><div class="message" data-message-id="184">
                <span class="chat-timestamp">00:59 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>thank you</span></span>
            </div><div class="message" data-message-id="185">
                <span class="chat-timestamp">08:11 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">Nicotine [Mod]:</span>
                <span class="content"><span>contact legal support if u want to remove your dox</span></span>
            </div><div class="message" data-message-id="186">
                <span class="chat-timestamp">12:07 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>ok</span></span>
            </div><div class="message" data-message-id="187">
                <span class="chat-timestamp">12:07 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>ok</span></span>
            </div><div class="message" data-message-id="188">
                <span class="chat-timestamp">12:14 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Pigeon is my pookie&lt;3</span></span>
            </div><div class="message" data-message-id="189">
                <span class="chat-timestamp">12:15 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>new phone who dis</span></span>
            </div><div class="message" data-message-id="190">
                <span class="chat-timestamp">12:17 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Me</span></span>
            </div><div class="message" data-message-id="191">
                <span class="chat-timestamp">12:18 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>the guy who doxxed the CIA director</span></span>
            </div><div class="message" data-message-id="192">
                <span class="chat-timestamp">12:19 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>your good boy</span></span>
            </div><div class="message" data-message-id="193">
                <span class="chat-timestamp">12:26 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>Me?</span></span>
            </div><div class="message" data-message-id="194">
                <span class="chat-timestamp">14:42 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>If you want?</span></span>
            </div><div class="message" data-message-id="195">
                <span class="chat-timestamp">14:42 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>If you want?</span></span>
            </div><div class="message" data-message-id="196">
                <span class="chat-timestamp">16:09 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>Sern</span></span>
            </div><div class="message" data-message-id="197">
                <span class="chat-timestamp">16:09 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>add me on telegram</span></span>
            </div><div class="message" data-message-id="198">
                <span class="chat-timestamp">16:09 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>@godofopsec</span></span>
            </div><div class="message" data-message-id="199">
                <span class="chat-timestamp">16:18 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I got banned</span></span>
            </div><div class="message" data-message-id="200">
                <span class="chat-timestamp">16:18 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>getting unbanned at the end of the year</span></span>
            </div><div class="message" data-message-id="201">
                <span class="chat-timestamp">17:58 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>just make a new account lmao</span></span>
            </div><div class="message" data-message-id="202">
                <span class="chat-timestamp">18:03 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I CANT FOR SOMERESON</span></span>
            </div><div class="message" data-message-id="203">
                <span class="chat-timestamp">18:03 UTC</span>
                <span class="author" style="color: #5555FF; font-weight: bold;">kiroshin [Helper]:</span>
                <span class="content"><span>салам епт</span></span>
            </div><div class="message" data-message-id="204">
                <span class="chat-timestamp">18:03 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>What</span></span>
            </div><div class="message" data-message-id="205">
                <span class="chat-timestamp">18:04 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>All staff is my pookie idk they still are</span></span>
            </div><div class="message" data-message-id="206">
                <span class="chat-timestamp">18:10 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I am in school rn lol</span></span>
            </div><div class="message" data-message-id="207">
                <span class="chat-timestamp">18:13 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Pigeon&lt;3</span></span>
            </div><div class="message" data-message-id="208">
                <span class="chat-timestamp">18:13 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>lol</span></span>
            </div><div class="message" data-message-id="209">
                <span class="chat-timestamp">18:19 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>xxqv&lt;3</span></span>
            </div><div class="message" data-message-id="210">
                <span class="chat-timestamp">18:23 UTC</span>
                <span class="author" style="color: #66B2FF; font-weight: bold; background-image: url('/static/gold.gif');">kolsfed [Founder]:</span>
                <span class="content"><span>✌️</span></span>
            </div><div class="message" data-message-id="211">
                <span class="chat-timestamp">21:10 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Wsg</span></span>
            </div><div class="message" data-message-id="212">
                <span class="chat-timestamp">21:10 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>OMG FOUNDER.</span></span>
            </div><div class="message" data-message-id="213">
                <span class="chat-timestamp">21:12 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I &lt;3 all staff</span></span>
            </div><div class="message" data-message-id="214">
                <span class="chat-timestamp">21:37 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>💀</span></span>
            </div><div class="message" data-message-id="215">
                <span class="chat-timestamp">21:39 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>what??&gt;</span></span>
            </div><div class="message" data-message-id="216">
                <span class="chat-timestamp">21:39 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I &lt;3 you to</span></span>
            </div><div class="message" data-message-id="217">
                <span class="chat-timestamp">21:42 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I AM BOREDD</span></span>
            </div><div class="message" data-message-id="218">
                <span class="chat-timestamp">21:42 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>what's your discord</span></span>
            </div><div class="message" data-message-id="219">
                <span class="chat-timestamp">21:43 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I got banned for doxxed a mod</span></span>
            </div><div class="message" data-message-id="220">
                <span class="chat-timestamp">21:43 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>sadly</span></span>
            </div><div class="message" data-message-id="221">
                <span class="chat-timestamp">21:43 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>what's your signal</span></span>
            </div><div class="message" data-message-id="222">
                <span class="chat-timestamp">21:43 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>what?</span></span>
            </div><div class="message" data-message-id="223">
                <span class="chat-timestamp">21:44 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>the app signal</span></span>
            </div><div class="message" data-message-id="224">
                <span class="chat-timestamp">21:44 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>sorry I am new to computers and things</span></span>
            </div><div class="message" data-message-id="225">
                <span class="chat-timestamp">21:44 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>download the app signal on your phone</span></span>
            </div><div class="message" data-message-id="226">
                <span class="chat-timestamp">21:44 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>it's like telegram but safer</span></span>
            </div><div class="message" data-message-id="227">
                <span class="chat-timestamp">21:46 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>MY MOM BLOCKED IT I GOT TEAMS</span></span>
            </div><div class="message" data-message-id="228">
                <span class="chat-timestamp">21:46 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>DANG I JUST WANT TO USE GOOGLE FREELY</span></span>
            </div><div class="message" data-message-id="229">
                <span class="chat-timestamp">21:47 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>TS shitty vpn</span></span>
            </div><div class="message" data-message-id="230">
                <span class="chat-timestamp">21:47 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>bro ain't no way</span></span>
            </div><div class="message" data-message-id="231">
                <span class="chat-timestamp">21:47 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>how old are you</span></span>
            </div><div class="message" data-message-id="232">
                <span class="chat-timestamp">21:47 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>💀</span></span>
            </div><div class="message" data-message-id="233">
                <span class="chat-timestamp">21:47 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>14 years old</span></span>
            </div><div class="message" data-message-id="234">
                <span class="chat-timestamp">21:48 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>what can you install</span></span>
            </div><div class="message" data-message-id="235">
                <span class="chat-timestamp">21:48 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>idk teams telegram and discord I am getting at the end of the year</span></span>
            </div><div class="message" data-message-id="236">
                <span class="chat-timestamp">21:49 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I have teams but I hate that</span></span>
            </div><div class="message" data-message-id="237">
                <span class="chat-timestamp">21:49 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I have teams but I hate that</span></span>
            </div><div class="message" data-message-id="238">
                <span class="chat-timestamp">21:49 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>you can't install signal?</span></span>
            </div><div class="message" data-message-id="239">
                <span class="chat-timestamp">21:49 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I am working on bypassing her thing</span></span>
            </div><div class="message" data-message-id="240">
                <span class="chat-timestamp">21:50 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>No it says unable to install</span></span>
            </div><div class="message" data-message-id="242">
                <span class="chat-timestamp">21:52 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I HATE THIS</span></span>
            </div><div class="message" data-message-id="243">
                <span class="chat-timestamp">21:54 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I am bored</span></span>
            </div><div class="message" data-message-id="244">
                <span class="chat-timestamp">21:54 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I am bored</span></span>
            </div><div class="message" data-message-id="245">
                <span class="chat-timestamp">21:55 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Get Teams and add me ig</span></span>
            </div><div class="message" data-message-id="246">
                <span class="chat-timestamp">21:59 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>done</span></span>
            </div><div class="message" data-message-id="247">
                <span class="chat-timestamp">21:59 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>w</span></span>
            </div><div class="message" data-message-id="247">
                <span class="chat-timestamp">07:57 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>Sern +rep</span></span>
            </div><div class="message" data-message-id="248">
                <span class="chat-timestamp">14:50 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Thank you</span></span>
            </div><div class="message" data-message-id="249">
                <span class="chat-timestamp">14:50 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Add me on teams</span></span>
            </div><div class="message" data-message-id="250">
                <span class="chat-timestamp">15:23 UTC</span>
                <span class="author" style="color: #5555FF; font-weight: bold;">kiroshin [Helper]:</span>
                <span class="content"><span>HI</span></span>
            </div><div class="message" data-message-id="252">
                <span class="chat-timestamp">15:26 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="253">
                <span class="chat-timestamp">15:26 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="254">
                <span class="chat-timestamp">15:56 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>xxqv add me on teams</span></span>
            </div><div class="message" data-message-id="255">
                <span class="chat-timestamp">16:25 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>on microsoft teams?</span></span>
            </div><div class="message" data-message-id="256">
                <span class="chat-timestamp">16:28 UTC</span>
                <span class="author" style="color: #66B2FF; font-weight: bold; background-image: url('/static/gold.gif');">kolsfed [Founder]:</span>
                <span class="content"><span>hi sern</span></span>
            </div><div class="message" data-message-id="256">
                <span class="chat-timestamp">16:29 UTC</span>
                <span class="author" style="color: #66B2FF; font-weight: bold; background-image: url('/static/gold.gif');">kolsfed [Founder]:</span>
                <span class="content"><span>how are you?</span></span>
            </div><div class="message" data-message-id="257">
                <span class="chat-timestamp">16:46 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>xxqv yes</span></span>
            </div><div class="message" data-message-id="258">
                <span class="chat-timestamp">16:47 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hekki kolsfed</span></span>
            </div><div class="message" data-message-id="259">
                <span class="chat-timestamp">16:47 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hello*</span></span>
            </div><div class="message" data-message-id="260">
                <span class="chat-timestamp">16:47 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>i have not microsoft teams</span></span>
            </div><div class="message" data-message-id="261">
                <span class="chat-timestamp">16:47 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>i have not microsoft teams</span></span>
            </div><div class="message" data-message-id="262">
                <span class="chat-timestamp">16:47 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>make a Microsoft acc</span></span>
            </div><div class="message" data-message-id="263">
                <span class="chat-timestamp">16:47 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>lol why is sending 2</span></span>
            </div><div class="message" data-message-id="264">
                <span class="chat-timestamp">16:47 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>yes wait</span></span>
            </div><div class="message" data-message-id="265">
                <span class="chat-timestamp">16:47 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>idk</span></span>
            </div><div class="message" data-message-id="266">
                <span class="chat-timestamp">16:48 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I am good kolsfed</span></span>
            </div><div class="message" data-message-id="267">
                <span class="chat-timestamp">16:51 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>lol i cant make a microsoft account</span></span>
            </div><div class="message" data-message-id="268">
                <span class="chat-timestamp">16:51 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Why???</span></span>
            </div><div class="message" data-message-id="269">
                <span class="chat-timestamp">16:51 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Asking for a number???</span></span>
            </div><div class="message" data-message-id="270">
                <span class="chat-timestamp">16:52 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>Yes</span></span>
            </div><div class="message" data-message-id="271">
                <span class="chat-timestamp">16:52 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>yes</span></span>
            </div><div class="message" data-message-id="272">
                <span class="chat-timestamp">16:53 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>i have not cash for a number</span></span>
            </div><div class="message" data-message-id="273">
                <span class="chat-timestamp">16:53 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>np I got you</span></span>
            </div><div class="message" data-message-id="274">
                <span class="chat-timestamp">16:53 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>there is a lot of methods</span></span>
            </div><div class="message" data-message-id="275">
                <span class="chat-timestamp">16:55 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>OMG I APPLYED FOR COUNCLI I AM STiLL WAITING FOR IT DID I PASS?</span></span>
            </div><div class="message" data-message-id="276">
                <span class="chat-timestamp">16:56 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>The CEO is Not active……..</span></span>
            </div><div class="message" data-message-id="277">
                <span class="chat-timestamp">16:56 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>who is the CEO admin???</span></span>
            </div><div class="message" data-message-id="278">
                <span class="chat-timestamp">16:57 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>is admin the CEO</span></span>
            </div><div class="message" data-message-id="279">
                <span class="chat-timestamp">16:59 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>yes bro</span></span>
            </div><div class="message" data-message-id="280">
                <span class="chat-timestamp">16:59 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>damn</span></span>
            </div><div class="message" data-message-id="281">
                <span class="chat-timestamp">17:00 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>How tf you dox Donald Trmup lol</span></span>
            </div><div class="message" data-message-id="282">
                <span class="chat-timestamp">17:03 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Did you make a account</span></span>
            </div><div class="message" data-message-id="283">
                <span class="chat-timestamp">17:04 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>Donald Trump dox is esay</span></span>
            </div><div class="message" data-message-id="284">
                <span class="chat-timestamp">17:04 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>this man have all emails and numbers in his cloud</span></span>
            </div><div class="message" data-message-id="285">
                <span class="chat-timestamp">17:06 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>your rightt</span></span>
            </div><div class="message" data-message-id="286">
                <span class="chat-timestamp">17:06 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Donald Trump sucks he's a nazi fr</span></span>
            </div><div class="message" data-message-id="287">
                <span class="chat-timestamp">17:27 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>Donald Trump is a child  Gooner [Pedo]</span></span>
            </div><div class="message" data-message-id="288">
                <span class="chat-timestamp">17:30 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I know</span></span>
            </div><div class="message" data-message-id="289">
                <span class="chat-timestamp">17:37 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I made some proxy links</span></span>
            </div><div class="message" data-message-id="290">
                <span class="chat-timestamp">17:40 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I am boreddddddddddddddddddddddddd</span></span>
            </div><div class="message" data-message-id="291">
                <span class="chat-timestamp">17:43 UTC</span>
                <span class="author" style="color: #66B2FF; font-weight: bold; background-image: url('/static/gold.gif');">kolsfed [Founder]:</span>
                <span class="content"><span>⚰️</span></span>
            </div><div class="message" data-message-id="292">
                <span class="chat-timestamp">17:43 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="293">
                <span class="chat-timestamp">17:43 UTC</span>
                <span class="author" style="color: #66B2FF; font-weight: bold; background-image: url('/static/gold.gif');">kolsfed [Founder]:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="294">
                <span class="chat-timestamp">17:43 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>wyd</span></span>
            </div><div class="message" data-message-id="295">
                <span class="chat-timestamp">17:44 UTC</span>
                <span class="author" style="color: #66B2FF; font-weight: bold; background-image: url('/static/gold.gif');">kolsfed [Founder]:</span>
                <span class="content"><span>work</span></span>
            </div><div class="message" data-message-id="296">
                <span class="chat-timestamp">17:48 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>yo guys</span></span>
            </div><div class="message" data-message-id="297">
                <span class="chat-timestamp">17:49 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>yeah???</span></span>
            </div><div class="message" data-message-id="298">
                <span class="chat-timestamp">18:12 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>The site updating no more council apps open</span></span>
            </div><div class="message" data-message-id="299">
                <span class="chat-timestamp">19:15 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>sadly</span></span>
            </div><div class="message" data-message-id="300">
                <span class="chat-timestamp">19:33 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="301">
                <span class="chat-timestamp">20:20 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>I have a fever lol......</span></span>
            </div><div class="message" data-message-id="302">
                <span class="chat-timestamp">20:25 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>LOOLLLLKK</span></span>
            </div><div class="message" data-message-id="303">
                <span class="chat-timestamp">20:25 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>lowkey tuff bro .....</span></span>
            </div><div class="message" data-message-id="304">
                <span class="chat-timestamp">20:28 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>10/10 Not Ragebait</span></span>
            </div><div class="message" data-message-id="305">
                <span class="chat-timestamp">20:32 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>ok?</span></span>
            </div><div class="message" data-message-id="306">
                <span class="chat-timestamp">20:38 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">Nicotine [Mod]:</span>
                <span class="content"><span>HI chat</span></span>
            </div><div class="message" data-message-id="307">
                <span class="chat-timestamp">20:39 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>HIIII</span></span>
            </div><div class="message" data-message-id="308">
                <span class="chat-timestamp">20:40 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">Nicotine [Mod]:</span>
                <span class="content"><span>hows goin Sern</span></span>
            </div><div class="message" data-message-id="309">
                <span class="chat-timestamp">20:42 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Good you?</span></span>
            </div><div class="message" data-message-id="310">
                <span class="chat-timestamp">20:42 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Good you?</span></span>
            </div><div class="message" data-message-id="311">
                <span class="chat-timestamp">20:43 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">Nicotine [Mod]:</span>
                <span class="content"><span>good, im just checkin around</span></span>
            </div><div class="message" data-message-id="312">
                <span class="chat-timestamp">20:44 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I am waiting for the results of the Council app</span></span>
            </div><div class="message" data-message-id="313">
                <span class="chat-timestamp">21:17 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>council apply is closed......</span></span>
            </div><div class="message" data-message-id="314">
                <span class="chat-timestamp">21:29 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I know sadly now</span></span>
            </div><div class="message" data-message-id="315">
                <span class="chat-timestamp">22:23 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>yoo manes</span></span>
            </div><div class="message" data-message-id="316">
                <span class="chat-timestamp">23:07 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="317">
                <span class="chat-timestamp">11:15 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>yo guys</span></span>
            </div><div class="message" data-message-id="318">
                <span class="chat-timestamp">11:15 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>how to doxxing lollllllll</span></span>
            </div><div class="message" data-message-id="319">
                <span class="chat-timestamp">11:53 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>haii</span></span>
            </div><div class="message" data-message-id="320">
                <span class="chat-timestamp">12:06 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>is this the same amnesia from /submit</span></span>
            </div><div class="message" data-message-id="321">
                <span class="chat-timestamp">13:01 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hello</span></span>
            </div><div class="message" data-message-id="322">
                <span class="chat-timestamp">14:07 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span><a href="discord.gg/unblock" target="_blank" onclick="window.location.href='discord.gg/unblock'; return false;" style="color: #2A9FD6; text-decoration: none;">discord.gg/unblock</a></span></span>
            </div><div class="message" data-message-id="323">
                <span class="chat-timestamp">16:59 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hello</span></span>
            </div><div class="message" data-message-id="324">
                <span class="chat-timestamp">20:34 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>iam sleeping lol</span></span>
            </div><div class="message" data-message-id="325">
                <span class="chat-timestamp">23:27 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>that's good</span></span>
            </div><div class="message" data-message-id="326">
                <span class="chat-timestamp">01:48 UTC</span>
                <span class="author" style="color: #2A9FD6">yen:</span>
                <span class="content"><span>yo</span></span>
            </div><div class="message" data-message-id="327">
                <span class="chat-timestamp">01:48 UTC</span>
                <span class="author" style="color: #2A9FD6">yen:</span>
                <span class="content"><span>yo</span></span>
            </div><div class="message" data-message-id="328">
                <span class="chat-timestamp">06:11 UTC</span>
                <span class="author" style="color: #2A9FD6">Stari4ok:</span>
                <span class="content"><span>Сап всем, новую задачу надо?</span></span>
            </div><div class="message" data-message-id="329">
                <span class="chat-timestamp">06:12 UTC</span>
                <span class="author" style="color: #2A9FD6">Stari4ok:</span>
                <span class="content"><span>У меня есть номер телефона парня который издевается над девочками младше его самого</span></span>
            </div><div class="message" data-message-id="330">
                <span class="chat-timestamp">10:25 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>Ready For the Netflix Ceo dox?</span></span>
            </div><div class="message" data-message-id="331">
                <span class="chat-timestamp">12:11 UTC</span>
                <span class="author" style="color: #2A9FD6">TheListick:</span>
                <span class="content"><span>парни как доксить?</span></span>
            </div><div class="message" data-message-id="332">
                <span class="chat-timestamp">12:58 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>zzqv yessssssssssssssssssssssssssssssssssss</span></span>
            </div><div class="message" data-message-id="333">
                <span class="chat-timestamp">14:15 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>W dox xxqv</span></span>
            </div><div class="message" data-message-id="334">
                <span class="chat-timestamp">14:45 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>haii</span></span>
            </div><div class="message" data-message-id="335">
                <span class="chat-timestamp">17:23 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>haiiiiiii</span></span>
            </div><div class="message" data-message-id="336">
                <span class="chat-timestamp">18:33 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>yo guys</span></span>
            </div><div class="message" data-message-id="337">
                <span class="chat-timestamp">18:34 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>i have a new spoofed telegram number</span></span>
            </div><div class="message" data-message-id="338">
                <span class="chat-timestamp">18:49 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>cool</span></span>
            </div><div class="message" data-message-id="339">
                <span class="chat-timestamp">19:46 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>what just happened</span></span>
            </div><div class="message" data-message-id="340">
                <span class="chat-timestamp">19:58 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hello guys</span></span>
            </div><div class="message" data-message-id="341">
                <span class="chat-timestamp">19:58 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hello to who ever is on</span></span>
            </div><div class="message" data-message-id="342">
                <span class="chat-timestamp">20:05 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>HOA got updated</span></span>
            </div><div class="message" data-message-id="343">
                <span class="chat-timestamp">20:15 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">Pigeon [Council]:</span>
                <span class="content"><span>meow</span></span>
            </div><div class="message" data-message-id="344">
                <span class="chat-timestamp">20:24 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hellloooooo</span></span>
            </div><div class="message" data-message-id="345">
                <span class="chat-timestamp">03:41 UTC</span>
                <span class="author" style="color: #2A9FD6">Jakeyk84:</span>
                <span class="content"><span>Hello, wanting any information available on my long term partner Nicole Maree fernandez plz</span></span>
            </div><div class="message" data-message-id="346">
                <span class="chat-timestamp">12:50 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Jakey what]</span></span>
            </div><div class="message" data-message-id="347">
                <span class="chat-timestamp">12:53 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>yo</span></span>
            </div><div class="message" data-message-id="348">
                <span class="chat-timestamp">12:53 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>Jakey its not deep</span></span>
            </div><div class="message" data-message-id="349">
                <span class="chat-timestamp">12:54 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>lol</span></span>
            </div><div class="message" data-message-id="350">
                <span class="chat-timestamp">19:14 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I AM BOREDDDDDDDDDDDDDDDDDDDDD</span></span>
            </div><div class="message" data-message-id="351">
                <span class="chat-timestamp">19:48 UTC</span>
                <span class="author" style="color: #2A9FD6">amenezinow:</span>
                <span class="content"><span>ку</span></span>
            </div><div class="message" data-message-id="352">
                <span class="chat-timestamp">22:03 UTC</span>
                <span class="author" style="color: #2A9FD6">IIIIIIII:</span>
                <span class="content"><span>1207281793531772978</span></span>
            </div><div class="message" data-message-id="353">
                <span class="chat-timestamp">23:19 UTC</span>
                <span class="author" style="color: #2A9FD6">fxckreal:</span>
                <span class="content"><span>куку</span></span>
            </div><div class="message" data-message-id="354">
                <span class="chat-timestamp">23:19 UTC</span>
                <span class="author" style="color: #2A9FD6">fxckreal:</span>
                <span class="content"><span>как у вас дела</span></span>
            </div><div class="message" data-message-id="355">
                <span class="chat-timestamp">23:40 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Ummm</span></span>
            </div><div class="message" data-message-id="356">
                <span class="chat-timestamp">12:56 UTC</span>
                <span class="author" style="color: #2A9FD6">ilikeeatingkids:</span>
                <span class="content"><span>yo</span></span>
            </div><div class="message" data-message-id="357">
                <span class="chat-timestamp">12:56 UTC</span>
                <span class="author" style="color: #2A9FD6">ilikeeatingkids:</span>
                <span class="content"><span>how do u dox</span></span>
            </div><div class="message" data-message-id="358">
                <span class="chat-timestamp">14:14 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>ummmmmmm</span></span>
            </div><div class="message" data-message-id="359">
                <span class="chat-timestamp">14:15 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>We dont really teach</span></span>
            </div><div class="message" data-message-id="360">
                <span class="chat-timestamp">14:55 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>yo guys</span></span>
            </div><div class="message" data-message-id="361">
                <span class="chat-timestamp">14:55 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>yo guys</span></span>
            </div><div class="message" data-message-id="362">
                <span class="chat-timestamp">15:16 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>yeah</span></span>
            </div><div class="message" data-message-id="363">
                <span class="chat-timestamp">15:16 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hello xxqv</span></span>
            </div><div class="message" data-message-id="364">
                <span class="chat-timestamp">20:17 UTC</span>
                <span class="author" style="color: #2A9FD6">hw:</span>
                <span class="content"><span>xd</span></span>
            </div><div class="message" data-message-id="365">
                <span class="chat-timestamp">20:17 UTC</span>
                <span class="author" style="color: #2A9FD6">hw:</span>
                <span class="content"><span>xd</span></span>
            </div><div class="message" data-message-id="366">
                <span class="chat-timestamp">22:59 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>helllllllo</span></span>
            </div><div class="message" data-message-id="367">
                <span class="chat-timestamp">23:18 UTC</span>
                <span class="author" style="color: #2A9FD6">Administrator:</span>
                <span class="content"><span>helo</span></span>
            </div><div class="message" data-message-id="368">
                <span class="chat-timestamp">11:19 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="369">
                <span class="chat-timestamp">14:07 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #94FAAC">Pigeon</span> [Council]:</span>
                <span class="content"><span>yo</span></span>
            </div><div class="message" data-message-id="370">
                <span class="chat-timestamp">15:07 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>helllololo</span></span>
            </div><div class="message" data-message-id="371">
                <span class="chat-timestamp">22:04 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">Cardiopatophobia</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="372">
                <span class="chat-timestamp">01:19 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');">Lucifer [Admin]:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="373">
                <span class="chat-timestamp">03:45 UTC</span>
                <span class="author" style="color: #bb71e4; font-weight: bold; background-image: url('/static/purple.gif');">wtf [Manager]:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="374">
                <span class="chat-timestamp">12:15 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>hi guys</span></span>
            </div><div class="message" data-message-id="375">
                <span class="chat-timestamp">08:41 UTC</span>
                <span class="author" style="color: #2A9FD6">ukoz:</span>
                <span class="content"><span>hello guys</span></span>
            </div><div class="message" data-message-id="376">
                <span class="chat-timestamp">08:41 UTC</span>
                <span class="author" style="color: #2A9FD6">ukoz:</span>
                <span class="content"><span>help me pls</span></span>
            </div><div class="message" data-message-id="377">
                <span class="chat-timestamp">08:41 UTC</span>
                <span class="author" style="color: #2A9FD6">ukoz:</span>
                <span class="content"><span>how to  get partners with doxbin</span></span>
            </div><div class="message" data-message-id="378">
                <span class="chat-timestamp">11:29 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">xxqv [Council]:</span>
                <span class="content"><span>yo guys</span></span>
            </div><div class="message" data-message-id="379">
                <span class="chat-timestamp">12:08 UTC</span>
                <span class="author" style="color: #bb71e4; font-weight: bold; background-image: url('/static/purple.gif');">wtf [Manager]:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="380">
                <span class="chat-timestamp">15:27 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hi guysss</span></span>
            </div><div class="message" data-message-id="381">
                <span class="chat-timestamp">18:28 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #FFFFFF">kiroshin</span> [Council]:</span>
                <span class="content"><span>салам епт</span></span>
            </div><div class="message" data-message-id="382">
                <span class="chat-timestamp">18:20 UTC</span>
                <span class="author" style="color: #2A9FD6">Xrayy:</span>
                <span class="content"><span>дайте норм логгер</span></span>
            </div><div class="message" data-message-id="383">
                <span class="chat-timestamp">11:31 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #9B318E; font-weight: bold;">soundcloud</span> has redeemed <span style="color: #780A48; font-weight: bold;">criminal</span> rank!</span></span>
            </div><div class="message" data-message-id="384">
                <span class="chat-timestamp">11:32 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">xyecoc</span> has redeemed <span style="color: #780A48; font-weight: bold;">criminal</span> rank!</span></span>
            </div><div class="message" data-message-id="385">
                <span class="chat-timestamp">11:33 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">9miceDev</span> has redeemed <span style="color: #780A48; font-weight: bold;">criminal</span> rank!</span></span>
            </div><div class="message" data-message-id="386">
                <span class="chat-timestamp">12:18 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">Administrator</span> has redeemed <span style="color: #780A48; font-weight: bold;">criminal</span> rank!</span></span>
            </div><div class="message" data-message-id="387">
                <span class="chat-timestamp">12:18 UTC</span>
                <span class="author" style="color: #780A48; font-weight: bold;">Administrator [Criminal]:</span>
                <span class="content"><span>when enjoying :)</span></span>
            </div><div class="message" data-message-id="388">
                <span class="chat-timestamp">12:19 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">angeI</span> has redeemed <span style="color: #780A48; font-weight: bold;">criminal</span> rank!</span></span>
            </div><div class="message" data-message-id="389">
                <span class="chat-timestamp">14:47 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="390">
                <span class="chat-timestamp">19:41 UTC</span>
                <span class="author" style="color: #2A9FD6">Arthas:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="391">
                <span class="chat-timestamp">19:41 UTC</span>
                <span class="author" style="color: #2A9FD6">Arthas:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="392">
                <span class="chat-timestamp">21:09 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hello</span></span>
            </div><div class="message" data-message-id="393">
                <span class="chat-timestamp">01:44 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I doxxed the Director of the FBI</span></span>
            </div><div class="message" data-message-id="394">
                <span class="chat-timestamp">08:21 UTC</span>
                <span class="author" style="color: #2A9FD6">federal:</span>
                <span class="content"><span>and whats the point</span></span>
            </div><div class="message" data-message-id="395">
                <span class="chat-timestamp">12:36 UTC</span>
                <span class="author" style="color: #2A9FD6">teslonomi:</span>
                <span class="content"><span>ребята привет</span></span>
            </div><div class="message" data-message-id="396">
                <span class="chat-timestamp">12:36 UTC</span>
                <span class="author" style="color: #2A9FD6">teslonomi:</span>
                <span class="content"><span>можете помочь кто то?</span></span>
            </div><div class="message" data-message-id="397">
                <span class="chat-timestamp">12:36 UTC</span>
                <span class="author" style="color: #2A9FD6">teslonomi:</span>
                <span class="content"><span>на пацанчика инфу нарыть нужно</span></span>
            </div><div class="message" data-message-id="398">
                <span class="chat-timestamp">12:36 UTC</span>
                <span class="author" style="color: #2A9FD6">teslonomi:</span>
                <span class="content"><span>к девочкам молодым не ровно дышит</span></span>
            </div><div class="message" data-message-id="399">
                <span class="chat-timestamp">12:36 UTC</span>
                <span class="author" style="color: #2A9FD6">teslonomi:</span>
                <span class="content"><span><a href="https://vk.com/ivangeta" target="_blank" onclick="window.location.href='https://vk.com/ivangeta'; return false;" style="color: #2A9FD6; text-decoration: none;">https://vk.com/ivangeta</a></span></span>
            </div><div class="message" data-message-id="400">
                <span class="chat-timestamp">13:26 UTC</span>
                <span class="author" style="color: #2A9FD6">necro:</span>
                <span class="content"><span>нет</span></span>
            </div><div class="message" data-message-id="401">
                <span class="chat-timestamp">13:27 UTC</span>
                <span class="author" style="color: #2A9FD6">necro:</span>
                <span class="content"><span>пидора ответ</span></span>
            </div><div class="message" data-message-id="402">
                <span class="chat-timestamp">13:27 UTC</span>
                <span class="author" style="color: #2A9FD6">necro:</span>
                <span class="content"><span>а</span></span>
            </div><div class="message" data-message-id="403">
                <span class="chat-timestamp">13:27 UTC</span>
                <span class="author" style="color: #2A9FD6">necro:</span>
                <span class="content"><span>а</span></span>
            </div><div class="message" data-message-id="404">
                <span class="chat-timestamp">15:32 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>привет милашки</span></span>
            </div><div class="message" data-message-id="405">
                <span class="chat-timestamp">17:10 UTC</span>
                <span class="author" style="color: #2A9FD6">anontos:</span>
                <span class="content"><span>qq</span></span>
            </div><div class="message" data-message-id="406">
                <span class="chat-timestamp">17:59 UTC</span>
                <span class="author" style="color: #2A9FD6">necros:</span>
                <span class="content"><span>q</span></span>
            </div><div class="message" data-message-id="407">
                <span class="chat-timestamp">19:02 UTC</span>
                <span class="author" style="color: #2A9FD6">punisher:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="408">
                <span class="chat-timestamp">19:03 UTC</span>
                <span class="author" style="color: #2A9FD6">punisher:</span>
                <span class="content"><span>How are you?</span></span>
            </div><div class="message" data-message-id="409">
                <span class="chat-timestamp">19:04 UTC</span>
                <span class="author" style="color: #2A9FD6">punisher:</span>
                <span class="content"><span>I hope this forum will make it to the top!</span></span>
            </div><div class="message" data-message-id="410">
                <span class="chat-timestamp">21:17 UTC</span>
                <span class="author" style="color: #2A9FD6">unforgetable:</span>
                <span class="content"><span>саламалейкум!</span></span>
            </div><div class="message" data-message-id="411">
                <span class="chat-timestamp">21:17 UTC</span>
                <span class="author" style="color: #2A9FD6">unforgetable:</span>
                <span class="content"><span>саламалейкум!</span></span>
            </div><div class="message" data-message-id="412">
                <span class="chat-timestamp">21:17 UTC</span>
                <span class="author" style="color: #2A9FD6">unforgetable:</span>
                <span class="content"><span>Саламалейкум!</span></span>
            </div><div class="message" data-message-id="413">
                <span class="chat-timestamp">02:15 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hello</span></span>
            </div><div class="message" data-message-id="414">
                <span class="chat-timestamp">03:43 UTC</span>
                <span class="author" style="color: #2A9FD6">byebardexsa:</span>
                <span class="content"><span>qq all</span></span>
            </div><div class="message" data-message-id="415">
                <span class="chat-timestamp">03:53 UTC</span>
                <span class="author" style="color: #2A9FD6">Voidx:</span>
                <span class="content"><span>Uo</span></span>
            </div><div class="message" data-message-id="416">
                <span class="chat-timestamp">08:19 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #9B318E; font-weight: bold;">monikoshisten</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="417">
                <span class="chat-timestamp">10:47 UTC</span>
                <span class="author" style="color: #2A9FD6">federal:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="418">
                <span class="chat-timestamp">12:10 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">federal</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="419">
                <span class="chat-timestamp">13:14 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>gng</span></span>
            </div><div class="message" data-message-id="420">
                <span class="chat-timestamp">13:14 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Crowned</span></span>
            </div><div class="message" data-message-id="421">
                <span class="chat-timestamp">13:37 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #9B318E; font-weight: bold;">Aventador</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="422">
                <span class="chat-timestamp">17:33 UTC</span>
                <span class="author" style="color: #2A9FD6">byebardexsa:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="423">
                <span class="chat-timestamp">17:54 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #9B318E; font-weight: bold;">pancreasis</span> has redeemed <span style="color: #FFD700; font-weight: bold;">rich</span> rank!</span></span>
            </div><div class="message" data-message-id="424">
                <span class="chat-timestamp">18:02 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hellloo</span></span>
            </div><div class="message" data-message-id="425">
                <span class="chat-timestamp">18:07 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>OMG CROWNED YOU GOT MOD!!!!</span></span>
            </div><div class="message" data-message-id="426">
                <span class="chat-timestamp">18:07 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>GOOD FOR YOUUUUUUUUUUUU</span></span>
            </div><div class="message" data-message-id="427">
                <span class="chat-timestamp">18:07 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');">kysev1 [Admin]:</span>
                <span class="content"><span>ahahaha</span></span>
            </div><div class="message" data-message-id="428">
                <span class="chat-timestamp">18:08 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="429">
                <span class="chat-timestamp">18:08 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>OMG and ADMIN</span></span>
            </div><div class="message" data-message-id="430">
                <span class="chat-timestamp">18:08 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');">kysev1 [Admin]:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="431">
                <span class="chat-timestamp">18:08 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>HELLLOOOOO</span></span>
            </div><div class="message" data-message-id="432">
                <span class="chat-timestamp">18:08 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>love this site</span></span>
            </div><div class="message" data-message-id="433">
                <span class="chat-timestamp">18:08 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');">kysev1 [Admin]:</span>
                <span class="content"><span>thx &lt;3</span></span>
            </div><div class="message" data-message-id="434">
                <span class="chat-timestamp">18:08 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>wyd rn</span></span>
            </div><div class="message" data-message-id="435">
                <span class="chat-timestamp">18:10 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #08f008; font-weight: bold;">Crowned</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="436">
                <span class="chat-timestamp">18:24 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Stop skids</span></span>
            </div><div class="message" data-message-id="437">
                <span class="chat-timestamp">18:24 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Crowned just did 70 doxs</span></span>
            </div><div class="message" data-message-id="438">
                <span class="chat-timestamp">18:31 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">fate</span> has redeemed <span style="color: #FFD700; font-weight: bold;">rich</span> rank!</span></span>
            </div><div class="message" data-message-id="439">
                <span class="chat-timestamp">18:42 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Fate you got rich rank good for you</span></span>
            </div><div class="message" data-message-id="440">
                <span class="chat-timestamp">18:43 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #9B318E; font-weight: bold;">Aventador</span> has redeemed <span style="color: #FFD700; font-weight: bold;">rich</span> rank!</span></span>
            </div><div class="message" data-message-id="441">
                <span class="chat-timestamp">18:44 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Aventador too</span></span>
            </div><div class="message" data-message-id="442">
                <span class="chat-timestamp">19:29 UTC</span>
                <span class="author" style="color: #2A9FD6">Plasmaguy:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="443">
                <span class="chat-timestamp">19:43 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #FFD700; font-weight: bold;">qqtyler</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="444">
                <span class="chat-timestamp">19:44 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #FFD700; font-weight: bold;">dmg</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="445">
                <span class="chat-timestamp">19:50 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hello</span></span>
            </div><div class="message" data-message-id="446">
                <span class="chat-timestamp">20:04 UTC</span>
                <span class="author" style="color: #2A9FD6">Plasmaguy:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="447">
                <span class="chat-timestamp">20:12 UTC</span>
                <span class="author" style="color: #2A9FD6">Plasmaguy:</span>
                <span class="content"><span>i love this so mouch</span></span>
            </div><div class="message" data-message-id="448">
                <span class="chat-timestamp">20:46 UTC</span>
                <span class="author" style="color: #2A9FD6">xkf:</span>
                <span class="content"><span>hi guys</span></span>
            </div><div class="message" data-message-id="449">
                <span class="chat-timestamp">20:47 UTC</span>
                <span class="author" style="color: #2A9FD6">xkf:</span>
                <span class="content"><span>Is there an active community here?</span></span>
            </div><div class="message" data-message-id="450">
                <span class="chat-timestamp">21:58 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>yes</span></span>
            </div><div class="message" data-message-id="451">
                <span class="chat-timestamp">21:59 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>We have a very active com I will send at least one dox every week</span></span>
            </div><div class="message" data-message-id="452">
                <span class="chat-timestamp">22:00 UTC</span>
                <span class="author" style="color: #2A9FD6">Arthas:</span>
                <span class="content"><span>More or less, in my opinion, yes. Compared to DB</span></span>
            </div><div class="message" data-message-id="453">
                <span class="chat-timestamp">02:31 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I am a former Doxbin mod</span></span>
            </div><div class="message" data-message-id="454">
                <span class="chat-timestamp">02:56 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #94FAAC">Pigeon</span> [Council]:</span>
                <span class="content"><span>skull</span></span>
            </div><div class="message" data-message-id="455">
                <span class="chat-timestamp">05:03 UTC</span>
                <span class="author" style="color: #66B2FF; font-weight: bold; background-image: url('/static/gold.gif');">Lucifer [Founder]:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="456">
                <span class="chat-timestamp">05:03 UTC</span>
                <span class="author" style="color: #66B2FF; font-weight: bold; background-image: url('/static/gold.gif');">Lucifer [Founder]:</span>
                <span class="content"><span>anybody active</span></span>
            </div><div class="message" data-message-id="457">
                <span class="chat-timestamp">17:07 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #94FAAC">Pigeon</span> [Council]:</span>
                <span class="content"><span>yo</span></span>
            </div><div class="message" data-message-id="460">
                <span class="chat-timestamp">17:20 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>закройся</span></span>
            </div><div class="message" data-message-id="463">
                <span class="chat-timestamp">17:21 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>зам заткни</span></span>
            </div><div class="message" data-message-id="465">
                <span class="chat-timestamp">17:21 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>ладно тогда просто скажи мяу :3</span></span>
            </div><div class="message" data-message-id="467">
                <span class="chat-timestamp">17:22 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>не надо затыкаться тогда</span></span>
            </div><div class="message" data-message-id="468">
                <span class="chat-timestamp">17:22 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>ты первый</span></span>
            </div><div class="message" data-message-id="469">
                <span class="chat-timestamp">21:08 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #FFFFFF">Kiroshin</span> [Council]:</span>
                <span class="content"><span>шо вы</span></span>
            </div><div class="message" data-message-id="470">
                <span class="chat-timestamp">05:59 UTC</span>
                <span class="author" style="color: #2A9FD6"><span style="color: #365DDA">federal</span>:</span>
                <span class="content"><span>larp <a href="lucifer.run" target="_blank" onclick="window.location.href='lucifer.run'; return false;" style="color: #2A9FD6; text-decoration: none;">lucifer.run</a> here oh my days</span></span>
            </div><div class="message" data-message-id="471">
                <span class="chat-timestamp">07:17 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>mama am i a good boy</span></span>
            </div><div class="message" data-message-id="472">
                <span class="chat-timestamp">09:38 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">Nicotine [Mod]:</span>
                <span class="content"><span>Hi chat</span></span>
            </div><div class="message" data-message-id="473">
                <span class="chat-timestamp">09:39 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>hi cuties</span></span>
            </div><div class="message" data-message-id="474">
                <span class="chat-timestamp">09:40 UTC</span>
                <span class="author" style="color: #08f008; font-weight: bold;">Nicotine [Mod]:</span>
                <span class="content"><span>sup amnesia</span></span>
            </div><div class="message" data-message-id="475">
                <span class="chat-timestamp">09:42 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>how ru</span></span>
            </div><div class="message" data-message-id="476">
                <span class="chat-timestamp">10:32 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #FFFFFF">dmg</span> [Council]:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="477">
                <span class="chat-timestamp">11:26 UTC</span>
                <span class="author" style="color: #2A9FD6">necroworld:</span>
                <span class="content"><span>Hello everyone, I've found a Russian pedophile, what can I do with him?</span></span>
            </div><div class="message" data-message-id="478">
                <span class="chat-timestamp">11:27 UTC</span>
                <span class="author" style="color: #2A9FD6">necroworld:</span>
                <span class="content"><span>It's a pity that Skype stopped working. I could have called a police squad to his place, but there are no options</span></span>
            </div><div class="message" data-message-id="480">
                <span class="chat-timestamp">11:31 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #FFFFFF">dmg</span> [Council]:</span>
                <span class="content"><span>Hi. Try sending a message to police, or call</span></span>
            </div><div class="message" data-message-id="481">
                <span class="chat-timestamp">11:37 UTC</span>
                <span class="author" style="color: #2A9FD6">necroworld:</span>
                <span class="content"><span>Okay, I'd like to increase the punishment.   The man is 46 years old, and he stalked a 15-year-old girl and threatened to rape and stab her.</span></span>
            </div><div class="message" data-message-id="482">
                <span class="chat-timestamp">12:15 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #FFFFFF">dmg</span> [Council]:</span>
                <span class="content"><span>In this case, you can call his parents, I don't know.</span></span>
            </div><div class="message" data-message-id="477">
                <span class="chat-timestamp">12:20 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #365DDA">hector</span> was temporarily muted for 1 hour.</span></span>
            </div><div class="message" data-message-id="478">
                <span class="chat-timestamp">15:05 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hello</span></span>
            </div><div class="message" data-message-id="480">
                <span class="chat-timestamp">15:51 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #FFFFFF">dmg</span> [Council]:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="479">
                <span class="chat-timestamp">16:48 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>hai</span></span>
            </div><div class="message" data-message-id="480">
                <span class="chat-timestamp">21:58 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');"><span style="color: #FFFFFF">Admin</span> [Admin]:</span>
                <span class="content"><span>⌃_⌃</span></span>
            </div><div class="message" data-message-id="481">
                <span class="chat-timestamp">06:41 UTC</span>
                <span class="author" style="color: #2A9FD6">necroworld:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="482">
                <span class="chat-timestamp">14:51 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #FFFFFF">dmg</span> [Council]:</span>
                <span class="content"><span>wasted</span></span>
            </div><div class="message" data-message-id="483">
                <span class="chat-timestamp">17:30 UTC</span>
                <span class="author" style="color: #2A9FD6">wasted:</span>
                <span class="content"><span>hi</span></span>
            </div><div class="message" data-message-id="484">
                <span class="chat-timestamp">10:34 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>hai</span></span>
            </div><div class="message" data-message-id="485">
                <span class="chat-timestamp">12:12 UTC</span>
                <span class="author" style="color: #2A9FD6">wasted:</span>
                <span class="content"><span>тут вообще есть русские?</span></span>
            </div><div class="message" data-message-id="486">
                <span class="chat-timestamp">12:33 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #FFFFFF">dmg</span> [Council]:</span>
                <span class="content"><span>есть)</span></span>
            </div><div class="message" data-message-id="487">
                <span class="chat-timestamp">16:03 UTC</span>
                <span class="author" style="color: #2A9FD6">wasted:</span>
                <span class="content"><span>о</span></span>
            </div><div class="message" data-message-id="488">
                <span class="chat-timestamp">20:29 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hello</span></span>
            </div><div class="message" data-message-id="489">
                <span class="chat-timestamp">21:06 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #5555FF; font-weight: bold;">Crowned</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="490">
                <span class="chat-timestamp">21:06 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">rr</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="491">
                <span class="chat-timestamp">21:06 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #780A48; font-weight: bold;">soundcloud</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="492">
                <span class="chat-timestamp">21:07 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">jackroot</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="493">
                <span class="chat-timestamp">21:07 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">antagonist</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="494">
                <span class="chat-timestamp">21:07 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #9B318E; font-weight: bold;">rr</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="495">
                <span class="chat-timestamp">21:07 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">antagonist</span> has redeemed <span style="color: #9B318E; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="496">
                <span class="chat-timestamp">21:07 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #9B318E; font-weight: bold;">mvdmail</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="497">
                <span class="chat-timestamp">21:07 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #9B318E; font-weight: bold;">jackroot</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="498">
                <span class="chat-timestamp">21:08 UTC</span>
                <span class="author" style="color: #9B318E; font-weight: bold;"><span style="color: #FF69B4">rr</span> [VIP]:</span>
                <span class="content"><span>W</span></span>
            </div><div class="message" data-message-id="499">
                <span class="chat-timestamp">21:08 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">User123Hacker</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="500">
                <span class="chat-timestamp">21:09 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">User123Hacker</span> has redeemed <span style="color: #FF69B4; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="501">
                <span class="chat-timestamp">21:09 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #780A48; font-weight: bold;">runet</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="502">
                <span class="chat-timestamp">21:10 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold; background-image: url('/static/red.gif');"><span style="color: #FFFFFF">Admin</span> [Admin]:</span>
                <span class="content"><span>🎄</span></span>
            </div><div class="message" data-message-id="503">
                <span class="chat-timestamp">21:14 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">adddd</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="504">
                <span class="chat-timestamp">21:14 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">adddd</span> has redeemed <span style="color: #FF69B4; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="505">
                <span class="chat-timestamp">21:15 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #2a9fd6; font-weight: bold;">yaw</span> has redeemed <span style="color: #FF69B4; font-weight: bold;">vip</span> rank!</span></span>
            </div><div class="message" data-message-id="506">
                <span class="chat-timestamp">21:15 UTC</span>
                <span class="author" style="color: #ff0000; font-weight: bold;">Ghostbin [System]:</span>
                <span class="content"><span><span style="color: #FF69B4; font-weight: bold;">yaw</span> has redeemed <span style="color: #8e949c; font-weight: bold;">colorchanges</span> rank!</span></span>
            </div><div class="message" data-message-id="507">
                <span class="chat-timestamp">21:19 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #FFFFFF">dmg</span> [Council]:</span>
                <span class="content"><span>это че за снег</span></span>
            </div><div class="message" data-message-id="508">
                <span class="chat-timestamp">21:19 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #FFFFFF">dmg</span> [Council]:</span>
                <span class="content"><span>о чат норммально работать начал</span></span>
            </div><div class="message" data-message-id="509">
                <span class="chat-timestamp">21:19 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #FFFFFF">dmg</span> [Council]:</span>
                <span class="content"><span>победа</span></span>
            </div><div class="message" data-message-id="510">
                <span class="chat-timestamp">22:35 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>мяу</span></span>
            </div><div class="message" data-message-id="511">
                <span class="chat-timestamp">23:18 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Xmas yeahhhhhhhhhhhh</span></span>
            </div><div class="message" data-message-id="512">
                <span class="chat-timestamp">23:18 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Xmas yeahhhhhhhhhhhh</span></span>
            </div><div class="message" data-message-id="513">
                <span class="chat-timestamp">23:18 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>I love ghostbin on here everyday</span></span>
            </div><div class="message" data-message-id="514">
                <span class="chat-timestamp">09:12 UTC</span>
                <span class="author" style="color: #2A9FD6">DimaKandreshkov:</span>
                <span class="content"><span>.</span></span>
            </div><div class="message" data-message-id="515">
                <span class="chat-timestamp">09:16 UTC</span>
                <span class="author" style="color: #2A9FD6">DimaKandreshkov:</span>
                <span class="content"><span>Привет всём</span></span>
            </div><div class="message" data-message-id="516">
                <span class="chat-timestamp">09:21 UTC</span>
                <span class="author" style="color: #2A9FD6">DimaKandreshkov:</span>
                <span class="content"><span>Hi</span></span>
            </div><div class="message" data-message-id="517">
                <span class="chat-timestamp">10:38 UTC</span>
                <span class="author" style="color: #5555FF; font-weight: bold;"><span style="color: #FFFFFF">mvdmail</span> [Helper]:</span>
                <span class="content"><span>Hi</span></span>
            </div><div class="message" data-message-id="518">
                <span class="chat-timestamp">12:08 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hekki</span></span>
            </div><div class="message" data-message-id="519">
                <span class="chat-timestamp">12:08 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>Hello</span></span>
            </div><div class="message" data-message-id="520">
                <span class="chat-timestamp">12:34 UTC</span>
                <span class="author" style="color: #2A9FD6">wasted:</span>
                <span class="content"><span>с кем можно поговорить</span></span>
            </div><div class="message" data-message-id="521">
                <span class="chat-timestamp">12:34 UTC</span>
                <span class="author" style="color: #2A9FD6">wasted:</span>
                <span class="content"><span>скучно оч</span></span>
            </div><div class="message" data-message-id="522">
                <span class="chat-timestamp">14:20 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;"><span style="color: #FFFFFF">dmg</span> [Council]:</span>
                <span class="content"><span>с рукой поговори</span></span>
            </div><div class="message" data-message-id="523">
                <span class="chat-timestamp">18:46 UTC</span>
                <span class="author" style="color: #9B318E; font-weight: bold;"><span style="color: #FF69B4">rr</span> [VIP]:</span>
                <span class="content"><span>yoo</span></span>
            </div><div class="message" data-message-id="524">
                <span class="chat-timestamp">19:43 UTC</span>
                <span class="author" style="color: #2A9FD6">Lord00:</span>
                <span class="content"><span>может типа кто докснуть?</span></span>
            </div><div class="message" data-message-id="525">
                <span class="chat-timestamp">20:37 UTC</span>
                <span class="author" style="color: #2A9FD6">colins:</span>
                <span class="content"><span>здарова</span></span>
            </div><div class="message" data-message-id="526">
                <span class="chat-timestamp">20:57 UTC</span>
                <span class="author" style="color: #2A9FD6">colins:</span>
                <span class="content"><span>эй чувакы</span></span>
            </div><div class="message" data-message-id="527">
                <span class="chat-timestamp">22:04 UTC</span>
                <span class="author" style="color: #2A9FD6">Sern:</span>
                <span class="content"><span>hello</span></span>
            </div><div class="message" data-message-id="528">
                <span class="chat-timestamp">22:04 UTC</span>
                <span class="author" style="color: #87cefa; font-weight: bold;">amnesia [Council]:</span>
                <span class="content"><span>hi</span></span>
            </div></div>
    <div class="chat-input-container">
        <input type="text" class="chat-input" id="messageInput" placeholder="Message Ghostbin" maxlength="200">
        <button class="chat-send-btn" onclick="sendMessage()">Send</button>
    </div>
</div>

<div id="chatSettingsModal" class="chat-msg-modal">
    <div class="chat-msg-modal-content" style="max-width: 300px;">
        <h3 style="color: #fff; margin: 0 0 20px 0; font-size: 16px;">Chat Settings</h3>
        <div class="chat-msg-button-container" style="gap: 15px;">
            <div style="display: flex; justify-content: space-between; align-items: center;">
                <span style="color: #fff;">Enable Chat</span>
                <label class="switch">
                    <input type="checkbox" id="chatEnabledToggle">
                    <span class="slider"></span>
                </label>
            </div>
        </div>
    </div>
</div>

<div class="chat-msg-modal" id="chatMessageModal" onclick="closeMessageModal(event)">
    <div class="chat-msg-modal-content">
        <div id="chat-msg-info"></div>
        <div class="chat-msg-button-container">
            <button id="chatBanMessageBtn" class="chat-msg-button" onclick="chatBanUser()" style="display: none;">Mute</button>
            <button id="chatDeleteMessageBtn" class="chat-msg-button" onclick="deleteSelectedMessage()" style="display: none;">Delete</button>
            <button id="chatVisitProfileBtn" class="chat-msg-button" onclick="visitProfile()" style="display: none;"></button>
            <button id="chatCopyMessageIdBtn" class="chat-msg-button" onclick="copyMessageId(this.dataset.messageId)" style="display: none;">Copy Message ID</button>
        </div>
    </div>
</div>

<script>
    let selectedMessage = null;

    window.isStaff = false;
    window.authenticatedUsername = 'None';

    function toggleChat() {
        const container = document.querySelector('.chat-container');
        container.classList.toggle('hidden');
        localStorage.setItem('chatWindowOpen', !container.classList.contains('hidden'));
        if (!container.classList.contains('hidden')) {
            document.getElementById('messageInput').focus();
            const chatMessages = document.getElementById('chatMessages');
            chatMessages.scrollTop = chatMessages.scrollHeight;
        }
    }

    document.addEventListener('DOMContentLoaded', function() {
        const chatOpen = localStorage.getItem('chatWindowOpen') === true;
        const container = document.querySelector('.chat-container');
        if (chatOpen) {
            container.classList.remove('hidden');
            const chatMessages = document.getElementById('chatMessages');
            chatMessages.scrollTop = chatMessages.scrollHeight;
        }

        const chatHeader = document.querySelector('.chat-header');
        const chatInputContainer = document.querySelector('.chat-input-container');
        
        [chatHeader, chatInputContainer].forEach(element => {
            element.addEventListener('touchmove', function(e) {
                e.preventDefault();
                e.stopPropagation();
            }, { passive: false });
            
            element.addEventListener('wheel', function(e) {
                e.preventDefault();
                e.stopPropagation();
            }, { passive: false });
        });

        const messageInput = document.getElementById('messageInput');
        messageInput.addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                sendMessage();
            }
        });
        loadMessages();
    });

    async function loadMessages() {
        const chatMessages = document.getElementById('chatMessages');

        const response = await fetch('/api/messages');
        if (!response.ok) {
            throw new Error(`Ошибка загрузки: ${response.status}`);
        }

        const data = await response.json();
        const messages = data.messages || [];

        messages.reverse().forEach(message => {
            addMessageToChat(message);
        });

        chatMessages.scrollTop = chatMessages.scrollHeight;
    }

    function sendMessage() {
        const messageInput = document.getElementById('messageInput');
        const content = messageInput.value.trim();
        if (content) {
            fetch(`/api/sendMessage?content=${encodeURIComponent(content)}&clientId=${localStorage.getItem("client_id")}`, {
                method: 'POST'
            })
            .then(response => response.json())
            .then(data => {
                messageInput.value = '';
                
                const chatMessages = document.getElementById('chatMessages');
                chatMessages.scrollTop = chatMessages.scrollHeight;
                
                if (!data.success && data.error && data.remaining) {
                    const messageInput = document.getElementById('messageInput');
                    const sendButton = document.querySelector('.chat-send-btn');
                    messageInput.disabled = true;
                    sendButton.disabled = true;

                    setTimeout(() => {
                        messageInput.disabled = false;
                        sendButton.disabled = false;
                        messageInput.focus();
                    }, data.remaining);
                }
            });
        }
    }

    function addMessageToChat(message) {
        const chatMessages = document.getElementById('chatMessages');
        const messageElement = document.createElement('div');
        messageElement.className = 'message';
        messageElement.dataset.messageId = message.messageID;
        let authorStyle = '';
        let displayName = message.displayName;
        
        if (message.userID === null) {
            authorStyle = 'color: #ff0000; font-weight: bold;';
            displayName = `${displayName} [System]`;
            messageElement.innerHTML = `
                <span class="chat-timestamp">${message.createdAt}</span>
                <span class="author" style="${authorStyle}">${displayName}:</span>
                <span class="content"><span>${linkifyText(message.content, true)}</span></span>
            `;
            messageElement.addEventListener('click', function(e) {
                if (!e.target.closest('a')) {
                    showMessageModal(message, e);
                }
            });
        } else {
            if (message.userID === null) {
                authorStyle = 'color: #fff';
                displayName = `${displayName} [Anonymous]`;
            } else if (message.rankData) {
                authorStyle = message.rankData.rankStyle || '';
                if (message.usernameColor) {
                    displayName = `<span style="color: ${message.usernameColor}">${displayName}</span> ${message.rankData.suffix}`;
                } else {
                    displayName = `${displayName} ${message.rankData.suffix}`;
                }
            } else {
                authorStyle = 'color: #2A9FD6';
                if (message.usernameColor) {
                    displayName = `<span style="color: ${message.usernameColor}">${displayName}</span>`;
                }
            }
            
            const content = linkifyText(message.content);
            
            messageElement.innerHTML = `
                <span class="chat-timestamp">${message.createdAt}</span>
                <span class="author" style="${authorStyle}">${displayName}:</span>
                <span class="content"><span>${content}</span></span>
            `;
            
            messageElement.addEventListener('click', function(e) {
                if (!e.target.closest('a')) {
                    showMessageModal(message, e);
                }
            });
        }
        
        chatMessages.appendChild(messageElement);
        
        const isNearBottom = chatMessages.scrollHeight - chatMessages.clientHeight - chatMessages.scrollTop < 100;
        if (isNearBottom) {
            chatMessages.scrollTop = chatMessages.scrollHeight;
        }
    }

    function linkifyText(text, isSystem = false) {
        if (!isSystem) {
            text = escapeHtml(text);
        }

        const urlPattern = /(https?:\/\/[^\s]+)|(?<![:/])((?:[\w-]+\.)+[\w-]+(?:\/[^\s]*)?)/g;
        let processedText = text.replace(urlPattern, function(url, fullUrl, shortUrl) {
            if (url.toLowerCase().endsWith('.gif')) {
                return url;
            }
            
            return `<a href="${url}" target="_blank" onclick="window.location.href='${url}'; return false;" style="color: #2A9FD6; text-decoration: none;">${url}</a>`;
        });

        if (window.authenticatedUsername) {
            const mentionRegex = new RegExp(`(^|\\s)(@${window.authenticatedUsername})(?![^<]*>|[^<>]*<\/)`, 'gi');
            processedText = processedText.replace(mentionRegex, '$1<span style="color: #2A9FD6 !important">$2</span>');
        }

        return processedText;
    }

    function escapeHtml(text) {
        const div = document.createElement('div');
        div.textContent = text;
        return div.innerHTML;
    }

    async function deleteMessage(messageID) {
        try {
            const response = await fetch(`/api/deleteMessage?messageID=${messageID}`);
            const data = await response.json();
            if (data.success) {
                const messageElement = document.querySelector(`[data-message-id="${messageID}"]`);
                if (messageElement) {
                    messageElement.replaceWith(messageElement.cloneNode(true));
                    messageElement.remove();
                }
                const modal = document.getElementById('chatMessageModal');
                modal.classList.remove('show');
                selectedMessage = null;
            } else {
                console.error('Failed to delete message:', data.error);
            }
        } catch (error) {
            console.error('Failed to delete message:', error);
        }
    }

    function deleteSelectedMessage() {
        if (selectedMessage) {
            const messageId = selectedMessage.messageID;
            selectedMessage = null;
            deleteMessage(messageId);
        }
    }

    function showMessageModal(message, event) {
        const modal = document.getElementById('chatMessageModal');
        const messageInfo = document.getElementById('chat-msg-info');
        const chatBanBtn = document.getElementById('chatBanMessageBtn');
        const copyMessageIdBtn = document.getElementById('chatCopyMessageIdBtn');
        const visitProfileBtn = document.getElementById('chatVisitProfileBtn');
        const deleteMessageBtn = document.getElementById('chatDeleteMessageBtn');
        
        let authorStyle = '';
        let displayName = message.displayName;
        
        if (!window.isStaff || (message.userID === null)) {
            chatBanBtn.style.display = 'none';
        } else {
            chatBanBtn.style.display = 'block';
            selectedMessage = message;
        }

        if (message.userID === null) {
            authorStyle = 'color: #ff0000; font-weight: bold;';
            displayName = `${displayName} [System]`;
            messageInfo.innerHTML = `
                <div style="margin-bottom: 10px; display: flex; align-items: center; gap: 5px;">
                    <span class="chat-timestamp">${message.createdAt}</span>
                    <span class="author" style="${authorStyle}; margin: 0;">${displayName}:</span>
                </div>
                <div class="content" style="color: #fff; word-break: break-word; margin: 0;">${linkifyText(message.content, true)}</div>
            `;
            visitProfileBtn.style.display = 'none';
        } else if (message.userID === null) {
            authorStyle = 'color: #fff';
            displayName = `${displayName} [Anonymous]`;
            messageInfo.innerHTML = `
                <div style="margin-bottom: 10px; display: flex; align-items: center; gap: 5px;">
                    <span class="chat-timestamp">${message.createdAt}</span>
                    <span class="author" style="${authorStyle}; margin: 0;">${displayName}:</span>
                </div>
                <div class="content" style="color: #fff; word-break: break-word; margin: 0;">${linkifyText(escapeHtml(message.content))}</div>
            `;
            visitProfileBtn.style.display = 'none';
        } else {
            if (message.rankData) {
                authorStyle = message.rankData.rankStyle || '';
                if (message.usernameColor) {
                    displayName = `<span style="color: ${message.usernameColor}">${displayName}</span> ${message.rankData.suffix}`;
                } else {
                    displayName = `${displayName} ${message.rankData.suffix}`;
                }
            } else {
                authorStyle = 'color: #2A9FD6';
                if (message.usernameColor) {
                    displayName = `<span style="color: ${message.usernameColor}">${displayName}</span>`;
                }
            }

            messageInfo.innerHTML = `
                <div style="margin-bottom: 10px; display: flex; align-items: center; gap: 5px;">
                    <span class="chat-timestamp">${message.createdAt}</span>
                    <span class="author" style="${authorStyle}; margin: 0;">${displayName}:</span>
                </div>
                <div class="content" style="color: #fff; word-break: break-word; margin: 0;">${linkifyText(escapeHtml(message.content))}</div>
            `;
            visitProfileBtn.style.display = 'block';
            visitProfileBtn.textContent = 'View Profile';
        }

        modal.classList.add('show');
        selectedMessage = message;

        if (window.isStaff) {
            deleteMessageBtn.style.display = 'block';
        } else {
            deleteMessageBtn.style.display = 'none';
        }

        copyMessageIdBtn.style.display = 'block';
        copyMessageIdBtn.dataset.messageId = message.messageID;
    }

    function chatBanUser() {
        if (!window.isStaff || !selectedMessage) return;
        
        const params = new URLSearchParams();
        if (selectedMessage.userID !== null) {
            params.append('userID', selectedMessage.userID);
        }

        fetch(`/api/chatBan?${params.toString()}`)
            .then(response => response.json())
            .then(data => {
                if (data.success) {
                    document.getElementById('chatMessageModal').classList.remove('show');
                }
            })
            .catch(error => console.error('Error:', error));
    }

    function closeMessageModal(event) {
        const modal = document.getElementById('chatMessageModal');
        const modalContent = modal.querySelector('.chat-msg-modal-content');
        if (!modalContent.contains(event.target)) {
            modal.classList.remove('show');
            selectedMessage = null;
        }
    }

    function visitProfile() {
        if (selectedMessage && selectedMessage.userID !== null) {
            window.location.href = `/user/@${selectedMessage.displayName}`;
        }
        document.getElementById('chatMessageModal').classList.remove('show');
        selectedMessage = null;
    }

    function copyMessageId(messageId) {
        navigator.clipboard.writeText(messageId);
        const copyBtn = document.getElementById('chatCopyMessageIdBtn');
        const originalText = copyBtn.textContent;
        copyBtn.textContent = 'Copied!';
        setTimeout(() => copyBtn.textContent = originalText, 1000);
    }

    window.addEventListener('click', function(event) {
        const modal = document.getElementById('chatMessageModal');
        if (event.target === modal) {
            closeMessageModal(event);
        }
    });

    document.getElementById('chatTitle').addEventListener('click', async function() {
        if (!window.isStaff) {
            return;
        }

        const response = await fetch('/api/manageChat');
        const data = await response.json();
        
        if (data.success) {
            document.getElementById('chatEnabledToggle').checked = data.settings.chatEnabled;
            
            document.getElementById('chatSettingsModal').classList.add('show');
        }
    });

    document.getElementById('chatEnabledToggle').addEventListener('change', async function() {
        const response = await fetch(`/api/manageChat?chatEnabled=${this.checked}`);
        const data = await response.json();
        if (!data.success) {
            this.checked = !this.checked;
        }
    });

    document.getElementById('chatSettingsModal').addEventListener('click', function(event) {
        if (event.target === this) {
            this.classList.remove('show');
        }
    });
</script>
<nav class="navbar">
    <div class="container">
        <div class="nav-brand">
            <a href="/" id="site-name">Ghostbin</a>
            <div class="online-count mobile-only" style="display: none;">0</div>
        </div>
        <button class="navbar-toggler" type="button">☰</button>
        <div class="nav-wrapper">
            <ul class="nav-menu">
                <li class="active">
                    <a href="/">Home</a>
                </li>
                <li class="">
                    <a href="/upload">Add Paste</a>
                </li>
                <li class="">
                    <a href="/users">Users</a>
                </li>
                <li class="">
                    <a href="/upgrades">Upgrades</a>
                </li>
                <li class="">
                    <a href="/hoa">Hall of Autism</a>
                </li>
                <li class="">
                    <a href="/partners">Partners</a>
                </li>
                <li class="">
                    <a href="/support">Support</a>
                </li>
                <li class="">
                    <a href="/mailer">Mailer</a>
                </li>
                
            </ul>

            

            <div class="online-count desktop-only" style="display: none;">0</div>
            <div class="nav-auth">
                
                    
                    <li>
                        <a href="/login" class="">Login</a>
                    </li>
                    <li>
                        <a href="/register" class="">Register</a>
                    </li>
                    
                
            </div>
        </div>
    </div>
</nav>
<script>
    const dropdown = document.querySelector('.dropdown');
        if (dropdown) {
            dropdown.querySelector('.dropdown-toggle').addEventListener('click', function(e) {
                e.stopPropagation();
                dropdown.classList.toggle('active');
            });

            document.addEventListener('click', function(e) {
                if (!dropdown.contains(e.target)) {
                    dropdown.classList.remove('active');
                }
            });
        }

        document.querySelector('.navbar-toggler').addEventListener('click', function() {
        document.querySelector('.nav-wrapper').classList.toggle('show');
    });
</script>




<div id="notification" class="notification-container">
    <div class="notification-header">
        <div class="notification-title">Announcement</div>
        <div class="notification-close">×</div>
    </div>
    <div class="notification-body" style="font-weight: bold;">
        Subscribe a <a href="https://t.me/ghostbin_news" target="_blank" style="color: red;">telegram channel</a>.
    </div>
    <div class="notification-footer">
        <button id="notificationOk" class="notification-btn primary">OK</button>
    </div>
</div>

<script>
    document.addEventListener('DOMContentLoaded', function () {
        if (!localStorage.getItem('notificationDismissed')) {
            setTimeout(function () {
                document.getElementById('notification').classList.add('show');
            }, 2500);
        }

        const closeButtons = document.querySelectorAll('.notification-close, #notificationOk');
        closeButtons.forEach(function (btn) {
            btn.addEventListener('click', function () {
                const notification = document.getElementById('notification');
                notification.classList.remove('show');
                localStorage.setItem('notificationDismissed', true);

                setTimeout(function () {
                    notification.style.display = 'none';
                }, 300);
            });
        });
    });
</script>
<script>
    const elements = document.querySelectorAll('[id="site-name"]');

    let siteName = "";

    if (window.location.hostname === "vilebin.net") {
        siteName = "Vilebin";
    } else {
        siteName = "Ghostbin";
    }

    elements.forEach(el => {
        el.textContent = siteName;
    });
</script>


<div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 125.77%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 61.5774%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 125.923%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 5.9003%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 109.68%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.6123%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 92.8755%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.9334%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 179.349%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 20.1487%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 142.672%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 98.6464%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 75.7472%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.5546%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 76.267%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 38.2547%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.582%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.6537%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 119.674%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 68.4468%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 120.35%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 83.8979%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 78.3653%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 41.2664%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 122.046%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 40.0364%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 104.506%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.5902%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 156.294%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 39.1549%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 85.007%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.6128%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 100.367%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.0939%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 153.346%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.11204%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 84.1714%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 87.0586%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 145.378%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 51.1186%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 109.273%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 80.5807%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 112.631%; opacity: 0.4; padding: 0px; margin: 0px; font-size: 4px; line-height: 13.6px; text-align: center; vertical-align: baseline; right: 42.7809%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 108.604%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 98.1569%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 90.9996%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 79.8261%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 136.823%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 85.5378%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 117.786%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 31.6627%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 92.419%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 87.9459%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 99.5407%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 55.7306%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 103.026%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 20.8921%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 135.796%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 20.7615%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 123.473%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 74.7323%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 81.8746%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 70.3086%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 120.437%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 99.6391%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 155.389%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.1888%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 79.5542%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 79.2845%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 170.86%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.5004%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 167.872%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 42.622%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 98.1991%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.8999%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 185.239%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.3463%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 111.957%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 94.5279%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 95.5652%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 85.2545%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 88.1419%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.4426%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.407%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 44.9642%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 78.8183%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 18.9415%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.77%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 92.4483%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 169.647%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 97.4047%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 119.378%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 81.9975%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 97.6178%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 25.9906%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.114%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 25.1929%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.279%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 14.0297%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 96.8826%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 97.6471%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 141.156%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.9901%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.949%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.4486%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 126.474%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 44.2534%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 157.093%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 15.0768%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 163.247%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 17.4259%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 118.308%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 53.1749%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 127.12%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 78.0825%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 161.722%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.2742%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.21%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.1739%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 168.176%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 55.1133%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 127.357%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 64.3668%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.845%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 3.55363%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 84.9156%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 77.0407%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 115.957%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 98.805%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.41%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.2121%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.745%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 5.83614%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 139.749%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.0999%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.937%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 51.2907%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 170.607%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 14.927%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 177.72%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 27.385%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 122.699%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.9562%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 103.556%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 76.6554%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 191.632%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 27.6094%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 177.092%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 27.0483%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 143.724%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 24.5791%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 103.87%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 39.5062%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.481%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.3457%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 126.674%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 63.7486%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 190.69%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 11.2233%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.569%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 4.26487%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 147.803%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 70.5948%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 188.285%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 19.5286%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 114.226%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 81.4815%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 101.987%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 30.752%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 136.192%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 22.3345%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 145.084%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 34.119%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 161.088%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 90.2357%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.079%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.4635%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 112.971%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 47.2503%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 133.368%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 11.7845%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.485%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 22.2222%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 136.82%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 79.798%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 152.301%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 64.8709%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 178.452%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 54.5455%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 114.54%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 79.798%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 133.787%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 31.5376%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 124.163%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 17.3962%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.435%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 92.0314%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 195.921%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 74.0741%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.954%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 42.5365%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 160.879%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 19.9776%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 122.49%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 72.8395%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 162.238%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 98.9899%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.649%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.42761%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 174.791%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.8833%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 117.992%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.8227%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 155.544%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.4198%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 167.992%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 18.743%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.728%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 31.6498%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 194.665%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 96.0718%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 111.297%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.8002%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 130.649%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 93.3782%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 112.552%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.9349%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 186.297%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 58.0247%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 196.234%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 95.8474%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 110.774%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 55.8923%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.536%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 20.4265%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 126.046%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.85634%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 137.762%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 89.7868%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 105.753%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 45.2301%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 190.272%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 74.9719%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 142.05%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.2121%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 164.017%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 8.75421%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 191.527%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 71.7172%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 161.611%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 34.3434%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 197.071%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 94.8373%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 117.155%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 59.4837%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 141.736%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.29517%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 190.586%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 29.8541%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.577%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.0269%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 160.983%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 69.1358%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 164.644%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 19.9776%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 151.987%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.1201%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.778%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.0999%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.498%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 25.2525%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 111.82%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 46.5769%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.197%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 11.3356%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 141.632%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 92.2559%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.092%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.8485%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 184.31%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 14.1414%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 111.297%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 60.3816%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 183.264%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 100%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 135.146%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 78.5634%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 105.962%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 25.8137%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.64%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 47.3625%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 104.812%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.9933%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.054%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.20314%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 172.699%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 33.1089%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 195.293%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.31538%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.598%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 73.9618%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 120.816%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.3232%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.962%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 69.1358%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 121.653%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 27.9461%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.954%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.6644%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 170.188%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 93.7149%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 160.042%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 61.7284%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 161.82%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 8.41751%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 128.87%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 95.2862%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.218%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 72.3906%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.004%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 42.312%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 142.05%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 61.5039%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.046%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 20.3143%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 104.393%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.0034%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 153.138%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 93.266%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 146.13%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.4321%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 116.527%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 35.6902%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 137.029%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 60.6061%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 132.113%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.9068%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.318%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 41.6386%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.632%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.8855%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 200.732%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.63187%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.724%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 20.3143%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 109.937%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 56.4534%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 151.674%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 74.2985%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 190.9%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 29.7419%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.184%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 96.7452%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 143.201%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.0763%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 177.72%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.9349%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.812%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.4759%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 157.113%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 51.6274%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 117.364%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 81.1448%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.063%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 92.0314%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.431%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 90.5724%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.126%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 18.6308%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 143.096%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 82.6038%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 188.18%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 60.7183%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 156.381%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 27.4972%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 167.887%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 81.257%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 151.778%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 77.6655%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.305%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 66.2177%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.054%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 91.4703%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 185.46%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 54.4332%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 196.862%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 64.5342%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 151.987%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.1582%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 123.431%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 62.514%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.431%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 76.8799%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.849%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 26.3749%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.151%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 56.0045%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 177.51%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 27.6094%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.167%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 91.1336%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 145.816%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 87.8788%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 138.18%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 83.3894%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.259%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 56.4534%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 142.782%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 63.9731%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.079%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 24.3547%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.013%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 85.5219%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 175.732%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 68.1257%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 156.904%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.1033%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 188.18%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.5443%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 146.444%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.9248%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 149.163%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 69.5847%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 160.879%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 54.9944%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.046%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.3277%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 169.665%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 73.1762%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 114.958%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.0494%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.95%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 61.9529%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.414%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 98.092%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.536%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 29.5174%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 174.268%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 81.1448%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 127.51%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 68.9113%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.481%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 75.3086%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 171.757%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.3277%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 144.874%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 5.72391%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 168.096%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 97.1942%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.887%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 38.8328%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 143.724%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 76.6554%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 114.958%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.3737%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.536%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 74.4108%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.937%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.3737%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 156.695%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 61.5039%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.95%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 39.2817%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.632%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.7003%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 130.439%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 15.9371%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 181.276%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 47.587%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 169.874%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 64.3098%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 196.653%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 14.7026%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 135.669%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 61.3917%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.205%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 44.22%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.255%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.4949%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.326%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 63.2997%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.201%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.6566%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 116.004%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.3636%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 127.092%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.1751%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 169.456%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 19.6409%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.586%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 34.3434%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.632%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.1156%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 108.368%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.6566%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.552%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 89.0011%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 103.452%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 34.6801%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 146.025%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.569%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.272%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 55.3311%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 169.665%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 61.6162%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 109.1%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 56.7901%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.05%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.7946%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 169.038%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 3.81594%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 138.285%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 96.4085%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.544%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 8.19304%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 181.695%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 13.1313%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.824%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 72.3906%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 125.314%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 89.2256%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.393%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.0629%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.536%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.7104%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 149.268%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 78.2267%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.745%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.9473%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.264%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 62.6263%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 107.113%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 17.284%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.795%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 19.8653%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.013%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.3199%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 101.569%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 68.1257%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 116.109%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 33.8945%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 126.987%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 95.0617%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.335%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 39.6184%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 118.515%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 50.6173%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 160.565%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 30.5275%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 106.799%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.7497%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.389%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.3008%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 163.494%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 31.3131%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 143.724%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 27.385%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 108.891%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 90.3479%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 128.347%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 8.08081%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.406%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 66.5544%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 190.272%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 59.596%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.745%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 51.8519%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 109.937%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.8485%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 188.598%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.7194%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 103.556%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.2155%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 135.669%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 59.9327%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.167%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 99.1021%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 161.82%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.5522%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 144.247%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 13.1313%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 133.473%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.4635%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 126.046%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 69.697%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 123.222%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 96.5208%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 141.109%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 27.1605%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.527%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 31.5376%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 160.669%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 27.8339%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 133.996%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.771%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 146.13%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 29.6296%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 144.874%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 89.4501%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 149.163%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 56.9024%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 184.31%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 31.7621%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 164.54%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.2278%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 104.707%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 4.60157%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.933%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 90.9091%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 139.958%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 33.3333%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 117.155%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 42.6487%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 162.971%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 39.3939%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 152.406%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.7946%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.435%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 34.5679%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 108.264%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 18.8552%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 178.87%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 80.8081%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 137.552%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 79.6857%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 164.54%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 95.6229%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 116.423%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.4523%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.289%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 80.9203%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 175.105%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.037%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 116.004%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 17.5084%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 123.431%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 50.1684%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 135.042%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.1886%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 170.397%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 58.1369%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 167.469%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.009%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.707%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 6.06061%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 136.506%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 51.8519%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 105.23%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 31.3131%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 151.046%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 93.266%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.377%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 41.9753%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.096%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 54.9944%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 138.389%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 15.0393%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 153.138%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 33.4456%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.996%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 94.2761%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 174.582%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 29.5174%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 105.335%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.2076%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.431%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 8.19304%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 150.105%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 69.248%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 117.678%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 80.8081%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.23%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 73.2884%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 149.477%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 25.5892%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 178.87%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 96.8575%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 153.138%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 58.0247%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 112.029%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 44.8934%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 184.937%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 64.422%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.833%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 15.1515%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 115.69%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 81.5937%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 141.213%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 68.9113%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 143.933%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 60.6061%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 125.314%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 75.8698%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 175.837%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 25.1403%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.992%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 26.7116%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 136.506%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.7688%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 108.577%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 47.2503%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.063%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 73.4007%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 109.205%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 30.4153%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 169.979%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.8855%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.954%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 87.991%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 181.59%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 17.8451%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.063%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 45.5668%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.326%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.6768%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.64%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.9349%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.285%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 94.8373%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 183.473%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 95.3984%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 114.958%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 51.1785%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.845%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 44.6689%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 149.059%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 5.49944%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 149.163%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 39.3939%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 178.138%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 71.7172%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 146.757%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.9473%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.799%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 92.0314%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 190.9%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 15.7127%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 191.946%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 59.4837%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 175.209%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.835%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 156.695%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 60.0449%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 124.268%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 30.4153%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.519%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 75.8698%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 186.506%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 5.61167%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.092%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 26.8238%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 145.188%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 68.9113%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 119.979%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 58.4736%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 104.393%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 17.8451%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 101.987%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.2121%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 105.23%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 42.312%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.586%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 77.5533%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 146.967%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 30.4153%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 132.531%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.1706%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 168.724%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 96.4085%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 185.356%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 20.5387%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 138.494%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.4366%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.954%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.63187%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 145.084%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.0584%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.381%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.5645%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 104.393%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 98.9899%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 200.209%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.5881%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 200.732%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 78.4512%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.134%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 8.30527%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 172.908%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 97.9798%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.54%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 14.2536%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 160.146%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.2705%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 115.9%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 6.62177%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.728%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 31.0887%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 114.017%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 44.1077%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 125.732%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.40741%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 151.36%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 40.6285%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 170.502%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.96857%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 161.192%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 24.6914%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 133.368%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 10.2132%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 101.569%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 70.2581%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 178.243%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 70.9315%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 103.766%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 61.1672%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 132.95%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 87.3176%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 141.841%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 81.257%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 115.795%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 85.2974%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 109.623%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 70.3704%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 103.87%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 89.3378%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 150%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 48.7093%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.891%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 60.4938%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 114.226%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 56.4534%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 196.13%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 6.50954%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.515%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 100%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 136.088%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.07071%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.64%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 60.8305%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 181.799%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 50.0561%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.218%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.5701%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 174.059%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.6611%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 120.502%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 91.358%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 125.314%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 4.3771%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.126%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 98.092%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.494%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 80.3591%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 135.46%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 62.514%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 144.665%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 80.9203%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.745%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 38.7205%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 105.544%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 50.7295%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.322%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 47.6992%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 168.619%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 22.5589%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 178.87%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 73.2884%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 125.941%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.3221%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 112.971%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 99.4388%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 115.795%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.5466%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 147.28%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 63.7486%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 157.845%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 14.5903%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.833%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 71.4927%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 106.067%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 10.7744%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.536%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.5488%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 195.816%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 45.4545%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.406%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 64.8709%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.64%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 85.9708%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 200.732%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 98.4287%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.644%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 61.1672%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 121.025%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.0584%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 130.23%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 96.0718%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 128.138%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.5758%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 119.351%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 68.6869%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.703%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 42.0875%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.962%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 24.3547%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.736%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.0988%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 136.088%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.037%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 155.753%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 26.1504%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 163.703%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 20.5387%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 117.05%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 24.018%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 117.155%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.5881%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.285%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.7565%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 186.82%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.9933%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 130.753%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 64.422%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 150%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 97.0819%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 177.824%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.44%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 105.439%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.1751%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.649%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 92.8171%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 171.13%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 22.8956%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 156.695%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 64.1975%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 146.862%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 44.4444%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 116.213%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.4983%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 169.665%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.835%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.151%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.6195%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.703%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.9562%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 197.176%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 46.4646%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 188.285%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.7104%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 136.611%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 74.7475%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 172.385%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 51.0662%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 151.464%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 56.5657%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.678%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 3.47924%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 122.176%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.5466%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 112.762%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 63.0752%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 171.757%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 85.6341%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.795%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.1493%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 111.402%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 17.3962%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 115.063%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.7497%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.414%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 75.3086%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 143.305%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 30.0786%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 167.782%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 46.6891%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 110.46%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 77.89%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.59%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 27.9461%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.59%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 53.0864%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.448%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 79.9102%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 118.41%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.5466%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.201%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 3.7037%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.904%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.9966%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 144.665%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 63.1874%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 163.703%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.6105%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 105.23%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 22.6712%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.285%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.6768%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.603%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 24.5791%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 169.561%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 90.2357%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.962%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.7935%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.238%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.1582%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 147.908%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 99.3266%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 199.791%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 15.2637%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.904%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 5.49944%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 188.808%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 64.0853%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 125.314%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 74.9719%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 104.184%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.1156%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.536%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 15.2637%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.159%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 54.7699%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 162.238%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 24.2424%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 132.008%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 64.6465%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 177.929%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.6644%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.636%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.7497%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 177.406%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 48.0359%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 124.686%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 40.2918%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 156.172%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 59.7082%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.603%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 82.716%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 137.029%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 60.8305%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.577%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 94.1639%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.414%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.7935%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.05%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 50.954%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 145.921%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.42761%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 170.607%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 19.8653%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.741%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.3221%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 191.109%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.7497%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 128.661%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 18.6308%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.092%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.835%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 136.192%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 44.6689%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 179.812%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 33.3333%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 196.339%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 41.0774%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 157.113%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 55.5556%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 185.879%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.3008%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 123.849%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 8.19304%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 183.054%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.9068%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 147.071%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 46.2402%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 124.372%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 26.1504%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 109.728%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 44.4444%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 112.238%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 46.9136%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 172.28%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 68.1257%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 142.364%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 80.6958%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 167.992%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 10.101%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.736%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 13.6925%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 191.632%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 33.8945%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 142.259%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 29.6296%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.113%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 20.651%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 111.088%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 60.2694%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.987%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 33.4456%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 190.167%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 25.0281%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.184%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 93.1538%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.728%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.85634%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.762%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.9978%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.481%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 11.6723%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 156.067%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.4949%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.498%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.4523%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.272%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.7565%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 128.347%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 51.1785%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.971%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 79.2368%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 114.958%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 92.7048%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 130.335%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 40.7407%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 150.314%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 58.9226%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 171.653%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 94.725%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 167.364%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 55.4433%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.51%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 59.2593%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 163.808%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 80.0224%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 133.682%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 89.1134%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.435%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 17.9574%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.812%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 24.018%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 194.77%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 87.4299%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 119.351%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 66.6667%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 116.423%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 85.4097%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.481%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 63.6364%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.439%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 55.6678%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 116.423%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.9349%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.498%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.6072%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.703%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 96.5208%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.858%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.5477%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 184.728%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 20.7632%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 160.669%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.1392%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 108.473%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 45.0056%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 130.335%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.4983%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 155.126%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 82.9405%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.414%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 61.1672%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 115.481%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 42.0875%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 162.866%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.771%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 199.059%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 34.7924%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 186.82%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 62.963%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.954%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.4343%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 101.569%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.9068%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.623%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.1201%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.226%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 83.6139%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 179.707%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 95.9596%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 197.594%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 50.2806%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 137.866%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 59.3715%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.849%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 4.82604%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 184.623%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 34.9046%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 181.381%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 70.0337%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 199.477%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 60.7183%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.494%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 45.5668%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.481%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 69.9214%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 130.544%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 41.0774%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.226%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.2873%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 125.628%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 47.2503%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.494%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.7688%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 101.046%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 76.6554%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 118.724%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 66.1055%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 188.18%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.7104%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.828%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 18.8552%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 145.188%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.3513%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 151.464%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 62.1773%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.184%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 50.6173%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 101.151%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 13.3558%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 120.293%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 59.3715%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 119.456%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 41.3019%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 144.351%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 85.2974%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 130.649%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.96857%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 181.172%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 90.0112%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 132.741%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 8.08081%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 200.732%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 73.8496%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 114.121%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 39.9551%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 183.682%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 87.5421%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.552%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 22.6712%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 164.017%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 82.9405%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.063%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.2828%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 144.561%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.3513%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.301%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 45.0056%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 157.322%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 5.38721%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 161.925%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 38.4961%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 109.728%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 50.7295%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 147.071%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 73.7374%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 195.816%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.51964%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 191.841%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.8227%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 186.715%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 83.7262%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 139.121%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 85.8586%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 178.138%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 92.2559%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 164.854%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 69.0236%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 156.485%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 59.2593%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 170.293%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 42.4242%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.992%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.8844%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.778%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 74.523%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 162.971%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 54.8822%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.41%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 73.9618%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.067%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.31538%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 111.192%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.9439%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 142.678%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.1201%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 143.201%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.3075%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 161.506%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.6768%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.079%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 60.6061%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.762%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.0079%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 196.025%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 58.5859%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 120.397%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 91.9192%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 130.021%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 55.3311%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 190.167%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.8833%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.201%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 11.2233%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 135.983%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 90.0112%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.916%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 75.6453%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.95%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 47.138%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 119.038%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 78.3389%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 123.536%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 31.8743%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 184.833%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.3232%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 104.707%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.4949%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 120.293%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.74411%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 141.841%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 97.3064%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 157.741%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 6.62177%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 105.962%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.5522%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 191.736%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.1751%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.063%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 45.7912%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 110.042%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 4.15264%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.929%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.1156%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 125.941%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.8687%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 150.523%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 95.3984%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 109.519%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.2278%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 169.247%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 98.8777%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.845%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 41.3019%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 145.397%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 58.2492%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.23%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.3008%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.381%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 76.431%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 196.025%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 71.4927%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 112.029%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.3636%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 108.996%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 62.1773%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 142.887%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.688%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 164.226%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.6813%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.469%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 93.7149%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 130.858%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.9809%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.485%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 10.4377%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.971%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 13.468%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.544%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 94.8373%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 112.029%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 85.7464%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 186.611%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.8844%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 162.762%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 41.8631%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 124.791%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 24.8036%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.586%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 71.2682%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 153.661%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 11.1111%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.619%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 92.4804%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 188.808%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 11.6723%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 172.385%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 69.9214%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 125%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 80.0224%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 156.799%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 19.7531%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.117%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 90.4602%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 167.573%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 78.4512%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 184.519%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.5073%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 116.318%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 29.6296%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.552%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 14.4781%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 122.699%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 33.8945%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.586%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 44.6689%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 168.305%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 15.6004%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.707%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 4.15264%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 199.686%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.7497%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 152.301%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.6599%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.439%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 24.9158%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 126.569%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 38.7205%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.636%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.4321%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.916%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.4635%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 100.837%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.3513%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.515%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 35.8025%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.469%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.3075%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 184.728%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.0763%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 194.979%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.8126%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 167.573%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 11.2233%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 127.615%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 56.7901%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.063%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 94.725%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 135.879%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 18.0696%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 111.506%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 40.6285%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 130.962%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 34.119%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 107.741%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 71.2682%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.322%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.3075%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.515%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 68.0135%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 124.895%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 51.4029%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 125.418%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 46.4646%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 110.042%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 81.5937%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 172.594%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.31538%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 135.46%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 18.4063%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 157.845%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 10.5499%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 185.669%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 31.7621%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.197%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 6.84624%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 133.577%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 29.2929%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 110.146%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.5522%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 177.092%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 63.1874%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.414%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 76.2065%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.259%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 54.9944%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.778%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.3446%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 108.054%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 97.4186%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.64%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 79.0123%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 132.427%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 17.284%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.728%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 58.8103%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 146.13%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.4759%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 171.548%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 77.4411%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 194.456%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 63.4119%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.833%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 97.8676%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.172%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.569%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.54%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 19.7531%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 127.301%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 35.3535%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 119.456%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.7228%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 150.941%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 93.4905%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 197.908%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 30.9764%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 113.18%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 62.514%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.205%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 39.1695%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 132.322%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 35.4658%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.096%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 69.5847%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 128.138%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 99.4388%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.841%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 14.7026%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.577%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 90.9091%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 139.54%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.7946%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.305%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 72.615%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.887%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 58.3614%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.996%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 19.6409%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 132.218%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 71.0438%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 177.72%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 35.6902%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 137.552%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 5.83614%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 178.347%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 27.385%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.54%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.6824%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.393%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.6588%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 100.837%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 83.6139%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.079%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 48.1481%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 123.117%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 93.3782%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 153.347%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 69.9214%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 174.059%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.8844%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 118.305%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 75.8698%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 122.385%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 90.3479%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 160.565%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 70.8193%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 153.556%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 76.0943%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 191.318%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 54.5455%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 149.791%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 42.8732%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 116.946%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.29517%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 119.247%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.5758%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 132.113%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 47.0258%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.674%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 25.1403%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.636%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 70.8193%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 155.858%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 18.0696%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 170.188%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.87654%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 174.477%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 6.84624%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 171.025%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.0079%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 179.184%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 92.7048%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 114.644%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.1706%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.013%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.7194%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 156.904%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.7194%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 129.184%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 59.7082%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.632%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 91.5825%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 157.008%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 82.9405%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 103.87%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.8844%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.9%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 38.3838%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 145.293%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.9933%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.623%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 77.6655%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.063%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.4198%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.013%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 38.2716%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 175.314%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 22.8956%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.649%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 95.6229%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.301%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 29.4052%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 144.561%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.1953%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 183.577%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 97.4186%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.013%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 63.7486%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.184%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 87.4299%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 194.142%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 34.2312%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 190.272%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 40.7407%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 200.314%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 66.5544%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 107.008%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 62.7385%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.159%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 85.1852%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 186.402%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.4198%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 162.657%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.76431%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 161.297%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 96.2963%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 179.707%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 44.5567%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.41%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 93.4905%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 138.494%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 46.5769%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.749%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 51.9641%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 127.72%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.9607%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 155.962%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 13.3558%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 112.238%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 79.2368%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 123.536%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 78.4512%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.41%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 30.5275%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.393%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 98.8777%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 149.791%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 42.0875%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.674%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.3232%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 149.268%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 26.5993%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 136.925%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.42761%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 188.808%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 76.0943%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 157.636%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 8.52974%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.326%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 62.2896%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 178.452%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.9473%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 117.155%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 41.7508%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 120.921%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 72.615%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 163.494%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 64.8709%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 120.711%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 20.4265%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 184.31%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.3008%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 179.498%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.4579%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 139.644%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 33.3333%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.272%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.7733%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.64%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.7318%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 188.18%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 97.4186%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 168.515%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 92.7048%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 153.87%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.8485%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 141.946%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 46.0157%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 199.268%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.1033%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.469%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 8.97868%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.59%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 27.0483%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 119.665%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 91.6947%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 121.548%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 31.8743%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 126.778%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 58.1369%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.092%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 76.6554%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 197.699%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 60.6061%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.435%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 54.9944%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 161.402%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 46.6891%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.431%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.76431%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 123.431%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 16.6105%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 121.862%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 5.05051%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 145.816%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 78.3389%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.904%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 53.3109%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 160.983%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 68.9113%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 170.921%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 17.7329%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 174.059%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 66.8911%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 138.18%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.8316%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.866%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 29.4052%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 161.611%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 89.899%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 181.59%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 5.16274%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.519%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 21.8855%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 130.439%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.0079%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 132.845%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 78.2267%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 171.967%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 76.2065%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 183.682%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 70.3704%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.527%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 13.8047%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 165.9%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.0831%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 118.828%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 24.1302%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.958%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 6.06061%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 110.983%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.0954%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 119.979%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 13.6925%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 155.126%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 38.3838%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 103.87%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.4321%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 177.51%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 64.7587%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 119.979%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 18.8552%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.289%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 90.3479%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 181.067%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.0976%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 126.151%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 79.798%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 175.523%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 48.0359%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 151.151%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 6.06061%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.393%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 77.3288%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 164.121%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.2334%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.021%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.4523%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 173.117%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 25.0281%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.121%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 49.046%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 189.226%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 25.7015%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 174.268%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 71.4927%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 146.234%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 45.2301%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.996%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.569%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.31%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 50.1684%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 110.983%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.7722%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 155.439%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 98.8777%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.063%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 26.3749%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 151.569%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 13.5802%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 128.661%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 62.2896%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 137.238%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 57.1268%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 126.464%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 99.5511%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 151.883%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 17.0595%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 171.025%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.40741%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 142.573%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 40.0673%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.883%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 38.945%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 136.088%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.2323%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 157.845%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.0269%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 126.255%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 24.2424%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 175.941%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.96857%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 186.82%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.624%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 177.615%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 8.30527%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.866%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 36.4759%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 154.916%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 77.2166%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 185.774%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 30.9764%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 198.849%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 51.8519%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 112.866%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 91.1336%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 134.1%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 56.3412%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 194.247%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 96.1841%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 155.439%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 63.4119%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 190.063%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 68.2379%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 114.017%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 39.1695%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 199.372%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 22.6712%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 103.347%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.51964%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 110.774%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.7318%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 111.715%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 53.5354%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.063%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 26.7116%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 159.31%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.6442%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 184.31%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.53984%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 172.699%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 14.4781%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.544%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 52.0763%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 103.87%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 88.5522%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 121.653%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 91.1336%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 103.138%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 43.8833%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 146.548%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 65.6566%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 126.151%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 75.5331%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 169.456%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 75.4209%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 183.054%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.3457%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 131.904%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 11.56%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 142.155%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.3401%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 110.356%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 23.2323%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 157.427%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 10.5499%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 194.247%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 54.0965%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 193.41%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 89.3378%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 102.406%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.29517%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 166.527%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.624%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 171.967%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 51.1785%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.046%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.7363%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 153.033%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 67.9012%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 111.402%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 86.9809%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 151.36%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 10.7744%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.264%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 11.4478%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.343%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 61.2795%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 101.151%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.1706%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 122.803%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 79.9102%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 110.879%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 99.1021%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 182.113%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 71.7172%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 178.975%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 85.073%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 195.711%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 58.1369%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 187.866%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 59.596%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 144.979%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 66.5544%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 172.176%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 45.4545%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.326%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.9607%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 174.686%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 18.8552%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 123.117%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 19.4164%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 170.816%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 32.3232%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 142.155%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 14.8148%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 136.925%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 34.2312%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 176.255%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 7.40741%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 148.849%; opacity: 1; padding: 0px; margin: 0px; font-size: 16px; line-height: 10px; text-align: center; vertical-align: baseline; right: 56.1167%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 152.301%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 33.5578%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 184.414%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.87654%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 124.372%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 83.165%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.272%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 99.4388%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 167.678%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 54.0965%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 184.31%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 77.2166%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 183.787%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 37.8227%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 117.469%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 9.87654%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 194.247%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 40.1796%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 178.87%; opacity: 1; padding: 0px; margin: 0px; font-size: 12px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.1706%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 137.762%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 99.5511%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 180.23%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 4.26487%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 101.36%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 81.3692%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 101.883%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 12.2334%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 162.448%; opacity: 1; padding: 0px; margin: 0px; font-size: 20px; line-height: 10px; text-align: center; vertical-align: baseline; right: 89.2256%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 143.305%; opacity: 1; padding: 0px; margin: 0px; font-size: 18px; line-height: 10px; text-align: center; vertical-align: baseline; right: 99.5511%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 140.586%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 84.9607%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 158.996%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 28.1706%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 138.285%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 46.1279%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 170.607%; opacity: 1; padding: 0px; margin: 0px; font-size: 10px; line-height: 10px; text-align: center; vertical-align: baseline; right: 18.4063%;">•</div><div class="snowflake" style="color: rgb(255, 255, 255); position: absolute; transform: translate3d(0px, 0px, 0px); width: 8px; height: 8px; font-family: arial, verdana; cursor: default; overflow: hidden; font-weight: normal; z-index: 0; display: block; bottom: 192.573%; opacity: 1; padding: 0px; margin: 0px; font-size: 14px; line-height: 10px; text-align: center; vertical-align: baseline; right: 70.7071%;">•</div></body></html>
