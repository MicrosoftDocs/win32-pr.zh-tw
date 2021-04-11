---
description: CursorType 屬性會設定或抓取目前的資料指標類型。
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: CursorType 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846356"
---
# <a name="cursortype-property"></a><span data-ttu-id="1a1ab-103">CursorType 屬性</span><span class="sxs-lookup"><span data-stu-id="1a1ab-103">CursorType Property</span></span>

> [!Note]  
> <span data-ttu-id="1a1ab-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="1a1ab-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="1a1ab-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="1a1ab-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="1a1ab-106">`CursorType`屬性會設定或抓取目前的資料指標類型。</span><span class="sxs-lookup"><span data-stu-id="1a1ab-106">The `CursorType` property sets or retrieves the current cursor type.</span></span>

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a><span data-ttu-id="1a1ab-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a1ab-107">Return Value</span></span>

<span data-ttu-id="1a1ab-108">傳回表示資料指標類型的整數值。</span><span class="sxs-lookup"><span data-stu-id="1a1ab-108">Returns an integer value representing the cursor type.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a1ab-109">備註</span><span class="sxs-lookup"><span data-stu-id="1a1ab-109">Remarks</span></span>

<span data-ttu-id="1a1ab-110">這個屬性的可能值為：</span><span class="sxs-lookup"><span data-stu-id="1a1ab-110">The possible values for this property are:</span></span>



| <span data-ttu-id="1a1ab-111">值</span><span class="sxs-lookup"><span data-stu-id="1a1ab-111">Value</span></span> | <span data-ttu-id="1a1ab-112">描述</span><span class="sxs-lookup"><span data-stu-id="1a1ab-112">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="1a1ab-113">0</span><span class="sxs-lookup"><span data-stu-id="1a1ab-113">0</span></span>     | <span data-ttu-id="1a1ab-114">箭號</span><span class="sxs-lookup"><span data-stu-id="1a1ab-114">Arrow</span></span>       |
| <span data-ttu-id="1a1ab-115">1</span><span class="sxs-lookup"><span data-stu-id="1a1ab-115">1</span></span>     | <span data-ttu-id="1a1ab-116">放大</span><span class="sxs-lookup"><span data-stu-id="1a1ab-116">Zoom In</span></span>     |
| <span data-ttu-id="1a1ab-117">2</span><span class="sxs-lookup"><span data-stu-id="1a1ab-117">2</span></span>     | <span data-ttu-id="1a1ab-118">縮小</span><span class="sxs-lookup"><span data-stu-id="1a1ab-118">Zoom Out</span></span>    |
| <span data-ttu-id="1a1ab-119">3</span><span class="sxs-lookup"><span data-stu-id="1a1ab-119">3</span></span>     | <span data-ttu-id="1a1ab-120">手</span><span class="sxs-lookup"><span data-stu-id="1a1ab-120">Hand</span></span>        |
| <span data-ttu-id="1a1ab-121">-1</span><span class="sxs-lookup"><span data-stu-id="1a1ab-121">-1</span></span>    | <span data-ttu-id="1a1ab-122">無</span><span class="sxs-lookup"><span data-stu-id="1a1ab-122">None</span></span>        |



 

<span data-ttu-id="1a1ab-123">此屬性是讀取/寫入，預設值為零。</span><span class="sxs-lookup"><span data-stu-id="1a1ab-123">This property is read/write with a default value of zero.</span></span> <span data-ttu-id="1a1ab-124">當圖片放大時，將 `CursorType` (0x3 的 **設定設** 為) 會將應用程式放入拖曳模式，讓使用者能夠在影片顯示區域內移動影像。</span><span class="sxs-lookup"><span data-stu-id="1a1ab-124">When the picture is zoomed in, setting `CursorType` to **Hand** (0x3) puts the application into drag mode, enabling the user to move the image inside the video display area.</span></span>

 

 



