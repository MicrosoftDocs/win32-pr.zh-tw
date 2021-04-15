---
description: '>colorkey 屬性會設定或抓取隱藏式輔助字幕中使用的色彩索引鍵。'
ms.assetid: 4d4b38e6-bd29-4e16-8f82-a5da9312d272
title: '>colorkey 屬性'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75620be88a861e02915c27324978382feefc5835
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467556"
---
# <a name="colorkey-property"></a><span data-ttu-id="9fefe-103">>colorkey 屬性</span><span class="sxs-lookup"><span data-stu-id="9fefe-103">ColorKey Property</span></span>

> [!Note]  
> <span data-ttu-id="9fefe-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="9fefe-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9fefe-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="9fefe-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9fefe-106">`ColorKey`屬性會設定或抓取隱藏式輔助字幕中使用的色彩索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9fefe-106">The `ColorKey` property sets or retrieves the color key used in closed captioning.</span></span>

``` syntax
[ iColorKey = ] MSWebDVD.ColorKey
```

## <a name="return-value"></a><span data-ttu-id="9fefe-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="9fefe-107">Return Value</span></span>

<span data-ttu-id="9fefe-108">傳回整數值，表示用來做為封閉標題文字之透明背景的色彩。</span><span class="sxs-lookup"><span data-stu-id="9fefe-108">Returns an integer value representing the color to use as a transparent background for closed-captioned text.</span></span> <span data-ttu-id="9fefe-109">256色彩中的預設值為洋紅，而在任何其他色彩深度中為非黑色。</span><span class="sxs-lookup"><span data-stu-id="9fefe-109">The default value in 256 colors is magenta, and off-black in any other color depth.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fefe-110">備註</span><span class="sxs-lookup"><span data-stu-id="9fefe-110">Remarks</span></span>

<span data-ttu-id="9fefe-111">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9fefe-111">This property is read/write.</span></span> <span data-ttu-id="9fefe-112">這個屬性只適用于已隱藏的標題（如果有的話），而不會套用至子圖片資料流程。</span><span class="sxs-lookup"><span data-stu-id="9fefe-112">This property applies only to the closed-captions, if any exist, not to the subpicture stream.</span></span>

 

 



