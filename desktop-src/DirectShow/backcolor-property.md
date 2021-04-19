---
description: 當原生影片的長寬比與物件的顯示區域不同時，背景色彩屬性會設定或抓取在影片矩形邊緣周圍出現的橫條色彩。
ms.assetid: 51576836-c648-4268-8475-0312dbd60963
title: '背景屬性 (DirectShow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37adb625080ca284c168c7286982e980f8919f3d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972940"
---
# <a name="backcolor-property-directshow"></a><span data-ttu-id="c1a68-103">背景屬性 (DirectShow) </span><span class="sxs-lookup"><span data-stu-id="c1a68-103">BackColor Property (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="c1a68-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="c1a68-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c1a68-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c1a68-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c1a68-106">`BackColor`當原生影片的長寬比與物件的顯示區域不同時，屬性會設定或抓取在影片矩形邊緣周圍出現的橫條色彩。</span><span class="sxs-lookup"><span data-stu-id="c1a68-106">The `BackColor` property sets or retrieves the color of the bars that appear around the edges of the video rectangle when the aspect ratio of the native video is not the same as that of the object's display area.</span></span>

``` syntax
[ iBackColor = ] MSWebDVD.BackColor
```

## <a name="return-value"></a><span data-ttu-id="c1a68-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1a68-107">Return Value</span></span>

<span data-ttu-id="c1a68-108">傳回整數值，表示背景色彩的 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="c1a68-108">Returns an integer value representing the RGB values of the back color.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1a68-109">備註</span><span class="sxs-lookup"><span data-stu-id="c1a68-109">Remarks</span></span>

<span data-ttu-id="c1a68-110">此屬性是讀取/寫入，預設值為 off-黑色 (0x100010) 。</span><span class="sxs-lookup"><span data-stu-id="c1a68-110">This property is read/write with a default value of off-black (0x100010).</span></span>

 

 



