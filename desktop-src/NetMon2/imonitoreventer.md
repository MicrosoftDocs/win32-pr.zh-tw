---
description: IMonitorEventer 介面提供提交事件以及配置和釋放監視資源的方法。
ms.assetid: d59a8b42-cce3-410b-a62e-97d66d058d90
title: 'IMonitorEventer 介面 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitorEventer
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 7d4ca58b5a0787638eee54b7733b4e1a8fbf7ffe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847937"
---
# <a name="imonitoreventer-interface"></a><span data-ttu-id="12d76-103">IMonitorEventer 介面</span><span class="sxs-lookup"><span data-stu-id="12d76-103">IMonitorEventer interface</span></span>

<span data-ttu-id="12d76-104">**IMonitorEventer** 介面提供提交事件以及配置和釋放監視資源的方法。</span><span class="sxs-lookup"><span data-stu-id="12d76-104">The **IMonitorEventer** interface provides methods for submitting events and allocating and freeing monitor resources.</span></span>

## <a name="members"></a><span data-ttu-id="12d76-105">成員</span><span class="sxs-lookup"><span data-stu-id="12d76-105">Members</span></span>

<span data-ttu-id="12d76-106">**IMonitorEventer** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="12d76-106">The **IMonitorEventer** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="12d76-107">**IMonitorEventer** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="12d76-107">**IMonitorEventer** also has these types of members:</span></span>

-   [<span data-ttu-id="12d76-108">方法</span><span class="sxs-lookup"><span data-stu-id="12d76-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="12d76-109">方法</span><span class="sxs-lookup"><span data-stu-id="12d76-109">Methods</span></span>

<span data-ttu-id="12d76-110">**IMonitorEventer** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="12d76-110">The **IMonitorEventer** interface has these methods.</span></span>



| <span data-ttu-id="12d76-111">方法</span><span class="sxs-lookup"><span data-stu-id="12d76-111">Method</span></span>                                                 | <span data-ttu-id="12d76-112">描述</span><span class="sxs-lookup"><span data-stu-id="12d76-112">Description</span></span>                                        |
|:-------------------------------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="12d76-113">**FreeEventData**</span><span class="sxs-lookup"><span data-stu-id="12d76-113">**FreeEventData**</span></span>](imonitoreventer-freeeventdata.md) | <span data-ttu-id="12d76-114">釋出配置給監視資料的空間。</span><span class="sxs-lookup"><span data-stu-id="12d76-114">Frees space allocated for monitor data.</span></span><br/> |
| [<span data-ttu-id="12d76-115">**GetEventData**</span><span class="sxs-lookup"><span data-stu-id="12d76-115">**GetEventData**</span></span>](imonitoreventer-geteventdata.md)   | <span data-ttu-id="12d76-116">配置監視器資料的空間。</span><span class="sxs-lookup"><span data-stu-id="12d76-116">Allocates space for monitor data.</span></span><br/>       |
| [<span data-ttu-id="12d76-117">**SendNMEvent**</span><span class="sxs-lookup"><span data-stu-id="12d76-117">**SendNMEvent**</span></span>](imonitoreventer-sendnmevent.md)     | <span data-ttu-id="12d76-118">將事件提交至 WMI。</span><span class="sxs-lookup"><span data-stu-id="12d76-118">Submits events to WMI.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="12d76-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="12d76-119">Requirements</span></span>



| <span data-ttu-id="12d76-120">需求</span><span class="sxs-lookup"><span data-stu-id="12d76-120">Requirement</span></span> | <span data-ttu-id="12d76-121">值</span><span class="sxs-lookup"><span data-stu-id="12d76-121">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="12d76-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="12d76-122">Minimum supported client</span></span><br/> | <span data-ttu-id="12d76-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12d76-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="12d76-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="12d76-124">Minimum supported server</span></span><br/> | <span data-ttu-id="12d76-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="12d76-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="12d76-126">標頭</span><span class="sxs-lookup"><span data-stu-id="12d76-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="12d76-127"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="12d76-127"><dt>Netmon.h</dt></span></span> </dl> |



 

