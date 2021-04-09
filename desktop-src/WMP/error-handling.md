---
title: 處理 (Windows Media Player SDK) 時發生錯誤
description: 錯誤處理
ms.assetid: f0567c77-a855-4b93-9fb7-a36cde63859f
keywords:
- Windows Media Player，錯誤處理
- Windows Media Player 物件模型、錯誤處理
- 物件模型、錯誤處理
- Windows Media Player ActiveX 控制項，錯誤處理
- ActiveX 控制項，錯誤處理
- Windows Media Player 的行動 ActiveX 控制項、錯誤處理
- Windows Media Player 行動電話，錯誤處理
- 遷移指南，錯誤處理
- 物件模型中的錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3b96e04d24009ee4b7e5819fdb26dfd6effd63
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104093576"
---
# <a name="error-handling-windows-media-player-sdk"></a><span data-ttu-id="123a3-112">處理 (Windows Media Player SDK) 時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="123a3-112">Error Handling (Windows Media Player SDK)</span></span>

<span data-ttu-id="123a3-113">Windows Media Player 6.4 ActiveX 控制項藉由在對話方塊和狀態列上顯示錯誤訊息，提供預設錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="123a3-113">The Windows Media Player 6.4 ActiveX control provides default error handling by displaying error messages in dialog boxes and on the status bar.</span></span> <span data-ttu-id="123a3-114">您也可以藉由處理腳本中的錯誤，提供自訂錯誤處理。</span><span class="sxs-lookup"><span data-stu-id="123a3-114">You can also provide custom error handling by processing errors in your script.</span></span> <span data-ttu-id="123a3-115">錯誤處理是事件驅動的，這表示您會收到每個錯誤的通知，且必須決定每個錯誤事件發生時如何處理。</span><span class="sxs-lookup"><span data-stu-id="123a3-115">Error handling is event driven, which means you receive a notification for each error, and must decide how to deal with each error event when it occurs.</span></span> <span data-ttu-id="123a3-116">如需使用6.4 版物件模型處理錯誤的詳細資訊，請參閱《 6.4 Player 物件模型指南》的「錯誤處理」一節，這是 Windows Media Player SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="123a3-116">For more information about handling errors using the version 6.4 object model, see the Error Handling section of the Version 6.4 Player Object Model Guide, which is part of the Windows Media Player SDK.</span></span>

<span data-ttu-id="123a3-117">Windows Media Player 7 或更新版本的物件模型會提供 **Error** 物件和 **ErrorItem** 物件來處理錯誤。</span><span class="sxs-lookup"><span data-stu-id="123a3-117">The Windows Media Player 7 or later object model provides the **Error** object and the **ErrorItem** object to handle errors.</span></span> <span data-ttu-id="123a3-118">這兩個物件會一起運作，以提供錯誤處理機制，讓您能夠完整且彈性地控制錯誤處理常式。</span><span class="sxs-lookup"><span data-stu-id="123a3-118">These two objects work together to provide you with an error handling mechanism that gives you complete and flexible control of the error handling process.</span></span> <span data-ttu-id="123a3-119">**Error** 物件提供 **ErrorItem** 物件集合的存取權;每個 **ErrorItem** 物件都會提供個別錯誤訊息的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="123a3-119">The **Error** object provides access to a collection of **ErrorItem** objects; each **ErrorItem** object provides details about an individual error message.</span></span>

<span data-ttu-id="123a3-120">發生錯誤時，錯誤資訊會張貼到錯誤佇列。</span><span class="sxs-lookup"><span data-stu-id="123a3-120">When an error occurs, the error information is posted to an error queue.</span></span> <span data-ttu-id="123a3-121">佇列是 **ErrorItem** 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="123a3-121">The queue is a collection of **ErrorItem** objects.</span></span> <span data-ttu-id="123a3-122">當每個錯誤新增至佇列時，它會與索引編號相關聯， (從) 零開始，可以用來識別特定的 **ErrorItem** 物件。</span><span class="sxs-lookup"><span data-stu-id="123a3-122">As each error is added to the queue, it is associated with an index number (beginning with zero) that can be used to identify the particular **ErrorItem** object.</span></span> <span data-ttu-id="123a3-123">*錯誤*。**errorCount** 屬性會捕獲錯誤佇列中的錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="123a3-123">The *Error*.**errorCount** property retrieves the number of errors in the error queue.</span></span> <span data-ttu-id="123a3-124">因為索引編號是以零為起始，所以張貼至佇列的最新錯誤一律會有等於 *錯誤* 的索引值。**errorCount** 減一。</span><span class="sxs-lookup"><span data-stu-id="123a3-124">Since the index numbers are zero-based, the most recent error posted to the queue will always have an index value equal to *Error*.**errorCount** minus one.</span></span>

<span data-ttu-id="123a3-125">您可以使用腳本來建立 Windows Media Player 的錯誤事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="123a3-125">You can create an error event handler for Windows Media Player using script.</span></span> <span data-ttu-id="123a3-126">下列 JScript 範例示範如何從錯誤佇列中取出最新的錯誤專案，並使用 Windows Media Player 7 或更新版本的物件模型來顯示錯誤碼和錯誤描述。</span><span class="sxs-lookup"><span data-stu-id="123a3-126">The following JScript example shows how to retrieve the most recent error item from the error queue and display the error code and error description using the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="123a3-127">使用 ID = "WMP9" 建立 **Player** 物件。</span><span class="sxs-lookup"><span data-stu-id="123a3-127">The **Player** object was created with ID = "WMP9".</span></span>


```C++
<!-- Create an error event handler for Windows Media Player 7 or later errors. -->
<SCRIPT  LANGUAGE = "JScript"  FOR = WMP9  EVENT = error()>

// Store the number of errors in the error queue.
var max = WMP9.error.errorCount;

// Retrieve most recent ErrorItem object.
var err = WMP9.error.item(max-1)

// Store the error code number.
var errNum = err.errorCode;

// Store the error description string.
var errDesc = err.errorDescription;

// Build a message string to notify the user.
var msg = "Error number: " + errNum + "\n";
msg += "Error description: " + errDesc;

// Display the message box.
alert(msg);

</SCRIPT>

```



<span data-ttu-id="123a3-128">**錯誤** 物件有兩種可供您使用的額外方法。</span><span class="sxs-lookup"><span data-stu-id="123a3-128">The **Error** object has two additional methods that you can use.</span></span> <span data-ttu-id="123a3-129">*錯誤*。**clearErrorQueue** 方法可讓您從錯誤佇列中移除所有錯誤，並將索引編號重設為零。</span><span class="sxs-lookup"><span data-stu-id="123a3-129">The *Error*.**clearErrorQueue** method allows you to remove all the errors from the error queue and reset the index number to zero.</span></span> <span data-ttu-id="123a3-130">您可以完全掌控此程式;您可以將錯誤保留在佇列中，只要您需要它們才能使用，然後在完成處理錯誤時清空佇列。</span><span class="sxs-lookup"><span data-stu-id="123a3-130">You have complete control over this process; you can keep errors in the queue for as long as you need them to be available, and then empty the queue when you're finished handling the errors.</span></span>

<span data-ttu-id="123a3-131">*錯誤*。**webHelp** 方法提供一種方式，可使用網際網路向使用者顯示最新的錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="123a3-131">The *Error*.**webHelp** method provides a way to display the most current error information to the user by using the Internet.</span></span> <span data-ttu-id="123a3-132">當呼叫時，這個方法會傳送佇列中第一個錯誤的所有相關資訊， (索引為零) 至 Microsoft Windows Media Player Web 說明，這會在目前的瀏覽器視窗中顯示錯誤的進一步資訊。</span><span class="sxs-lookup"><span data-stu-id="123a3-132">When called, this method transfers all relevant information about the first error in the queue (the one with index zero) to Microsoft Windows Media Player Web Help, which displays further information about the error in the current browser window.</span></span>

## <a name="related-topics"></a><span data-ttu-id="123a3-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="123a3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="123a3-134">**Error 物件**</span><span class="sxs-lookup"><span data-stu-id="123a3-134">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="123a3-135">**ErrorItem 物件**</span><span class="sxs-lookup"><span data-stu-id="123a3-135">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="123a3-136">**物件模型遷移指南**</span><span class="sxs-lookup"><span data-stu-id="123a3-136">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




