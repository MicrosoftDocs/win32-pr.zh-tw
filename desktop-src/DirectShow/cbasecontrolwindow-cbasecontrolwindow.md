---
description: CBaseControlWindow。 CBaseControlWindow 函式-函數方法。
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
ms.openlocfilehash: 47c8277a76dbf0fbb9e05262eea5b419466044cc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096336"
---
# <a name="cbasecontrolwindowcbasecontrolwindow-constructor"></a><span data-ttu-id="1d9df-103">CBaseControlWindow. CBaseControlWindow 函數</span><span class="sxs-lookup"><span data-stu-id="1d9df-103">CBaseControlWindow.CBaseControlWindow constructor</span></span>

<span data-ttu-id="1d9df-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="1d9df-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d9df-105">語法</span><span class="sxs-lookup"><span data-stu-id="1d9df-105">Syntax</span></span>


```C++
CBaseControlWindow(
   CBaseMediaFilter *pFilter,
   CCritSec         *pInterfaceLock,
   TCHAR            *pName,
   LPUNKNOWN        pUnk,
   HRESULT          *phr
);
```



## <a name="parameters"></a><span data-ttu-id="1d9df-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d9df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d9df-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="1d9df-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="1d9df-108">擁有媒體篩選物件的指標。</span><span class="sxs-lookup"><span data-stu-id="1d9df-108">Pointer to the owning media filter object.</span></span>

</dd> <dt>

<span data-ttu-id="1d9df-109">*pInterfaceLock*</span><span class="sxs-lookup"><span data-stu-id="1d9df-109">*pInterfaceLock*</span></span> 
</dt> <dd>

<span data-ttu-id="1d9df-110">要用於鎖定的重要區段指標。</span><span class="sxs-lookup"><span data-stu-id="1d9df-110">Pointer to the critical section to use for locking.</span></span>

</dd> <dt>

<span data-ttu-id="1d9df-111">*pName*</span><span class="sxs-lookup"><span data-stu-id="1d9df-111">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="1d9df-112">物件描述的指標。</span><span class="sxs-lookup"><span data-stu-id="1d9df-112">Pointer to the object description.</span></span>

</dd> <dt>

<span data-ttu-id="1d9df-113">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="1d9df-113">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="1d9df-114">如果物件是匯總的一部分，則為控制 **IUnknown** 介面的指標;否則，必須是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1d9df-114">Pointer to the controlling **IUnknown** interface, if the object is part of an aggregate; otherwise, must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1d9df-115">*phr*</span><span class="sxs-lookup"><span data-stu-id="1d9df-115">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1d9df-116">變數的指標，此變數會接收 HRESULT 值，指出函式方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="1d9df-116">Pointer to a variable that receives an HRESULT value indicating the success or failure of the constructor method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d9df-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d9df-117">Requirements</span></span>



| <span data-ttu-id="1d9df-118">需求</span><span class="sxs-lookup"><span data-stu-id="1d9df-118">Requirement</span></span> | <span data-ttu-id="1d9df-119">值</span><span class="sxs-lookup"><span data-stu-id="1d9df-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d9df-120">標頭</span><span class="sxs-lookup"><span data-stu-id="1d9df-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1d9df-121"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1d9df-121"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1d9df-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="1d9df-122">Library</span></span><br/> | <dl> <span data-ttu-id="1d9df-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1d9df-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d9df-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d9df-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d9df-125">**CBaseControlWindow 類別**</span><span class="sxs-lookup"><span data-stu-id="1d9df-125">**CBaseControlWindow Class**</span></span>](cbasecontrolwindow.md)
</dt> </dl>

 

 




