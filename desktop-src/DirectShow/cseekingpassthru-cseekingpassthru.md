---
description: 函式方法。
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: 'CSeekingPassThru. CSeekingPassThru (Seekpt. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a93ed9706762b9a1672bfae85550ee4c2aceeead
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995601"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a><span data-ttu-id="81928-103">CSeekingPassThru. CSeekingPassThru 函數</span><span class="sxs-lookup"><span data-stu-id="81928-103">CSeekingPassThru.CSeekingPassThru constructor</span></span>

<span data-ttu-id="81928-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="81928-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="81928-105">語法</span><span class="sxs-lookup"><span data-stu-id="81928-105">Syntax</span></span>


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="81928-106">參數</span><span class="sxs-lookup"><span data-stu-id="81928-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81928-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="81928-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="81928-108">包含物件名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="81928-108">String containing the name of the object.</span></span> <span data-ttu-id="81928-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md) 。</span><span class="sxs-lookup"><span data-stu-id="81928-109">See [**CBaseObject**](cbaseobject.md) for more information.</span></span>

</dd> <dt>

<span data-ttu-id="81928-110">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="81928-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="81928-111">這個物件之擁有者的指標。</span><span class="sxs-lookup"><span data-stu-id="81928-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="81928-112">如果物件已匯總，請將指標傳遞至匯總物件的 **IUnknown** 介面。</span><span class="sxs-lookup"><span data-stu-id="81928-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="81928-113">否則，請將此參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="81928-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="81928-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="81928-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="81928-115">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="81928-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="81928-116">忽略。</span><span class="sxs-lookup"><span data-stu-id="81928-116">Ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81928-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="81928-117">Requirements</span></span>



| <span data-ttu-id="81928-118">需求</span><span class="sxs-lookup"><span data-stu-id="81928-118">Requirement</span></span> | <span data-ttu-id="81928-119">值</span><span class="sxs-lookup"><span data-stu-id="81928-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81928-120">標頭</span><span class="sxs-lookup"><span data-stu-id="81928-120">Header</span></span><br/>  | <dl> <span data-ttu-id="81928-121"><dt>Seekpt (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="81928-121"><dt>Seekpt.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="81928-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="81928-122">Library</span></span><br/> | <dl> <span data-ttu-id="81928-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="81928-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81928-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81928-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81928-125">**CSeekingPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="81928-125">**CSeekingPassThru Class**</span></span>](cseekingpassthru.md)
</dt> </dl>

 

 




