---
title: ScriptCommand 事件
description: 收到同步處理的命令或 URL 時，就會發生 ScriptCommand 事件。 |ScriptCommand 事件
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- ScriptCommand 事件 Windows Media Player
- ScriptCommand 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，ScriptCommand 事件
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f9ca7ec22694956e1d91d055e8db057a91ecca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995527"
---
# <a name="playerscriptcommand-event"></a><span data-ttu-id="313a5-107">ScriptCommand 事件</span><span class="sxs-lookup"><span data-stu-id="313a5-107">Player.ScriptCommand event</span></span>

<span data-ttu-id="313a5-108">收到同步處理的命令或 URL 時，就會發生 **ScriptCommand** 事件。</span><span class="sxs-lookup"><span data-stu-id="313a5-108">The **ScriptCommand** event occurs when a synchronized command or URL is received.</span></span>

## <a name="syntax"></a><span data-ttu-id="313a5-109">語法</span><span class="sxs-lookup"><span data-stu-id="313a5-109">Syntax</span></span>


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a><span data-ttu-id="313a5-110">參數</span><span class="sxs-lookup"><span data-stu-id="313a5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="313a5-111">*scType*</span><span class="sxs-lookup"><span data-stu-id="313a5-111">*scType*</span></span> 
</dt> <dd>

<span data-ttu-id="313a5-112">字串，指定指令碼命令的類型。</span><span class="sxs-lookup"><span data-stu-id="313a5-112">String specifying the type of script command.</span></span>

</dd> <dt>

<span data-ttu-id="313a5-113">*參數*</span><span class="sxs-lookup"><span data-stu-id="313a5-113">*Param*</span></span> 
</dt> <dd>

<span data-ttu-id="313a5-114">指定指令碼命令的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="313a5-114">**String** specifying the script command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="313a5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="313a5-115">Return value</span></span>

<span data-ttu-id="313a5-116">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="313a5-116">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="313a5-117">備註</span><span class="sxs-lookup"><span data-stu-id="313a5-117">Remarks</span></span>

<span data-ttu-id="313a5-118">命令可內嵌在 Windows Media 檔案或資料流程的音效和影像中。</span><span class="sxs-lookup"><span data-stu-id="313a5-118">Commands can be embedded among the sounds and images of a Windows Media file or stream.</span></span> <span data-ttu-id="313a5-119">這些命令是與資料流程中指定時間相關聯的一對 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="313a5-119">The commands are a pair of Unicode strings associated with a designated time in the stream.</span></span> <span data-ttu-id="313a5-120">當資料流程到達與命令相關聯的時間時，Windows Media Player 控制項會傳送具有兩個參數的 **ScriptCommand** 事件。</span><span class="sxs-lookup"><span data-stu-id="313a5-120">When the stream reaches the time associated with the command, the Windows Media Player control sends a **ScriptCommand** event with two parameters.</span></span> <span data-ttu-id="313a5-121">其中一個參數指定要傳送的命令類型，另一個參數則指定命令。</span><span class="sxs-lookup"><span data-stu-id="313a5-121">One parameter specifies the type of command being sent, and the other parameter specifies the command.</span></span> <span data-ttu-id="313a5-122">參數的類型是用來決定如何處理命令參數。</span><span class="sxs-lookup"><span data-stu-id="313a5-122">The type of parameter is used to determine how the command parameter is processed.</span></span> <span data-ttu-id="313a5-123">任何類型的命令都可以內嵌在檔案或資料流程中，以供 **ScriptCommand** 事件處理。</span><span class="sxs-lookup"><span data-stu-id="313a5-123">Any type of command can be embedded in a file or stream to be handled by the **ScriptCommand** event.</span></span>

<span data-ttu-id="313a5-124">下表列出 Windows Media Player 自動處理的指令碼命令類型。</span><span class="sxs-lookup"><span data-stu-id="313a5-124">The following table lists script command types that are automatically processed by Windows Media Player.</span></span>



| <span data-ttu-id="313a5-125">類型</span><span class="sxs-lookup"><span data-stu-id="313a5-125">Type</span></span>                   | <span data-ttu-id="313a5-126">Description</span><span class="sxs-lookup"><span data-stu-id="313a5-126">Description</span></span>                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="313a5-127">CAPTION</span><span class="sxs-lookup"><span data-stu-id="313a5-127">CAPTION</span></span>                | <span data-ttu-id="313a5-128">控制項會在 *ClosedCaption* 所指定的 DIV 中顯示相關聯的文字。**captioningID**。</span><span class="sxs-lookup"><span data-stu-id="313a5-128">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="313a5-129">事件</span><span class="sxs-lookup"><span data-stu-id="313a5-129">EVENT</span></span>                  | <span data-ttu-id="313a5-130">告訴控制項執行針對指定事件所定義的指示。</span><span class="sxs-lookup"><span data-stu-id="313a5-130">Tells the control to execute instructions defined for the specified event.</span></span>                                                                                          |
| <span data-ttu-id="313a5-131">檔案名</span><span class="sxs-lookup"><span data-stu-id="313a5-131">FILENAME</span></span>               | <span data-ttu-id="313a5-132">控制項會重設其 **URL** 屬性、嘗試開啟指定的檔案，並立即開始播放新的資料流程。</span><span class="sxs-lookup"><span data-stu-id="313a5-132">The control resets its **URL** property, attempts to open the specified file, and begins playing the new stream immediately.</span></span>                                        |
| <span data-ttu-id="313a5-133">OPENEVENT</span><span class="sxs-lookup"><span data-stu-id="313a5-133">OPENEVENT</span></span>              | <span data-ttu-id="313a5-134">緩衝相關聯的事件種類命令，以及時執行事件腳本。</span><span class="sxs-lookup"><span data-stu-id="313a5-134">Buffers the associated EVENT type command for timely execution of the EVENT script.</span></span>                                                                                 |
| <span data-ttu-id="313a5-135">SYNCHRONIZEDLYRICLYRIC</span><span class="sxs-lookup"><span data-stu-id="313a5-135">SYNCHRONIZEDLYRICLYRIC</span></span> | <span data-ttu-id="313a5-136">*Param* 參數包含已同步處理的歌詞文字。</span><span class="sxs-lookup"><span data-stu-id="313a5-136">The *Param* parameter contains the synchronized lyric text.</span></span> <span data-ttu-id="313a5-137">Windows Media Player 會在 [ **立即播放** ] 功能的 [隱藏式輔助字幕] 區域中顯示歌詞文字。</span><span class="sxs-lookup"><span data-stu-id="313a5-137">Windows Media Player displays the lyric text in the closed caption area of the **Now Playing** feature.</span></span> |
| <span data-ttu-id="313a5-138">TEXT</span><span class="sxs-lookup"><span data-stu-id="313a5-138">TEXT</span></span>                   | <span data-ttu-id="313a5-139">控制項會在 *ClosedCaption* 所指定的 DIV 中顯示相關聯的文字。**captioningID**。</span><span class="sxs-lookup"><span data-stu-id="313a5-139">The control displays the associated text in the DIV specified by *ClosedCaption*.**captioningID**.</span></span>                                                                  |
| <span data-ttu-id="313a5-140">URL</span><span class="sxs-lookup"><span data-stu-id="313a5-140">URL</span></span>                    | <span data-ttu-id="313a5-141">如果 *設定* 為，控制項會自動開啟使用預設網際網路瀏覽器指定的 URL。**invokeURLs** 屬性設定為 true。</span><span class="sxs-lookup"><span data-stu-id="313a5-141">The control automatically opens the URL specified using the default Internet browser if the *Settings*.**invokeURLs** property is set to true.</span></span>                      |



 

<span data-ttu-id="313a5-142">只要您提供交互程式碼來處理命令，您就可以內嵌任何其他類型的命令。</span><span class="sxs-lookup"><span data-stu-id="313a5-142">You can embed any other type of command as long as you provide reciprocal code to handle the command.</span></span> <span data-ttu-id="313a5-143">雖然 Windows Media Player 控制項會忽略未知的命令，但是仍會將它們移交給 **ScriptCommand** 事件。</span><span class="sxs-lookup"><span data-stu-id="313a5-143">Though unknown commands are ignored by the Windows Media Player control, they are still handed off to the **ScriptCommand** event.</span></span>

<span data-ttu-id="313a5-144">如果 *設定*，則會在您的預設網頁瀏覽器中自動叫用 Windows Media Player 控制項所收到的 URL 命令。**invokeURLs** 屬性設定為 true。</span><span class="sxs-lookup"><span data-stu-id="313a5-144">URL commands received by the Windows Media Player control are invoked automatically in your default Web browser if the *Settings*.**invokeURLs** property is set to true.</span></span> <span data-ttu-id="313a5-145">您可以使用這些 *設定*。**defaultFrame** 屬性，以指定網頁出現的目標框架。</span><span class="sxs-lookup"><span data-stu-id="313a5-145">You can use the *Settings*.**defaultFrame** property to specify the target frame in which the webpage appears.</span></span>

<span data-ttu-id="313a5-146">傳送給 Windows Media Player 的 URL 會相對於 *設定* 所指定的基底 url 進行處理。**baseURL** 屬性。</span><span class="sxs-lookup"><span data-stu-id="313a5-146">The URL sent to Windows Media Player is processed relative to the base URL specified by the *Settings*.**baseURL** property.</span></span> <span data-ttu-id="313a5-147">基底 URL 會與相對指定的 URL 串連，以產生完整指定的 URL，以 **ScriptCommand** 事件的命令參數形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="313a5-147">The base URL is concatenated with the relatively specified URL, resulting in a fully specified URL that is passed as the command parameter by the **ScriptCommand** event.</span></span>

<span data-ttu-id="313a5-148">Windows Media Player 控制項一律會以下列方式處理傳入的 URL 類型命令：</span><span class="sxs-lookup"><span data-stu-id="313a5-148">The Windows Media Player control always processes incoming URL-type commands in the following manner:</span></span>

1.  <span data-ttu-id="313a5-149">收到 URL 類型命令。</span><span class="sxs-lookup"><span data-stu-id="313a5-149">A URL-type command is received.</span></span>
2.  <span data-ttu-id="313a5-150">*設定*。**baseURL** 是用來從指令碼命令中指定的相對 URL 建立完整的 url。</span><span class="sxs-lookup"><span data-stu-id="313a5-150">*Settings*.**baseURL** is used to create a full URL from the relative URL specified in the script command.</span></span>
3.  <span data-ttu-id="313a5-151">呼叫 *ScriptCommand* 。</span><span class="sxs-lookup"><span data-stu-id="313a5-151">*ScriptCommand* is called.</span></span>
4.  <span data-ttu-id="313a5-152">*ScriptCommand* 傳回之後，*設定*。**invokeURLs** 已核取。</span><span class="sxs-lookup"><span data-stu-id="313a5-152">After *ScriptCommand* returns, *Settings*.**invokeURLs** is checked.</span></span>
5.  <span data-ttu-id="313a5-153">如果 *設定*，則為。**invokeURLs** 為 true，而且命令是 URL 類型，會叫用指定的 url。</span><span class="sxs-lookup"><span data-stu-id="313a5-153">If *Settings*.**invokeURLs** is true and the command is a URL-type, the specified URL is invoked.</span></span> <span data-ttu-id="313a5-154">如果 *設定*，則為。**invokeURLs** 為 false，或如果命令不是 URL 類型，則會忽略此命令。</span><span class="sxs-lookup"><span data-stu-id="313a5-154">If *Settings*.**invokeURLs** is false or if the command is not a URL-type, the command is ignored.</span></span>

<span data-ttu-id="313a5-155">撰寫 Windows Media 檔案時，您可以將兩個符號和框架名稱串連在參數欄位中，以指定要在其中顯示新 URL 的框架。</span><span class="sxs-lookup"><span data-stu-id="313a5-155">When authoring a Windows Media file, you can specify which frame the new URL is displayed in by concatenating two ampersands and the name of the frame in the parameter field.</span></span> <span data-ttu-id="313a5-156">下列範例說明一般 *ScriptCommand* 參數。</span><span class="sxs-lookup"><span data-stu-id="313a5-156">The example below illustrates typical *ScriptCommand* parameters.</span></span> <span data-ttu-id="313a5-157">它會指定必須在 *myframe* 框架中啟動 URL *mypage.aspx* 。</span><span class="sxs-lookup"><span data-stu-id="313a5-157">It specifies that the URL *mypage* must be launched in the *myframe* frame.</span></span>


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



<span data-ttu-id="313a5-158">如果正在掃描檔案 (向前轉送或快速反轉) ，則不會呼叫 ScriptCommand 事件。</span><span class="sxs-lookup"><span data-stu-id="313a5-158">The ScriptCommand event is not called if the file is being scanned (fast-forwarded or fast-reversed).</span></span>

<span data-ttu-id="313a5-159">事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入之 JScript 檔案中的方法。</span><span class="sxs-lookup"><span data-stu-id="313a5-159">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="313a5-160">此參數名稱的類型必須完全如所示，包括大小寫。</span><span class="sxs-lookup"><span data-stu-id="313a5-160">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="313a5-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="313a5-161">Requirements</span></span>



| <span data-ttu-id="313a5-162">需求</span><span class="sxs-lookup"><span data-stu-id="313a5-162">Requirement</span></span> | <span data-ttu-id="313a5-163">值</span><span class="sxs-lookup"><span data-stu-id="313a5-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="313a5-164">版本</span><span class="sxs-lookup"><span data-stu-id="313a5-164">Version</span></span><br/> | <span data-ttu-id="313a5-165">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="313a5-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="313a5-166">DLL</span><span class="sxs-lookup"><span data-stu-id="313a5-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="313a5-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="313a5-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="313a5-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="313a5-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="313a5-169">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="313a5-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="313a5-170">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="313a5-170">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="313a5-171">**設定. baseURL**</span><span class="sxs-lookup"><span data-stu-id="313a5-171">**Settings.baseURL**</span></span>](settings-baseurl.md)
</dt> <dt>

[<span data-ttu-id="313a5-172">**設定. defaultFrame**</span><span class="sxs-lookup"><span data-stu-id="313a5-172">**Settings.defaultFrame**</span></span>](settings-defaultframe.md)
</dt> <dt>

[<span data-ttu-id="313a5-173">**設定. invokeURLs**</span><span class="sxs-lookup"><span data-stu-id="313a5-173">**Settings.invokeURLs**</span></span>](settings-invokeurls.md)
</dt> </dl>

 

 





