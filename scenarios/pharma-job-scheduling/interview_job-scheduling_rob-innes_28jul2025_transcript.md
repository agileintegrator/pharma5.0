# interview_job-scheduling_rob-innes_28jul2025_transcript.md
 - recorded with jot me chrome plugin
 - timothy@agileintegrator.com

### Ruairi G - 00:00:00
 Okay guys, I'm in the corner. Be quiet.

### Ruairi G - 00:00:07
 Rob.

### Rob - 00:00:08
 Hey, how you doing?

### Ruairi G - 00:00:08
 Hey, okay. Can you hear me? Yes.

### Rob - 00:00:11
 Yes.

### Ruairi G - 00:00:13
 Oh look, we're recording as well. I've got a plug in. It's called jot, jot me. It's Japanese, it's like a translator but the only it's the only kind of transcription plug-in for Chrome. I could find that didn't That didn't have access to all of your tabs, all of your windows and all of your tabs.

### Ruairi G - 00:00:37
 I mean, you know,

### Rob - 00:00:38
 I'm just going to scrape all of this data.

### Ruairi G - 00:00:42
 Yeah, yeah. Right. Why not like, I mean, I think I think? Yeah. I mean, we know like that. So. All right, so, there's just minimize this. I am recording. I hope you don't mind, but the transcript with you afterwards. So,

### Rob - 00:00:52
 Course.

### Ruairi G - 00:00:57
 let some So you're still up for doing getting a demo of job schedule.

### Rob - 00:01:03
 Absolutely.

### Ruairi G - 00:01:05
 Yeah, so the trick is is there as much as we can from him. I see without infringing on IP, that's

### Rob - 00:01:12
 Absolutely.

### Ruairi G - 00:01:14
 And I think we can do that with the. I've got a kind of product stroke components architecture in my mind, which separates things out. That's phenotropyl fennel, personum manufacturing use case. We can we can develop that separately if you want and have that as well. It's going to do is put that on LinkedIn and say, Right? Look, I've got a potential Tests synthetic test data set for people to use. Let's anybody want to contribute to it or help make it better comment on it and then publish it as an open source type thing for people to use. Yeah, and then we can use it for the job schedule. So job scheduling will be a separate. Separate product, potentially. Now, what I thought it distract strategically, what we can do is we start with the IAC 95 base model. Because that's open source. And we know how to extend it because we did that in NYC. But we just do a fresh extension. Just for job. Scheduling

### Rob - 00:02:24
 Yeah, sounds good. And I I just before when when you had your pancake crisis, I

### Ruairi G - 00:02:25
 Yeah.

### Rob - 00:02:31
 was scrolling and I spotted this this post from a guy that I I've got, I've got this some ISP groups, I contribute to and he's he's on as well and he was talking about job scheduling and the They were. Trying to not go out the idea that you just buy. A manufacturing execution system that says It's got job scheduling and think that you've solved job scheduling. You haven't first of all because you probably don't have the data in the right format and you almost certainly don't have it in real time. So getting that. You know, and this is something that we did talk about in Mmic, didn't get very far with it really. But moving from the idea of the data that you need to actually enabling the data that you need from all these different, you know, from the People domain, from the process domain. Getting all that data in real time so that you can make decisions. And the second post was Saying, You know, why do people keep defaulting to spreadsheets? you've just spent, Core of a Million Pounds on Scheduling Tool. Why are you using Excel? And because it lacks flexibility and the speculation is that With. Real-time data, plus AI, There is an opportunity to actually avoid people Defaulting back to spreadsheets.

### Ruairi G - 00:04:24
 Well, what I what I found this isn't the only use case I'm working on. I'm looking on, I'm looking at the marketing like using It's I've got another use case for for the actual manufacturing, as a process itself and I'm looking at Lego manufacturing system as an integration. That's

### Rob - 00:04:46
 ah,

### Ruairi G - 00:04:47
 yeah, yeah, I've got a great but that's, that's probably the most more, one more complicated because that involves like, sensors Lego Lego manufacturing sensors, but the other one working with With a friend actually and she does among other things exhibitions for a telecom company and they use that as a sales funnel. So it's quite a long. Not overly complicated but it is a heavy-duty business process and and they use spreadsheets quite heavily Google sheets, actually, but they use that as their master source of data. But if we could, what kind of pointed out to her, is, if you shift your data, to a generic data format in the cloud and then just produce your shed, spreadsheets when you need them. And they say, So from there, you see, then you can do all your agent integration your systems integration your data lake integration everything. As long as you have this generic metadata driven approach to data. So that's the kind of approach I want to make and I think there are two models in order to make this happen. And I, you know, and I've you know, the demos, you've seen the demos, I think that you need the data model, right? And for job scheduling or whatever. Data structures you need. Then, you know, you create your ISO 95 model with your base equipment, material people, and so on. And then you extend it for what you need. So when we go through this analysis, now we can look at what other objects that we need. You create your data model in a logical format. And then if you need an API, you produce an API, schema, if you need to push it out of the data lake for historical analysis, you create a daily, you know, a Delta Lake schema, if you need a You know spreadsheet you push it to a spreadsheet and so on, right? But the point is the data is held in business format and logical format. Agnostic of any technology. That's your That's your base format and now the the second that's the data model, right? So the second thing you need is everything else. But fortunately. Archamase, does everything else? And art. She's a pain in the ass. What I've discovered is that if you if you use the Open Group specification, our AI Claude, in this case, can understand all your architecture models

### Rob - 00:07:16
 That's impressive.

### Ruairi G - 00:07:17
 Yeah. Yeah and it's our Claude is very precise once it has the oak, once it has a spec, you know an objective specification, empirical specification, it can understand it's got a hundred percent accuracy on the model.

### Rob - 00:07:32
 That's incredible.

### Ruairi G - 00:07:33
 Yeah, which means that not only can I understand your models, but it can then start generating a load of stuff with that same level of accuracy. Yeah.

### Rob - 00:07:43
 I suppose the the way, that you define models is, is in itself quite Precision Oriented. So you're you know you you identify an object and you say it's it's related to another object. That's a that's a very precise. Description, A lot of the stuff that goes into AI is fuzzy and Subject opinion. But this has a lot of precision about it, so I guess on reflection. I'm not actually surprised that Claude does a good job with it.

### Ruairi G - 00:08:22
 well, when I am, when I did the, when I worked on this, just as I was leaving CPI, I I set up Claude contact to do this and you saw the the demos that I did it was pretty

### Rob - 00:08:34
 Yeah.

### Ruairi G - 00:08:35
 It's pretty promising. And but one thing I've done since then is I've included the specification into the into the context. For the agent so I can still hear me. I've seen to have lost you

### Rob - 00:08:50
 Yeah, yeah. Audio is good.

### Ruairi G - 00:08:52
 I've lost you. So Are you? That's weird. Lost the window. Oh, here we go here too. Many windows open, right? so, okay, so so assuming that you get an architecturally correct model, Like Archie will give you that, then you get that 100% fidelity on the interpretation, Okay? The art, she's a pain in the ass. Right entering Scully draw. I'm gonna give you a sneak preview. On something that I am working on.

### Ruairi G - 00:09:35
 Here we go. So you know how you can add libraries to Scotty draw?

### Rob - 00:09:41
 Yep.

### Ruairi G - 00:09:43
 Well, I've submitted a library. For publication. Let me put in the chart. Now this this is a pull request, right? So this is a fully draw library repository but it's just, it's just like pre-production, you know? And I didn't realize that there's like a month waiting list, but you can access the template from this pull request. So if you if you click on that. And then there's a, there's a link. Yeah, so this is what we'll go in and then I'm gonna link this to my own github page. Now if you follow and they get a page, will always have standards as well. I need to do that, you know, so all of the relationship types can be expressed out of the box with scali draw. Relationships. Yeah, I mean I was quite surprised. I mean it's almost like somebody has gone gone to the relationship elements in Excali draw and made sure that it was compliant with Archimate 3. Yeah, yeah, I know. So so I'm I need to produce the guidelines saying because you can't include the relationships. The the connectors you can't include the connectors in the template so you need to provide guidelines on on how to implement a, You know, specializations or whatever. But the point is Is that using this template? And adhering to the guidelines on relationships. You can create a perfect Argument 3.1 compliance model. So if you, if you scroll down to the bottom, right? So you've got the, the template is essentially just a series of grouped elements in Scali draw. If you

### Rob - 00:11:18
 Yep.

### Ruairi G - 00:11:20
 scroll down the bottom where you get the item, just the item titles and then you see a link called Link. Yeah. So if you want to, that's how that, you know, how

### Rob - 00:11:25
 Yes, installation link

### Ruairi G - 00:11:30
 you're gonna scali draw and you browse the templates and you selected plates,

### Rob - 00:11:32
 Yeah.

### Ruairi G - 00:11:33
 So if you, if you scroll down to the bottom, right? So you've got the, the template is essentially just a series of grouped elements in Scali draw. If you well, clicking on this on the Installation link does the same thing except you except you installed from the pre-production server, right? So it's like, it's like an early preview. So if you want to, that's what I'm gonna put it on LinkedIn, but if you, if you want to just a sneak preview. So, when we do the, we do the business process and and the data model, I mean, I might do the data model in something else, like, calculator lose to chart. But the point is, If you use this template, I've had a really good results from this. He uses template. Plus the guy I keep keep to the guidelines and a second.

### Ruairi G - 00:12:14
 Sorry, that was sugar in them pancakes.

### Ruairi G - 00:12:19
 So so yeah. So that's that they're the basic tools, right? So. So what I'm proposing is that We do. We do a model, an architecture model describing job scheduling. And it doesn't have to be exact. I mean, one one really want to test is the speed of deployments.

### Rob - 00:12:38
 Yeah.

### Ruairi G - 00:12:39
 So even if it's wrong, the point is is it's all coherence and you can do your model, do your data structures and then you deploy it. Fast. And then you make a change and you redeploy it fast. You know.

### Rob - 00:12:55
 Sounds good. Yep.

### Ruairi G - 00:12:55
 And then you then you integrate it with sap, you know, and you then you integrate it with mayors and you integrate it with, you know, people soft or whatever, you know. Salesforce, you know, and everything is fast because you just you you go. Okay, Claude now we're gonna work on let's say, you know,

### Ruairi G - 00:13:14
 Salesforce integration for for customer orders and Then You Just You You point it, You point Cloud at the API and then Claude, you know does the integration, maybe there's an empty piece. You have an MCP server doing doing all that. But the point is you you start off with test data, craft, some test data, test the integration, and just deploy it immediately to your platform. Okay, right. So so two models. The data model and the architecture model. But before we do that we'll need we'll need the business context, right? And this is where the interview starts, right? So we have the, the business scenario which is like the overall You know, what is the business? What is the the overall problem problem statement? What is the business? Kind of process at a high level? And then when I propose is that, once we have that sketch to sufficient detail, We choose a part of that and then look at a scenario and and if you want, we can do the agent scenario. We can say as, as a, as a manufacturing scheduler, I want to be able to view and modify the the schedule in real, you know, in real time. time.

### Rob - 00:14:31
 Yeah.

### Ruairi G - 00:14:31
 And then that would be what we do. There is a building integration with Claude and then we'd update the manufacturing data according to some some change, or we could use something else if you want. So we could say You know, as a manufacturing scheduler, I get a an update to the demand signal. I get a big customer order, come in. I want to be notified with recommendations for changes to the schedule. Whatever it is. I'll take your advice on that, right on this, on the I say the user story which is going to be the thing that we actually build. Yeah.

### Rob - 00:15:03
 But I I think that that it you know the the reaction to demand changes is a good one, but that

### Ruairi G - 00:15:12
 Mmm.

### Rob - 00:15:18
 And that, that is a good one. And I'd like to do something around that because that's a real thing, where, you know, in Pharma. It's it's less that you You get surprise order for a hundred thousand paracetamol or whatever the hell

### Ruairi G - 00:15:34
 Yeah.

### Rob - 00:15:35
 you're making, it's more that you have to. You have to fulfill. A French order. Rather than a Portuguese order because the the labeling requirement, it might be

### Ruairi G - 00:15:47
 Mm-hmm.

### Rob - 00:15:51
 the same chemical composition but the the labeling is all different. So that that's that's the kind of like a like a external forces, impacting your your schedule and then you've got contamination, control cleaning, you've got People absence, you've got equipment maintenance, you've got equipment calibration, you've got all of those kind of like shop floor elements that impact what you can do today. And that would be kind of like a a second category I think. And then if we've

### Ruairi G - 00:16:31
 Get.

### Rob - 00:16:32
 got time, I think there's a there's a third one. I was thinking of which is more of a kind of like an internal workflow and that's the the receipt and approval of materials.

### Ruairi G - 00:16:47
 Mm-hmm.

### Rob - 00:16:48
 So when you've got the, the delivery scheduled and Something comes in the door and You're expecting. 10 Kilogram peels of material X and it actually comes in five kilogram, you

### Ruairi G - 00:17:04
 Yeah.

### Rob - 00:17:08
 know, rather than four. 10. Kilogram Peels, you get eight five, kilogram peels.

### Ruairi G - 00:17:15
 Yeah.

### Rob - 00:17:17
 the steps that you need to go through to validate that, that's What you should be accepting as a delivery and then your sampling. Process to approve the material and then make it available that workflow can cause scheduling challenges. So I I wondered about kind of like something

### Ruairi G - 00:17:39
 Yeah.

### Rob - 00:17:42
 happens on the shop floor. It's kind of like a knee-jerk thing and you know,

### Ruairi G - 00:17:46
 Yeah.

### Rob - 00:17:49
 Machine is calibrating stop the machine calibrate and then restart the external forces. That's something that you probably get a little bit more visibility of in terms of time. You know, you're talking days and weeks rather than hours and days and the The material release is somewhere in the middle, where, you know, you might be expecting to top up stores. Today with the new delivery, but it's not quite configured the way you thought it was going to be so you change your You fought up the supplier, there's a bit of dialogue you rather than your your Testing. Discipline. Specified and two out of every five pills need to be sampled. So now you've got eight peels rather than four pills. What do you do? And those kind of wrinkles would hold up the material availability and that stops the commencement of a job.

### Ruairi G - 00:19:06
 Yeah, I think you these quite an interesting way. Look at it.

### Rob - 00:19:07
 so the kind of like the kind of like three different classes of, I mean, you could be really granular and say that people is is different from equipment, which of course is, but I think it's more of a, they're more similar than say people, absence, and demand sensing those are quite different

### Ruairi G - 00:19:36
 So, I think you got potentially for categories. I mean, not this is by chain guy, I think about it in terms of supply chain inputs. Physical. Inputs to your process people materials equipment, right outputs, which is your it's not demand, it is, it is shipment out. So this fulfillment it is one step

### Rob - 00:19:59
 Yep.

### Ruairi G - 00:20:02
 removed from demand, right? But it's not, it's not demand and then you have constraints. And in a way it makes kind of makes and then you got internal constraints and external constraints. So the the configuration of your manufacturing process will be an intercaternal constraint. Your demand signal will be an external constraint. And that's it. And that that's I like that split because it it it provides a technical point of separation, so that the integration patterns, For all of those different categories, those four different categories are all different. and the way you deploy changes or the way, the way, the way you kind of realize those those different factors if you like Is all different, right? So if you you know, it makes it makes sense from a engineering point of view, split them up in that way. It also it also maps on to the domains as well. The internal constraints are all part of manufacture or actually all part of what we call process domain.

### Ruairi G - 00:21:11
 A manufacturing inputs is is external to that and and you can split up the different inputs. According to different domains. Like, you know, materials imbalance is all part of imbalance supply chain domain outbound is all part of fulfillment domain. Um, your external constraints. Then again, you know, you could split those up according to According to domains like demand signal is what we call profit domain. Most other people call it. Order, I think order management.

### Rob - 00:21:40
 Yeah. Yeah.

### Ruairi G - 00:21:42
 So so yeah, I think that's a good way to think about it. Um, and maybe this demo, if we could choose one of these areas, one of these four areas for the initial demo, and if it works for one, then we could start picking off all the other four. And at the end of this, we'll we could have an all singing all dancing demo.

### Rob - 00:22:00
 Sure.

### Ruairi G - 00:22:01
 What would demonstrate pretty much your entire integration landscape for job

### Rob - 00:22:04
 Yep.

### Ruairi G - 00:22:04
 search?

### Rob - 00:22:05
 Yep.

### Ruairi G - 00:22:06
 so, the question is, What is a compelling user story? That's also very easy.

### Ruairi G - 00:22:20
 You mentioned reaction to a new order. What I thought is that You can introduce the idea prioritization. So, you know, you've prioritize the French order yet. The guys from Lisbon I've come along because they have a You know, the executive from the, from the, from the customer knows the chief executive of the manufacturer, He's you say. All right, Well, we now have to prize prioritize the smaller order and we have to see what impact that has on the Frenchies. So that's one. And then you have all the internal stuff like contamination control calibration of equipment yeah, other internal factors and then you have the external factors that you spoke about including like people scheduling Mercedes materials and so on and so forth and then That's that's supply chain really I guess so then you have, you know, changes to demand signal, new orders, anything in there.

### Rob - 00:23:10
 I think the demand one, maybe is It's not. I don't think any of them are particularly easy, but I think maybe that's an easier one. There's also just a Just a thought here, when When we're thinking about, Drug substance.

### Ruairi G - 00:23:45
 Hmm.

### Rob - 00:23:46
 We will have different challenges compared to drug. Product. So, the If you're a Packing site. Where you bring in API? And you are. stamping out the the tablets and putting them in blister packs, for example, That. That would have a separate profile to an API manufacturing plant because that is more about chemistry. whereas, when you take in the, the dry bulk powders,

### Ruairi G - 00:24:32
 Yeah.

### Rob - 00:24:34
 I mean, some of them are toxic but largely as long as they're maintained in prop environment, they're inert and you can You know, you can, you can feel around appeal with API in it, you know, around the factory. You can put on a shelf in the warehouse, you can take out, you know, it's it's more stable than the chemical synthesis process earlier in the in the plant or air, in another plant and the, the finished goods of the API, plant become the starting materials for the packing plant.

### Ruairi G - 00:25:15
 Yeah. Yeah, now I got that.

### Rob - 00:25:19
 So we might, we might need to, to say, we're going to do a packing facility. We're going to do our Tablet. Oral solid doors, tableting and packing. Plant. That's the scope of our version one and version two, we extend it back into doing a you know, chemical synthesis starting materials and you know, chemical processes

### Ruairi G - 00:25:44
 Yeah.

### Rob - 00:25:51
 fermentation

### Ruairi G - 00:25:53
 Yeah.

### Rob - 00:25:54
 Drying.

### Ruairi G - 00:25:55
 so the the reseller so if you want to use a final paracetam There are in, you can produce a blister pack in fight. There are certain countries you can get this non in Europe actually but you can also get it as a food supplement in in the US and they yeah and I send it in in these little

### Rob - 00:26:15
 oh,

### Ruairi G - 00:26:18
 capsules He's obviously using the guy uses a handheld or an or bags of powder bags like powder. In a plastic jar with like Foods Supplement written on the front of it. No. Yeah, this is legal by the way. It is legal. so, But it's a great use case because it's not because it's not regulated, you know, you don't get into, you know, it's it's in a complete it's in a made-up world but it's actually not made of It's real, you know. This is a real substance that you can buy on the Internet. Actually the manufacturing in Russia.

### Rob - 00:26:55
 Do they?

### Ruairi G - 00:26:55
 In Yeah, yeah. They it's expensive expensive. I mean, it's a great drug. Like, it's amazing. It's amazing drug but because it's not regulated in the Europe. Europe. You can't buy it. I'm super cheap to make and they sell it like about thirst, you know, about 30 quid for a packet of 30 tablets And it costs like pennies to make.

### Rob - 00:27:19
 What, what is it? What do people use it for?

### Ruairi G - 00:27:21
 It's a new tropic it's like modafinil but much more much more. It's it's really

### Rob - 00:27:23
 Okay.

### Ruairi G - 00:27:25
 clean. It's got very, it's got virtually. No side effects, they developed it journey during the 80s as part of the cosmonaut program. Yeah. And they since they since refined it, So so it's what it does, is it produces the simulates, the the blood flow in the brain. It's got a half-life of about four or five hours. And it gives you really heightened concentration memory, you know, cognitive it. Did. They mark It was described in in the early papers, the early scientific papers as providing improved, operant performance. It's it's on the schedule of this scheduled drug for the Anti-Doping agency, for World Athletics, because it's a student. If you take it after about three in the afternoon, then you can't sleep. But it's actually it's not it's not prescribed, you know, it's not it's not it's not a illegal and it does have it. It is said to have some, there have been some studies showing positive effects for Topical Alzheimer's patients. Yeah, but it also it's prescribed there is some there's there's a like a kidney function or a liver function disorder that it that it has a kind of a strange benefit towards so you can actually get it on prescription for this kind of quite specific condition in the US. Problem is, it's not, there's no money in it, you know? So, no, the big pharma

### Rob - 00:28:57
 Right.

### Ruairi G - 00:28:59
 companies have have been interested in, you know, in getting this approved because, you know, it's Really cheap to make, you know? And you know it's it's not it's not competitive. So anyway, so there you go, it's legal but it's you know, it's not approved. It's a really simple molecule, you know, so it's it's a really good case study I think.

### Rob - 00:29:22
 Cool. Okay.

### Ruairi G - 00:29:23
 For an end-to-end. So it's you think you think to start with maybe the packaging rather than the rather than the

### Rob - 00:29:30
 It's just, it's just simpler. Yeah.

### Ruairi G - 00:29:33
 Yeah. Okay. But because we got the we have the The drug. Definition File. The drug. What's it called? Drug manufacturer DMF.

### Rob - 00:29:46
 The master file. The drug master file. Yeah.

### Ruairi G - 00:29:48
 Dogma which which does a pretty good job. You start with the chemistry and it does a pretty good job of identifying all the input materials including

### Rob - 00:29:56
 Yep.

### Ruairi G - 00:29:57
 packaging. So I sent it to you. Right? So so we have all the input materials which will be

### Rob - 00:29:58
 Yes, yes.

### Ruairi G - 00:30:02
 great. When we, you know, when we start doing the job scheduling for packaging, we could that's all our inputs. So, do you want to? What what's the? So we can we do manufacturing process, and then we've got packaging process. It's not controversial, if we split it up like that,

### Rob - 00:30:24
 No tablet. And and packing would commonly be run on the adjacent lines.

### Ruairi G - 00:30:32
 yeah, okay, so we got tableting Well tableting wait, let's say manufacturing where we were actually manufacture. You know, we take the input materials, we combine them do stuff to them and we get power.

### Rob - 00:30:45
 Yeah.

### Ruairi G - 00:30:46
 Is that that's not is that housing?

### Rob - 00:30:47
 That's that's what it's it's the top level. Function is tableting, you would have a blending process.

### Ruairi G - 00:30:53
 Yeah.

### Ruairi G - 00:30:57
 Yeah.

### Rob - 00:30:58
 so the, you know, those big hoppers That that, you know, on the the continuous, manufacturing, press that mmic, they've got this this giant hopper. Well, the the Putin prescribed amounts of And the API powder along with excipients. So the excipients are Materials that help with either binding, the API protecting the API.

### Ruairi G - 00:31:34
 Mmm.

### Rob - 00:31:35
 Or things like disintegrants, which are the expand. So when it's when it touches water, so when it's ingested water, plus these, in disintegrants, kind of like

### Ruairi G - 00:31:47
 Yeah.

### Rob - 00:31:51
 like expand and it breaks apart the tablet, that's part of the, the enhancing

### Ruairi G - 00:31:51
 Yeah. Yeah.

### Rob - 00:31:57
 the metabolism of the, the drug. And but the blending is quite important to make sure that you don't get like strong concentrations of API in, you know, one

### Ruairi G - 00:32:11
 Hmm.

### Rob - 00:32:12
 Or things like disintegrants, which are the expand. So, when it's when it touches water, so when it's ingested water, plus these in disintegrates kind of particular part of the, of the mix. So you don't get one. That's got 40 milligrams and the next one's got 400 milligrams. It's it's

### Ruairi G - 00:32:21
 Yeah.

### Rob - 00:32:23
 Really well blended so that you can stamp out and Regularly consistently, get the right dosage in each each tablet. So, blending

### Ruairi G - 00:32:37
 Yeah.

### Rob - 00:32:38
 is part of the, the tablet in process. I mean, you could, you could call it something as a separate stage blending tableting packing, but I think people would generally understand that the tablet process includes. Blending.

### Ruairi G - 00:32:54
 Do you ever have some capsules and tablets coming off the same line, or

### Rob - 00:32:58
 Not of the same line, but they could be in in adjacent. So you could you you would use the, the blending. Formulation. Might be standard but then it would that you'd have to split it and put put some into you know, the capsule. Formulation would be chemically similar, if not identical. But the packaging form has got different requirements. So the with the capsule you tend to have uncompressed material,

### Ruairi G - 00:33:40
 Yeah.

### Rob - 00:33:41
 And so inside that material, you you need something that breaks down the capsule in the In the gut. But then you've just got the the powders inside.

### Ruairi G - 00:33:58
 Yeah.

### Rob - 00:33:58
 whereas, In the tableting, you're compressing all of these different things into the solid form.

### Ruairi G - 00:34:05
 Yeah, so that's quite it is not quite a common use case. I've got a basic drug and I want to produce it in both capsules and tablets and I want to use it. I want to do that in the same facility.

### Rob - 00:34:16
 I think that now this is, this is we ideally have a pharmacist in the room to answer this, but my understanding is

### Ruairi G - 00:34:26
 Yeah.

### Rob - 00:34:27
 that some materials are You know, you can get paracetamol in tablet or capture form.

### Ruairi G - 00:34:38
 Yeah.

### Rob - 00:34:39
 But my understanding is that some materials are easier to handle in capture form. Ie the the don't take to tableting very well. So the the material splinter or, you know, it breaks apart, or it, or it, and it degrades and tablet forms. It's difficult to hold in tablet form. In that case, you use a capsule. So I, although, there are examples of the same material going into the two different forms, I would say that it's an active choice for stability. you know, something that that actually

### Ruairi G - 00:35:24
 Hmm.

### Rob - 00:35:28
 People have thought about to see this material just isn't good in in tablet form.

### Ruairi G - 00:35:33
 Yeah, and that's why they say topicing. Yeah so so the manufacturing process is specific to the output form.

### Rob - 00:35:39
 Yes.

### Ruairi G - 00:35:40
 Yeah, okay so you don't have like a single blending which then goes off into how this thing encapsulfilling that you don't get that, right?

### Rob - 00:35:47
 No, because like I said, if you're if your tableting you would put in an excipient that helps to disintegrate the the material and you'd have another

### Ruairi G - 00:35:55
 Yeah. Yeah.

### Rob - 00:35:58
 material that is binding the API. To get together. You, you would have something you'd have a coating on the tablets, you know, that protects them in the upper part of your of your gut until they get into the, into the stomach and that would be materially different in the capture form. The API is just the API. You know, that's

### Ruairi G - 00:36:23
 Yeah. Yeah.

### Rob - 00:36:25
 you know, 400 milligrams 500 milligrams of paracetamol is Is the same powders, but the way that they're brought together would be would be different. So you would have You, you could have an API plant or an API line, that's generating the dry powders. And then, Some that goes into capsule form. Some of it goes into

### Ruairi G - 00:36:54
 I think, I think I've got a good, a good model, right? So So let's say, we got four four linear processes, broadly speaking, right? So we can keep this really high level. We don't go need to go into blending and coating and everything, right? So we can actually keep it at the level of tableting. As an entire process or capsule filling, creation. Whatever. As an entire

### Rob - 00:37:11
 Yeah.

### Ruairi G - 00:37:14
 process, right? So then we have four stages Receiving inputs, then the drug manufacturer which could be targeting. Then we got packaging.

### Rob - 00:37:25
 Yeah.

### Ruairi G - 00:37:25
 And then, we got dispatch. Right. So, that's level what we call Level One. I think it was an NYC. So we could then do two variants of manufacturing and packing.

### Rob - 00:37:39
 but,

### Ruairi G - 00:37:40
 So we have the same receiving process and we the same dispatch process. So it starts off and receiving, then splits into two, And then we wanted them is for cuts fuels, and one of them is for tablets. and then you make your capsules, fill your capsules, and you make your tablets two separate lines, And then they both go into two separate packing lines and you you fill your capsules. Put them in bottles and you you know compress your or you take all your tablets and you put it in blister packs.

### Rob - 00:38:07
 Yep.

### Ruairi G - 00:38:08
 And then it, then it rejoins again and it comes back into dispatch. Yeah that would be that's really easy. I mean, it's six six processes. And it's really simple to model and they both use the same data model. They both use the same input materials and you can even have going to the same customer. customer

### Rob - 00:38:29
 If you could yeah.

### Ruairi G - 00:38:31
 Like Tesco's.

### Rob - 00:38:32
 Yeah, you could have a good, it would probably go to a wholesaler.

### Ruairi G - 00:38:39
 Yeah. Yeah. That's

### Rob - 00:38:41
 But yeah, essentially it ends up in the Tesco shelf.

### Ruairi G - 00:38:45
 Yeah, so so if you're doing it, you could, you do this for the Russian market, right? And it would send, it would send blister packs, the final paracetam to To your pharmacists distributor, but it could also resell the powder to the guy in Arkansas. The Audi Arabia.

### Ruairi G - 00:39:09
 I think maybe we shouldn't use this one as these games.

### Rob - 00:39:13
 Yeah, moving moving. Quite powder from Russia, to Saudi Arabia, to America is

### Ruairi G - 00:39:13
 But yeah.

### Rob - 00:39:19
 probably going to get into trouble.

### Ruairi G - 00:39:20
 Yeah. Yeah, we're certainly get some questions. Okay. But I mean you see I think that's a pretty good use case, right? So but I mean, if you can see the parallels to paracetamol, I mean, you brackets Tesco's, you know? Okay, so that's good. Now, in terms of automation, so yeah, that's that's the architecture picture. We can see that. And underneath it we got the base Isa 95 process. What? What other So, we need to determine these the actual specific user story. We're going to focus on Problem statement. What what some Where which we need to do the data model, figure out which parts of the model we need to kind of you know expand what would be a good. User story. What? He's was exciting user story because none of this is complicated, right?

### Rob - 00:40:03
 and I, I

### Ruairi G - 00:40:06
 right? So

### Rob - 00:40:07
 i I think start with the, the demand one, I think, you know, we've got A rush, you know, we've we've we typically ship 30,000. Of product X to France every fortnight.

### Ruairi G - 00:40:28
 Yeah.

### Rob - 00:40:28
 For some reason. And this, this could be a You know, one of the distributors. Are wholesalers. They had water damage in the warehouse.

### Ruairi G - 00:40:36
 Mmm.

### Rob - 00:40:40
 So, product was spoiled.

### Ruairi G - 00:40:40
 Yeah. Yeah.

### Rob - 00:40:43
 So France would really appreciate a Double order. In the next fortnight. so, the French So, if you're GSK GSK France, Their one of their two main distributors has lost. All of their stock. So, the product going into the French market is severely constrained.

### Ruairi G - 00:41:11
 Yeah.

### Ruairi G - 00:41:15
 Yeah.

### Rob - 00:41:16
 So they want to make rather than 30,000. They want to make 60,000 over the next fortnight or or for the next two consecutive fortnights they want double. so, you've got The materials, but your schedule has got. Belgium, Denmark, Germany, you know which ones can you shuffle around to say, we want to put more volume towards France? Can I for example, put on a assuming that you run two shifts, could I run three shifts for The next month could I? Increase our batch size. For the next month, can I delay a shipment to some of these other European countries so that I can reallocate capacity to France. Those are you know, some of the material, you know, they they might, they might conceivably have Unlabeled. Product.

### Ruairi G - 00:42:34
 Yeah.

### Rob - 00:42:35
 As you know prefinished goods and it they call it late-stage customization where you wait until the last minute to label something up. It's the same chemical. chemical. Component. But You don't put it into the packaging until the The last minute.

### Ruairi G - 00:42:59
 Okay, I got it. Okay, coming up on time, right? So I yeah, really good. So, how about this, right? So we start with our our basics, Our basic business in setup is we got three customers, France, Germany, and Portugal, right? They all take a mix of tablets and powder. For our drug France, takes 30,000, tablets and whatever the equivalent is in powders, right? They've had water damage. One of their warehouse, the main warehouse, which is, which has got, which is destroyed all of the powder tablets are okay, because they're in water type district parks. Um so the question is they want it. They want to double powder orders for the next month. Do it. Fortnightly and a question is, Can we do it? What impact will this have on the schedule? You know any material? So basically just understand

### Rob - 00:43:49
 Yeah.

### Ruairi G - 00:43:51
 the whole kind of scheduling process that's so that's the basic setup and then I got three further questions. Which is what if we introduce two to three shifts. What if we what is, what is the, the max batch size? What if we change the batch sizes? What if we delay shipments for other customer? So there's just some of the questions that we can answer.

### Rob - 00:44:14
 Yeah.

### Ruairi G - 00:44:15
 Yeah.

### Rob - 00:44:17
 I mean, that's, that's realistic. That is realistic Tim. That's The.

### Ruairi G - 00:44:22
 So so that's pretty good. So I can do an architecture model. It's really simple. We our first, Our first use case requires input materials. Willing to basic information about, you know, the manufacturing process will will need order numbers. I didn't get all we need to order numbers for the other customers. I'll do that offline. Yeah, that's that's everything and I'll be able to do the data model and anything we need. I'll just extend the day tomorrow which is anything. That's not an ISA 95.

### Rob - 00:44:58
 Just ping me any questions or or any kind of like progress stuff and just say, does this look right? Or you know what what might have missed or you know,

### Ruairi G - 00:45:09
 Well.

### Rob - 00:45:09
 anything like that.

### Ruairi G - 00:45:10
 One thing that we need to decide is you know that without doing integrations with job, scheduling tools is is how we do the visualization. So we can do, we can work from like Google sheets or spreadsheets or whatever. But think about think about the best way of visualizing your jobs. You know, and and you know I think that we can work with Spreadsheets or

### Rob - 00:45:26
 Okay, okay.

### Ruairi G - 00:45:31
 Powerpoints or you know, whatever we want. It's got to be, You know, simple but like think of think of graphs or, You know,

### Rob - 00:45:39
 Yeah.

### Ruairi G - 00:45:39
 Maybe maybe just, you know, buckets of I have a think about the visualization of your job, right? I mean you've I haven't seen, you know, Pharma scheduling tools, but you have right. So think about Don't think about tools. Just think about what will be a really nice way. You got a schedule, right? The effect is agents change the schedule and then what is that visual thing? That shows that. Yeah.

### Rob - 00:46:02
 Yeah. I'll work on that.

### Ruairi G - 00:46:04
 Um yeah, have a look at that. And yeah, if we can build this, we can publish it. I'd love to go to, you know, get get back onto Graham and do a demo with some of the some of the folks that we'd

### Rob - 00:46:15
 Yeah.

### Ruairi G - 00:46:16
 think, or the very least, let's just publish it on LinkedIn and you know general

### Rob - 00:46:18
 Yes. Absolutely. Yeah. Yeah.

### Ruairi G - 00:46:19
 interest Yeah, yeah. Okay. We're out of time.

### Rob - 00:46:24
 I know, I know I need to rush sorry. Tim and this was, this was really

### Ruairi G - 00:46:26
 Yeah. Yeah.

### Rob - 00:46:29
 invigorating. I love this.

### Ruairi G - 00:46:30
 Well, let's let's try and do it like Yeah, yeah. Okay. All right. See you soon.

### Rob - 00:46:32
 Yeah. Yeah.

### Ruairi G - 00:46:35
 Yeah. Right.

### Rob - 00:46:35
 Tears. Yeah. Cheers fight.
