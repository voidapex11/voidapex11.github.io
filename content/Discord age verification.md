This is an article about discords age verification push, and what I found reading about it. In the [first press release](https://discord.com/press-releases/discord-launches-teen-by-default-settings-globally) about this, they claim that "`Facial scans never leave your device. Discord and our vendor partners never receive it.`" and that "`IDs are used to get your age only and then deleted.`". However, they are woolly about when exactly this will happen, e.g. "`Identity documents`...`are deleted quickly— in`**`most`**`cases, immediately`". 

Digging into where this is sent, I found this quote suggests that discords main age verification provider is [k-ID](https://www.k-id.com/)
> Discord and k-ID do not permanently store personal identity documents or your video selfies. Images
> [Source](https://support.discord.com/hc/en-us/articles/33362401287959-What-s-Changing-for-UK-and-Australian-Users#h_01KBKHG0AXD0XK806RNTYHM2W9)

Reading k-ID's [privacy policy](https://www.k-id.com/privacy-policy) I found that the technology that discord uses for face scans was lightly k-ID's "`Facial Age Estimation`" technology, which is provided to them by [Privately](https://www.privately.eu).
> k-ID does NOT store the information that you provide to prove your age and/or parent/guardian status. **All** **we store is the result of the validation process (i.e., whether you passed or failed).** In the case of Facial Age Estimation (“**FAE**”) technology provided by Privately, the facial image you provide is processed **solely on your device** – we don’t actually see any faces that are processed via this solution.
> [Source](https://www.k-id.com/privacy-policy), emphasis in original.

This conclusion is reinforced by k-ID's [subprocessors page](https://security.k-id.com/subprocessors).
![[Privately_subprocessor.png]]

And finally, in Privately's [privacy policy](https://www.privately.eu/privacy-policy-en), they have this to say about user data. I think that k-ID uses the FaceAssure SDK, but I could not find any more detail other than that it, according to Privately, matches the claims made by Discord and k-ID about user data.
> - FaceAssure SDKs deployed in client solutions: We do not collect any user data since end user relationships are managed by Clients themselves within their closed environments. 
> - FaceAssure Web browser Solution: In this implementation we are subprocessors of data and will process user data on the browser of the user on behalf of our Client. We will only retain a session ID and an age range and no other Personal Identifiable Information about the end user.

> - Through OWAS Safety SDK deployed in client applications: We do not acquire any user data.
> - Through AgeAssure SDK deployed in client solutions :We do not acquire any user data.
> - AgeAssure Web browser Solution: We will retain a session ID and an age range and no other Personal Identifiable Information about the end user for the duration that is required by our Client.

This suggests that the data does not leave the client, that is to say your, device.

I hope this has cleared up some questions about your data being processed by discord age verification, but if you want to learn about the processing of government ID's, you'll have to wait for me, or someone else to read through 10 more privacy policy's.