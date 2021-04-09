---
description: ShowMenu 方法會在螢幕上顯示指定的功能表。
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: ShowMenu 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c64b2a08c8881001cc47c972ad8cc865af8a174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688071"
---
# <a name="showmenu-method"></a><span data-ttu-id="a6fb7-103">ShowMenu 方法</span><span class="sxs-lookup"><span data-stu-id="a6fb7-103">ShowMenu Method</span></span>

> [!Note]  
> <span data-ttu-id="a6fb7-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="a6fb7-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="a6fb7-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a6fb7-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="a6fb7-106">`ShowMenu`方法會在螢幕上顯示指定的功能表。</span><span class="sxs-lookup"><span data-stu-id="a6fb7-106">The `ShowMenu` method displays the specified menu on the screen.</span></span>

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a><span data-ttu-id="a6fb7-107">參數</span><span class="sxs-lookup"><span data-stu-id="a6fb7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6fb7-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*</span><span class="sxs-lookup"><span data-stu-id="a6fb7-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*</span></span>
</dt> <dd>

<span data-ttu-id="a6fb7-109">將功能表識別碼指定為整數。</span><span class="sxs-lookup"><span data-stu-id="a6fb7-109">Specifies the menu ID as an Integer.</span></span>



| <span data-ttu-id="a6fb7-110">值</span><span class="sxs-lookup"><span data-stu-id="a6fb7-110">Value</span></span> | <span data-ttu-id="a6fb7-111">描述</span><span class="sxs-lookup"><span data-stu-id="a6fb7-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="a6fb7-112">2</span><span class="sxs-lookup"><span data-stu-id="a6fb7-112">2</span></span>     | <span data-ttu-id="a6fb7-113">標題 (Top) </span><span class="sxs-lookup"><span data-stu-id="a6fb7-113">Title (Top)</span></span> |
| <span data-ttu-id="a6fb7-114">3</span><span class="sxs-lookup"><span data-stu-id="a6fb7-114">3</span></span>     | <span data-ttu-id="a6fb7-115">Root</span><span class="sxs-lookup"><span data-stu-id="a6fb7-115">Root</span></span>        |
| <span data-ttu-id="a6fb7-116">4</span><span class="sxs-lookup"><span data-stu-id="a6fb7-116">4</span></span>     | <span data-ttu-id="a6fb7-117">子圖片</span><span class="sxs-lookup"><span data-stu-id="a6fb7-117">Subpicture</span></span>  |
| <span data-ttu-id="a6fb7-118">5</span><span class="sxs-lookup"><span data-stu-id="a6fb7-118">5</span></span>     | <span data-ttu-id="a6fb7-119">音訊</span><span class="sxs-lookup"><span data-stu-id="a6fb7-119">Audio</span></span>       |
| <span data-ttu-id="a6fb7-120">6</span><span class="sxs-lookup"><span data-stu-id="a6fb7-120">6</span></span>     | <span data-ttu-id="a6fb7-121">角度</span><span class="sxs-lookup"><span data-stu-id="a6fb7-121">Angle</span></span>       |
| <span data-ttu-id="a6fb7-122">7</span><span class="sxs-lookup"><span data-stu-id="a6fb7-122">7</span></span>     | <span data-ttu-id="a6fb7-123">章節</span><span class="sxs-lookup"><span data-stu-id="a6fb7-123">Chapter</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6fb7-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6fb7-124">Return Value</span></span>

<span data-ttu-id="a6fb7-125">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="a6fb7-125">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6fb7-126">備註</span><span class="sxs-lookup"><span data-stu-id="a6fb7-126">Remarks</span></span>

<span data-ttu-id="a6fb7-127">DVD 功能表名稱可能有點令人困惑。</span><span class="sxs-lookup"><span data-stu-id="a6fb7-127">DVD menu names can be somewhat confusing.</span></span> <span data-ttu-id="a6fb7-128">標題功能表是影片管理員功能表的另一個名稱，也就是整個光碟的主功能表;它通常會列出光碟上所有可用的影片標題集。根功能表是一個影片標題集的功能表，其中可包含一個標題或一組標題。</span><span class="sxs-lookup"><span data-stu-id="a6fb7-128">The title menu is another name for the Video Manager Menu, the main menu for the entire disc; it generally lists all the video title sets available on the disc. The root menu is the menu for one video title set, which can contain one title or a group of titles.</span></span> <span data-ttu-id="a6fb7-129">標題集中的所有標題都會共用相同的子圖片、音訊和角度功能表。</span><span class="sxs-lookup"><span data-stu-id="a6fb7-129">All the titles in a title set share the same Subpicture, Audio, and Angle menus.</span></span>

 

 



