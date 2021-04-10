---
description: 指定拓撲載入器如何連接此拓撲節點，以及此節點是否為選擇性節點。
ms.assetid: 8d70e1af-607b-47c3-9808-091c95fd05b7
title: 'MF_TOPONODE_CONNECT_METHOD 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3db5fef529ef451fa02ac4a29e62002b0a1996a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194587"
---
# <a name="mf_toponode_connect_method-attribute"></a><span data-ttu-id="7237d-103">MF \_ TOPONODE \_ CONNECT \_ METHOD 屬性</span><span class="sxs-lookup"><span data-stu-id="7237d-103">MF\_TOPONODE\_CONNECT\_METHOD attribute</span></span>

<span data-ttu-id="7237d-104">指定拓撲載入器如何連接此拓撲節點，以及此節點是否為選擇性節點。</span><span class="sxs-lookup"><span data-stu-id="7237d-104">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>

## <a name="data-type"></a><span data-ttu-id="7237d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="7237d-105">Data type</span></span>

<span data-ttu-id="7237d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7237d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="7237d-107">備註</span><span class="sxs-lookup"><span data-stu-id="7237d-107">Remarks</span></span>

<span data-ttu-id="7237d-108">這個屬性會套用至所有節點類型。</span><span class="sxs-lookup"><span data-stu-id="7237d-108">This attribute applies to all node types.</span></span>

<span data-ttu-id="7237d-109">此屬性值是來自 [**MF \_ CONNECT \_ 方法**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method)列舉的位 **or** of 旗標。</span><span class="sxs-lookup"><span data-stu-id="7237d-109">The attribute value is a bitwise **OR** of flags from the [**MF\_CONNECT\_METHOD**](/windows/desktop/api/mfidl/ne-mfidl-mf_connect_method) enumeration.</span></span> <span data-ttu-id="7237d-110">如果未設定此屬性，則預設值為 [ **MF \_ CONNECT \_ 允許 \_ 解碼器]**。</span><span class="sxs-lookup"><span data-stu-id="7237d-110">If this attribute is not set, the default value is **MF\_CONNECT\_ALLOW\_DECODER**.</span></span>

<span data-ttu-id="7237d-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="7237d-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7237d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7237d-112">Requirements</span></span>



| <span data-ttu-id="7237d-113">需求</span><span class="sxs-lookup"><span data-stu-id="7237d-113">Requirement</span></span> | <span data-ttu-id="7237d-114">值</span><span class="sxs-lookup"><span data-stu-id="7237d-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7237d-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7237d-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7237d-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7237d-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7237d-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7237d-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7237d-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7237d-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7237d-119">標頭</span><span class="sxs-lookup"><span data-stu-id="7237d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7237d-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="7237d-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7237d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7237d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7237d-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="7237d-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7237d-123">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7237d-123">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="7237d-124">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="7237d-124">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="7237d-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="7237d-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="7237d-126">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="7237d-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




