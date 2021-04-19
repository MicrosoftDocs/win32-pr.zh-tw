---
description: GetClassID 方法會捕獲篩選準則的類別識別碼。 這個方法會實 IPersist：： GetClassID 方法。
ms.assetid: c3a8b6ab-b36f-493e-9436-6784e25e2511
title: 'CBaseFilter. GetClassID 方法 (Amfilter .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetClassID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 02dfe8452da6366454dcc1cfeeed93c379c89bd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977551"
---
# <a name="cbasefiltergetclassid-method"></a><span data-ttu-id="d4706-104">CBaseFilter. GetClassID 方法</span><span class="sxs-lookup"><span data-stu-id="d4706-104">CBaseFilter.GetClassID method</span></span>

<span data-ttu-id="d4706-105">方法會抓取 `GetClassID` 篩選準則的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4706-105">The `GetClassID` method retrieves the class identifier of the filter.</span></span> <span data-ttu-id="d4706-106">這個方法會實 **IPersist：： GetClassID** 方法。</span><span class="sxs-lookup"><span data-stu-id="d4706-106">This method implements the **IPersist::GetClassID** method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4706-107">語法</span><span class="sxs-lookup"><span data-stu-id="d4706-107">Syntax</span></span>


```C++
HRESULT GetClassID(
   CLSID *pClsID
);
```



## <a name="parameters"></a><span data-ttu-id="d4706-108">參數</span><span class="sxs-lookup"><span data-stu-id="d4706-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4706-109">*pClsID*</span><span class="sxs-lookup"><span data-stu-id="d4706-109">*pClsID*</span></span> 
</dt> <dd>

<span data-ttu-id="d4706-110">接收類別識別碼之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="d4706-110">Pointer to a variable that receives the class identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4706-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4706-111">Return value</span></span>

<span data-ttu-id="d4706-112">傳回 S \_ OK 或 E \_ 指標。</span><span class="sxs-lookup"><span data-stu-id="d4706-112">Returns S\_OK or E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4706-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4706-113">Requirements</span></span>



| <span data-ttu-id="d4706-114">需求</span><span class="sxs-lookup"><span data-stu-id="d4706-114">Requirement</span></span> | <span data-ttu-id="d4706-115">值</span><span class="sxs-lookup"><span data-stu-id="d4706-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4706-116">標頭</span><span class="sxs-lookup"><span data-stu-id="d4706-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d4706-117"><dt>Amfilter (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d4706-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d4706-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="d4706-118">Library</span></span><br/> | <dl> <span data-ttu-id="d4706-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d4706-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4706-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4706-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4706-121">**CBaseFilter 類別**</span><span class="sxs-lookup"><span data-stu-id="d4706-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




