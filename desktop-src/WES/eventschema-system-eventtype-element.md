---
title: 系統 (的) 元素
description: 包含識別提供者及其啟用方式、事件、寫入事件之通道的資訊，以及處理常式和執行緒識別碼之類的系統資訊。
ms.assetid: c532cfa3-b722-4227-a403-5c050d62a92c
keywords:
- 系統元素 EventLog
topic_type:
- apiref
api_name:
- System
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fef0f9f9e24a855564a8d3df2f94610ff9a8248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967518"
---
# <a name="system-eventtype-element"></a><span data-ttu-id="9e0ef-104">系統 (的) 元素</span><span class="sxs-lookup"><span data-stu-id="9e0ef-104">System (EventType) Element</span></span>

<span data-ttu-id="9e0ef-105">包含識別提供者及其啟用方式、事件、寫入事件之通道的資訊，以及處理常式和執行緒識別碼之類的系統資訊。</span><span class="sxs-lookup"><span data-stu-id="9e0ef-105">Contains information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span>

``` syntax
<xs:element name="System"
    type="SystemPropertiesType"
 />
```

<span data-ttu-id="9e0ef-106">**系統** 專案是由「[**事件**](eventschema-eventtype-complextype.md)類型」複雜類型所定義。</span><span class="sxs-lookup"><span data-stu-id="9e0ef-106">The **System** element is defined by the [**EventType**](eventschema-eventtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e0ef-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e0ef-107">Requirements</span></span>



| <span data-ttu-id="9e0ef-108">需求</span><span class="sxs-lookup"><span data-stu-id="9e0ef-108">Requirement</span></span> | <span data-ttu-id="9e0ef-109">值</span><span class="sxs-lookup"><span data-stu-id="9e0ef-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9e0ef-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e0ef-110">Minimum supported client</span></span><br/> | <span data-ttu-id="9e0ef-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e0ef-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9e0ef-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e0ef-112">Minimum supported server</span></span><br/> | <span data-ttu-id="9e0ef-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e0ef-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e0ef-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9e0ef-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e0ef-115">**父元素**</span><span class="sxs-lookup"><span data-stu-id="9e0ef-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="9e0ef-116">**Event - 事件**</span><span class="sxs-lookup"><span data-stu-id="9e0ef-116">**Event**</span></span>](eventschema-event-element.md)
</dt> </dl>

 

 





