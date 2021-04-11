---
description: 指定是否可在此拓撲節點上變更媒體類型。
ms.assetid: 8805ed63-1408-40bc-bb82-f3c51576dfa4
title: 'MF_TOPONODE_LOCKED 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70776b1a5ba9c5c35cd2a2d97618de4b3a65abb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691260"
---
# <a name="mf_toponode_locked-attribute"></a><span data-ttu-id="4f16a-103">MF \_ TOPONODE \_ 鎖定屬性</span><span class="sxs-lookup"><span data-stu-id="4f16a-103">MF\_TOPONODE\_LOCKED attribute</span></span>

<span data-ttu-id="4f16a-104">指定是否可在此拓撲節點上變更媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4f16a-104">Specifies whether the media types can be changed on this topology node.</span></span>

## <a name="data-type"></a><span data-ttu-id="4f16a-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="4f16a-105">Data type</span></span>

<span data-ttu-id="4f16a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4f16a-106">**UINT32**</span></span>

<span data-ttu-id="4f16a-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="4f16a-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f16a-108">備註</span><span class="sxs-lookup"><span data-stu-id="4f16a-108">Remarks</span></span>

<span data-ttu-id="4f16a-109">這個屬性會套用至所有節點類型。</span><span class="sxs-lookup"><span data-stu-id="4f16a-109">This attribute applies to all node types.</span></span>

<span data-ttu-id="4f16a-110">如果這個屬性的值為非零值，拓撲載入器不會變更媒體類型。</span><span class="sxs-lookup"><span data-stu-id="4f16a-110">If value of this attribute is nonzero, the topology loader will not change the media types.</span></span> <span data-ttu-id="4f16a-111">當節點正在使用中時，此屬性會設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="4f16a-111">This attribute is set to **TRUE** when the node is in use.</span></span>

<span data-ttu-id="4f16a-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="4f16a-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f16a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4f16a-113">Requirements</span></span>



| <span data-ttu-id="4f16a-114">需求</span><span class="sxs-lookup"><span data-stu-id="4f16a-114">Requirement</span></span> | <span data-ttu-id="4f16a-115">值</span><span class="sxs-lookup"><span data-stu-id="4f16a-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4f16a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4f16a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4f16a-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f16a-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4f16a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4f16a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4f16a-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4f16a-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4f16a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4f16a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f16a-121"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4f16a-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f16a-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f16a-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f16a-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4f16a-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4f16a-124">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4f16a-124">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4f16a-125">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4f16a-125">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4f16a-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="4f16a-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="4f16a-127">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="4f16a-127">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




