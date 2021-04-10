---
description: 指定原始程式檔的大小總計（以位元組為單位）。 這個屬性會套用至展示描述項。 媒體來源可以選擇性地設定這個屬性。
ms.assetid: 722ebb14-c3e8-4f83-8fa2-e006b1094a59
title: 'MF_PD_TOTAL_FILE_SIZE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec7fc868c2438b576beff358ff722b3cb61851a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852428"
---
# <a name="mf_pd_total_file_size-attribute"></a><span data-ttu-id="0aea4-105">MF \_ PD \_ TOTAL \_ FILE \_ SIZE 屬性</span><span class="sxs-lookup"><span data-stu-id="0aea4-105">MF\_PD\_TOTAL\_FILE\_SIZE attribute</span></span>

<span data-ttu-id="0aea4-106">指定原始程式檔的大小總計（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0aea4-106">Specifies the total size of the source file, in bytes.</span></span> <span data-ttu-id="0aea4-107">這個屬性會套用至展示描述項。</span><span class="sxs-lookup"><span data-stu-id="0aea4-107">This attribute applies to presentation descriptors.</span></span> <span data-ttu-id="0aea4-108">媒體來源可以選擇性地設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="0aea4-108">A media source can optionally set this attribute.</span></span>

## <a name="data-type"></a><span data-ttu-id="0aea4-109">資料類型</span><span class="sxs-lookup"><span data-stu-id="0aea4-109">Data type</span></span>

<span data-ttu-id="0aea4-110">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="0aea4-110">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="0aea4-111">備註</span><span class="sxs-lookup"><span data-stu-id="0aea4-111">Remarks</span></span>

<span data-ttu-id="0aea4-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="0aea4-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aea4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0aea4-113">Requirements</span></span>



| <span data-ttu-id="0aea4-114">需求</span><span class="sxs-lookup"><span data-stu-id="0aea4-114">Requirement</span></span> | <span data-ttu-id="0aea4-115">值</span><span class="sxs-lookup"><span data-stu-id="0aea4-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0aea4-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0aea4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0aea4-117">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0aea4-117">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0aea4-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0aea4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0aea4-119">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0aea4-119">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="0aea4-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0aea4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0aea4-121"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="0aea4-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0aea4-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0aea4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aea4-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="0aea4-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="0aea4-124">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="0aea4-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="0aea4-125">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="0aea4-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="0aea4-126">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="0aea4-126">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="0aea4-127">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="0aea4-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




