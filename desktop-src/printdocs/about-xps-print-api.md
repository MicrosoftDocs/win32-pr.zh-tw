---
description: XPS&\# 160;列印&\# 160;API 提供了列印多工緩衝處理器的介面，可讓應用程式用來列印將 XPS 檔傳送至印表機的作業。
ms.assetid: d3bf7b1d-df21-4e7b-803b-45b65d46b2ca
title: 關於 XPS 列印 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b1467458a737a6faaddb5ed45c81623207ccdb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115488"
---
# <a name="about-the-xps-print-api"></a><span data-ttu-id="73a6a-103">關於 XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="73a6a-103">About the XPS Print API</span></span>

<span data-ttu-id="73a6a-104">[XPS 列印 API](xps-printing.md)提供了列印多工緩衝處理器的介面，可讓應用程式用來列印將 XPS 檔傳送至印表機的作業。</span><span class="sxs-lookup"><span data-stu-id="73a6a-104">The [XPS Print API](xps-printing.md) provides an interface to the print spooler that applications can use to print jobs that send XPS documents to a printer.</span></span>

<span data-ttu-id="73a6a-105">如果目的地印表機使用 XPSDrv 印表機驅動程式，則「XPS 列印」 API 可讓 XPSDrv 印表機驅動程式在列印多工緩衝處理器處理列印工作時接收檔事件。</span><span class="sxs-lookup"><span data-stu-id="73a6a-105">If the destination printer uses an XPSDrv printer driver, the XPS Print API makes it possible for the XPSDrv printer driver to receive document events as the print spooler processes a print job.</span></span> <span data-ttu-id="73a6a-106">如需傳送至 XPSDrv 印表機驅動程式的檔事件描述，請參閱 [XPS 驅動程式檔事件](/windows-hardware/drivers/print/xps-driver-document-events)。</span><span class="sxs-lookup"><span data-stu-id="73a6a-106">For a description of the document events that are sent to the XPSDrv printer driver see [XPS Driver Document Events](/windows-hardware/drivers/print/xps-driver-document-events).</span></span>

<span data-ttu-id="73a6a-107">如果目的地印表機使用 GDI 印表機驅動程式，則 [Xps 列印 API](xps-printing.md) 可讓系統處理將列印工作資料從 XPS 格式轉換成增強型中繼檔的必要轉換， (EMF) 格式，也就是 GDI 印表機驅動程式所使用的格式。</span><span class="sxs-lookup"><span data-stu-id="73a6a-107">If the destination printer uses a GDI printer driver, the [XPS Print API](xps-printing.md) lets the system handle the necessary conversion of the print job data from XPS format to the Enhanced Metafile (EMF) format that the GDI printer driver uses.</span></span> <span data-ttu-id="73a6a-108">如需 GDI 印表機驅動程式檔事件的說明，請參閱 [DocumentEvent 函數](documentevent.md)。</span><span class="sxs-lookup"><span data-stu-id="73a6a-108">For a description of the GDI printer driver document events see [DocumentEvent Function](documentevent.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="73a6a-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="73a6a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73a6a-110">使用 XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="73a6a-110">Using the XPS Print API</span></span>](using-the-xps-print-api.md)
</dt> <dt>

[<span data-ttu-id="73a6a-111">XPS 列印 API 參考</span><span class="sxs-lookup"><span data-stu-id="73a6a-111">XPS Print API Reference</span></span>](xpsprint-api.md)
</dt> </dl>

 

 
