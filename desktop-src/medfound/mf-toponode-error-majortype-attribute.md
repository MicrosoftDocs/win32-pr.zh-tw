---
description: 包含拓撲節點的主要媒體類型。 因為找不到正確的解碼器，所以拓撲無法載入時，就會設定這個屬性。
ms.assetid: eb837fe6-12c9-479c-a0be-63b24093e6fd
title: 'MF_TOPONODE_ERROR_MAJORTYPE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68ace0cd3bec4f32536e7d0d8d29bcea60d997
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973889"
---
# <a name="mf_toponode_error_majortype-attribute"></a><span data-ttu-id="8acbd-104">MF \_ TOPONODE \_ ERROR \_ MAJORTYPE 屬性</span><span class="sxs-lookup"><span data-stu-id="8acbd-104">MF\_TOPONODE\_ERROR\_MAJORTYPE attribute</span></span>

<span data-ttu-id="8acbd-105">包含拓撲節點的主要媒體類型。</span><span class="sxs-lookup"><span data-stu-id="8acbd-105">Contains the major media type for a topology node.</span></span> <span data-ttu-id="8acbd-106">因為找不到正確的解碼器，所以拓撲無法載入時，就會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="8acbd-106">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>

## <a name="data-type"></a><span data-ttu-id="8acbd-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="8acbd-107">Data type</span></span>

<span data-ttu-id="8acbd-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="8acbd-108">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="8acbd-109">備註</span><span class="sxs-lookup"><span data-stu-id="8acbd-109">Remarks</span></span>

<span data-ttu-id="8acbd-110">這個屬性會套用至所有節點類型。</span><span class="sxs-lookup"><span data-stu-id="8acbd-110">This attribute applies to all node types.</span></span>

<span data-ttu-id="8acbd-111">拓撲載入器可能會設定屬性。</span><span class="sxs-lookup"><span data-stu-id="8acbd-111">The topology loader might set the attribute.</span></span> <span data-ttu-id="8acbd-112">應用程式通常會讀取此屬性，但不會設定它。</span><span class="sxs-lookup"><span data-stu-id="8acbd-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="8acbd-113">如需可能值的清單，請參閱 [主要媒體類型](media-type-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="8acbd-113">For a list of possible values, see [Major Media Types](media-type-guids.md).</span></span>

<span data-ttu-id="8acbd-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="8acbd-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="8acbd-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8acbd-115">Requirements</span></span>



| <span data-ttu-id="8acbd-116">需求</span><span class="sxs-lookup"><span data-stu-id="8acbd-116">Requirement</span></span> | <span data-ttu-id="8acbd-117">值</span><span class="sxs-lookup"><span data-stu-id="8acbd-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8acbd-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8acbd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8acbd-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8acbd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8acbd-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8acbd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8acbd-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8acbd-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8acbd-122">標頭</span><span class="sxs-lookup"><span data-stu-id="8acbd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="8acbd-123"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8acbd-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8acbd-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8acbd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8acbd-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="8acbd-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="8acbd-126">**IMFAttributes：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="8acbd-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="8acbd-127">**IMFAttributes：： SetGUID**</span><span class="sxs-lookup"><span data-stu-id="8acbd-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="8acbd-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="8acbd-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="8acbd-129">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="8acbd-129">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




