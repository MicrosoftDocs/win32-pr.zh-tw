---
description: 指定內容的 MIME 類型。
ms.assetid: bbcfb3e6-a86a-4621-b8d9-92ace60e8c10
title: 'MF_PD_MIME_TYPE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce1893253af139a73555d3a4fd483e9f59c5ae1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979226"
---
# <a name="mf_pd_mime_type-attribute"></a><span data-ttu-id="4ac21-103">MF \_ PD \_ MIME \_ 類型屬性</span><span class="sxs-lookup"><span data-stu-id="4ac21-103">MF\_PD\_MIME\_TYPE attribute</span></span>

<span data-ttu-id="4ac21-104">指定內容的 MIME 類型。</span><span class="sxs-lookup"><span data-stu-id="4ac21-104">Specifies the MIME type of the content.</span></span>

## <a name="data-type"></a><span data-ttu-id="4ac21-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="4ac21-105">Data type</span></span>

<span data-ttu-id="4ac21-106">寬字元字串</span><span class="sxs-lookup"><span data-stu-id="4ac21-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="4ac21-107">備註</span><span class="sxs-lookup"><span data-stu-id="4ac21-107">Remarks</span></span>

<span data-ttu-id="4ac21-108">這個屬性會套用至展示描述項。</span><span class="sxs-lookup"><span data-stu-id="4ac21-108">This attribute applies to presentation descriptors.</span></span>

<span data-ttu-id="4ac21-109">透過 [MIMEType](../properties/props-system-mimetype.md) 針對媒體檔案公開的 mime 類型可能會有一種偏差，可選擇適用于數位生活網路聯盟的 mime 類型， (DLNA) 。</span><span class="sxs-lookup"><span data-stu-id="4ac21-109">The MIME type exposed through [System.MIMEType](../properties/props-system-mimetype.md) for media files may have a bias towards choosing MIME types suitable for Digital Living Network Alliance (DLNA).</span></span>

<span data-ttu-id="4ac21-110">MF \_ PD \_ MIME \_ 類型和 [MIMEType](../properties/props-system-mimetype.md) 可能不一定相符。</span><span class="sxs-lookup"><span data-stu-id="4ac21-110">MF\_PD\_MIME\_TYPE and [System.MIMEType](../properties/props-system-mimetype.md) may not always match.</span></span>

<span data-ttu-id="4ac21-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="4ac21-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ac21-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ac21-112">Requirements</span></span>



| <span data-ttu-id="4ac21-113">需求</span><span class="sxs-lookup"><span data-stu-id="4ac21-113">Requirement</span></span> | <span data-ttu-id="4ac21-114">值</span><span class="sxs-lookup"><span data-stu-id="4ac21-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4ac21-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4ac21-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4ac21-116">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ac21-116">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="4ac21-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4ac21-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4ac21-118">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4ac21-118">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="4ac21-119">標頭</span><span class="sxs-lookup"><span data-stu-id="4ac21-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ac21-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ac21-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ac21-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ac21-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ac21-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4ac21-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4ac21-123">**IMFAttributes：： GetString**</span><span class="sxs-lookup"><span data-stu-id="4ac21-123">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="4ac21-124">**IMFAttributes：： SetString**</span><span class="sxs-lookup"><span data-stu-id="4ac21-124">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="4ac21-125">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="4ac21-125">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="4ac21-126">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="4ac21-126">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 
