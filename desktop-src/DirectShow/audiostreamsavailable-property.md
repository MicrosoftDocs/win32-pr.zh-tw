---
description: AudioStreamsAvailable 屬性會抓取目前標題中可用的音訊資料流程數目。
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: AudioStreamsAvailable 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846180"
---
# <a name="audiostreamsavailable-property"></a><span data-ttu-id="a905a-103">AudioStreamsAvailable 屬性</span><span class="sxs-lookup"><span data-stu-id="a905a-103">AudioStreamsAvailable Property</span></span>

> [!Note]  
> <span data-ttu-id="a905a-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="a905a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a905a-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a905a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a905a-106">屬性會抓取 `AudioStreamsAvailable` 目前標題中可用的音訊資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="a905a-106">The `AudioStreamsAvailable` property retrieves the number of audio streams available in the current title.</span></span>

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a><span data-ttu-id="a905a-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="a905a-107">Return Value</span></span>

<span data-ttu-id="a905a-108">傳回從1到8的整數值，代表目前標題中可用的音訊資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="a905a-108">Returns an integer value from 1 through 8 representing the number of audio streams available in the current title.</span></span>

## <a name="remarks"></a><span data-ttu-id="a905a-109">備註</span><span class="sxs-lookup"><span data-stu-id="a905a-109">Remarks</span></span>

<span data-ttu-id="a905a-110">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="a905a-110">This property is read-only with no default value.</span></span> <span data-ttu-id="a905a-111">多個音訊串流的主要用途是提供一種以上語言的電影 soundtracks。</span><span class="sxs-lookup"><span data-stu-id="a905a-111">The primary use of multiple audio streams is to provide movie soundtracks in more than one language.</span></span> <span data-ttu-id="a905a-112">一般而言，並非光碟上的每個標題都已啟用所有音訊串流。</span><span class="sxs-lookup"><span data-stu-id="a905a-112">Typically, not every title on a disc has all audio streams enabled.</span></span> <span data-ttu-id="a905a-113">例如，功能電影可能有三種不同語言的 soundtracks，但結尾可能只有英文的聲段。</span><span class="sxs-lookup"><span data-stu-id="a905a-113">For example, the feature movie might have soundtracks in three different languages, but the trailers might have only an English soundtrack.</span></span> <span data-ttu-id="a905a-114">在使用者可以選取資料流程之前，應用程式必須判斷目前的標題中有哪些可用的資料流程。</span><span class="sxs-lookup"><span data-stu-id="a905a-114">Before a user can select a stream, the application must determine which streams are available within the current title.</span></span> <span data-ttu-id="a905a-115">請注意，特定資料流程是由0到7的索引所識別。</span><span class="sxs-lookup"><span data-stu-id="a905a-115">Note that particular streams are identified by an index from zero through 7.</span></span>

<span data-ttu-id="a905a-116">光碟通常會顯示一個顯示可用 soundtracks 的功能表，讓使用者可以選取要啟用的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="a905a-116">Discs generally present a menu showing the available soundtracks, enabling the user to select the audio stream to enable.</span></span>

## <a name="see-also"></a><span data-ttu-id="a905a-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a905a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a905a-118">**GetAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="a905a-118">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> </dl>

 

 



