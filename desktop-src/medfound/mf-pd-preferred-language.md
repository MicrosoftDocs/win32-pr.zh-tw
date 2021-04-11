---
description: 包含媒體來源慣用的 RFC 1766 語言。
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: 'MF_PD_PREFERRED_LANGUAGE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bb121c7181724ef06b3e8fe9239342a140104a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194986"
---
# <a name="mf_pd_preferred_language-attribute"></a><span data-ttu-id="84f4f-103">MF \_ PD \_ 慣用 \_ 語言屬性</span><span class="sxs-lookup"><span data-stu-id="84f4f-103">MF\_PD\_PREFERRED\_LANGUAGE attribute</span></span>

<span data-ttu-id="84f4f-104">包含媒體來源慣用的 RFC 1766 語言。</span><span class="sxs-lookup"><span data-stu-id="84f4f-104">Contains the preferred RFC 1766 language of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="84f4f-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="84f4f-105">Data type</span></span>

<span data-ttu-id="84f4f-106">**WCHAR**</span><span class="sxs-lookup"><span data-stu-id="84f4f-106">**WCHAR**</span></span>

## <a name="getset"></a><span data-ttu-id="84f4f-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="84f4f-107">Get/set</span></span>

<span data-ttu-id="84f4f-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。</span><span class="sxs-lookup"><span data-stu-id="84f4f-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="84f4f-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="84f4f-109">To set this attribute, call [**IMFAttributes::Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="84f4f-110">適用於</span><span class="sxs-lookup"><span data-stu-id="84f4f-110">Applies to</span></span>

[<span data-ttu-id="84f4f-111">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="84f4f-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="84f4f-112">備註</span><span class="sxs-lookup"><span data-stu-id="84f4f-112">Remarks</span></span>

<span data-ttu-id="84f4f-113">[MF \_ PD \_ 慣用 \_ 語言] 屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="84f4f-113">The MF\_PD\_PREFERRED\_LANGUAGE attribute is optional.</span></span> <span data-ttu-id="84f4f-114">應用程式可以在媒體來源 (（例如網路來源) ）上設定此屬性，以指定其慣用語言。</span><span class="sxs-lookup"><span data-stu-id="84f4f-114">An application can set this attribute on a media source (such as a network source) to specify its preferred language.</span></span>

<span data-ttu-id="84f4f-115">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="84f4f-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="84f4f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="84f4f-116">Requirements</span></span>



| <span data-ttu-id="84f4f-117">需求</span><span class="sxs-lookup"><span data-stu-id="84f4f-117">Requirement</span></span> | <span data-ttu-id="84f4f-118">值</span><span class="sxs-lookup"><span data-stu-id="84f4f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="84f4f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84f4f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="84f4f-120">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84f4f-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="84f4f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84f4f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="84f4f-122">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84f4f-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="84f4f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="84f4f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="84f4f-124"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="84f4f-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84f4f-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84f4f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84f4f-126">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="84f4f-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="84f4f-127">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="84f4f-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




