---
description: InactivateWindow 方法會會視窗。 在基類中，這個方法會隱藏視窗。
ms.assetid: b575d4fd-dee1-4ae5-abb4-e92ae361e82a
title: 'CBaseWindow. InactivateWindow 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.InactivateWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d1c5e925a3d9b510918636a221d5ad6e1b7da736
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990211"
---
# <a name="cbasewindowinactivatewindow-method"></a><span data-ttu-id="dc59c-104">CBaseWindow. InactivateWindow 方法</span><span class="sxs-lookup"><span data-stu-id="dc59c-104">CBaseWindow.InactivateWindow method</span></span>

<span data-ttu-id="dc59c-105">`InactivateWindow`方法會會視窗。</span><span class="sxs-lookup"><span data-stu-id="dc59c-105">The `InactivateWindow` method inactivates the window.</span></span> <span data-ttu-id="dc59c-106">在基類中，這個方法會隱藏視窗。</span><span class="sxs-lookup"><span data-stu-id="dc59c-106">In the base class, this method hides the window.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc59c-107">語法</span><span class="sxs-lookup"><span data-stu-id="dc59c-107">Syntax</span></span>


```C++
virtual HRESULT InactivateWindow();
```



## <a name="parameters"></a><span data-ttu-id="dc59c-108">參數</span><span class="sxs-lookup"><span data-stu-id="dc59c-108">Parameters</span></span>

<span data-ttu-id="dc59c-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="dc59c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dc59c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="dc59c-110">Return value</span></span>

<span data-ttu-id="dc59c-111">傳回下表所示的其中一個 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="dc59c-111">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="dc59c-112">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dc59c-112">Return code</span></span>                                                                             | <span data-ttu-id="dc59c-113">Description</span><span class="sxs-lookup"><span data-stu-id="dc59c-113">Description</span></span>                            |
|-----------------------------------------------------------------------------------------|----------------------------------------|
| <dl> <span data-ttu-id="dc59c-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dc59c-114"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="dc59c-115">成功。</span><span class="sxs-lookup"><span data-stu-id="dc59c-115">Success.</span></span><br/>                    |
| <dl> <span data-ttu-id="dc59c-116"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="dc59c-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="dc59c-117">視窗已經處於非使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="dc59c-117">Window is already inactive.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dc59c-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc59c-118">Requirements</span></span>



| <span data-ttu-id="dc59c-119">需求</span><span class="sxs-lookup"><span data-stu-id="dc59c-119">Requirement</span></span> | <span data-ttu-id="dc59c-120">值</span><span class="sxs-lookup"><span data-stu-id="dc59c-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc59c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="dc59c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="dc59c-122"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dc59c-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="dc59c-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="dc59c-123">Library</span></span><br/> | <dl> <span data-ttu-id="dc59c-124"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dc59c-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc59c-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc59c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc59c-126">**CBaseWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="dc59c-126">**CBaseWindow Class**</span></span>](cbasewindow.md)
</dt> </dl>

 

 




