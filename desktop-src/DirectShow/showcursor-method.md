---
description: 當 MSWebDVD 物件處於全螢幕模式時，ShowCursor 方法會讓資料指標可見。
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: ShowCursor 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846415"
---
# <a name="showcursor-method"></a><span data-ttu-id="647bd-103">ShowCursor 方法</span><span class="sxs-lookup"><span data-stu-id="647bd-103">ShowCursor Method</span></span>

> [!Note]  
> <span data-ttu-id="647bd-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="647bd-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="647bd-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="647bd-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="647bd-106">`ShowCursor`當 **MSWebDVD** 物件處於全螢幕模式時，方法會讓資料指標可見。</span><span class="sxs-lookup"><span data-stu-id="647bd-106">The `ShowCursor` method makes the cursor visible when the **MSWebDVD** object is in full-screen mode.</span></span>

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a><span data-ttu-id="647bd-107">參數</span><span class="sxs-lookup"><span data-stu-id="647bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="647bd-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span><span class="sxs-lookup"><span data-stu-id="647bd-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span></span>
</dt> <dd>

<span data-ttu-id="647bd-109">指定是否將資料指標顯示為布林值。</span><span class="sxs-lookup"><span data-stu-id="647bd-109">Specifies whether to show the cursor as a Boolean.</span></span>



| <span data-ttu-id="647bd-110">值</span><span class="sxs-lookup"><span data-stu-id="647bd-110">Value</span></span> | <span data-ttu-id="647bd-111">描述</span><span class="sxs-lookup"><span data-stu-id="647bd-111">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="647bd-112">true</span><span class="sxs-lookup"><span data-stu-id="647bd-112">true</span></span>  | <span data-ttu-id="647bd-113">顯示游標</span><span class="sxs-lookup"><span data-stu-id="647bd-113">Show the cursor</span></span>        |
| <span data-ttu-id="647bd-114">false</span><span class="sxs-lookup"><span data-stu-id="647bd-114">false</span></span> | <span data-ttu-id="647bd-115">不要顯示資料指標</span><span class="sxs-lookup"><span data-stu-id="647bd-115">Do not show the cursor</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="647bd-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="647bd-116">Return Value</span></span>

<span data-ttu-id="647bd-117">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="647bd-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="647bd-118">備註</span><span class="sxs-lookup"><span data-stu-id="647bd-118">Remarks</span></span>

<span data-ttu-id="647bd-119">當 DVD 顯示進入全螢幕模式時，游標會在3到5秒內消失。</span><span class="sxs-lookup"><span data-stu-id="647bd-119">When the DVD display goes into full-screen mode, the cursor disappears within 3 to 5 seconds.</span></span> <span data-ttu-id="647bd-120">如果您的應用程式的控制項按鈕是在全螢幕模式中顯示，請使用這個方法來再次顯示資料指標。</span><span class="sxs-lookup"><span data-stu-id="647bd-120">Use this method to make the cursor visible again if your application's control buttons are visible in full-screen mode.</span></span>

 

 



