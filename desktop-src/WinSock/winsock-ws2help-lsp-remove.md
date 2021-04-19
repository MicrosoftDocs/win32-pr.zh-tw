---
description: 多層式服務提供者的 Winsock 目錄變更事件 (LSP) 移除作業。
ms.assetid: 86FF17F7-8CCF-4A03-899F-42BFACDF3F54
title: WINSOCK_WS2HELP_LSP_REMOVE 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_REMOVE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 597cd2f8cfc3bb7727301e64af53671bafbd9469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983804"
---
# <a name="winsock_ws2help_lsp_remove-event"></a><span data-ttu-id="1ca91-103">WINSOCK \_ WS2HELP \_ LSP \_ 移除事件</span><span class="sxs-lookup"><span data-stu-id="1ca91-103">WINSOCK\_WS2HELP\_LSP\_REMOVE event</span></span>

> [!Note]  
> <span data-ttu-id="1ca91-104">已淘汰分層服務提供者。</span><span class="sxs-lookup"><span data-stu-id="1ca91-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="1ca91-105">從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="1ca91-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="1ca91-106">**Winsock \_ WS2HELP \_ lsp \_ REMOVE** 事件是多層式服務提供者的 winsock 目錄變更事件， (LSP) 移除作業。</span><span class="sxs-lookup"><span data-stu-id="1ca91-106">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is a Winsock catalog change event for a layered service provider (LSP) removal operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_REMOVE = {0x2, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="1ca91-107">參數</span><span class="sxs-lookup"><span data-stu-id="1ca91-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ca91-108">*LSP 名稱*</span><span class="sxs-lookup"><span data-stu-id="1ca91-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="1ca91-109">從要移除的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **SZPROTOCOL** 成員取得的 LSP 名稱。</span><span class="sxs-lookup"><span data-stu-id="1ca91-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> <dt>

<span data-ttu-id="1ca91-110">*目錄*</span><span class="sxs-lookup"><span data-stu-id="1ca91-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="1ca91-111">Winsock 目錄 (32 位或64位) ，其中 LSP 正在移除。</span><span class="sxs-lookup"><span data-stu-id="1ca91-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being removed.</span></span> <span data-ttu-id="1ca91-112">這是一個整數值，也就是32或64。</span><span class="sxs-lookup"><span data-stu-id="1ca91-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="1ca91-113">*安裝程式*</span><span class="sxs-lookup"><span data-stu-id="1ca91-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="1ca91-114">讓 LSP 移除呼叫的應用程式模組檔案名。</span><span class="sxs-lookup"><span data-stu-id="1ca91-114">The module filename of the application making the LSP remove call.</span></span>

</dd> <dt>

<span data-ttu-id="1ca91-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="1ca91-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="1ca91-116">要從中移除 LSP 之 Winsock 傳輸提供者的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="1ca91-116">The GUID value of the Winsock transport provider that the LSP is being removed from.</span></span>

</dd> <dt>

<span data-ttu-id="1ca91-117">*類別*</span><span class="sxs-lookup"><span data-stu-id="1ca91-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="1ca91-118">要移除的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **dwCatalogEntryId** 成員。</span><span class="sxs-lookup"><span data-stu-id="1ca91-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being removed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ca91-119">備註</span><span class="sxs-lookup"><span data-stu-id="1ca91-119">Remarks</span></span>

<span data-ttu-id="1ca91-120">從 Winsock 類別目錄移除通訊協定專案時，系統會針對 LSP 移除作業追蹤 **winsock \_ WS2HELP \_ lsp \_ 移除** 事件。</span><span class="sxs-lookup"><span data-stu-id="1ca91-120">The **WINSOCK\_WS2HELP\_LSP\_REMOVE** event is traced for an LSP removal operation when a protocol entry is removed from the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ca91-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ca91-121">Requirements</span></span>



| <span data-ttu-id="1ca91-122">需求</span><span class="sxs-lookup"><span data-stu-id="1ca91-122">Requirement</span></span> | <span data-ttu-id="1ca91-123">值</span><span class="sxs-lookup"><span data-stu-id="1ca91-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1ca91-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ca91-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1ca91-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ca91-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1ca91-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ca91-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1ca91-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ca91-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ca91-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ca91-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ca91-129">Winsock 追蹤的控制權</span><span class="sxs-lookup"><span data-stu-id="1ca91-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="1ca91-130">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="1ca91-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="1ca91-131">Winsock 追蹤層級</span><span class="sxs-lookup"><span data-stu-id="1ca91-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="1ca91-132">Winsock 目錄變更追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="1ca91-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
