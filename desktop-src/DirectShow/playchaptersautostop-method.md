---
description: PlayChaptersAutoStop 方法會在指定的章節中開始播放指定的標題，並針對指定的章節數開始播放。
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: PlayChaptersAutoStop 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187455"
---
# <a name="playchaptersautostop-method"></a><span data-ttu-id="9be73-103">PlayChaptersAutoStop 方法</span><span class="sxs-lookup"><span data-stu-id="9be73-103">PlayChaptersAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="9be73-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="9be73-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9be73-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="9be73-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9be73-106">方法會在指定的 `PlayChaptersAutoStop` 章節中開始播放指定的標題，並針對指定的章節數開始播放。</span><span class="sxs-lookup"><span data-stu-id="9be73-106">The `PlayChaptersAutoStop` method starts playback at the specified chapter in the specified title and for the number of chapters specified.</span></span>

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a><span data-ttu-id="9be73-107">參數</span><span class="sxs-lookup"><span data-stu-id="9be73-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9be73-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="9be73-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="9be73-109">將標題指定為整數值。</span><span class="sxs-lookup"><span data-stu-id="9be73-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="9be73-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="9be73-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="9be73-111">將開始章節指定為整數值。</span><span class="sxs-lookup"><span data-stu-id="9be73-111">Specifies the start chapter as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="9be73-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*</span><span class="sxs-lookup"><span data-stu-id="9be73-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*</span></span>
</dt> <dd>

<span data-ttu-id="9be73-113">指定要當作整數值播放的章節數目。</span><span class="sxs-lookup"><span data-stu-id="9be73-113">Specifies the number of chapters to play as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9be73-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="9be73-114">Return Value</span></span>

<span data-ttu-id="9be73-115">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="9be73-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9be73-116">備註</span><span class="sxs-lookup"><span data-stu-id="9be73-116">Remarks</span></span>

<span data-ttu-id="9be73-117">播放最後一章之後，這個方法會讓 [**EC \_ DVD \_ 章節 \_ AUTOSTOP**](ec-dvd-chapter-autostop.md) 事件通知傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="9be73-117">When the last chapter has played, this method causes an [**EC\_DVD\_CHAPTER\_AUTOSTOP**](ec-dvd-chapter-autostop.md) event notification to be sent to the application.</span></span>

 

 



