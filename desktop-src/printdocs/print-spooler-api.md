---
description: 「列印多工緩衝處理器」 API 提供了一個介面，讓應用程式的「列印多工緩衝處理器」管理印表機和列印工作。
ms.assetid: b6cc0c9d-9f28-4e80-b847-39c72d98bed6
title: 列印多工緩衝處理器 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7287b9da3ac19d2ab9c39152d5917960e465e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027120"
---
# <a name="print-spooler-api"></a><span data-ttu-id="2d49b-103">列印多工緩衝處理器 API</span><span class="sxs-lookup"><span data-stu-id="2d49b-103">Print Spooler API</span></span>

<span data-ttu-id="2d49b-104">「列印多工緩衝處理器」 API 提供了一個介面，讓應用程式的「列印多工緩衝處理器」管理印表機和列印工作。</span><span class="sxs-lookup"><span data-stu-id="2d49b-104">The Print Spooler API provides an interface to the print spooler for applications to manage printers and print jobs.</span></span>

<span data-ttu-id="2d49b-105">應用程式會使用「列印多工緩衝處理器」 API 作為其程式設計的一部分，而不是直接由使用者使用。</span><span class="sxs-lookup"><span data-stu-id="2d49b-105">The Print Spooler API is used by an application as part of its programming and not directly by end users.</span></span>

<span data-ttu-id="2d49b-106">本節包含下列主題的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2d49b-106">This section contains information about the following topics.</span></span>



| <span data-ttu-id="2d49b-107">主題</span><span class="sxs-lookup"><span data-stu-id="2d49b-107">Topic</span></span>                                                                                             | <span data-ttu-id="2d49b-108">描述</span><span class="sxs-lookup"><span data-stu-id="2d49b-108">Description</span></span>                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d49b-109">列印多工緩衝處理器 API 參考</span><span class="sxs-lookup"><span data-stu-id="2d49b-109">Print Spooler API Reference</span></span>](printing-and-print-spooler-reference.md)<br/>                | <span data-ttu-id="2d49b-110">有關「列印多工緩衝處理器 API」的函式、結構和其他元素的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="2d49b-110">Detailed information about the functions, structures, and other elements of the Print Spooler API.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="2d49b-111">非同步列印通知參考</span><span class="sxs-lookup"><span data-stu-id="2d49b-111">Asynchronous Printing Notification Reference</span></span>](asynchronous-printing-notification.md)<br/> | <span data-ttu-id="2d49b-112">描述應用程式和列印多工緩衝處理器裝載的元件（如印表機驅動程式和埠監視器）之間的非同步通訊所使用的函式、介面和列舉。</span><span class="sxs-lookup"><span data-stu-id="2d49b-112">Descriptions of the functions, interfaces, and enumerations that are used in asynchronous communication between applications and print-spooler-hosted components, such as printer drivers and port monitors.</span></span><br/> |
| [<span data-ttu-id="2d49b-113">印表機驅動程式安裝參考</span><span class="sxs-lookup"><span data-stu-id="2d49b-113">Printer Driver Installation Reference</span></span>](printer-driver-installation-reference.md)<br/>     | <span data-ttu-id="2d49b-114">描述在電腦上安裝和設定印表機驅動程式的功能。</span><span class="sxs-lookup"><span data-stu-id="2d49b-114">Describes the functions that install and configure printer drivers on a computer.</span></span><br/>                                                                                                                            |



 

<span data-ttu-id="2d49b-115">下圖顯示「列印多工緩衝處理器」 API 與原生 Windows 應用程式可以使用的其他列印 Api 的關聯性。</span><span class="sxs-lookup"><span data-stu-id="2d49b-115">The following diagram shows the relationship of the Print Spooler API to the other Print APIs that a native Windows application can use.</span></span>

![此圖表顯示列印多工緩衝處理器 api 與原生 windows 應用程式可以使用的其他列印 api 的關聯性](images/print-apis-ps.png)

## <a name="related-topics"></a><span data-ttu-id="2d49b-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="2d49b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d49b-118">XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="2d49b-118">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="2d49b-119">列印票證 API</span><span class="sxs-lookup"><span data-stu-id="2d49b-119">Print Ticket API</span></span>](print-ticket-api.md)
</dt> <dt>

[<span data-ttu-id="2d49b-120">GDI 列印 API</span><span class="sxs-lookup"><span data-stu-id="2d49b-120">GDI Print API</span></span>](gdi-printing.md)
</dt> </dl>

 

 




