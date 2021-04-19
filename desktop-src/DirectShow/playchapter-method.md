---
description: PlayChapter 方法會從目前標題內的指定章節開始播放。
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: PlayChapter 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106998422"
---
# <a name="playchapter-method"></a><span data-ttu-id="12b69-103">PlayChapter 方法</span><span class="sxs-lookup"><span data-stu-id="12b69-103">PlayChapter Method</span></span>

> [!Note]  
> <span data-ttu-id="12b69-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="12b69-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="12b69-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="12b69-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="12b69-106">`PlayChapter`方法會從目前標題內的指定章節開始播放。</span><span class="sxs-lookup"><span data-stu-id="12b69-106">The `PlayChapter` method starts playback from the specified chapter within the current title.</span></span>

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a><span data-ttu-id="12b69-107">參數</span><span class="sxs-lookup"><span data-stu-id="12b69-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12b69-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="12b69-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="12b69-109">將目前標題中的章節索引指定為整數。</span><span class="sxs-lookup"><span data-stu-id="12b69-109">Specifies the chapter index in the current title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12b69-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="12b69-110">Return Value</span></span>

<span data-ttu-id="12b69-111">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="12b69-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12b69-112">備註</span><span class="sxs-lookup"><span data-stu-id="12b69-112">Remarks</span></span>

<span data-ttu-id="12b69-113">到達指定章節的結尾時，此方法會繼續播放後續章節（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="12b69-113">When the end of the specified chapter is reached, this method continues playing subsequent chapters, if any exist.</span></span> <span data-ttu-id="12b69-114">如果您只想要播放指定的章節，請使用 [**PlayChaptersAutoStop**](playchaptersautostop-method.md)。</span><span class="sxs-lookup"><span data-stu-id="12b69-114">If you want to play only a specified chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="12b69-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12b69-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12b69-116">**PlayChapterInTitle**</span><span class="sxs-lookup"><span data-stu-id="12b69-116">**PlayChapterInTitle**</span></span>](playchapterintitle-method.md)
</dt> </dl>

 

 



