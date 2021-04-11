---
description: 指定播放 Advanced 系統格式所需的時間， (ASF) 檔，以 100-毫微秒單位表示。
ms.assetid: 3d36808b-aa13-4205-ad92-97e951ee827e
title: 'MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac62dfbd86dfcbd001555343309568033787186b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944689"
---
# <a name="mf_pd_asf_fileproperties_play_duration-attribute"></a><span data-ttu-id="ef18e-103">MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 播放 \_ 持續時間屬性</span><span class="sxs-lookup"><span data-stu-id="ef18e-103">MF\_PD\_ASF\_FILEPROPERTIES\_PLAY\_DURATION attribute</span></span>

<span data-ttu-id="ef18e-104">指定播放 Advanced 系統格式所需的時間， (ASF) 檔，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="ef18e-104">Specifies the time needed to play an Advanced Systems Format (ASF) file, in 100-nanosecond units.</span></span>

<span data-ttu-id="ef18e-105">此值包含預先進行的時間。</span><span class="sxs-lookup"><span data-stu-id="ef18e-105">This value includes the preroll time.</span></span> <span data-ttu-id="ef18e-106">若要取得實際的播放持續時間，請取得 [ [**MF \_ PD \_ duration**](mf-pd-duration-attribute.md) ] 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="ef18e-106">To retrieve the actual playback duration, get the value of the [**MF\_PD\_DURATION**](mf-pd-duration-attribute.md) attribute.</span></span> <span data-ttu-id="ef18e-107">但是，如果預先進行的值大於播放持續時間，則 [ **MF \_ PD \_ 持續時間** ] 的值為零。</span><span class="sxs-lookup"><span data-stu-id="ef18e-107">However, if the preroll value is greater than the play duration, the value of **MF\_PD\_DURATION** is zero.</span></span>

## <a name="data-type"></a><span data-ttu-id="ef18e-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="ef18e-108">Data type</span></span>

<span data-ttu-id="ef18e-109">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="ef18e-109">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="ef18e-110">備註</span><span class="sxs-lookup"><span data-stu-id="ef18e-110">Remarks</span></span>

<span data-ttu-id="ef18e-111">此屬性適用于 ASF 內容的表示描述項。</span><span class="sxs-lookup"><span data-stu-id="ef18e-111">This attribute applies to presentation descriptors for ASF content.</span></span>

<span data-ttu-id="ef18e-112">[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。</span><span class="sxs-lookup"><span data-stu-id="ef18e-112">The [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) method generates this attribute from the ASF metadata.</span></span>

## <a name="examples"></a><span data-ttu-id="ef18e-113">範例</span><span class="sxs-lookup"><span data-stu-id="ef18e-113">Examples</span></span>


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



## <a name="requirements"></a><span data-ttu-id="ef18e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef18e-114">Requirements</span></span>



| <span data-ttu-id="ef18e-115">需求</span><span class="sxs-lookup"><span data-stu-id="ef18e-115">Requirement</span></span> | <span data-ttu-id="ef18e-116">值</span><span class="sxs-lookup"><span data-stu-id="ef18e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef18e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef18e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ef18e-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef18e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ef18e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef18e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ef18e-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef18e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ef18e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ef18e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef18e-122"><dt>Wmcontainer。h</dt></span><span class="sxs-lookup"><span data-stu-id="ef18e-122"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef18e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef18e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef18e-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="ef18e-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ef18e-125">**IMFAttributes：： GetGUID**</span><span class="sxs-lookup"><span data-stu-id="ef18e-125">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="ef18e-126">**IMFAttributes：： SetGUID**</span><span class="sxs-lookup"><span data-stu-id="ef18e-126">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="ef18e-127">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="ef18e-127">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="ef18e-128">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="ef18e-128">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="ef18e-129">ASF 標頭物件</span><span class="sxs-lookup"><span data-stu-id="ef18e-129">ASF Header Object</span></span>](asf-file-structure.md)
</dt> <dt>

[<span data-ttu-id="ef18e-130">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="ef18e-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




