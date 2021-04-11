---
description: TotalTitleTime 屬性會抓取目前標題的總播放時間。
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: TotalTitleTime 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a300a2da8de2698a74e0d72362818bd8a2a5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849672"
---
# <a name="totaltitletime-property"></a><span data-ttu-id="45aad-103">TotalTitleTime 屬性</span><span class="sxs-lookup"><span data-stu-id="45aad-103">TotalTitleTime Property</span></span>

> [!Note]  
> <span data-ttu-id="45aad-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="45aad-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="45aad-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="45aad-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="45aad-106">`TotalTitleTime`屬性會捕獲目前標題的總播放時間。</span><span class="sxs-lookup"><span data-stu-id="45aad-106">The `TotalTitleTime` property retrieves the total playback time for the current title.</span></span>

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a><span data-ttu-id="45aad-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="45aad-107">Return Value</span></span>

<span data-ttu-id="45aad-108">以字串格式傳回目前標題的總播放時間，格式為 "hh： mm： ss： ff"。</span><span class="sxs-lookup"><span data-stu-id="45aad-108">Returns the total playing time of the current title as a String in the format "hh:mm:ss:ff".</span></span>

## <a name="remarks"></a><span data-ttu-id="45aad-109">備註</span><span class="sxs-lookup"><span data-stu-id="45aad-109">Remarks</span></span>

<span data-ttu-id="45aad-110">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="45aad-110">This property is read-only with no default value.</span></span> <span data-ttu-id="45aad-111">傳回的字串將會是11個字元，格式為 "hh： mm： ss： ff" (小時、分鐘、秒、畫面格) 。</span><span class="sxs-lookup"><span data-stu-id="45aad-111">The returned string will be 11 characters long in the format "hh:mm:ss:ff" (hours, minutes, seconds, frames).</span></span>

## <a name="see-also"></a><span data-ttu-id="45aad-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="45aad-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45aad-113">**PlayAtTime**</span><span class="sxs-lookup"><span data-stu-id="45aad-113">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="45aad-114">**PlayAtTimeInTitle**</span><span class="sxs-lookup"><span data-stu-id="45aad-114">**PlayAtTimeInTitle**</span></span>](playattimeintitle-method.md)
</dt> </dl>

 

 



