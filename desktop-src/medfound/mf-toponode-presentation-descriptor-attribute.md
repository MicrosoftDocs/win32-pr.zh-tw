---
description: 包含媒體來源之展示描述項的指標。
ms.assetid: 4f2c1ad8-fda9-482f-b82a-9838d15d2785
title: 'MF_TOPONODE_PRESENTATION_DESCRIPTOR 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d95fae4f2c4d4a482c2a62d57e0835ea4f1c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691256"
---
# <a name="mf_toponode_presentation_descriptor-attribute"></a><span data-ttu-id="1b85a-103">MF \_ TOPONODE \_ 展示 \_ 描述項屬性</span><span class="sxs-lookup"><span data-stu-id="1b85a-103">MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR attribute</span></span>

<span data-ttu-id="1b85a-104">包含媒體來源之展示描述項的指標。</span><span class="sxs-lookup"><span data-stu-id="1b85a-104">Contains a pointer to the presentation descriptor for the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="1b85a-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="1b85a-105">Data type</span></span>

<span data-ttu-id="1b85a-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="1b85a-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="1b85a-107">備註</span><span class="sxs-lookup"><span data-stu-id="1b85a-107">Remarks</span></span>

<span data-ttu-id="1b85a-108">此屬性適用于 (_ \* MF \_ 拓撲 \_ SOURCESTREAM \_ 節點 \* \* ) 的來源節點。</span><span class="sxs-lookup"><span data-stu-id="1b85a-108">This attribute applies to source nodes (_\*MF\_TOPOLOGY\_SOURCESTREAM\_NODE\*\*).</span></span>

<span data-ttu-id="1b85a-109">屬性的值是標記法描述項的 [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="1b85a-109">The value of the attribute is a pointer to the presentation descriptor's [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span> <span data-ttu-id="1b85a-110">這是必要屬性。</span><span class="sxs-lookup"><span data-stu-id="1b85a-110">This attribute is required.</span></span>

<span data-ttu-id="1b85a-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="1b85a-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b85a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="1b85a-112">Requirements</span></span>



| <span data-ttu-id="1b85a-113">需求</span><span class="sxs-lookup"><span data-stu-id="1b85a-113">Requirement</span></span> | <span data-ttu-id="1b85a-114">值</span><span class="sxs-lookup"><span data-stu-id="1b85a-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1b85a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1b85a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1b85a-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b85a-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1b85a-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1b85a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1b85a-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1b85a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="1b85a-119">標頭</span><span class="sxs-lookup"><span data-stu-id="1b85a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b85a-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1b85a-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b85a-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b85a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b85a-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="1b85a-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="1b85a-123">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="1b85a-123">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="1b85a-124">**IMFAttributes：： SetUnknown**</span><span class="sxs-lookup"><span data-stu-id="1b85a-124">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="1b85a-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="1b85a-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="1b85a-126">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="1b85a-126">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 




