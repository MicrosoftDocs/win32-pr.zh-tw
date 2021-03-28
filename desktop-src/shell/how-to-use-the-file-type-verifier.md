---
description: 本主題說明如何使用 Windows 7 SDK 中所提供的檔案類型驗證器。
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: 如何使用檔案類型驗證器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f083897499f972f945867a0c02318df192e734d9
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/28/2021
ms.locfileid: "104195635"
---
# <a name="how-to-use-the-file-type-verifier"></a><span data-ttu-id="3ea53-103">如何使用檔案類型驗證器</span><span class="sxs-lookup"><span data-stu-id="3ea53-103">How to Use the File Type Verifier</span></span>

<span data-ttu-id="3ea53-104">本主題說明如何使用 [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)中所提供的檔案類型驗證器。</span><span class="sxs-lookup"><span data-stu-id="3ea53-104">This topic describes how to use the File Type Verifier that is provided in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3ea53-105">如果您的程式會從 Windows Shell 建立使用者預期要與之互動的檔案類型 (通常儲存在使用者的已知資料夾（例如 **我的檔**) ）中，請務必測試您的應用程式，並確認它所建立的檔案已正確註冊，並在流覽和搜尋檔案時提供高品質的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="3ea53-105">If your program creates file types that users are expected to interact with from the Windows Shell (typically stored in a user's known folder such as **My Documents**), it is very important to test your application and verify that the files it creates are properly registered and provide a high-quality user experience when browsing and searching files.</span></span> <span data-ttu-id="3ea53-106">如果您希望使用者在 Windows 7 上執行您的應用程式，而該應用程式依賴許多 Shell 功能的高品質檔案類型處理常式，則這點特別重要。</span><span class="sxs-lookup"><span data-stu-id="3ea53-106">This is especially important if you expect users to run your applications on Windows 7, which relies on high-quality file type handlers for many of the Shell features.</span></span>

<span data-ttu-id="3ea53-107">若要使用檔案類型驗證器驗證您的檔案類型，請遵循下列步驟。</span><span class="sxs-lookup"><span data-stu-id="3ea53-107">To verify your file type using the File Type Verifier, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="3ea53-108">指示</span><span class="sxs-lookup"><span data-stu-id="3ea53-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="3ea53-109">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="3ea53-109">Step 1:</span></span>

<span data-ttu-id="3ea53-110">在您的測試環境上安裝應用程式，並將檔案類型驗證器複製到該環境。</span><span class="sxs-lookup"><span data-stu-id="3ea53-110">Install the application on your test environment, and copy the File Type Verifier to that environment.</span></span> <span data-ttu-id="3ea53-111">檔案類型驗證器可在 [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)中取得。</span><span class="sxs-lookup"><span data-stu-id="3ea53-111">The File Type Verifier is available in the [Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

### <a name="step-2"></a><span data-ttu-id="3ea53-112">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="3ea53-112">Step 2:</span></span>

<span data-ttu-id="3ea53-113">使用您的應用程式建立要測試的檔案。</span><span class="sxs-lookup"><span data-stu-id="3ea53-113">Use your application to create a file to be tested.</span></span>

### <a name="step-3"></a><span data-ttu-id="3ea53-114">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="3ea53-114">Step 3:</span></span>

<span data-ttu-id="3ea53-115">開機檔案類型驗證器。</span><span class="sxs-lookup"><span data-stu-id="3ea53-115">Start the File Type Verifier.</span></span>

### <a name="step-4"></a><span data-ttu-id="3ea53-116">步驟 4：</span><span class="sxs-lookup"><span data-stu-id="3ea53-116">Step 4:</span></span>

<span data-ttu-id="3ea53-117">選取檔案類型的類別，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="3ea53-117">Select the category for your file type, as shown in the following screen shot.</span></span>

![顯示拖放功能的螢幕擷取畫面。](images/file-assoc/filetypeverifier1.png)

<span data-ttu-id="3ea53-119">類別選取專案會決定要由工具執行的一組測試。</span><span class="sxs-lookup"><span data-stu-id="3ea53-119">The category selection determines the set of tests that will be run by the tool.</span></span> <span data-ttu-id="3ea53-120">如果您的型別可能落在多個類別之下 (例如，.TIF 檔案可能是圖片或檔，視內容而定) ，請使用每個適當的類別再次執行工具。</span><span class="sxs-lookup"><span data-stu-id="3ea53-120">If your type could fall under more than one category (for example, a TIF file might be a Picture or a Document depending on the content), run the tool again with each appropriate category.</span></span>

### <a name="step-5"></a><span data-ttu-id="3ea53-121">步驟 5：</span><span class="sxs-lookup"><span data-stu-id="3ea53-121">Step 5:</span></span>

<span data-ttu-id="3ea53-122">使用 Windows 檔案總管，找出要測試的檔案，並使用滑鼠將它拖曳至檔案類型驗證器中的目標，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="3ea53-122">Using Windows Explorer, locate a file to be tested and use the mouse to drag it to the target in File Type Verifier, as shown in the following screen shot.</span></span>

![顯示拖放功能的螢幕擷取畫面](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a><span data-ttu-id="3ea53-124">步驟 6：</span><span class="sxs-lookup"><span data-stu-id="3ea53-124">Step 6:</span></span>

<span data-ttu-id="3ea53-125">等候檔案類型驗證器工具繼續進行一系列的測試。</span><span class="sxs-lookup"><span data-stu-id="3ea53-125">Wait for the File Type Verifier tool to proceed through a series of tests.</span></span> <span data-ttu-id="3ea53-126">進度列會顯示測試的進度，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="3ea53-126">The progress of the testing is shown by the progress bar, as in the following screen shot.</span></span>

![顯示進度列的螢幕擷取畫面](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a><span data-ttu-id="3ea53-128">步驟 7：</span><span class="sxs-lookup"><span data-stu-id="3ea53-128">Step 7:</span></span>

<span data-ttu-id="3ea53-129">檢查檔案類型測試的結果摘要，如下列螢幕擷取畫面所示。</span><span class="sxs-lookup"><span data-stu-id="3ea53-129">Review the results summary of your Document file type tests, as shown in the following screen shot.</span></span>

![顯示結果摘要的螢幕擷取畫面](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a><span data-ttu-id="3ea53-131">步驟 8：</span><span class="sxs-lookup"><span data-stu-id="3ea53-131">Step 8:</span></span>

<span data-ttu-id="3ea53-132">按一下 [摘要] 頁面上的任何結果，以查看詳細記錄。</span><span class="sxs-lookup"><span data-stu-id="3ea53-132">Click any of the results on the summary page to view the detailed log.</span></span> <span data-ttu-id="3ea53-133">預覽處理常式的範例記錄檔會顯示在下列螢幕擷取畫面中。</span><span class="sxs-lookup"><span data-stu-id="3ea53-133">An example log for a preview handler is shown in the following screen shot.</span></span>

![顯示預覽處理常式記錄檔的螢幕擷取畫面](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a><span data-ttu-id="3ea53-135">步驟 9：</span><span class="sxs-lookup"><span data-stu-id="3ea53-135">Step 9:</span></span>

<span data-ttu-id="3ea53-136">若要儲存記錄檔的複本，請按一下記錄檔顯示底部的 [ **儲存記錄** 檔]，然後選擇適當的位置以將它儲存在您的電腦上。</span><span class="sxs-lookup"><span data-stu-id="3ea53-136">To save a copy of the log file, click **Save Log File** at the bottom of the log display and choose an appropriate location for storing it on your computer.</span></span>

### <a name="step-10"></a><span data-ttu-id="3ea53-137">步驟 10：</span><span class="sxs-lookup"><span data-stu-id="3ea53-137">Step 10:</span></span>

<span data-ttu-id="3ea53-138">如果回報失敗，請在您的應用程式中進行適當的變更，然後再次執行工具，以確認測試中不再顯示失敗。</span><span class="sxs-lookup"><span data-stu-id="3ea53-138">If failures are reported, make the appropriate changes in your application and run the tool again to verify that the failures are no longer showing up in the tests.</span></span> <span data-ttu-id="3ea53-139">如果回報警告，請評估這些警告，並決定它們是否與您的特定檔案類型相關，並視需要對您的應用程式進行適當的變更。</span><span class="sxs-lookup"><span data-stu-id="3ea53-139">If warnings are reported, evaluate them and decide whether they are relevant for your particular file type and make the appropriate changes to your application as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ea53-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ea53-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ea53-141">Windows 7 SDK</span><span class="sxs-lookup"><span data-stu-id="3ea53-141">Windows 7 SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



