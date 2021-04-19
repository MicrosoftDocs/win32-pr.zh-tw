---
title: IWMPDVD back 方法
description: Back 方法會將顯示從子功能表變更為其父功能表。
ms.assetid: 81d033d4-f570-44a5-898a-e419101c04fa
keywords:
- back 方法 Windows Media Player
- back 方法 Windows Media Player，IWMPDVD 介面
- IWMPDVD 介面 Windows Media Player，back 方法
topic_type:
- apiref
api_name:
- IWMPDVD.back
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cd31cd6365843a6905760c4447ea679e15e70ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997029"
---
# <a name="iwmpdvdback-method"></a><span data-ttu-id="e1016-106">IWMPDVD：： back 方法</span><span class="sxs-lookup"><span data-stu-id="e1016-106">IWMPDVD::back method</span></span>

<span data-ttu-id="e1016-107">**Back** 方法會將顯示從子功能表變更為其父功能表。</span><span class="sxs-lookup"><span data-stu-id="e1016-107">The **back** method changes the display from a submenu to its parent menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1016-108">語法</span><span class="sxs-lookup"><span data-stu-id="e1016-108">Syntax</span></span>


```CSharp
public void back();
```


```VB

Public Sub back()
Implements IWMPDVD.back
```





## <a name="parameters"></a><span data-ttu-id="e1016-109">參數</span><span class="sxs-lookup"><span data-stu-id="e1016-109">Parameters</span></span>

<span data-ttu-id="e1016-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e1016-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1016-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e1016-111">Return value</span></span>

<span data-ttu-id="e1016-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e1016-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1016-113">備註</span><span class="sxs-lookup"><span data-stu-id="e1016-113">Remarks</span></span>

<span data-ttu-id="e1016-114">每個 DVD 的撰寫方式不同。</span><span class="sxs-lookup"><span data-stu-id="e1016-114">Every DVD is authored differently.</span></span> <span data-ttu-id="e1016-115">某些 Dvd 的撰寫目的是讓 `back` 方法可從根功能表中取得，但叫用時，它不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="e1016-115">Some DVDs are authored so that the `back` method is available from the root menu, but when invoked, it will do nothing.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1016-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1016-116">Requirements</span></span>



| <span data-ttu-id="e1016-117">需求</span><span class="sxs-lookup"><span data-stu-id="e1016-117">Requirement</span></span> | <span data-ttu-id="e1016-118">值</span><span class="sxs-lookup"><span data-stu-id="e1016-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1016-119">版本</span><span class="sxs-lookup"><span data-stu-id="e1016-119">Version</span></span><br/>   | <span data-ttu-id="e1016-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="e1016-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e1016-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="e1016-121">Namespace</span></span><br/> | <span data-ttu-id="e1016-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e1016-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e1016-123">組件</span><span class="sxs-lookup"><span data-stu-id="e1016-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e1016-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="e1016-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1016-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1016-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1016-126">**IWMPDVD 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="e1016-126">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





