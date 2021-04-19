---
title: 啟用記錄
description: 啟用記錄
ms.assetid: 50fc1d71-b650-4ba5-a6e1-631c0b9fe8ad
keywords:
- Windows Media 裝置管理員，記錄
- 裝置管理員，記錄
- 桌面應用程式，記錄
- 服務提供者，記錄
- 程式設計指南，記錄
- logging
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e95be13e93a5a58bb728d5600c6fdea9801ec2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966792"
---
# <a name="enabling-logging"></a><span data-ttu-id="cb5bc-109">啟用記錄</span><span class="sxs-lookup"><span data-stu-id="cb5bc-109">Enabling Logging</span></span>

<span data-ttu-id="cb5bc-110">Windows Media 裝置管理員提供可在執行時間將資訊儲存至文字檔的記錄物件。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-110">Windows Media Device Manager provides a logging object that can save information to a text file at run time.</span></span> <span data-ttu-id="cb5bc-111">應用程式和服務提供者的開發人員可以使用此物件，在其應用程式或服務提供者執行時，將訊息儲存在記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-111">Developers of both applications and service providers can use this object to store messages in a log file while their application or service provider is running.</span></span> <span data-ttu-id="cb5bc-112">此物件在處理受 DRM 保護的檔案時特別有用，因為 Windows Media 裝置管理員將不允許您將偵錯工具附加至處理受 DRM 保護之檔案的處理常式。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-112">This object is especially useful when handling DRM-protected files, because Windows Media Device Manager will not allow you to attach a debugger to a process that is handling DRM-protected files.</span></span>

<span data-ttu-id="cb5bc-113">記錄器是具有類別識別碼 CLSID \_ WMDMLogger 的 COM 物件，此物件會公開一個介面 [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-113">The logger is a COM object with the class ID CLSID\_WMDMLogger that exposes one interface, [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span> <span data-ttu-id="cb5bc-114">元件不需要憑證就能使用記錄物件。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-114">Components do not need a certificate to use the logging object.</span></span>

<span data-ttu-id="cb5bc-115">根據預設，不論應用程式是否使用 **IWMDMLogger**，Windows Media 裝置管理員都會維護記錄檔。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-115">By default, Windows Media Device Manager maintains a log file, regardless of whether an application uses **IWMDMLogger**.</span></span> <span data-ttu-id="cb5bc-116">此記錄檔是簡單的文字檔，且每個專案都包含一個專案，其前面會加上以 YYYYMMDDHHMMSS.FFFFFF 格式的時間戳記，並使用24小時的當地時間。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-116">This log file is a simple text file, and each entry includes an entry preceded by a time stamp in the format YYYYMMDDHHMMSS, using 24-hour local time.</span></span> <span data-ttu-id="cb5bc-117">Windows Media 裝置管理員會記錄所有 API 呼叫，以及您藉由呼叫 **IWMDMLogger** 訊息加入的任何專案。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-117">Windows Media Device Manager logs all API calls, along with any entries you add by calling **IWMDMLogger** messages.</span></span> <span data-ttu-id="cb5bc-118">在呼叫 [**Reset**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) 之前，所有記錄檔專案都會附加至檔案，或檔案超過其大小上限。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-118">All log file entries are appended to the file until [**Reset**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-reset) is called, or the file exceeds its maximum size.</span></span> <span data-ttu-id="cb5bc-119">檔案會在每次記錄作業之後自動關閉。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-119">The file is closed automatically after each logging operation.</span></span> <span data-ttu-id="cb5bc-120">應用程式專案和系統專案會使用相同的記錄檔。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-120">The same log file is used for application entries and system entries.</span></span>

<span data-ttu-id="cb5bc-121">下列步驟顯示如何使用記錄物件：</span><span class="sxs-lookup"><span data-stu-id="cb5bc-121">The following steps show how to use the logging object:</span></span>

1.  <span data-ttu-id="cb5bc-122">在您的專案中包含 wmdmlog。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-122">Include wmdmlog.h in your project.</span></span>
2.  <span data-ttu-id="cb5bc-123">藉由呼叫 **CoCreateInstance** (CLSID \_ WMDMLogger) 並要求 **IWMDMLogger** 介面，建立記錄物件。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-123">Create a logging object by calling **CoCreateInstance**(CLSID\_WMDMLogger) and requesting the **IWMDMLogger** interface.</span></span> <span data-ttu-id="cb5bc-124">將介面指標指派給全域變數。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-124">Assign the interface pointer to a global variable.</span></span>
3.  <span data-ttu-id="cb5bc-125">藉由呼叫 [**IWMDMLogger：： IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); 驗證記錄是否已啟用。如果不是，請藉由呼叫 [**IWMDMLogger：： enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable)來啟用它。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-125">Verify that logging is enabled by calling [**IWMDMLogger::IsEnabled**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-isenabled); if it is not, enable it by calling [**IWMDMLogger::Enable**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-enable).</span></span>
4.  <span data-ttu-id="cb5bc-126">指定自訂記錄檔的名稱和大小。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-126">Specify a custom log file name and size.</span></span> <span data-ttu-id="cb5bc-127">這是藉由呼叫 [**IWMDMLogger：： SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) 和 [**IWMDMLogger：： SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams)來完成。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-127">This is done by calling [**IWMDMLogger::SetLogFileName**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setlogfilename) and [**IWMDMLogger::SetSizeParams**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-setsizeparams).</span></span>
5.  <span data-ttu-id="cb5bc-128">在您的程式碼中，您想要在記錄檔中建立專案的位置點，呼叫 [**IWMDMLogger：： LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) ，以記錄包含變數的字串 (這個方法類似于 **wsprintf** ，方法是讓您將包含變數值的字串格式化) ，或呼叫 [**IWMDMLogger：： LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) 來記錄常數位符串。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-128">At points in your code where you want to make an entry in the log, call either [**IWMDMLogger::LogDword**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logdword) to log strings containing variables (this method is similar to **wsprintf** in the way it allows you to format a string containing a variable value), or call [**IWMDMLogger::LogString**](/windows/desktop/api/wmdmlog/nf-wmdmlog-iwmdmlogger-logstring) to log constant strings.</span></span>

<span data-ttu-id="cb5bc-129">如需範例程式碼，請參閱 [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger)方法的參考頁面。</span><span class="sxs-lookup"><span data-stu-id="cb5bc-129">For example code, see the reference pages for the methods of [**IWMDMLogger**](/windows/desktop/api/wmdmlog/nn-wmdmlog-iwmdmlogger).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb5bc-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="cb5bc-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb5bc-131">**應用程式和服務提供者的一般工作**</span><span class="sxs-lookup"><span data-stu-id="cb5bc-131">**Tasks Common to Applications and Service Providers**</span></span>](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




