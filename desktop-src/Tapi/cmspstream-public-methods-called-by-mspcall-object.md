---
description: 下列清單包含 MSPCall 物件所呼叫的 CMSPStream 方法。
ms.assetid: 7a59ca78-b5e8-45e9-8fdb-89402ffef916
title: MSPCall 物件呼叫的 CMSPStream 方法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89744f9e4cf2739fa11f07edc4be7e331beb620a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987616"
---
# <a name="cmspstream-public-methods-called-by-mspcall-object"></a><span data-ttu-id="a7589-103">CMSPStream 由 MSPCall 物件呼叫的公用方法</span><span class="sxs-lookup"><span data-stu-id="a7589-103">CMSPStream Public Methods Called by MSPCall Object</span></span>



| <span data-ttu-id="a7589-104">CMSPStream 公用方法</span><span class="sxs-lookup"><span data-stu-id="a7589-104">CMSPStream public methods</span></span>                                 | <span data-ttu-id="a7589-105">Description</span><span class="sxs-lookup"><span data-stu-id="a7589-105">Description</span></span>                                                                             |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="a7589-106">**Init**</span><span class="sxs-lookup"><span data-stu-id="a7589-106">**Init**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-init)                           | <span data-ttu-id="a7589-107">建立資料流程時由 **MSPCall** 呼叫。</span><span class="sxs-lookup"><span data-stu-id="a7589-107">Called by the **MSPCall** when the stream is created.</span></span>                                   |
| [<span data-ttu-id="a7589-108">**關閉**</span><span class="sxs-lookup"><span data-stu-id="a7589-108">**ShutDown**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-shutdown)                   | <span data-ttu-id="a7589-109">由 **MSPCall** 呼叫以取消選取所有的終端物件，並釋放呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="a7589-109">Called by the **MSPCall** to unselect all terminal objects and release the call object.</span></span> |
| [<span data-ttu-id="a7589-110">**GetState**</span><span class="sxs-lookup"><span data-stu-id="a7589-110">**GetState**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-getstate)                   | <span data-ttu-id="a7589-111">由 MSPCall 物件呼叫，以取得資料流程的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="a7589-111">Called by the MSPCall object to get the current status of the stream.</span></span>                   |
| [<span data-ttu-id="a7589-112">**HandleTSPData**</span><span class="sxs-lookup"><span data-stu-id="a7589-112">**HandleTSPData**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-handletspdata)         | <span data-ttu-id="a7589-113">衍生的呼叫物件可以呼叫這個方法，讓資料流程處理 TSP 命令。</span><span class="sxs-lookup"><span data-stu-id="a7589-113">Derived call object may call this method to let the stream handle the TSP commands.</span></span>     |
| [<span data-ttu-id="a7589-114">**ProcessGraphEvent**</span><span class="sxs-lookup"><span data-stu-id="a7589-114">**ProcessGraphEvent**</span></span>](/windows/desktop/api/Mspstrm/nf-mspstrm-cmspstream-processgraphevent) | <span data-ttu-id="a7589-115">由 MSPCall 物件呼叫，讓資料流程處理圖形事件。</span><span class="sxs-lookup"><span data-stu-id="a7589-115">Called by the MSPCall object to let the stream handle graph events.</span></span>                     |



 

 

 



