---
description: 類別識別碼 (與此拓撲節點相關聯之媒體基礎轉換 (MFT) 的 CLSID) 。
ms.assetid: 6aa6e649-d23d-4d8d-be80-2b8814b07a57
title: 'MF_TOPONODE_TRANSFORM_OBJECTID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea96e09a75374bfe048b531492fc913f764d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512273"
---
# <a name="mf_toponode_transform_objectid-attribute"></a><span data-ttu-id="e0d0e-103">MF \_ TOPONODE \_ 轉換 \_ OBJECTID 屬性</span><span class="sxs-lookup"><span data-stu-id="e0d0e-103">MF\_TOPONODE\_TRANSFORM\_OBJECTID attribute</span></span>

<span data-ttu-id="e0d0e-104">類別識別碼 (與此拓撲節點相關聯之媒體基礎轉換 (MFT) 的 CLSID) 。</span><span class="sxs-lookup"><span data-stu-id="e0d0e-104">The class identifier (CLSID) of the Media Foundation transform (MFT) associated with this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="e0d0e-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="e0d0e-105">Data type</span></span>

<span data-ttu-id="e0d0e-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="e0d0e-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="e0d0e-107">備註</span><span class="sxs-lookup"><span data-stu-id="e0d0e-107">Remarks</span></span>

<span data-ttu-id="e0d0e-108">這個屬性會套用至 (**MF \_ 拓撲 \_ 轉換 \_ 節點**) 的轉換節點。</span><span class="sxs-lookup"><span data-stu-id="e0d0e-108">This attribute applies to transform nodes (**MF\_TOPOLOGY\_TRANSFORM\_NODE**).</span></span>

<span data-ttu-id="e0d0e-109">應用程式可以使用這個屬性來初始化 transfrom-節點。</span><span class="sxs-lookup"><span data-stu-id="e0d0e-109">Applications can use this attribute to initialize a transfrom node.</span></span> <span data-ttu-id="e0d0e-110">如果設定此屬性，您就不需要呼叫 [**IMFTopologyNode：： SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) 與 MFT 或啟用物件的指標。</span><span class="sxs-lookup"><span data-stu-id="e0d0e-110">If you set this attribute, you do not have to call [**IMFTopologyNode::SetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) with a pointer to an MFT or activation object.</span></span> <span data-ttu-id="e0d0e-111">相反地，如果您呼叫 **SetObject**，就不需要設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e0d0e-111">Conversely, if you call **SetObject**, you do not need to set this attribute.</span></span> <span data-ttu-id="e0d0e-112">如需詳細資訊，請參閱 [建立拓撲](creating-topologies.md)。</span><span class="sxs-lookup"><span data-stu-id="e0d0e-112">For more information, see [Creating Topologies](creating-topologies.md).</span></span>

<span data-ttu-id="e0d0e-113">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="e0d0e-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0d0e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0d0e-114">Requirements</span></span>



| <span data-ttu-id="e0d0e-115">需求</span><span class="sxs-lookup"><span data-stu-id="e0d0e-115">Requirement</span></span> | <span data-ttu-id="e0d0e-116">值</span><span class="sxs-lookup"><span data-stu-id="e0d0e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d0e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0d0e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e0d0e-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0d0e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e0d0e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0d0e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e0d0e-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0d0e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e0d0e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e0d0e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0d0e-122"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e0d0e-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0d0e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e0d0e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0d0e-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="e0d0e-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e0d0e-125">**IMFAttributes：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="e0d0e-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="e0d0e-126">**IMFAttributes：： SetGUID**</span><span class="sxs-lookup"><span data-stu-id="e0d0e-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="e0d0e-127">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="e0d0e-127">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="e0d0e-128">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="e0d0e-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e0d0e-129">建立拓撲</span><span class="sxs-lookup"><span data-stu-id="e0d0e-129">Creating Topologies</span></span>](creating-topologies.md)
</dt> <dt>

[<span data-ttu-id="e0d0e-130">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="e0d0e-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




