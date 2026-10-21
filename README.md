/*
 * Mod Title: Canada 2011
 * Mod Author: Simjim39
 * Mod Version: 0.1
 * Mod Description: Canadian Federal Election of 2011
 * 
 * Coding License: Apache License 2.0
 * Writing License: Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)
 * 
 * For the coding in this mod, I hereby release the code under the terms and conditions of the Apache License 2.0. The full text of the license can be found at:
 * https://choosealicense.com/licenses/apache-2.0/
 * 
 * For the writing in this mod, including documentation, text files, and other non-software written works, I hereby release the content under the terms and conditions of the Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) license. The full text of the license can be found at:
 * https://creativecommons.org/licenses/by-nc/4.0/legalcode
 * 
 * By using, distributing, or modifying this mod, you agree to abide by the terms and conditions of both the Apache License 2.0 and the Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) license.
*/

document.getElementById("inner_window_1").children[0].innerHTML = `<h3>Do you have what it takes to win a Canadian parliamentary election?</h3>`

document.getElementById("inner_window_1").children[1].innerHTML = `<li>Select a party and a leader to find out.</li><li>You will answer questions about your platform and positions, and also about your campaign strategy.</li><li>The answers will affect your popularity for better or worse, both nationally and in individual ridings.</li><li>Walk the fine line between appealing to your base and winning a majority of the votes.</li><li>Context details are included for <span class='mytooltip'>highlighted<span class='mytooltiptext'>This is a context detail.</span></span> text.</li>`;

campaignTrail_temp.CandidText = "Please select your party:"
campaignTrail_temp.VpText = "Please select your leader:"
campaignTrail_temp.HomeStateText = "Leader's Riding:"

campaignTrail_temp.modBoxTheme = {
     "header_color": "#d62718",
     "header_text_color": "#ffffff",
     "description_text_color": "#ffffff",
     "description_background_color": "#d62718",
     "main_color": "#fafafa",
     "secondary_color": "#d62718",
     "ui_text_color": "#ffffff"
}

campaignTrail_temp.global_parameter_json = [
    {
        "model": "campaign_trail.global_parameter",
        "pk": 1,
        "fields": {
            "vote_variable": 1.125,
            "max_swing": 0.12,
            "start_point": 0.94,
            "candidate_issue_weight": 3,
            "running_mate_issue_weight": 0,
            "issue_stance_1_max": -0.71,
            "issue_stance_2_max": -0.3,
            "issue_stance_3_max": -0.125,
            "issue_stance_4_max": 0.125,
            "issue_stance_5_max": 0.3,
            "issue_stance_6_max": 0.71,
            "global_variance": 0.01,
            "state_variance": 0.005,
            "question_count": 36,
            "default_map_color_hex": "#C9C9C9",
            "no_state_map_color_hex": "#999999"
        }
    }
]

campaignTrail_temp.election_json = [
    {
        "model": "campaign_trail.election",
        "pk": 20,
        "fields": {
            "year": 2011,
            "display_year": "canada 2011",
            "summary": "<p>On March 25th 2011 a motion of no confidence was passed by the opposition parties of the Bloc Quebecois, Liberals and NDP with the writs of election also being issued by the Governor General after being advised by the Prime Minister. Stephen Harper's Conservatives campaign on finally achieving a Majority Government while Michael Ignatieff's Liberals and Gilles Duceppe's Bloc Quebecois campaign to stop keep the tories at a Minority, Jack Layton's NDP also wish to stop a Conservative Majority but also want to overtake the Liberals and Bloc in their number of seats while Elizabeth May's Greens want to finally elect one of their candidates into Parliament. Who will achieve their goals, and who will concede, ultimately it's all up to YOU.</p>",
            "image_url": "https://i.imgur.com/pBSr6D7h.jpg",
            "winning_electoral_vote_number": 155,
            "advisor_url": "https://i.imgur.com/fqcyyD3h.jpg",
            "recommended_reading": "",
            "has_visits": 0,
            "no_electoral_majority_image": ""
        }
    }
]

campaignTrail_temp.temp_election_list = [
    {
        "id": 20,
        "year": 2011,
        "is_premium": 0,
        "display_year": "Canada2011"
    }
]

campaignTrail_temp.credits = "<button onclick='funcredits()'>Simjim39</button>";

funcredits = function() {
    credits = ["Created by Simjim39", "", "Inspired by Diefenbaker '57 and Canada 2025", "", "Map adapted from Wikipedia user Eric0892", "", "Tooltips and election charts adapted from 2023 Netherlands", "", "Music player adapted from 2024: Arnold Amendment and Germany 2021 - Between Decades"]
    text = "CREDITS:\n\n"
    for (i in credits) {
        text += credits[i] + "\n"
    }
    alert(text)
}

RecReading = true
campaignTrail_temp.election_json[0].fields.recommended_reading = "<div style='color: black; overflow: auto'><b>The Canadian parliamentary system</b><br><a href='https://www.ourcommons.ca/procedure/our-procedure/parliamentaryFramework/c_g_parliamentaryframework-e.html' target='_blank'>Our Commons: Canadian Parliamentary System</a><br><br><b>Party Platforms</b><br><a href='https://web.archive.org/web/20250425153842/https://liberal.ca/wp-content/uploads/sites/292/2025/04/Canada-Strong.pdf' target='_blank'>Liberal Platform: Canada Strong</a><br><a href='https://web.archive.org/web/20250428214243/https://canada-first-for-a-change.s3.us-west-2.amazonaws.com/20250418_CPCPlatform_8-5x11_EN_R1-pages.pdf' target='_blank'>Conservative Platform: Canada First — <i>For A Change</i></a><br><a href='https://web.archive.org/web/20250428221305/https://www.ndp.ca/campaign-commitments' target='_blank'>NDP Platform: Made for People. Built for Canada.</a><br><a href='https://web.archive.org/web/20250428160324/https://www.blocquebecois.org/wp-content/uploads/2025/03/blocqcplateforme-2025web.pdf' target='_blank'>Bloc Québécois Platform: Choisis le Québec</a><br><a href='https://web.archive.org/web/20250428060119/https://cdn.greenparty.ca/wp-content/uploads/2025/04/GP_Platform_English_FINAL.pdf' target='_blank'>Green Platform: Change. Vote For It.</a><br><a href='https://web.archive.org/web/20250815051352/https://cdn.prod.website-files.com/61b95f3fa12ab59a52d3ffd4/6881384073f8f49c025cfe2d_ppc-platform-en-2025.pdf' target='_blank'>PPC Platform: Ideas that put People first.</a><br><br><b>The Election in the Media</b><br><a href='https://newsinteractives.cbc.ca/features/2025/federal-party-platforms/#intro' target='_blank'>Compare the election promises (CBC)</a><br><a href='https://www.ctvnews.ca/federal-election-2025/party-platforms/' target='_blank'>Party Platform Tracker (CTV)</a><br><a href='https://votecompass.cbc.ca/' target='_blank'>Vote Compass (CBC)</a><br><a href='https://www.youtube.com/watch?v=7yWno5Zn-uk' target='_blank'>Federal Leaders' Debate 2025</a><br><a href='https://www.youtube.com/watch?v=5psgJFXPpwE' target='_blank'>Vote Canadian: A 22 Minutes Election Special</a><br><br></be><b>Interviews with Nardwuar</b><br><a href='https://www.youtube.com/watch?v=TZmh_PNMImE' target='_blank'>Nardwuar vs. Prime Minister Mark Carney</a><br><a href='https://www.youtube.com/watch?v=stlWcmJSNuk' target='_blank'>Nardwuar vs. Jagmeet Singh (2025)</a><br><a href='https://www.youtube.com/watch?v=Q3yyCjOFDu4' target='_blank'>Nardwuar vs. Elizabeth May</a><br></div>"

campaignTrail_temp.candidate_json = [
    {
        "model": "campaign_trail.candidate",
        "pk": 300,
        "fields": {
            "first_name": "",
            "last_name": "CPC",
            "election": 20,
            "party": "Conservative",
            "state": "Canada",
            "priority": 1,
            "description": "<g><ul><li>Abbreviation: CPC</li><li>Name: Conservative party of Canada </li><li>Current Status: In Government </li></ul><p>Although the Conservative Party has existed in Canada since the days of John a MacDonald though rebanded itself to the Progressive Conservative Party in the 1940s, it would split into largely two parties with the Reform party capturing the western vote while the PCs themselves would be crushed by the liberals in 1993. The Progressive Conservative Party would be in a state of shock and limbo for the next decade until 2003 when uniting with the Alliance Party which was in all actuality just the renamed Reform Party. This merger would create the new Conservative Party which only 3 years later defeated the Liberals and gained a Minority. But now the Conservatives are planning to win a Majority Government and if everything goes to plan, that’s exactly what they’ll get.</p></g>",
            "color_hex": "#EA6D6A",
            "secondary_color_hex": null,
            "is_active": 1,
            "image_url": "https://i.imgur.com/f1f5c31h.jpg",
            "electoral_victory_message": "",
            "electoral_loss_message": "",
            "no_electoral_majority_message": "",
            "description_as_running_mate": null,
            "candidate_score": 1,
            "running_mate": false
        }
    },
    {
        "model": "campaign_trail.candidate",
        "pk": 310,
        "fields": {
            "first_name": "Steven",
            "last_name": "Harper",
            "election": 20,
            "party": "Conservative",
            "state": "MP of Calgary-Southwest",
            "priority": 1,
            "description": "",
            "color_hex": "#EA6D6A",
            "secondary_color_hex": null,
            "is_active": 0,
            "image_url": "https://i.imgur.com/eT5GgA5h.jpg",
            "description_as_running_mate": "<p>‘We Canadians are inheritors of a great legacy, and it is our duty to strengthen and protect it for the generations still to come. Tonight, I pledge to you that Canada’s Government will use every legal means at our disposal to protect our democracy, to protect our economy, and to protect Canada’ -Stephen Harper has been leader of the Conservative Party since its creation and the year prior had been elected as leader of the Alliance party in 2002 with him also being involved with the Reform Party. In 2004 which was also the first election for the at the time new Conservative Party took part in, he was able to knock down the Liberal Party under the new Prime Minister Paul Martin to a minority while then 2 years later winning a minority government. But not all is in his favour as the 3 opposition parties of the Bloc, NDP and Liberals technically still hold a Majority of seats and if he truly does want to bring a conservative agenda to Canada then he must win a Majority Government.</p>",
            "candidate_score": 1,
            "running_mate": true
        }
    },
    {
        "model": "campaign_trail.candidate",
        "pk": 301,
        "fields": {
            "first_name": "",
            "last_name": "NDP",
            "election": 20,
            "party": "Social Democracy",
            "state": "Canada",
            "priority": 1,
            "description": "<g><ul><li>Abbreviation: NDP</li><li>Name: New Democratic Party </li><li>Current Status: 4th most seats in Commons </li></ul><p>The NDP has debatedly been around for 80 years since the days of the Progressives and Cooperation Commonwealth, but technically was formed in 1961 when the CCF ( Cooperation Commonwealth Federation ) merged with the CLC ( Canadian Labour Congress ) to create the New Democratic Party. Ever since then NDP has usually had a respectable showing in parliament with it like other parties having its fair share of gaining and losing seats with their peak of seats coming in 1988 with 43 under leader Ed Broadbent while their worst loss would happen in 1993 when the New Democrats went just under 12 seats needed for official party status as it was the only election it participated it where they gained seats below the threshold. But since a change in leadership, the NDP in the last 3 past elections has gained more and more seats and share of the popular vote. And now with a weakening Liberals and Bloc the NDP hope to make a large gain and possibly become something much more than the party in 4th place.</p></g>",
            "color_hex": "#6495ED",
            "secondary_color_hex": null,
            "is_active": 1,
            "image_url": "https://i.imgur.com/42jIPzbh.jpg",
            "electoral_victory_message": "",
            "electoral_loss_message": "",
            "no_electoral_majority_message": "",
            "description_as_running_mate": null,
            "candidate_score": 1,
            "running_mate": false
        }
    },
    {
        "model": "campaign_trail.candidate",
        "pk": 311,
        "fields": {
            "first_name": "Jack",
            "last_name": "Layton",
            "election": 20,
            "party": "New Democratic",
            "state": "MP of Toronto-Danforth",
            "priority": 1,
            "description": "",
            "color_hex": "#6495ED",
            "secondary_color_hex": null,
            "is_active": 0,
            "image_url": "https://i.imgur.com/TJSVOa7h.jpg",
            "description_as_running_mate": "<p>'Canadians can get Parliament working again. Here's how to do that: elect more New Democrats' -Jack Layton has for much of his life fought for the rights of Canadians everywhere whether it be union men, the gay community, indigenous groups, and many more. He became leader of the NDP in 2003 and in the past 3 elections has only seen more and more gains for the New Democrats. Though not everything has been good for him as in 2010 he had been diagnosed with Prostate Cancer which forced him to take less of a role as leader and now requires him to use a cane. In this election he hopes to bring the NDP to the 2nd largest party with the weakening of the Liberals and Bloc and stop the conservatives from achieving their majority government.</p>",
            "candidate_score": 1,
            "running_mate": true
        }
    },
    {
        "model": "campaign_trail.candidate",
        "pk": 302,
        "fields": {
            "first_name": "",
            "last_name": "LPC",
            "election": 20,
            "party": "Liberal Party of Canada",
            "state": "Canada",
            "priority": 1,
            "description": "<g><ul><li>Abbreviation: LPC</li><li>Name: Liberal Party of Canada</li><li>Current Status: Official Oppisition </li></ul><p>The liberal party is technically considered to be the longest continuous party in Canada's history with it existing since Canada's first election of 1867 but nevertheless still being able to adapt through policy and leadership changes over the years. In 2004 minister of finance Paul Martin succeeded Jean Cretchin in becoming Prime Minister though Creechin's resignation was largely forced by pressure from his own caucus and recent unpopularity. However in an election only 6 months after becoming PM, his government was plunged into a minority by the newly formed Conservative Party with the Bloc Quebecois and NDP also eating away at martins support leading to his government's decline. In the election of 2006 Martin would be defeated by Stephen Harper’s Conservatives and subsequently resigned as leader of the liberal party, but the Liberals would still only continue to decline from then with them losing around 20 seats in the election of 2008 while an attempt at a failed Coalition would only severely decrease the Liberals popularity. In this election the Liberals have to try and survive by stopping the Conservatives from achieving a Majority Government and remain as the Opposition.</p></g>",
            "color_hex": "#F4A460",
            "secondary_color_hex": null,
            "is_active": 1,
            "image_url": "https://i.imgur.com/x9MCi8B.png?3=",
            "electoral_victory_message": "",
            "electoral_loss_message": "",
            "no_electoral_majority_message": "",
            "description_as_running_mate": null,
            "candidate_score": 1,
            "running_mate": false
        }
    },
    {
        "model": "campaign_trail.candidate",
        "pk": 312,
        "fields": {
            "first_name": "Michael",
            "last_name": "Ignatieff",
            "election": 20,
            "party": "LPC",
            "state": "MP of Etobicoke-Lakeshore",
            "priority": 1,
            "description": "",
            "color_hex": "#F4A460",
            "secondary_color_hex": null,
            "is_active": 0,
            "image_url": "https://i.imgur.com/rHQGUi6h.jpg",
            "description_as_running_mate": "<p>'One of the greatest feelings in life is the conviction that you have lived the life you wanted to live-with the rough and the smooth, the good and the bad-but yours, shaped by your own choices, and not someone else's' -Michael Ignatieff is truly a figure of the post Cold War era with him spending many years abroad in other countries before coming back home to Canada in the mid 2000s. He was admired by a centrist crowd for his stances on the War on Terror and the Iraq war with his position largely being one of moderation which appeals to many Canadians. After the resignation of Stephane Dion he became leader of the Liberal Party in 2009 and has ever since tried to keep the Liberal Party stable. His goals this election is to keep the Conservatives at a Minority Government and try to gain more seats for a firmer place as the opposition.</p>",
            "candidate_score": 1,
            "running_mate": true
        }
    },
    {
        "model": "campaign_trail.candidate",
        "pk": 303,
        "fields": {
            "first_name": "",
            "last_name": "BQ",
            "election": 20,
            "party": "French Sepratist",
            "state": "Canada",
            "priority": 1,
            "description": "<g><ul><li>Abbreviation: BQ</li><li>Name: Bloc Quebcois </li><li>Current Status: 3rd most seats in commons </li></ul><p>[NOT PLAYABLE FOR NOW ]</p><p>Even though the Bloc Quebecois has only been around in Federal Politics since 1993, the struggle between the French and Anglo populations of Canada has been a struggle for this country since Confederation and the existence of the Bloc only exists because of this divide. The party was originally formed from MPs of the Progressive Conservative Party upset with Brian Mulroney's government and MPs from the Liberal party upset with their new leader Jean Chrétien. They would gain the Majority of seats in Quebec and have remained the Largest party in terms of seats since. But recently the Bloc has not been performing well so their main goal this election is just to retain a majority of seats in Quebec or at the very least a respectable amount of seats to keep defending the rights of the Quebecois.</p></g>",
            "color_hex": "#99C955",
            "secondary_color_hex": null,
            "is_active": 1,
            "image_url": "https://i.imgur.com/x8381BSh.jpg",
            "electoral_victory_message": "",
            "electoral_loss_message": "",
            "no_electoral_majority_message": "",
            "description_as_running_mate": null,
            "candidate_score": 1,
            "running_mate": false
        }
    },
    {
        "model": "campaign_trail.candidate",
        "pk": 304,
        "fields": {
            "first_name": "",
            "last_name": "GPC",
            "election": 20,
            "party": "Green Party",
            "state": "Canada",
            "priority": 1,
            "description": "<g><ul><li>Abbreviation: GPC</li><li>Name: Green Party of Canada</li><li>Current Status: 0 seats in Commons </li></ul><p>[NOT PLAYABLE FOR NOW]</p><p>The Green Party has existed in Canada since the 80s and early rise of environmental issues but for 2 decades was only seen as a minuscule party and similar in size to other parties that only the most astute in federal politics have actually heard of. But that would begin to change in the early 2000s as the issue of Climate Change became larger and also the effect of better leadership started to increase the vote share of the Greens with an independent MP even briefly joining the party in 2008 though it didn’t last. In the last election the Greens achieved 4 percent of the popular vote with their Party Leader even almost winning a seat in Hamilton. As the election approaches the Greens only goal is to get more votes and get a green MP into Parliament. </p></g>",
            "color_hex": "#87CEFA",
            "secondary_color_hex": null,
            "is_active": 1,
            "image_url": "https://i.imgur.com/BpaYb6fh.jpg",
            "electoral_victory_message": "",
            "electoral_loss_message": "",
            "no_electoral_majority_message": "",
            "description_as_running_mate": null,
            "candidate_score": 1,
            "running_mate": false
        }
    },
    {
        "model": "campaign_trail.candidate",
        "pk": 305,
        "fields": {
            "first_name": "",
            "last_name": "Others",
            "election": 20,
            "party": "Others",
            "state": "Canada",
            "priority": 1,
            "description": "",
            "color_hex": "#808080",
            "secondary_color_hex": null,
            "is_active": 0,
            "image_url": "",
            "electoral_victory_message": "",
            "electoral_loss_message": "",
            "no_electoral_majority_message": "",
            "description_as_running_mate": null,
            "candidate_score": 1,
            "running_mate": false
        }
    },
    {
        "model": "campaign_trail.candidate",
        "pk": 313,
        "fields": {
            "first_name": "Gilles",
            "last_name": "Duceppe",
            "election": 20,
            "party": "Bloc Quebcois",
            "state": "MP of Laurier-Sainte Marie",
            "priority": 1,
            "description": "",
            "color_hex": "#99C955",
            "secondary_color_hex": null,
            "is_active": 0,
            "image_url": "https://i.imgur.com/Fa4RBaOh.jpg",
            "description_as_running_mate": "<p>[NOT PLAYABLE FOR NOW]</p><p>“Life is a constant battle for dignity and respect; we must never surrender our principles” -Gilles Duceppe was the interim leader of the Bloc since its first Leader Lucien Bouchard resigned and then replaced the Blocs unpopular leader of Michel Gauthier and has been the leader of the bloc in every election since 1997. He has been able to maintain the support of the Quebecois for more than a decade but things especially recently are now beginning to change. Be it the bloc's many failures in past years, them now being seen as the establishment in politics, or just general dissatisfaction from their base it appears that this election will be rough for the bloc and Duceppe is the only man that can stop its own armageddon. </p>",
            "candidate_score": 1,
            "running_mate": true
        }
    },
    {
        "model": "campaign_trail.candidate",
        "pk": 314,
        "fields": {
            "first_name": "Elizabeth",
            "last_name": "may",
            "election": 20,
            "party": "Green Party",
            "state": "Running for MP in Saanich-Gulf Islands",
            "priority": 1,
            "description": "",
            "color_hex": "#87CEFA",
            "secondary_color_hex": null,
            "is_active": 0,
            "image_url": "https://i.imgur.com/lmcXqmyh.jpg",
            "description_as_running_mate": "<p>[NOT PLAYABLE FOR NOW]</p><p>A patchwork solution of provincial targets is an admission of defeat and a statement that we have failed our children and grandchildren -Elizabeth May is currently the leader of the Green Party but her political career started back in the 80s when after several failed attempts at relevance, she was able to get a position in Malroneys government but then left, she the ran for and became the leader of the Green Party in 2006 and for the past few elections has been steadily growing the Greens relevance. In this election she plans on focusing the Green parties campaign on her own race in victory so that she can get the Green Party an Elected seat in Parliament.</p>",
            "candidate_score": 1,
            "running_mate": true
        }
    },
    {
        "model": "campaign_trail.candidate",
        "pk": 315,
        "fields": {
            "first_name": "Placeholder",
            "last_name": "Placeholder",
            "election": 20,
            "party": "Placeholder",
            "state": "Placeholder",
            "priority": 1,
            "description": "",
            "color_hex": "#808080",
            "secondary_color_hex": null,
            "is_active": 0,
            "image_url": "",
            "description_as_running_mate": "",
            "candidate_score": 1,
            "running_mate": true
        }
    }
]

campaignTrail_temp.running_mate_json = [
    {
        "model": "campaign_trail.running_mate",
        "pk": 172512,
        "fields": {
            "candidate": 300,
            "running_mate": 310
        }
    },
    {
        "model": "campaign_trail.running_mate",
        "pk": 172513,
        "fields": {
            "candidate": 301,
            "running_mate": 311
        }
    },
    {
        "model": "campaign_trail.running_mate",
        "pk": 172514,
        "fields": {
            "candidate": 302,
            "running_mate": 312
        }
    },
    {
        "model": "campaign_trail.running_mate",
        "pk": 172515,
        "fields": {
            "candidate": 303,
            "running_mate": 313
        }
    },
    {
        "model": "campaign_trail.running_mate",
        "pk": 172516,
        "fields": {
            "candidate": 304,
            "running_mate": 314
        }
    },
    {
        "model": "campaign_trail.running_mate",
        "pk": 172517,
        "fields": {
            "candidate": 305,
            "running_mate": 315
        }
    },
    {
        "model": "campaign_trail.running_mate",
        "pk": 172518,
        "fields": {
            "candidate": 306,
            "running_mate": 316
        }
    }
]

campaignTrail_temp.opponents_default_json = [
    {
        "election": 20,
        "candidates": [
            300,
            301,
            302,
            304,
            303,
            306,
            305
        ]
    }
]

function addDynamicCSS() {
    var css = `
        .inner_window_question h3 .mytooltip{
            color: #345beb;
        }

        .mytooltip {
            position: relative;
            display: inline-block;
            cursor: pointer;
            color: #345beb;
        }

        .mytooltip .mytooltiptext {
            width: 240px;
            background-color: #E8FBFF;
            color: black;
            text-align: center;
            border-radius: 6px;
            padding: 10px;
            position: absolute;
            z-index: 99;
            bottom: 110%;
            left: 50%;
            margin-left: -130px;
            opacity: 0;
            transition: opacity 0.3s;
            border: 1px solid black;
            pointer-events: none;
            font-size: 13px !important;
            line-height: 1.5em !important;
            font-weight: normal !important;
            font-style: normal !important;
        }

        .mytooltip .mytooltiptext::after {
            content: " ";
            position: absolute;
            top: 100%; /* At the bottom of the tooltip */
            left: 50%;
            margin-left: -5px;
            border-width: 5px;
            border-style: solid;
            border-color: black transparent transparent transparent;
        }

        .mytooltip .mytooltiptext img {
            max-width: 240px;
            height: auto;
        }

        .mytooltip:hover .mytooltiptext {
            opacity: 1;
            transition-delay: 0.5s;
        }
    `;

    var styleElem = document.createElement('style');
    styleElem.type = 'text/css';

    styleElem.appendChild(document.createTextNode(css));

    document.head.appendChild(styleElem);
}

document.getElementById("header").src = "https://i.imgur.com/6lfqSMDh.jpg";
$("#game_window")[0].style.backgroundImage = "url(https://i.imgur.com/EPkdtPN.jpeg)";
nct_stuff.themes[nct_stuff.selectedTheme].coloring_title = "#EA6D6A"
nct_stuff.themes[nct_stuff.selectedTheme].coloring_window = "#FFFFFF"
document.getElementsByClassName("game_header")[0].style.backgroundColor = nct_stuff.themes[nct_stuff.selectedTheme].coloring_title
$(".container")[0].style.backgroundColor = "#FFFFFF"
document.body.background = "https://i.imgur.com/vAMuvqw.jpeg"

HistHexcolour = ["#EA6D6A", "#6495ED", "#87CEFA", "#F4A460", "#99C955", "#6F5D9A", "#808080"];
HistName = [" LPC", " CPC", " BQ", " NDP", " GPC", " PPC", " Others"];
HistEV = [169, 144, 22, 7, 1, 0, 0];
HistPV = ["8,595,488", "8,113,484", "1,236,349", "1,234,673", "238,892", "136,977", "85,800"];
HistPVP = ["43.8%", "41.3%", "6.3%", "6.3%", "1.2%", "0.7%", "0.4%"];

quotes = [
    `Skate to where the puck is going, not where it has been — Wayne Gretzky`,
    `Canada is not a country for the cold of heart or the cold of feet — Pierre Trudeau`,
    `Keep your head up and your stick on the ice`,
    `The greatest way to defend democracy is to make it work — Tommy Douglas`,
    `I've always found that you can control people better if you don't see too much of them — William Lyon Mackenzie King`,
    `The Americans are our best friends whether we like it or not — Robert N. Thompson`,
    `Qu'est-ce qu'on fait? On se crache dans les mains et on recommence! — Jacques Parizeau`
]
customquote = quotes[Math.floor((Math.random() * quotes.length))]
corrr = "\n<h2>THE CAMPAIGN TRAIL</h2><font id='wittyquote' size='4' color='white'><em>" + customquote + "</em></font>"

function updateElements() {
    mutationObserver.disconnect()

    var gameHeader = document.getElementsByClassName("game_header")[0];

    if (gameHeader.getAttribute("id") !== "modifiedHeader") {
        gameHeader.innerHTML = corrr;
        gameHeader.setAttribute("id", "modifiedHeader");
    }

    // Remove "continue" buttons for non-playable characters
    const running_mate_id = document.getElementById("running_mate_id")
    const continue_button = document.getElementById("running_mate_id_button")
    if (running_mate_id && continue_button && running_mate_id.value != 310 && running_mate_id.value != 311 && running_mate_id.value != 312) {
        continue_button.parentElement.removeChild(continue_button)
    }

    // Remove default summary list
    const candidate_summary = document.getElementById("candidate_summary")
    if (candidate_summary && candidate_summary.childElementCount > 1) {
        candidate_summary.removeChild(candidate_summary.firstElementChild)
    }

    // Replace electoral system options
    const form = document.querySelector('form[name="game_type_selection"]');
    if (form) {
        const select = form.querySelector('select[name="game_type_id"]');
        const h3 = form.querySelector('h3');
        const option = select.querySelector('option[value="1"]');

        const voting_system = "Default (First-Past-the-Post)"
        const seat_allocation = "How would you like the seats to be allocated?"

        if (option && option.textContent !== voting_system) {
            option.textContent = voting_system;
        }
        if (select && select.querySelector('option[value="2"]')) {
            const queryTwo = select.querySelector('option[value="2"]');
            if (queryTwo) {
                queryTwo.remove();
            }
        }
        if (h3 && h3.textContent !== seat_allocation) {
            h3.textContent = seat_allocation;
        }
    }

    // Replace electoral system description
    const opponentSelectionDescription = document.getElementById("opponent_selection_description_window");
    if (opponentSelectionDescription) {
        opponentSelectionDescription.innerHTML = `<p><strong>Use the default method of allocating seats in the Canadian House of Commons.</strong></p><p>Canada uses a first-past-the-post voting system where the local candidate with the most votes in each riding is elected to the House of Commons to become a Member of Parliament (MP).</p><p>The party that wins the most seats usually forms government with its leader becoming Prime Minister. However, the incumbent Prime Minister can attempt to stay in power even if their party does not win the most seats as long as they can maintain the confidence of Parliament (as occurred after the 1925 election).</p><p>The first-past-the-post voting system means that large parties usually have better vote efficiency, winning more seats per vote. However, small parties can still do well if their vote is concentrated.</p>`;
    }
    
    mutationObserver.observe(document.documentElement, { childList: true, subtree: true });
}

var mutationObserver = new MutationObserver(updateElements);
mutationObserver.observe(document.documentElement, { childList: true, subtree: true });

// Initialise custom music

$("#music_player")[0].children[0].style.display = "none"
$("#music_player")[0].children[1].style.display = "none"

document.getElementById("modLoadReveal").style.display = "none"
document.getElementById("modloaddiv").style.display = "none"

musicBox = document.getElementById("music_player")
musicBox.style.display = ""

var trackSel;
e = campaignTrail_temp
e.selectedSoundtrack = 0

toTime = (seconds) => {
    var date = new Date(null);
    date.setSeconds(seconds);
    return date.toISOString().substr(11, 8);
}

function nextTrack() {
    console.log("next track")
    e = campaignTrail_temp
    audio = $("#campaigntrailmusic")[0];
    tracklist_length = e.soundtracks[e.selectedSoundtrack].tracklist.length;
    if (tracklist_length == 1) {
        audio.currentTime = 0
        audio.play()
        return
    }
    let selected = Number(document.querySelector('input[name="trackSelector"]:checked').value);
    var newSel;
    if (audio.shuffle) {
        newSel = Math.floor(Math.random() * (tracklist_length - 1));
        if (newSel >= selected) {
            newSel += 1;
        }
    } else {
        newSel = clamp(selected + 1, tracklist_length - 1, 0);
    }
    let buttons = Array.from(document.getElementById("trackSel").children).filter(f => {
        return f.tagName == "LABEL"
    }).map(f => f.children[0])
    buttons[newSel].click()
}

generateTime = () => {
    // Get the audio element
    e = campaignTrail_temp
    var audio = document.getElementById("campaigntrailmusic");

    timeTracker = document.createElement("div");
    timeTracker.style = `
      text-align:left;
      border-style:solid;
      border-width:3px;
      height:180px;
      width:200px;
      background-color:#999999;
      float:right;
      padding: 10px;
    `
    $("#trackSelParent")[0].prepend(timeTracker);
    $("#trackSelParent")[0].prepend(document.createElement("br"));

    // Create a new element to display the current position of the audio
    var positionDisplay = document.createElement("gg");
    positionDisplay.id = "position-display";

    // Create a new slider element to change the time
    var timeSlider = document.createElement("input");
    timeSlider.type = "range";
    timeSlider.min = 0;
    timeSlider.max = 1;
    timeSlider.step = 0.001;
    timeSlider.value = 0;
    timeSlider.style.width = "200px";
    timeSlider.id = "time-slider";

    var pausePlay = document.createElement("button");
    pausePlay.id = "position-display";
    pausePlay.innerHTML = "<b>Pause</b>"
    pausePlay.style.width = "100%";
    pausePlay.style.margin = "2px";
    pausePlay.addEventListener("click", event => {
        event.preventDefault();
        updatePositionDisplay();
        let audio = document.getElementById("campaigntrailmusic");
        if (audio.paused) {
            audio.play();
            event.target.innerHTML = "<b>Pause</b>";
            return;
        }
        audio.pause();
        event.target.innerHTML = "<b>Play</b>";
        return;
    })

    var shuffle = document.createElement("button");
    shuffle.id = "shuffle-button";
    shuffle.innerHTML = audio.shuffle ? "<b>Unshuffle</b>" : "<b>Shuffle</b>";
    shuffle.style.width = "100%";
    shuffle.style.margin = "2px";
    shuffle.addEventListener("click", event => {
        event.preventDefault();
        audio = document.getElementById("campaigntrailmusic");
        if (audio.shuffle) {
            audio.shuffle = false;
            event.target.innerHTML = "<b>Shuffle</b>"
            return;
        }
        audio.shuffle = true;
        event.target.innerHTML = "<b>Unshuffle</b>"
    })

    var skipButton = document.createElement("button");
    skipButton.id = "skip-button";
    skipButton.innerHTML = "<b>Skip</b>"
    skipButton.style.width = "50%";
    skipButton.style.margin = "2px"; // Add margin
    skipButton.addEventListener("click", event => {
        event.preventDefault();
        nextTrack();
    })

    var loopButton = document.createElement("button");
    loopButton.id = "loop-button";
    loopButton.innerHTML = audio.loopEnabled ? "<b>Unloop</b>" : "<b>Loop</b>";  // Check the initial loop state
    loopButton.style.width = "50%";  // Match the width with skipButton
    loopButton.style.margin = "2px";
    loopButton.addEventListener("click", event => {
        event.preventDefault();
        audio = document.getElementById("campaigntrailmusic");
        audio.loopEnabled = !audio.loopEnabled;
        audio.loop = audio.loopEnabled;  // Set the audio's loop property
        event.target.innerHTML = audio.loopEnabled ? "<b>Unloop</b>" : "<b>Loop</b>";  // Toggle the button text
    });

    var buttonContainer = document.createElement("div");
    buttonContainer.style.display = "flex"; // Makes children inline
    buttonContainer.style.justifyContent = "space-between";
    skipButton.style.flex = "1"; // Makes it take up equal space
    skipButton.style.marginRight = "5px"; // Adds some space between the buttons

    loopButton.style.marginRight = "0px";

    buttonContainer.appendChild(skipButton);
    buttonContainer.appendChild(loopButton);

    var volumeLabel = document.createElement("gg");
    volumeLabel.id = "volume-label";
    volumeLabel.innerHTML = "<br><b>Volume: </b>"

    var volumeSlider = document.createElement("input");
    volumeSlider.type = "range";
    volumeSlider.min = 0;
    volumeSlider.max = 1;
    volumeSlider.step = 0.001;
    volumeSlider.value = 0;
    volumeSlider.style.width = "200px";
    volumeSlider.id = "volume-slider";

    volumeSlider.value = audio.volume;

    timeTracker.appendChild(pausePlay);
    timeTracker.appendChild(shuffle);
    timeTracker.appendChild(buttonContainer);
    timeTracker.appendChild(document.createElement("br"));
    timeTracker.appendChild(positionDisplay);
    timeTracker.appendChild(timeSlider);
    timeTracker.appendChild(volumeLabel);
    timeTracker.appendChild(volumeSlider);

    updatePositionDisplay();

    //for (let i = 0; i < 10; i++)
    //timeTracker.append(document.createElement("br"));


    // Function to update the position display
    function updatePositionDisplay() {
        positionDisplay.innerHTML = "<b>Time:</b> " + toTime(audio.currentTime) + "<br>";
        timeSlider.value = audio.duration ? audio.currentTime / audio.duration : 0;
    }

    // Function to change the time of the audio
    function changeTime() {
        positionDisplay.innerHTML = "<b>Time:</b> " + toTime(audio.currentTime) + "<br>";
        audio.currentTime = timeSlider.value * audio.duration;
    }

    updateVolume = event => {
        audio.volume = event.target.value;
    }

    // Update the position display and slider every second
    setInterval(updatePositionDisplay, 1000);

    // Listen for changes to the time slider and change the time of the audio
    timeSlider.addEventListener("input", changeTime);
    volumeSlider.addEventListener("input", updateVolume)
}

function newMusicPlayer(soundtracks) {
    campaignTrail_temp.soundtracks = soundtracks;
    trackSel = document.createElement("div");
    trackSel.id = "trackSelParent"
    let z = `<div id='trackSel' style="text-align:left;border-style:solid;border-width:3px;overflow-y: scroll;overflow-x: hidden;height:200px; width:500px;background-color:#999999;float:right;">`
    z += `<b><select id='selectSoundtrack'><option value='` + soundtracks[e.selectedSoundtrack].name + `'>` + soundtracks[e.selectedSoundtrack].name + "</option>"
    for (i in soundtracks) {
        if (soundtracks[e.selectedSoundtrack] != soundtracks[i]) {
            z += `<option value='` + soundtracks[i].name + `'>` + soundtracks[i].name + `</option>`
        }
    }
    z += `</select></b><br><br>`
    // <label><input type="radio" name="option" value="option1">Option 1</label><br>
    for (i in soundtracks[e.selectedSoundtrack].tracklist) {
        let a = soundtracks[e.selectedSoundtrack].tracklist[i]
        let b = `<label><input class="trackSelector" type="radio" name="trackSelector" value="` + i + `">` + a.name + `</label><br>`
        z += b
    }
    z += "</div><br><br>"
    trackSel.innerHTML = z

    // select correct song

    musicBox.appendChild(trackSel);
    Array.from(document.getElementById("trackSel").children).filter(f => {
        return f.tagName == "LABEL"
    }).map(f => f.children[0])[0].checked = true

    // set soundtrack changer

    soundtrackSelector = document.getElementById("selectSoundtrack")
    soundtrackSelector.onchange = function () {
        for (i in soundtracks) {
            if (soundtracks[i].name == soundtrackSelector.value) {
                e.selectedSoundtrack = i
                break
            }
        }
        document.getElementById("trackSelParent").remove()
        newMusicPlayer(soundtracks)
    }

    var matches = document.querySelectorAll('.trackSelector');

    for (match in matches) {
        matches[match].onchange = function () {
            audio = $("#campaigntrailmusic")[0];
            audio.src = soundtracks[e.selectedSoundtrack].tracklist[this.value].url
            audio.currentTime = 0
        }
    }

    musicBox.children[2].loop = false
    musicBox.children[2].src = soundtracks[e.selectedSoundtrack].tracklist[0].url

    musicBox.children[2].onended = nextTrack;

    for (w = 0; w < 7; w++) {
        document.getElementById("trackSelParent").appendChild(document.createElement("br"))
    }

    generateTime();
}

clamp = function (a, max, min, overflow = true) {
    if (overflow) {
        return a > max ? min : a < min ? max : a;
    }
    return a > max ? max : a < min ? min : a;
}


// Track list for start
var soundtracks_start = {
    0: {
        name: "Introduction",
        tracklist: [
            {
                "name": "O Canada — Sunday 7pm Choir",
                "url": "https://audio.jukehost.co.uk/wDIZq9LM9juuTefsZvuBSthNYNlghG4k"
            },
        ]
    }
}

// Set up new music player
var audio = document.getElementById("campaigntrailmusic");
audio.volume = 0.3;
audio.shuffle = true;
audio.loopEnabled = false;
newMusicPlayer(soundtracks_start);
