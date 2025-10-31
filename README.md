<html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400..900&family=DM+Serif+Display:ital@0;1&family=Dancing+Script:wght@400..700&family=Playfair+Display:ital,wght@0,400..900;1,400..900&family=Quicksand:wght@300..700&display=swap" rel="stylesheet">
        <link rel="stylesheet" href="valentine-confession.css">
        <title>Valentine Confession</title>
    </head>
    <body>
        <p class="instruction">Click the heart!</p>
        <div class="container">
            <label>
            <div class="heart">
                <img src="https://upload.wikimedia.org/wikipedia/commons/4/42/Love_Heart_SVG.svg"></img>
            </div>
            <input id="messageState" type="checkbox" style="display:none"/>
            </label>
            <div class="message">
                <h1 style="font-family: Cinzel, serif; font-size: 40px; letter-spacing: 1.2px;">HIIII!</h1>
                <p> 
                    <span>
                        &emsp;  I’ve been meaning to tell you this for a while now, but I never really found the right time—or maybe I was just too nervous to say it. But today, I finally decided to be honest about what I feel. Every time we talk, even about small things, you somehow make my day a little brighter.
                    </span>
                    <br> <br>
                    <span>
                        &emsp;  I catch myself smiling when I think about our conversations, and honestly, I realize that I’ve started to like you—more than just a friend and I just wanted you to know how wonderful you are and how much you have come to mean to me, and I this in my heart to tell.
                    </span>      
                </p>
                <br>
                <div class="sincere">
                    <p style="font-weight: bold;"> With Love,</p>
                    <p>Your Admirer</p>
                 </div>
            </div>
        </div>
        <script src="jquery.js"></script>
        <script src="jquery2.1.js"></script>
        <script defer src="valentine-confession.js"></script>
    </body>
</html>
*{
	box-sizing: border-box;
}

h1,
p {
	font-family: "Quicksand";
  font-optical-sizing: auto;
}

h1 {
	font-weight: 200;
}

body {
	margin: 0px;
}

.instruction{
	position: absolute;
	font-size: 1.6rem;
	color: rgba(255, 0, 0, 0.554);
	top: 36%;
	left: 50%;
	transform: translate(-50%, -50%);
}

.container {
	position: relative;
	width: 100%;
	height: 100vh;
	overflow: hidden;
}

.heart {
	position: absolute;
	left: 50%;
	top: 50%;
	text-align: center;
	transform: translate(-50%, -50%);
	transition: transform 2s;
	z-index: 1;
	cursor: pointer;
}

.heart > img {
	width: 50px;
	height: auto;

	animation-name: beat;
	animation-duration: 2s;
	animation-timing-function: ease-in-out;
	animation-iteration-count: infinite;
	animation-play-state: running;
}

.message {
	padding: 25px;
	background-color: #eee;
	font-family: "Quicksand", serif;
  font-optical-sizing: auto;
	font-size: clamp(16px, 10vw, 17px);
	text-align: justify;
	line-height: 1.5em;
	width: 80%;
	max-width: 550px;
	height: 78%;
	position: absolute;
	left: 50%;
	top: 50%;
	transform: translate(-50%, -50%);
	z-index: 0;

	animation-name: openmsg;
	animation-duration: 2s;
	animation-timing-function: linear;
	animation-play-state: paused;
	animation-fill-mode: forwards;
	box-shadow: 0 10px 20px rgba(0, 0, 0, 0.19), 0 6px 6px rgba(0, 0, 0, 0.23);
	border-radius: 5px;
	overflow: scroll;
	scrollbar-width: none;
}
 
.message .sincere{
	text-align: left;
	font-family: "Cinzel, serif";
	font-size: 14px;
	line-height: 1.2em;
}

.message .sincere p{
	margin: 0;
}

@keyframes beat {
	0% {
		width: 50px;
	}
	25% {
		width: 58px;
	}
	30% {
		width: 50px;
	}
	50% {
		width: 45px;
	}
	60% {
		width: 50px;
	}
	75% {
		width: 58px;
	}
	100% {
		width: 50px;
	}
}

@keyframes openmsg {
	0% {
		height: 0px;
		padding: 0px 20px;
	}
	100% {
		height: 75%;
		padding: 20px 20px;
	}
}

@keyframes heartMove {
	0% {
		top: 50%
	}
	100% {
		top: 85%;
		transform: translate(-50%, 0);
	}
}

.openNor {
	animation-direction: normal;
	animation-play-state: running;
}

.closeNor {
	animation-direction: reverse;
	animation-play-state: running;
}

.no-anim {
	animation: none;
}

.closed {
	height: 0px;
	padding: 0px 20px;
}

.bottom {
	bottom: 5px;
}

.openHer {
	animation-name: heartMove;
	animation-duration: 2s;
	animation-timing-function: linear;
	animation-play-state: running;
	animation-fill-mode: forwards;
}

.closeHer {
	animation-name: heartMove;
	animation-duration: 2s;
	animation-timing-function: linear;
	animation-play-state: running;
	animation-direction: reverse;
	animation-fill-mode: forwards;
}

.beating > img {
	animation-name: beat;
	animation-duration: 2s;
	animation-timing-function: ease-in-out;
	animation-iteration-count: infinite;
	animation-play-state: running;
}

.openedHer {
	top: 85%;
	transform: translate(-50%, 0);
}
