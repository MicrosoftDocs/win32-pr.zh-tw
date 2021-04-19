---
description: GetVideoSize 方法會抓取原生的影片維度。
ms.assetid: 50db2c15-4064-4d18-94f0-f6cf05f1d236
title: GetVideoSize 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89b96d01c3f22eaae78a442f3496f3c7c7416eac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972954"
---
# <a name="getvideosize-method"></a><span data-ttu-id="668c1-103">GetVideoSize 方法</span><span class="sxs-lookup"><span data-stu-id="668c1-103">GetVideoSize Method</span></span>

> [!Note]  
> <span data-ttu-id="668c1-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="668c1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="668c1-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="668c1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="668c1-106">方法會抓取 `GetVideoSize` 原生的影片維度。</span><span class="sxs-lookup"><span data-stu-id="668c1-106">The `GetVideoSize` method retrieves the native video dimensions.</span></span>

``` syntax
[ oSizeRect = ] MSWebDVD.GetVideoSize()
```

## <a name="return-value"></a><span data-ttu-id="668c1-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="668c1-107">Return Value</span></span>

<span data-ttu-id="668c1-108">傳回 [DVDRect](dvdrect-object.md) 物件，其中包含四個讀取/寫入屬性： (左上角) x; (左上角) y、寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="668c1-108">Returns a [DVDRect](dvdrect-object.md) object containing four read/write properties: (top left) x; (top left) y, Width, and Height.</span></span> <span data-ttu-id="668c1-109">**X** 和 **y** 屬性會設定為零，而其他兩個屬性會反映 cd 上所撰寫的影片矩形的寬度和高度。</span><span class="sxs-lookup"><span data-stu-id="668c1-109">The **x** and **y** properties are set to zero and the other two properties reflect the width and height of the video rectangle as authored on the disc.</span></span>

 

 



