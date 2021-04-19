---
description: Winsock 類別目錄重設作業的 winsock 目錄變更事件。
ms.assetid: BE8DC0DB-0F96-4015-87F5-ECF25AE164AA
title: WINSOCK_WS2HELP_LSP_RESET 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_RESET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 219eb85dec0cdda77ca8741ae42df1f63d1a7dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978282"
---
# <a name="winsock_ws2help_lsp_reset-event"></a><span data-ttu-id="5dea5-103">WINSOCK \_ WS2HELP \_ LSP \_ 重設事件</span><span class="sxs-lookup"><span data-stu-id="5dea5-103">WINSOCK\_WS2HELP\_LSP\_RESET event</span></span>

> [!Note]  
> <span data-ttu-id="5dea5-104">已淘汰分層服務提供者。</span><span class="sxs-lookup"><span data-stu-id="5dea5-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="5dea5-105">從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="5dea5-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="5dea5-106">Winsock **\_ WS2HELP \_ LSP \_ reset** 事件是 winsock 目錄重設作業的 winsock 目錄變更事件。</span><span class="sxs-lookup"><span data-stu-id="5dea5-106">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is a Winsock catalog change event for a Winsock catalog reset operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_RESET = {0x4, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="5dea5-107">參數</span><span class="sxs-lookup"><span data-stu-id="5dea5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5dea5-108">*目錄*</span><span class="sxs-lookup"><span data-stu-id="5dea5-108">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="5dea5-109">要重設的 (32 位或64位) 的 Winsock 目錄。</span><span class="sxs-lookup"><span data-stu-id="5dea5-109">The Winsock catalog (32-bit or 64-bit) that is being reset.</span></span> <span data-ttu-id="5dea5-110">這是一個整數值，也就是32或64。</span><span class="sxs-lookup"><span data-stu-id="5dea5-110">This is an integer value that is either 32 or 64.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5dea5-111">備註</span><span class="sxs-lookup"><span data-stu-id="5dea5-111">Remarks</span></span>

<span data-ttu-id="5dea5-112">在重設 Winsock 類別目錄時，會追蹤 winsock 多層式服務提供者 (LSP) 作業的 **winsock \_ WS2HELP \_ LSP \_ 重設** 事件。</span><span class="sxs-lookup"><span data-stu-id="5dea5-112">The **WINSOCK\_WS2HELP\_LSP\_RESET** event is traced for an Winsock Layered Service Provider (LSP) operation when the Winsock catalog is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="5dea5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5dea5-113">Requirements</span></span>



| <span data-ttu-id="5dea5-114">需求</span><span class="sxs-lookup"><span data-stu-id="5dea5-114">Requirement</span></span> | <span data-ttu-id="5dea5-115">值</span><span class="sxs-lookup"><span data-stu-id="5dea5-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5dea5-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5dea5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5dea5-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dea5-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5dea5-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5dea5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5dea5-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5dea5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5dea5-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5dea5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5dea5-121">Winsock 追蹤的控制權</span><span class="sxs-lookup"><span data-stu-id="5dea5-121">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="5dea5-122">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="5dea5-122">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="5dea5-123">Winsock 追蹤層級</span><span class="sxs-lookup"><span data-stu-id="5dea5-123">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="5dea5-124">Winsock 目錄變更追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="5dea5-124">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
