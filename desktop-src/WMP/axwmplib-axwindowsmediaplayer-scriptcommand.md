---
title: AxWindowsMediaPlayer 物件的 ScriptCommand 事件
description: 收到同步處理的命令或 URL 時，就會發生 ScriptCommand 事件。 |AxWindowsMediaPlayer 物件的 ScriptCommand 事件
ms.assetid: b6c613b2-f1b0-43d3-9992-c01d1e00e644
keywords:
- AxWindowsMediaPlayer 物件的 ScriptCommand 事件 Windows Media Player
topic_type:
- apiref
api_name:
- ScriptCommand Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49d004fbfc265784ef77969258ff168670d9907f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990227"
---
# <a name="scriptcommand-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="d0923-105">AxWindowsMediaPlayer 物件的 ScriptCommand 事件</span><span class="sxs-lookup"><span data-stu-id="d0923-105">ScriptCommand Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="d0923-106">收到同步處理的命令或 URL 時，就會發生 ScriptCommand 事件。</span><span class="sxs-lookup"><span data-stu-id="d0923-106">The ScriptCommand event occurs when a synchronized command or URL is received.</span></span>

``` syntax
[C#]
private void player_ScriptCommand(
  object sender,
  _WMPOCXEvents_ScriptCommandEvent e
)

[Visual Basic]
Private Sub player_ScriptCommand(  
  sender As Object, 
  e As _WMPOCXEvents_ScriptCommandEvent
) Handles player.ScriptCommand
```

## <a name="event-data"></a><span data-ttu-id="d0923-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="d0923-107">Event Data</span></span>

<span data-ttu-id="d0923-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ ScriptCommandEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="d0923-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEventHandler**.</span></span> <span data-ttu-id="d0923-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ ScriptCommandEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="d0923-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_ScriptCommandEvent**, which contains the following properties related to this event.</span></span>



| <span data-ttu-id="d0923-110">屬性</span><span class="sxs-lookup"><span data-stu-id="d0923-110">Property</span></span> | <span data-ttu-id="d0923-111">描述</span><span class="sxs-lookup"><span data-stu-id="d0923-111">Description</span></span>                                                   |
|----------|---------------------------------------------------------------|
| <span data-ttu-id="d0923-112">scType</span><span class="sxs-lookup"><span data-stu-id="d0923-112">scType</span></span>   | <span data-ttu-id="d0923-113">StringSpecifies 指令碼命令的類型。</span><span class="sxs-lookup"><span data-stu-id="d0923-113">System.StringSpecifies the type of script command.</span></span><br/> |
| <span data-ttu-id="d0923-114">參數</span><span class="sxs-lookup"><span data-stu-id="d0923-114">param</span></span>    | <span data-ttu-id="d0923-115">StringSpecifies 指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="d0923-115">System.StringSpecifies the script command.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="d0923-116">備註</span><span class="sxs-lookup"><span data-stu-id="d0923-116">Remarks</span></span>

<span data-ttu-id="d0923-117">命令可內嵌在 Windows Media 檔案或資料流程的音效和影像中。</span><span class="sxs-lookup"><span data-stu-id="d0923-117">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="d0923-118">這些命令是與資料流程中指定時間相關聯的一對 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="d0923-118">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="d0923-119">當資料流程到達與命令相關聯的時間時，Windows Media Player 控制項會傳送具有兩個參數的 **ScriptCommand** 事件。</span><span class="sxs-lookup"><span data-stu-id="d0923-119">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="d0923-120">其中一個參數指定要傳送的命令類型，另一個參數則指定命令。</span><span class="sxs-lookup"><span data-stu-id="d0923-120">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="d0923-121">參數的類型是用來決定如何處理命令參數。</span><span class="sxs-lookup"><span data-stu-id="d0923-121">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="d0923-122">任何類型的命令都可以內嵌在檔案或資料流程中，以供 **ScriptCommand** 事件處理。</span><span class="sxs-lookup"><span data-stu-id="d0923-122">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="d0923-123">下表列出 Windows Media Player 自動處理的指令碼命令類型。</span><span class="sxs-lookup"><span data-stu-id="d0923-123">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="d0923-124">類型</span><span class="sxs-lookup"><span data-stu-id="d0923-124">Type</span></span>                   | <span data-ttu-id="d0923-125">Description</span><span class="sxs-lookup"><span data-stu-id="d0923-125">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0923-126">CAPTION</span><span class="sxs-lookup"><span data-stu-id="d0923-126">CAPTION</span></span>                | <span data-ttu-id="d0923-127">控制項會在 IWMPClosedCaption 所指定的 HTML 元素中顯示相關聯的文字。**captioningId**。</span><span class="sxs-lookup"><span data-stu-id="d0923-127">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="d0923-128">事件</span><span class="sxs-lookup"><span data-stu-id="d0923-128">EVENT</span></span>                  | <span data-ttu-id="d0923-129">控制項會執行針對指定事件所定義的指示。</span><span class="sxs-lookup"><span data-stu-id="d0923-129">The control executes instructions defined for the specified event.</span></span>                                                                                                  |
| <span data-ttu-id="d0923-130">檔案名</span><span class="sxs-lookup"><span data-stu-id="d0923-130">FILENAME</span></span>               | <span data-ttu-id="d0923-131">控制項會重設其 **URL** 屬性、嘗試開啟指定的檔案，並立即開始播放新的資料流程。</span><span class="sxs-lookup"><span data-stu-id="d0923-131">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="d0923-132">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="d0923-132">OPENEVENT</span></span>              | <span data-ttu-id="d0923-133">緩衝相關聯的事件種類命令，以及時執行事件腳本。</span><span class="sxs-lookup"><span data-stu-id="d0923-133">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="d0923-134">SYNCHRONIZEDLYRICLYRIC</span><span class="sxs-lookup"><span data-stu-id="d0923-134">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="d0923-135">*Param* 參數包含已同步處理的歌詞文字。</span><span class="sxs-lookup"><span data-stu-id="d0923-135">The *param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="d0923-136">Windows Media Player 會在 [ **立即播放** ] 功能的 [隱藏式輔助字幕] 區域中顯示歌詞文字。</span><span class="sxs-lookup"><span data-stu-id="d0923-136">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="d0923-137">TEXT</span><span class="sxs-lookup"><span data-stu-id="d0923-137">TEXT</span></span>                   | <span data-ttu-id="d0923-138">控制項會在 IWMPClosedCaption 所指定的 HTML 元素中顯示相關聯的文字。**captioningId**。</span><span class="sxs-lookup"><span data-stu-id="d0923-138">The control displays the associated text in the HTML element specified by IWMPClosedCaption.**captioningId**.</span></span>                                                       |
| <span data-ttu-id="d0923-139">URL</span><span class="sxs-lookup"><span data-stu-id="d0923-139">URL</span></span>                    | <span data-ttu-id="d0923-140">如果 IWMPSettings，控制項會自動開啟使用預設網際網路瀏覽器指定的 URL。**invokeURLs** 屬性設定為 true。</span><span class="sxs-lookup"><span data-stu-id="d0923-140">The control automatically opens the URL specified using the default Internet browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span>                    |



 

<span data-ttu-id="d0923-141">只要您提供程式碼來處理命令，您就可以內嵌任何其他類型的命令。</span><span class="sxs-lookup"><span data-stu-id="d0923-141">You can embed any other type of command as long as you provide code to handle the command.</span></span> <span data-ttu-id="d0923-142">雖然 Windows Media Player 控制項會忽略未知的命令，但是仍會將它們移交給 **ScriptCommand** 事件。</span><span class="sxs-lookup"><span data-stu-id="d0923-142">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="d0923-143">如果以向前快轉或倒轉模式掃描檔案，就不會呼叫 ScriptCommand 事件。</span><span class="sxs-lookup"><span data-stu-id="d0923-143">The ScriptCommand event is not called if the file is being scanned in fast forward or rewind mode.</span></span>

<span data-ttu-id="d0923-144">如果 IWMPSettings，則會在您的預設網頁瀏覽器中自動叫用 Windows Media Player 控制項所收到的 URL 命令。**invokeURLs** 屬性設定為 true。</span><span class="sxs-lookup"><span data-stu-id="d0923-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the IWMPSettings.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="d0923-145">您可以使用 IWMPSettings。**defaultFrame** 屬性，以指定網頁出現的目標框架。</span><span class="sxs-lookup"><span data-stu-id="d0923-145">You can use the IWMPSettings.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="d0923-146">傳送給 Windows Media Player 的 URL 會相對於 IWMPSettings 所指定的基底 URL 進行處理。**baseURL** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d0923-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the IWMPSettings.**baseURL** property.</span></span> <span data-ttu-id="d0923-147">基底 URL 會與相對 URL 串連，以產生完整指定的 URL，該 URL 會以 **ScriptCommand** 事件的命令參數形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="d0923-147">The base URL is concatenated with the relative URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="d0923-148">Windows Media Player 控制項一律會以下列方式處理傳入的 URL 命令：</span><span class="sxs-lookup"><span data-stu-id="d0923-148">The Windows Media Player control always processes incoming URL commands in the following manner:</span></span>

1.  <span data-ttu-id="d0923-149">收到 URL 類型命令。</span><span class="sxs-lookup"><span data-stu-id="d0923-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="d0923-150">IWMPSettings.**baseURL** 是用來從指令碼命令中指定的相對 URL 建立完整的 url。</span><span class="sxs-lookup"><span data-stu-id="d0923-150">IWMPSettings.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="d0923-151">呼叫 **ScriptCommand** 。</span><span class="sxs-lookup"><span data-stu-id="d0923-151">**ScriptCommand** is called.</span></span>
4.  <span data-ttu-id="d0923-152">**ScriptCommand** 傳回之後，IWMPSettings。**invokeURLs** 已核取。</span><span class="sxs-lookup"><span data-stu-id="d0923-152">After **ScriptCommand** returns, IWMPSettings.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="d0923-153">如果為 IWMPSettings，則為。**invokeURLs** 為 true，而且命令是 URL 命令，會叫用指定的 url。</span><span class="sxs-lookup"><span data-stu-id="d0923-153">If IWMPSettings.**invokeURLs** is true and the command is a URL command, the specified URL is invoked.</span></span> <span data-ttu-id="d0923-154">如果為 IWMPSettings，則為。**invokeURLs** 為 false，或如果命令不是 URL 命令，則會忽略此命令。</span><span class="sxs-lookup"><span data-stu-id="d0923-154">If IWMPSettings.**invokeURLs** is false or if the command is not a URL command, the command is ignored.</span></span>

<span data-ttu-id="d0923-155">撰寫 Windows Media 檔案時，您可以將兩個符號和框架名稱串連在參數欄位中，以指定要在其中顯示新 URL 的框架。</span><span class="sxs-lookup"><span data-stu-id="d0923-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="d0923-156">下列範例說明一般 **ScriptCommand** 參數。</span><span class="sxs-lookup"><span data-stu-id="d0923-156">The following example illustrates typical **ScriptCommand** parameters.</span></span> <span data-ttu-id="d0923-157">它會指定必須在 *myframe* 框架中啟動 URL *mypage.aspx* 。</span><span class="sxs-lookup"><span data-stu-id="d0923-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```CSharp
scType = "URL"
Param = https://myweb/mypage.html&&myframe
```



<span data-ttu-id="d0923-158">如果正在掃描檔案 (快速轉送或倒轉) ，則不會呼叫 ScriptCommand 事件。</span><span class="sxs-lookup"><span data-stu-id="d0923-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or rewound).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0923-159">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0923-159">Requirements</span></span>



| <span data-ttu-id="d0923-160">需求</span><span class="sxs-lookup"><span data-stu-id="d0923-160">Requirement</span></span> | <span data-ttu-id="d0923-161">值</span><span class="sxs-lookup"><span data-stu-id="d0923-161">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0923-162">版本</span><span class="sxs-lookup"><span data-stu-id="d0923-162">Version</span></span><br/>   | <span data-ttu-id="d0923-163">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d0923-163">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="d0923-164">命名空間</span><span class="sxs-lookup"><span data-stu-id="d0923-164">Namespace</span></span><br/> | <span data-ttu-id="d0923-165">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="d0923-165">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="d0923-166">組件</span><span class="sxs-lookup"><span data-stu-id="d0923-166">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d0923-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d0923-167"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0923-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0923-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0923-169">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d0923-169">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d0923-170">**AxWindowsMediaPlayer (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d0923-170">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d0923-171">**IWMPClosedCaption. captioningId (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d0923-171">**IWMPClosedCaption.captioningId (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d0923-172">**IWMPSettings. baseURL (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d0923-172">**IWMPSettings.baseURL (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-baseurl--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d0923-173">**IWMPSettings. defaultFrame (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d0923-173">**IWMPSettings.defaultFrame (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-defaultframe--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d0923-174">**IWMPSettings. invokeURLs (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d0923-174">**IWMPSettings.invokeURLs (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-invokeurls--vb-and-c.md)
</dt> </dl>

 

 





