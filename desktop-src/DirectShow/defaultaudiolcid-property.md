---
description: DVDAdm. DefaultAudioLCID 屬性會設定或抓取使用者指定之音訊資料流程預設 LCID 的登錄設定。
ms.assetid: ed347a5e-d4cc-42f1-8b75-0a0a2ca40476
title: DefaultAudioLCID 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe302adaa555d59b2c1dcd50d749e9afdc2de740
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106967014"
---
# <a name="defaultaudiolcid-property"></a><span data-ttu-id="729e8-103">DefaultAudioLCID 屬性</span><span class="sxs-lookup"><span data-stu-id="729e8-103">DefaultAudioLCID Property</span></span>

> [!Note]  
> <span data-ttu-id="729e8-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="729e8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="729e8-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="729e8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="729e8-106">`DVDAdm.DefaultAudioLCID`屬性會設定或抓取使用者指定之音訊資料流程預設 LCID 的登錄設定。</span><span class="sxs-lookup"><span data-stu-id="729e8-106">The `DVDAdm.DefaultAudioLCID` property sets or retrieves the registry setting for the user-specified default LCID for the audio stream.</span></span>

``` syntax
[ iAudioLCID = ] DVD.DVDAdm.DefaultAudioLCID
```

## <a name="return-value"></a><span data-ttu-id="729e8-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="729e8-107">Return Value</span></span>

<span data-ttu-id="729e8-108">傳回整數值，表示儲存在 DVD 應用程式之登錄設定中的使用者指定預設音訊 LCID。</span><span class="sxs-lookup"><span data-stu-id="729e8-108">Returns an Integer value representing the user-specified default audio LCID as stored in the registry settings for the DVD application.</span></span> <span data-ttu-id="729e8-109">此值不一定與 DVD 上所撰寫的預設音訊資料流程相同。</span><span class="sxs-lookup"><span data-stu-id="729e8-109">This value is not necessarily the same as the default audio stream as authored on the DVD.</span></span>

## <a name="remarks"></a><span data-ttu-id="729e8-110">備註</span><span class="sxs-lookup"><span data-stu-id="729e8-110">Remarks</span></span>

<span data-ttu-id="729e8-111">此屬性是讀取/寫入，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="729e8-111">This property is read/write with no default value.</span></span> <span data-ttu-id="729e8-112">如果未指定預設音訊 LCID，MSDVDAdm 物件將會播放標示為光碟上預設資料流程的音訊串流。</span><span class="sxs-lookup"><span data-stu-id="729e8-112">If no default audio LCID is specified, the MSDVDAdm object will play the audio stream that is marked as the default stream on the disc.</span></span>

## <a name="see-also"></a><span data-ttu-id="729e8-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="729e8-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="729e8-114">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="729e8-114">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



