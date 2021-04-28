---
description: CTransformOutputPin。 CTransformOutputPin 函式-函數方法。
ms.assetid: 6213ce92-d98a-4fb6-b66c-e7cdea6dff0d
title: 'CTransformOutputPin. CTransformOutputPin (Transfrm. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1f7cb9dd811c878eba258a6087e00a85d4c24a0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084866"
---
# <a name="ctransformoutputpinctransformoutputpin-constructor"></a><span data-ttu-id="dcb2c-103">CTransformOutputPin. CTransformOutputPin 函數</span><span class="sxs-lookup"><span data-stu-id="dcb2c-103">CTransformOutputPin.CTransformOutputPin constructor</span></span>

<span data-ttu-id="dcb2c-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="dcb2c-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcb2c-105">語法</span><span class="sxs-lookup"><span data-stu-id="dcb2c-105">Syntax</span></span>


```C++
CTransformOutputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a><span data-ttu-id="dcb2c-106">參數</span><span class="sxs-lookup"><span data-stu-id="dcb2c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcb2c-107">*pObjectName*</span><span class="sxs-lookup"><span data-stu-id="dcb2c-107">*pObjectName*</span></span> 
</dt> <dd>

<span data-ttu-id="dcb2c-108">包含物件之偵錯工具名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="dcb2c-108">String containing the debug name of the object.</span></span> <span data-ttu-id="dcb2c-109">如需詳細資訊，請參閱 [**CBaseObject**](cbaseobject.md)。</span><span class="sxs-lookup"><span data-stu-id="dcb2c-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="dcb2c-110">*pTransformFilter*</span><span class="sxs-lookup"><span data-stu-id="dcb2c-110">*pTransformFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="dcb2c-111">建立此 pin 之篩選準則的指標，其必須是 [**CTransformFilter**](ctransformfilter.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="dcb2c-111">Pointer to the filter that created this pin, which must be a [**CTransformFilter**](ctransformfilter.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="dcb2c-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="dcb2c-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="dcb2c-113">變數的指標，此變數會接收 **HRESULT** 值，指出方法的成功或失敗。</span><span class="sxs-lookup"><span data-stu-id="dcb2c-113">Pointer to a variable that receives an **HRESULT** value indicating the success or failure of the method.</span></span> <span data-ttu-id="dcb2c-114">在建立物件之前，將值初始化為「 \_ 確定」。</span><span class="sxs-lookup"><span data-stu-id="dcb2c-114">Initialize the value to S\_OK before creating the object.</span></span> <span data-ttu-id="dcb2c-115">只有在發生錯誤時，才會變更此值。</span><span class="sxs-lookup"><span data-stu-id="dcb2c-115">The value is changed only if an error occurs.</span></span>

</dd> <dt>

<span data-ttu-id="dcb2c-116">*pName*</span><span class="sxs-lookup"><span data-stu-id="dcb2c-116">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="dcb2c-117">包含 pin 名稱的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="dcb2c-117">Wide-character string containing the pin name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcb2c-118">備註</span><span class="sxs-lookup"><span data-stu-id="dcb2c-118">Remarks</span></span>

<span data-ttu-id="dcb2c-119">*PName* 參數會指定 [**IPin：： QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo)方法所傳回的 pin 名稱。</span><span class="sxs-lookup"><span data-stu-id="dcb2c-119">The *pName* parameter specifies the pin name, which is returned by the [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) method.</span></span> <span data-ttu-id="dcb2c-120">不過，此字串不會用於 pin 識別碼。</span><span class="sxs-lookup"><span data-stu-id="dcb2c-120">However, the string is not used for the pin identifier.</span></span> <span data-ttu-id="dcb2c-121">此類別的 pin 識別碼一律為 "Out"。</span><span class="sxs-lookup"><span data-stu-id="dcb2c-121">The pin identifier for this class is always "Out".</span></span> <span data-ttu-id="dcb2c-122">如需詳細資訊，請參閱 [**QueryId**](ctransformoutputpin-queryid.md)。</span><span class="sxs-lookup"><span data-stu-id="dcb2c-122">For more information, see [**QueryId**](ctransformoutputpin-queryid.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dcb2c-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcb2c-123">Requirements</span></span>



| <span data-ttu-id="dcb2c-124">需求</span><span class="sxs-lookup"><span data-stu-id="dcb2c-124">Requirement</span></span> | <span data-ttu-id="dcb2c-125">值</span><span class="sxs-lookup"><span data-stu-id="dcb2c-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb2c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="dcb2c-126">Header</span></span><br/>  | <dl> <span data-ttu-id="dcb2c-127"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="dcb2c-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="dcb2c-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="dcb2c-128">Library</span></span><br/> | <dl> <span data-ttu-id="dcb2c-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="dcb2c-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




