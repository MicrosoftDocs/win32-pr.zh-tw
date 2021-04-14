---
description: 如何尋找媒體檔案的持續時間。
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: 如何尋找媒體檔案的持續時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8915e52e97a4532b1d174166ec2863e26d18e34a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104514329"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a><span data-ttu-id="7f6db-103">如何尋找媒體檔案的持續時間</span><span class="sxs-lookup"><span data-stu-id="7f6db-103">How to Find the Duration of a Media File</span></span>

<span data-ttu-id="7f6db-104">若要尋找媒體檔案的持續時間，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="7f6db-104">To find the duration of a media file, perform the following steps:</span></span>

1.  <span data-ttu-id="7f6db-105">使用 [來源解析程式](source-resolver.md) 來建立可剖析媒體檔案的媒體來源。</span><span class="sxs-lookup"><span data-stu-id="7f6db-105">Use the [Source Resolver](source-resolver.md) to create a media source that can parse the media file.</span></span>
2.  <span data-ttu-id="7f6db-106">在媒體來源上呼叫 [**IMFMediaSource：： CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) 。</span><span class="sxs-lookup"><span data-stu-id="7f6db-106">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source.</span></span> <span data-ttu-id="7f6db-107">這個方法會傳回描述媒體檔案內容的簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="7f6db-107">This method returns presentation descriptor that describes the contents of the media file.</span></span>
3.  <span data-ttu-id="7f6db-108">藉由呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)方法，查詢適用于 [MF \_ PD \_ DURATION](mf-pd-duration-attribute.md)屬性的簡報描述項。</span><span class="sxs-lookup"><span data-stu-id="7f6db-108">Query the presentation descriptor for the [MF\_PD\_DURATION](mf-pd-duration-attribute.md) attribute by calling the [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) method.</span></span> <span data-ttu-id="7f6db-109">屬性的值（如果有的話）是檔案持續時間（以 100-毫微秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="7f6db-109">The value of the attribute, if present, is the file duration in 100-nanosecond units.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7f6db-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="7f6db-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f6db-111">音訊/視訊播放</span><span class="sxs-lookup"><span data-stu-id="7f6db-111">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> </dl>

 

 



