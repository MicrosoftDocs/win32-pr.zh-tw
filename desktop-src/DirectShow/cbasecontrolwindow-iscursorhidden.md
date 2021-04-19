---
description: IsCursorHidden 方法會抓取 m \_ bCursorHidden 資料成員的目前狀態。
ms.assetid: 4b97b89d-876a-470c-ac41-a88fecb52b2d
title: 'CBaseControlWindow. IsCursorHidden 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsCursorHidden
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 90f02c6cac5fb3ef1edeaa8e03f7bc54a03acb49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996514"
---
# <a name="cbasecontrolwindowiscursorhidden-method"></a><span data-ttu-id="35837-103">CBaseControlWindow. IsCursorHidden 方法</span><span class="sxs-lookup"><span data-stu-id="35837-103">CBaseControlWindow.IsCursorHidden method</span></span>

<span data-ttu-id="35837-104">方法會抓取 `IsCursorHidden` **m \_ bCursorHidden** 資料成員的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="35837-104">The `IsCursorHidden` method retrieves the current state of the **m\_bCursorHidden** data member.</span></span>

## <a name="syntax"></a><span data-ttu-id="35837-105">語法</span><span class="sxs-lookup"><span data-stu-id="35837-105">Syntax</span></span>


```C++
HRESULT IsCursorHidden(
   long *CursorHidden
);
```



## <a name="parameters"></a><span data-ttu-id="35837-106">參數</span><span class="sxs-lookup"><span data-stu-id="35837-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35837-107">*CursorHidden*</span><span class="sxs-lookup"><span data-stu-id="35837-107">*CursorHidden*</span></span> 
</dt> <dd>

<span data-ttu-id="35837-108">**M \_ bCursorHidden** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="35837-108">Pointer to the value of **m\_bCursorHidden**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35837-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="35837-109">Return value</span></span>

<span data-ttu-id="35837-110">未使用參數呼叫時，如果資料指標是隱藏的，則會傳回 OATRUE，如果資料指標是可見的，則會傳回 OAFALSE。</span><span class="sxs-lookup"><span data-stu-id="35837-110">When called without a parameter, returns OATRUE if the cursor is hidden, or OAFALSE if the cursor is visible.</span></span>

## <a name="remarks"></a><span data-ttu-id="35837-111">備註</span><span class="sxs-lookup"><span data-stu-id="35837-111">Remarks</span></span>

<span data-ttu-id="35837-112">內建物件應該在沒有 *CursorHidden* 參數的情況下呼叫此成員函式，以避免鎖定重要區段。</span><span class="sxs-lookup"><span data-stu-id="35837-112">Internal objects should call this member function without the *CursorHidden* parameter to avoid locking the critical section.</span></span> <span data-ttu-id="35837-113">外部物件會透過 [**IVideoWindow：： IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden)方法，使用 *CursorHidden* 參數存取這個成員函式。</span><span class="sxs-lookup"><span data-stu-id="35837-113">External objects access this member function with the *CursorHidden* parameter through the [**IVideoWindow::IsCursorHidden**](/windows/desktop/api/Control/nf-control-ivideowindow-iscursorhidden) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="35837-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="35837-114">Requirements</span></span>



| <span data-ttu-id="35837-115">需求</span><span class="sxs-lookup"><span data-stu-id="35837-115">Requirement</span></span> | <span data-ttu-id="35837-116">值</span><span class="sxs-lookup"><span data-stu-id="35837-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35837-117">標頭</span><span class="sxs-lookup"><span data-stu-id="35837-117">Header</span></span><br/>  | <dl> <span data-ttu-id="35837-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="35837-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="35837-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="35837-119">Library</span></span><br/> | <dl> <span data-ttu-id="35837-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="35837-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35837-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35837-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35837-122">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="35837-122">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




