---
description: 指定簡報的持續時間，以 100-毫微秒單位表示。
ms.assetid: abc21696-ea97-41ff-9341-6d9e9dcb19ec
title: 'MF_PD_DURATION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace7bd4f897de0220c2c449ce4fa891ac52eb200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996824"
---
# <a name="mf_pd_duration-attribute"></a><span data-ttu-id="f0472-103">MF \_ PD \_ DURATION 屬性</span><span class="sxs-lookup"><span data-stu-id="f0472-103">MF\_PD\_DURATION attribute</span></span>

<span data-ttu-id="f0472-104">指定簡報的持續時間，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="f0472-104">Specifies the duration of a presentation, in 100-nanosecond units.</span></span>

## <a name="data-type"></a><span data-ttu-id="f0472-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="f0472-105">Data type</span></span>

<span data-ttu-id="f0472-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f0472-106">**UINT64**</span></span>

<span data-ttu-id="f0472-107">視為 **LONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="f0472-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0472-108">備註</span><span class="sxs-lookup"><span data-stu-id="f0472-108">Remarks</span></span>

<span data-ttu-id="f0472-109">媒體來源可以在簡報描述項上設定此屬性，以指出簡報的持續時間。</span><span class="sxs-lookup"><span data-stu-id="f0472-109">Media sources can set this attribute on a presentation descriptor to indicate the duration of the presentation.</span></span>

<span data-ttu-id="f0472-110">這個屬性是帶正負號的值，雖然它會儲存為 **UINT64**。</span><span class="sxs-lookup"><span data-stu-id="f0472-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="f0472-111">但是，屬性絕對不能包含負數值。</span><span class="sxs-lookup"><span data-stu-id="f0472-111">However, the attribute should never contain a negative value.</span></span>

<span data-ttu-id="f0472-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="f0472-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="f0472-113">範例</span><span class="sxs-lookup"><span data-stu-id="f0472-113">Examples</span></span>

<span data-ttu-id="f0472-114">下列範例顯示如何從媒體來源取得簡報持續時間。</span><span class="sxs-lookup"><span data-stu-id="f0472-114">The following example shows how to get the presentation duration from a media source.</span></span>


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="f0472-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0472-115">Requirements</span></span>



| <span data-ttu-id="f0472-116">需求</span><span class="sxs-lookup"><span data-stu-id="f0472-116">Requirement</span></span> | <span data-ttu-id="f0472-117">值</span><span class="sxs-lookup"><span data-stu-id="f0472-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0472-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0472-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f0472-119">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0472-119">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="f0472-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0472-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f0472-121">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0472-121">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="f0472-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f0472-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0472-123"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f0472-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0472-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0472-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0472-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f0472-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f0472-126">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="f0472-126">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="f0472-127">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="f0472-127">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="f0472-128">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f0472-128">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[<span data-ttu-id="f0472-129">展示描述項屬性</span><span class="sxs-lookup"><span data-stu-id="f0472-129">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> <dt>

[<span data-ttu-id="f0472-130">簡報描述項</span><span class="sxs-lookup"><span data-stu-id="f0472-130">Presentation Descriptors</span></span>](presentation-descriptors.md)
</dt> </dl>

 

 




