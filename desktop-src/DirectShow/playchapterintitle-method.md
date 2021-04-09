---
description: PlayChapterInTitle 方法會在指定的標題中播放指定的章節。
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: PlayChapterInTitle 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381a63c36c61a8853dcba6a587adb1f078b8cfaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845676"
---
# <a name="playchapterintitle-method"></a><span data-ttu-id="432de-103">PlayChapterInTitle 方法</span><span class="sxs-lookup"><span data-stu-id="432de-103">PlayChapterInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="432de-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="432de-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="432de-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="432de-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="432de-106">`PlayChapterInTitle`方法會在指定的標題中播放指定的章節。</span><span class="sxs-lookup"><span data-stu-id="432de-106">The `PlayChapterInTitle` method plays the specified chapter in the specified title.</span></span>

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a><span data-ttu-id="432de-107">參數</span><span class="sxs-lookup"><span data-stu-id="432de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="432de-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="432de-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="432de-109">將標題指定為整數值。</span><span class="sxs-lookup"><span data-stu-id="432de-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="432de-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="432de-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="432de-111">將章節指定為整數值。</span><span class="sxs-lookup"><span data-stu-id="432de-111">Specifies the chapter as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="432de-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="432de-112">Return Value</span></span>

<span data-ttu-id="432de-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="432de-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="432de-114">備註</span><span class="sxs-lookup"><span data-stu-id="432de-114">Remarks</span></span>

<span data-ttu-id="432de-115">這個方法會在指定的章節開始播放，然後繼續無限期地播放。</span><span class="sxs-lookup"><span data-stu-id="432de-115">This method starts playback at the specified chapter and then continues playing indefinitely.</span></span> <span data-ttu-id="432de-116">如果您只想要播放特定的章節，請使用 [**PlayChaptersAutoStop**](playchaptersautostop-method.md)。</span><span class="sxs-lookup"><span data-stu-id="432de-116">If you want to play only a particular chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

 

 



