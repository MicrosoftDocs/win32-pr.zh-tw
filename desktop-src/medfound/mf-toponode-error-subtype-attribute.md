---
description: 包含拓撲節點的媒體子類型。 因為找不到正確的解碼器，所以拓撲無法載入時，就會設定這個屬性。
ms.assetid: 89da33c8-97af-4c56-8bdb-2ac588810d77
title: 'MF_TOPONODE_ERROR_SUBTYPE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1233fb62c271a6f4fd84ec8b2c0b34aa6c49b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992008"
---
# <a name="mf_toponode_error_subtype-attribute"></a><span data-ttu-id="b7d37-104">MF \_ TOPONODE \_ 錯誤 \_ 子類型屬性</span><span class="sxs-lookup"><span data-stu-id="b7d37-104">MF\_TOPONODE\_ERROR\_SUBTYPE attribute</span></span>

<span data-ttu-id="b7d37-105">包含拓撲節點的媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="b7d37-105">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="b7d37-106">因為找不到正確的解碼器，所以拓撲無法載入時，就會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="b7d37-106">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>

## <a name="data-type"></a><span data-ttu-id="b7d37-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="b7d37-107">Data type</span></span>

<span data-ttu-id="b7d37-108">**GUID**</span><span class="sxs-lookup"><span data-stu-id="b7d37-108">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="b7d37-109">備註</span><span class="sxs-lookup"><span data-stu-id="b7d37-109">Remarks</span></span>

<span data-ttu-id="b7d37-110">這個屬性會套用至所有節點類型。</span><span class="sxs-lookup"><span data-stu-id="b7d37-110">This attribute applies to all node types.</span></span>

<span data-ttu-id="b7d37-111">拓撲載入器可能會設定屬性。</span><span class="sxs-lookup"><span data-stu-id="b7d37-111">The topology loader might set the attribute.</span></span> <span data-ttu-id="b7d37-112">應用程式通常會讀取此屬性，但不會設定它。</span><span class="sxs-lookup"><span data-stu-id="b7d37-112">Applications typically read this attribute but do not set it.</span></span>

<span data-ttu-id="b7d37-113">如需可能值的清單，請參閱 [媒體類型 guid](media-type-guids.md)。</span><span class="sxs-lookup"><span data-stu-id="b7d37-113">For a list of possible values, see [Media Type GUIDs](media-type-guids.md).</span></span>

<span data-ttu-id="b7d37-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="b7d37-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d37-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7d37-115">Requirements</span></span>



| <span data-ttu-id="b7d37-116">需求</span><span class="sxs-lookup"><span data-stu-id="b7d37-116">Requirement</span></span> | <span data-ttu-id="b7d37-117">值</span><span class="sxs-lookup"><span data-stu-id="b7d37-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d37-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b7d37-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d37-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7d37-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b7d37-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b7d37-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d37-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b7d37-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b7d37-122">標頭</span><span class="sxs-lookup"><span data-stu-id="b7d37-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7d37-123"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d37-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7d37-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7d37-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d37-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="b7d37-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b7d37-126">**IMFAttributes：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="b7d37-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="b7d37-127">**IMFAttributes：： SetGUID**</span><span class="sxs-lookup"><span data-stu-id="b7d37-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="b7d37-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="b7d37-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="b7d37-129">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="b7d37-129">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> </dl>

 

 




