---
description: GetClassID 方法會捕獲類別識別碼。 這個方法會實 IPersist：： GetClassID 方法。
ms.assetid: 95038b11-b56f-4ab9-aefa-4735651c3731
title: 'CBaseMediaFilter. GetClassID 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dafacba684711c5c04a155d2609e0bc68450fa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995632"
---
# <a name="cbasemediafiltergetclassid-method"></a><span data-ttu-id="12e2c-104">CBaseMediaFilter. GetClassID 方法</span><span class="sxs-lookup"><span data-stu-id="12e2c-104">CBaseMediaFilter.GetClassID method</span></span>

<span data-ttu-id="12e2c-105">`GetClassID`方法會捕獲類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="12e2c-105">The `GetClassID` method retrieves the class identifier.</span></span> <span data-ttu-id="12e2c-106">這個方法會實 **IPersist：： GetClassID** 方法。</span><span class="sxs-lookup"><span data-stu-id="12e2c-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="12e2c-107">語法</span><span class="sxs-lookup"><span data-stu-id="12e2c-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="12e2c-108">參數</span><span class="sxs-lookup"><span data-stu-id="12e2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12e2c-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="12e2c-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="12e2c-110">接收類別識別碼之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="12e2c-110">Pointer to a variable that receives the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12e2c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="12e2c-111">Return value</span></span>

<span data-ttu-id="12e2c-112">傳回 S \_ OK 或 E \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="12e2c-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="12e2c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="12e2c-113">Requirements</span></span>



| <span data-ttu-id="12e2c-114">需求</span><span class="sxs-lookup"><span data-stu-id="12e2c-114">Requirement</span></span> | <span data-ttu-id="12e2c-115">值</span><span class="sxs-lookup"><span data-stu-id="12e2c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12e2c-116">標頭</span><span class="sxs-lookup"><span data-stu-id="12e2c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="12e2c-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="12e2c-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="12e2c-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="12e2c-118">Library</span></span><br/> | <dl> <span data-ttu-id="12e2c-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="12e2c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12e2c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12e2c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e2c-121">**CBaseMediaFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="12e2c-121">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




