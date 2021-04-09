---
description: 多層式服務提供者的 Winsock 目錄變更事件 (LSP) 安裝作業。
ms.assetid: 76A3D175-8CDC-486C-8341-D6314BCEC113
title: WINSOCK_WS2HELP_LSP_INSTALL 事件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WINSOCK_WS2HELP_LSP_INSTALL
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2d95a77f68bafd29fde3bbf34336d9b31d2a412e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944800"
---
# <a name="winsock_ws2help_lsp_install-event"></a><span data-ttu-id="8a668-103">WINSOCK \_ WS2HELP \_ LSP \_ 安裝事件</span><span class="sxs-lookup"><span data-stu-id="8a668-103">WINSOCK\_WS2HELP\_LSP\_INSTALL event</span></span>

> [!Note]  
> <span data-ttu-id="8a668-104">已淘汰分層服務提供者。</span><span class="sxs-lookup"><span data-stu-id="8a668-104">Layered Service Providers are deprecated.</span></span> <span data-ttu-id="8a668-105">從 Windows 8 和 Windows Server 2012 開始，請使用 [Windows 篩選平台](../fwp/windows-filtering-platform-start-page.md)。</span><span class="sxs-lookup"><span data-stu-id="8a668-105">Starting with Windows 8 and Windows Server 2012, use [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md).</span></span>

 

<span data-ttu-id="8a668-106">**Winsock \_ WS2HELP \_ lsp \_ 安裝** 事件是多層式服務提供者的 winsock 目錄變更事件， (LSP) 安裝作業。</span><span class="sxs-lookup"><span data-stu-id="8a668-106">The **WINSOCK\_WS2HELP\_LSP\_INSTALL** event is a Winsock catalog change event for a layered service provider (LSP) installation operation.</span></span>


```C++
const EVENT_DESCRIPTOR WINSOCK_WS2HELP_LSP_INSTALL = {0x1, 0x0, 0x10, 0x0, 0x0, 0x0, 0x8000000000000000};
```



## <a name="parameters"></a><span data-ttu-id="8a668-107">參數</span><span class="sxs-lookup"><span data-stu-id="8a668-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a668-108">*LSP 名稱*</span><span class="sxs-lookup"><span data-stu-id="8a668-108">*LSP Name*</span></span> 
</dt> <dd>

<span data-ttu-id="8a668-109">從所安裝的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **SZPROTOCOL** 成員取得的 LSP 名稱。</span><span class="sxs-lookup"><span data-stu-id="8a668-109">The name of the LSP as obtained from the **szProtocol** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span>

</dd> <dt>

<span data-ttu-id="8a668-110">*目錄*</span><span class="sxs-lookup"><span data-stu-id="8a668-110">*Catalog*</span></span> 
</dt> <dd>

<span data-ttu-id="8a668-111">Winsock 目錄 (32 位或64位) 安裝 LSP 的位置。</span><span class="sxs-lookup"><span data-stu-id="8a668-111">The Winsock catalog (32-bit or 64-bit) where the LSP is being installed.</span></span> <span data-ttu-id="8a668-112">這是一個整數值，也就是32或64。</span><span class="sxs-lookup"><span data-stu-id="8a668-112">This is an integer value that is either 32 or 64.</span></span>

</dd> <dt>

<span data-ttu-id="8a668-113">*安裝程式*</span><span class="sxs-lookup"><span data-stu-id="8a668-113">*Installer*</span></span> 
</dt> <dd>

<span data-ttu-id="8a668-114">讓 LSP 安裝呼叫的應用程式模組檔案名。</span><span class="sxs-lookup"><span data-stu-id="8a668-114">The module filename of the application making the LSP install call.</span></span>

</dd> <dt>

<span data-ttu-id="8a668-115">*GUID*</span><span class="sxs-lookup"><span data-stu-id="8a668-115">*GUID*</span></span> 
</dt> <dd>

<span data-ttu-id="8a668-116">要在其中安裝 LSP 之 Winsock 傳輸提供者的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="8a668-116">The GUID value of the Winsock transport provider that the LSP is being installed under.</span></span>

</dd> <dt>

<span data-ttu-id="8a668-117">*類別*</span><span class="sxs-lookup"><span data-stu-id="8a668-117">*Category*</span></span> 
</dt> <dd>

<span data-ttu-id="8a668-118">要安裝的 LSP 之 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)結構的 **dwCatalogEntryId** 成員。</span><span class="sxs-lookup"><span data-stu-id="8a668-118">The **dwCatalogEntryId** member of the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for the LSP being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a668-119">備註</span><span class="sxs-lookup"><span data-stu-id="8a668-119">Remarks</span></span>

<span data-ttu-id="8a668-120">當通訊協定專案安裝到 Winsock 類別目錄時，系統會針對 LSP 安裝作業追蹤 **WINSOCK \_ WS2HELP \_ lsp \_ 安裝** 事件。</span><span class="sxs-lookup"><span data-stu-id="8a668-120">The **WINSOCK\_WS2HELP\_LSP\_INSTALL** event is traced for an LSP install operation when a protocol entry is installed into the Winsock catalog.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a668-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a668-121">Requirements</span></span>



| <span data-ttu-id="8a668-122">需求</span><span class="sxs-lookup"><span data-stu-id="8a668-122">Requirement</span></span> | <span data-ttu-id="8a668-123">值</span><span class="sxs-lookup"><span data-stu-id="8a668-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8a668-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a668-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8a668-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a668-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8a668-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a668-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8a668-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8a668-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a668-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a668-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a668-129">Winsock 追蹤的控制權</span><span class="sxs-lookup"><span data-stu-id="8a668-129">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="8a668-130">Winsock 追蹤</span><span class="sxs-lookup"><span data-stu-id="8a668-130">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="8a668-131">Winsock 追蹤層級</span><span class="sxs-lookup"><span data-stu-id="8a668-131">Winsock Tracing Levels</span></span>](winsock-tracing-levels.md)
</dt> <dt>

[<span data-ttu-id="8a668-132">Winsock 目錄變更追蹤詳細資料</span><span class="sxs-lookup"><span data-stu-id="8a668-132">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

 
