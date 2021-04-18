---
description: 提供列印多工緩衝處理器的介面。 應用程式可以使用此 API 將 XPS 檔傳送至印表機。
ms.assetid: df06ddcb-e573-461c-99a3-8f108fe2c143
title: XPS 列印 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30c53322a8ae6a03c3ac4bb71fc680f719999546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983417"
---
# <a name="xps-print-api"></a><span data-ttu-id="fd7fa-104">XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="fd7fa-104">XPS Print API</span></span>

<span data-ttu-id="fd7fa-105">\[XPS 列印 API 不受支援，未來可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-105">\[The XPS Print API is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="fd7fa-106">用戶端應用程式應該改用 [列印檔案套件 API](./tailored-app-printing-api.md) 。\]</span><span class="sxs-lookup"><span data-stu-id="fd7fa-106">Client applications should use the [Print Document Package API](./tailored-app-printing-api.md) instead.\]</span></span>

<span data-ttu-id="fd7fa-107">提供列印多工緩衝處理器的介面。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-107">Provides an interface to the print spooler.</span></span> <span data-ttu-id="fd7fa-108">應用程式可以使用此 API 將 XPS 檔傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-108">Applications can use this API to send XPS documents to a printer.</span></span>

<span data-ttu-id="fd7fa-109">本節包含下列主題的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-109">This section contains information about the following topics.</span></span>

<dl>

[<span data-ttu-id="fd7fa-110">關於 XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="fd7fa-110">About the XPS Print API</span></span>](about-xps-print-api.md)  
[<span data-ttu-id="fd7fa-111">使用 XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="fd7fa-111">Using the XPS Print API</span></span>](using-the-xps-print-api.md)  
[<span data-ttu-id="fd7fa-112">XPS 列印 API 參考</span><span class="sxs-lookup"><span data-stu-id="fd7fa-112">XPS Print API Reference</span></span>](xpsprint-interfaces.md)  
</dl>

<span data-ttu-id="fd7fa-113">使用 xps [檔 api](/previous-versions/windows/desktop/dd316976(v=vs.85))來建立 xps 檔的原生 Windows 應用程式，可使用 XPS 列印 API 將 xps 檔內容傳送至印表機。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-113">Native Windows applications that create XPS documents, such as by using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)), can use the XPS Print API to send XPS document content to a printer.</span></span>

<span data-ttu-id="fd7fa-114">下圖顯示 XPS 列印 API 與原生 Windows 應用程式可以使用的其他列印 Api 的關聯性。</span><span class="sxs-lookup"><span data-stu-id="fd7fa-114">The following diagram shows the relationship of the XPS Print API to the other Print APIs that a native Windows application can use.</span></span>

![此圖顯示 xps 列印 api 與原生 windows 應用程式可使用的其他列印 api 之間的關聯性](images/print-apis-xps.png)

## <a name="related-topics"></a><span data-ttu-id="fd7fa-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="fd7fa-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd7fa-117">**System.printing.printqueue.addjob**</span><span class="sxs-lookup"><span data-stu-id="fd7fa-117">**AddJob**</span></span>](addjob.md)
</dt> <dt>

[<span data-ttu-id="fd7fa-118">列印多工緩衝處理器 API</span><span class="sxs-lookup"><span data-stu-id="fd7fa-118">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="fd7fa-119">列印票證 API</span><span class="sxs-lookup"><span data-stu-id="fd7fa-119">Print Ticket API</span></span>](print-ticket-api.md)
</dt> <dt>

[<span data-ttu-id="fd7fa-120">GDI 列印 API</span><span class="sxs-lookup"><span data-stu-id="fd7fa-120">GDI Print API</span></span>](gdi-printing.md)
</dt> </dl>

 

 
