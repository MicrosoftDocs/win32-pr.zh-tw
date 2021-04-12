---
description: GDI 列印 API 會提供應用程式與裝置無關的列印介面。
ms.assetid: 3115c9e0-05c9-462d-8238-fc035ea32d4e
title: GDI 列印 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0239282543a68c6fe8b5d6503d085582fd9c20db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192718"
---
# <a name="gdi-print-api"></a><span data-ttu-id="b7067-103">GDI 列印 API</span><span class="sxs-lookup"><span data-stu-id="b7067-103">GDI Print API</span></span>

<span data-ttu-id="b7067-104">GDI 列印 API 會提供應用程式與裝置無關的列印介面。</span><span class="sxs-lookup"><span data-stu-id="b7067-104">The GDI Print API provides applications with a device-independent printing interface.</span></span> <span data-ttu-id="b7067-105">如果應用程式使用 GDI 來呈現文字和圖形，請使用此介面。</span><span class="sxs-lookup"><span data-stu-id="b7067-105">Use this interface if the application uses GDI to render text and graphics.</span></span>

<span data-ttu-id="b7067-106">如果您撰寫適用于 Windows Vista 或更新版本 Windows 的應用程式，請考慮使用「 [Xps 檔 api](/previous-versions/windows/desktop/dd316976(v=vs.85)) 」和「 [xps 列印 api](xps-printing.md) 」來使用 XPSDrv 列印驅動程式所支援的較高效能圖形介面。</span><span class="sxs-lookup"><span data-stu-id="b7067-106">If you write applications for Windows Vista or later versions of Windows, consider using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)) and the [XPS Print API](xps-printing.md) to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span>

<span data-ttu-id="b7067-107">本節提供下列主題的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b7067-107">This section provides information about the following topics.</span></span>



| <span data-ttu-id="b7067-108">主題</span><span class="sxs-lookup"><span data-stu-id="b7067-108">Topic</span></span>                                                                                             | <span data-ttu-id="b7067-109">描述</span><span class="sxs-lookup"><span data-stu-id="b7067-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7067-110">關於 GDI 列印 API</span><span class="sxs-lookup"><span data-stu-id="b7067-110">About the GDI Print API</span></span>](about-the-gdi-print-api.md)<br/>                                 | <span data-ttu-id="b7067-111">GDI 列印功能的總覽。</span><span class="sxs-lookup"><span data-stu-id="b7067-111">An overview of the GDI printing functionality.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="b7067-112">使用 GDI 列印 API</span><span class="sxs-lookup"><span data-stu-id="b7067-112">Using the GDI Print API</span></span>](using-the-printing-functions.md)<br/>                            | <span data-ttu-id="b7067-113">在應用程式中使用 GDI 列印 API 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b7067-113">Information about using the GDI Print API in an application.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="b7067-114">GDI 列印 API 參考</span><span class="sxs-lookup"><span data-stu-id="b7067-114">GDI Print API Reference</span></span>](gdi-print-api-reference.md)<br/>                                 | <span data-ttu-id="b7067-115">GDI 列印 API 的函式、結構和其他元素的詳細說明。</span><span class="sxs-lookup"><span data-stu-id="b7067-115">Detailed descriptions of the functions, structures, and other elements of the GDI Print API.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="b7067-116">Microsoft XPS 檔轉換器 (MXDC) </span><span class="sxs-lookup"><span data-stu-id="b7067-116">Microsoft XPS Document Converter (MXDC)</span></span>](microsoft-xps-document-converter--mxdc-.md)<br/> | <span data-ttu-id="b7067-117">[MICROSOFT XPS 檔轉換器 (MXDC) ](microsoft-xps-document-converter--mxdc-.md)是一種元件，可讓應用程式搭配具有 XPSDrv 列印驅動程式的印表機使用 GDI 列印 API。</span><span class="sxs-lookup"><span data-stu-id="b7067-117">The [Microsoft XPS Document Converter (MXDC)](microsoft-xps-document-converter--mxdc-.md) is a component that enables applications to use the GDI Print API with printers that have an XPSDrv Print Driver.</span></span><br/>                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="b7067-118">Microsoft XPS Document Writer (MXDW) </span><span class="sxs-lookup"><span data-stu-id="b7067-118">Microsoft XPS Document Writer (MXDW)</span></span>](microsoft-xps-document-writer.md)<br/>              | <span data-ttu-id="b7067-119">[MICROSOFT XPS Document Writer (MXDW) ](microsoft-xps-document-writer.md)提供具有「儲存為 xps」或「匯出至 xps」功能的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b7067-119">The [Microsoft XPS Document Writer (MXDW)](microsoft-xps-document-writer.md) provides applications with "save as XPS" or "export to XPS" functionality.</span></span> <span data-ttu-id="b7067-120">未以原生方式建立 XPS 檔內容的應用程式可以使用 MXDW 建立 XPS 檔檔，而不需要使用 [xps 檔 API](/previous-versions/windows/desktop/dd316976(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="b7067-120">Applications that do not natively create XPS document content can use the MXDW to create XPS document files without using the [XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85)).</span></span> <span data-ttu-id="b7067-121">不過，XPS 檔 API 提供的應用程式能夠使用 XPSDrv 列印驅動程式所支援的較高效能圖形介面。</span><span class="sxs-lookup"><span data-stu-id="b7067-121">The XPS Document API, however, provides an application with the ability to use the higher-performance graphics interfaces that are supported by XPSDrv print drivers.</span></span><br/> |



 

<span data-ttu-id="b7067-122">下圖顯示 GDI 列印 API 與應用程式可使用的其他列印 Api 的關聯性。</span><span class="sxs-lookup"><span data-stu-id="b7067-122">The following diagram shows the relationship of the GDI Print API to the other print APIs that an application can use.</span></span>

![顯示 gdi 列印 api 與 win32 應用程式可使用的其他列印 api 關聯性的圖表](images/print-apis-gdi.png)

## <a name="related-topics"></a><span data-ttu-id="b7067-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7067-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7067-125">**System.printing.printqueue.addjob**</span><span class="sxs-lookup"><span data-stu-id="b7067-125">**AddJob**</span></span>](addjob.md)
</dt> <dt>

<span data-ttu-id="b7067-126">[XPS 檔 API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7067-126">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b7067-127">XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="b7067-127">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="b7067-128">列印多工緩衝處理器 API</span><span class="sxs-lookup"><span data-stu-id="b7067-128">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="b7067-129">列印票證 API</span><span class="sxs-lookup"><span data-stu-id="b7067-129">Print Ticket API</span></span>](print-ticket-api.md)
</dt> </dl>

 

