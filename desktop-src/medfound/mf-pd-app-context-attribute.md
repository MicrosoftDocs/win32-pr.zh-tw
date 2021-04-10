---
description: 包含從受保護媒體路徑到展示描述項的指標 (PMP) 。
ms.assetid: cf12552e-0963-46fa-9a26-44dd601ab68c
title: 'MF_PD_APP_CONTEXT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8971ead121407ff1a7793c16b14f6b02d3dd102e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194285"
---
# <a name="mf_pd_app_context-attribute"></a><span data-ttu-id="a1bf3-103">MF \_ PD \_ 應用程式 \_ 內容屬性</span><span class="sxs-lookup"><span data-stu-id="a1bf3-103">MF\_PD\_APP\_CONTEXT attribute</span></span>

<span data-ttu-id="a1bf3-104">包含從受保護媒體路徑到展示描述項的指標 (PMP) 。</span><span class="sxs-lookup"><span data-stu-id="a1bf3-104">Contains a pointer to the presentation descriptor from the Protected Media Path (PMP).</span></span>

## <a name="data-type"></a><span data-ttu-id="a1bf3-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a1bf3-105">Data type</span></span>

<span data-ttu-id="a1bf3-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="a1bf3-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="a1bf3-107">備註</span><span class="sxs-lookup"><span data-stu-id="a1bf3-107">Remarks</span></span>

<span data-ttu-id="a1bf3-108">在 PMP 程式中建立的媒體來源 proxy 會使用這個屬性，將遠端表示描述項儲存在應用程式的呈現描述項上。</span><span class="sxs-lookup"><span data-stu-id="a1bf3-108">The media source proxy, which is created in the PMP process, uses this attribute to store the remote presentation descriptor on the application's presentation descriptor.</span></span>

<span data-ttu-id="a1bf3-109">這個屬性的值是 [_ *IMFPresentationDescriptor* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="a1bf3-109">The value of this attribute is a pointer to the [_ *IMFPresentationDescriptor*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) interface.</span></span>

<span data-ttu-id="a1bf3-110">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="a1bf3-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1bf3-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1bf3-111">Requirements</span></span>



| <span data-ttu-id="a1bf3-112">需求</span><span class="sxs-lookup"><span data-stu-id="a1bf3-112">Requirement</span></span> | <span data-ttu-id="a1bf3-113">值</span><span class="sxs-lookup"><span data-stu-id="a1bf3-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1bf3-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1bf3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a1bf3-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1bf3-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a1bf3-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1bf3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a1bf3-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1bf3-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a1bf3-118">標頭</span><span class="sxs-lookup"><span data-stu-id="a1bf3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1bf3-119"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1bf3-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1bf3-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1bf3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1bf3-121">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="a1bf3-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a1bf3-122">**IMFAttributes::GetUnknown**</span><span class="sxs-lookup"><span data-stu-id="a1bf3-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="a1bf3-123">**IMFAttributes：： SetUnknown**</span><span class="sxs-lookup"><span data-stu-id="a1bf3-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="a1bf3-124">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="a1bf3-124">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




