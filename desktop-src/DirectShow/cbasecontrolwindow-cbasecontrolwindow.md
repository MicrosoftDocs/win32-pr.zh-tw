---
description: 函式方法。
ms.assetid: 575f7f94-5f55-4834-bdb6-0db877187388
title: 'CBaseControlWindow. CBaseControlWindow (Ctlutil. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.CBaseControlWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9eb3e50daef8ec4ad11bf96a8f0b605f4c8fe679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990136"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a><span data-ttu-id="351ae-103">CBaseControlWindow. CBaseControlWindow 函數</span><span class="sxs-lookup"><span data-stu-id="351ae-103">CBaseControlWindow.CBaseControlWindow constructor</span></span>

<span data-ttu-id="351ae-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="351ae-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="351ae-105">語法</span><span class="sxs-lookup"><span data-stu-id="351ae-105">Syntax</span></span>


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a><span data-ttu-id="351ae-106">參數</span><span class="sxs-lookup"><span data-stu-id="351ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="351ae-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="351ae-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="351ae-108">擁有媒體篩選物件的指標。</span><span class="sxs-lookup"><span data-stu-id="351ae-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="351ae-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="351ae-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="351ae-110">要用於鎖定的重要區段指標。</span><span class="sxs-lookup"><span data-stu-id="351ae-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="351ae-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="351ae-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="351ae-112">物件描述的指標。</span><span class="sxs-lookup"><span data-stu-id="351ae-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="351ae-113">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="351ae-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="351ae-114">如果物件是匯總的一部分，則為控制 **IUnknown** 介面的指標;否則，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="351ae-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="351ae-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="351ae-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="351ae-116">變數的指標，此變數會接收 HRESULT 值，指出函式方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="351ae-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="351ae-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="351ae-117">Requirements</span></span>



| <span data-ttu-id="351ae-118">需求</span><span class="sxs-lookup"><span data-stu-id="351ae-118">Requirement</span></span> | <span data-ttu-id="351ae-119">值</span><span class="sxs-lookup"><span data-stu-id="351ae-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="351ae-120">標頭</span><span class="sxs-lookup"><span data-stu-id="351ae-120">Header</span></span><br/>  | <dl> <span data-ttu-id="351ae-121"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="351ae-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="351ae-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="351ae-122">Library</span></span><br/> | <dl> <span data-ttu-id="351ae-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="351ae-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="351ae-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="351ae-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="351ae-125">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="351ae-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




