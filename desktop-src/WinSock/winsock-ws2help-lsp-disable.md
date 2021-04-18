---
description: 多層式服務提供者的 Winsock 目錄變更事件 (LSP) 停用作業。
ms.assetid: 6BCEECB1-92AD-47D8-952B-D0FD2A78EB45
title: WINSOCK_WS2HELP_LSP_DISABLE 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_DISABLE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6d785bfbd96d35717be7bbf76dab8f28f41c9fc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978283"
---
# <a name="winsock_ws2help_lsp_disable-event"></a><span data-ttu-id="e0c67-103">WINSOCK \_ WS2HELP \_ LSP \_ 停用事件</span><span class="sxs-lookup"><span data-stu-id="e0c67-103">WINSOCK\_WS2HELP\_LSP\_DISABLE event</span></span>

> [!Note]  
> <span data-ttu-id="e0c67-104">已淘汰分層服務提供者。</span><span class="sxs-lookup"><span data-stu-id="e0c67-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="e0c67-105">從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="e0c67-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="e0c67-106">**Winsock \_ WS2HELP \_ lsp \_ 停** 用事件是多層式服務提供者的 winsock 目錄變更事件， (lsp) 停用作業。</span><span class="sxs-lookup"><span data-stu-id="e0c67-106">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is a Winsock catalog change event for a layered service provider (LSP) disable operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_DISABLE = {0x3, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="e0c67-107">參數</span><span class="sxs-lookup"><span data-stu-id="e0c67-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0c67-108">*LSP 名稱*</span><span class="sxs-lookup"><span data-stu-id="e0c67-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c67-109">針對正在停用的 LSP，從 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **SZPROTOCOL** 成員取得的 LSP 名稱。</span><span class="sxs-lookup"><span data-stu-id="e0c67-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="e0c67-110">*目錄*</span><span class="sxs-lookup"><span data-stu-id="e0c67-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c67-111">Winsock 目錄 (32 位或64位) 在 LSP 正在停用的位置。</span><span class="sxs-lookup"><span data-stu-id="e0c67-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being disabled.</span></span> <span data-ttu-id="e0c67-112">這是一個整數值，也就是32或64。</span><span class="sxs-lookup"><span data-stu-id="e0c67-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="e0c67-113">*安裝程式*</span><span class="sxs-lookup"><span data-stu-id="e0c67-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c67-114">讓 LSP 停用呼叫的應用程式模組檔案名。</span><span class="sxs-lookup"><span data-stu-id="e0c67-114">The module filename of the application making the LSP disable call.</span></span>

</dd> <dt>

<span data-ttu-id="e0c67-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="e0c67-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c67-116">要停用 LSP 之 Winsock 傳輸提供者的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="e0c67-116">The GUID value of the Winsock transport provider that the LSP is being disabled.</span></span>

</dd> <dt>

<span data-ttu-id="e0c67-117">*類別*</span><span class="sxs-lookup"><span data-stu-id="e0c67-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="e0c67-118">正在停用的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **dwCatalogEntryId** 成員。</span><span class="sxs-lookup"><span data-stu-id="e0c67-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being disabled.</span></span>

</dd> </dl>

<span data-ttu-id="e0c67-119">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e0c67-119">This event has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0c67-120">備註</span><span class="sxs-lookup"><span data-stu-id="e0c67-120">Remarks</span></span>

<span data-ttu-id="e0c67-121">Winsock **\_ WS2HELP \_ lsp \_ 停** 用事件是在 winsock 類別目錄中停用通訊協定專案時，針對 LSP 停用作業進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="e0c67-121">The **WINSOCK\_WS2HELP\_LSP\_DISABLE** event is traced for an LSP disable operation when a protocol entry is disabled in the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0c67-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0c67-122">Requirements</span></span>



| <span data-ttu-id="e0c67-123">需求</span><span class="sxs-lookup"><span data-stu-id="e0c67-123">Requirement</span></span> | <span data-ttu-id="e0c67-124">值</span><span class="sxs-lookup"><span data-stu-id="e0c67-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e0c67-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0c67-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e0c67-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0c67-126">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e0c67-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0c67-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e0c67-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0c67-128">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e0c67-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0c67-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0c67-130">Winsock 追蹤的控制權</span><span class="sxs-lookup"><span data-stu-id="e0c67-130">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="e0c67-131">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="e0c67-131">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="e0c67-132">Winsock 追蹤層級</span><span class="sxs-lookup"><span data-stu-id="e0c67-132">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="e0c67-133">Winsock 目錄變更追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="e0c67-133">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
