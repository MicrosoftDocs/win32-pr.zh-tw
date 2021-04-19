---
description: CheckTransform 方法會檢查輸入媒體類型是否與輸出媒體類型相容。
ms.assetid: 349145e5-c12d-41df-ae37-7846f8aaa423
title: 'CTransformFilter. CheckTransform 方法 (Transfrm .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CheckTransform
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2b3302304e6a0f9df41005f7ed63d9316a3cd410
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995778"
---
# <a name="ctransformfilterchecktransform-method"></a><span data-ttu-id="03e58-103">CTransformFilter. CheckTransform 方法</span><span class="sxs-lookup"><span data-stu-id="03e58-103">CTransformFilter.CheckTransform method</span></span>

<span data-ttu-id="03e58-104">`CheckTransform`方法會檢查輸入媒體類型是否與輸出媒體類型相容。</span><span class="sxs-lookup"><span data-stu-id="03e58-104">The `CheckTransform` method checks whether an input media type is compatible with an output media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="03e58-105">語法</span><span class="sxs-lookup"><span data-stu-id="03e58-105">Syntax</span></span>


```C++
virtual HRESULT CheckTransform(
   const CMediaType *mtIn,
   const CMediaType *mtOut
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="03e58-106">參數</span><span class="sxs-lookup"><span data-stu-id="03e58-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03e58-107">*mtIn*</span><span class="sxs-lookup"><span data-stu-id="03e58-107">*mtIn*</span></span> 
</dt> <dd>

<span data-ttu-id="03e58-108">指定輸入類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="03e58-108">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the input type.</span></span>

</dd> <dt>

<span data-ttu-id="03e58-109">*mtOut*</span><span class="sxs-lookup"><span data-stu-id="03e58-109">*mtOut*</span></span> 
</dt> <dd>

<span data-ttu-id="03e58-110">指定輸出類型之 [**CMediaType**](cmediatype.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="03e58-110">Pointer to a [**CMediaType**](cmediatype.md) object that specifies the output type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03e58-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="03e58-111">Return value</span></span>

<span data-ttu-id="03e58-112">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="03e58-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="03e58-113">可能的值包括下表所示的值。</span><span class="sxs-lookup"><span data-stu-id="03e58-113">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="03e58-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="03e58-114">Return code</span></span>                                                                                                | <span data-ttu-id="03e58-115">Description</span><span class="sxs-lookup"><span data-stu-id="03e58-115">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="03e58-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="03e58-116"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="03e58-117">媒體類型是相容的。</span><span class="sxs-lookup"><span data-stu-id="03e58-117">The media types are compatible.</span></span><br/>     |
| <dl> <span data-ttu-id="03e58-118"><dt>**\_ \_ \_ 未接受 VFW E \_ 類型**</dt></span><span class="sxs-lookup"><span data-stu-id="03e58-118"><dt>**VFW\_E\_TYPE\_NOT\_ACCEPTED**</dt></span></span> </dl> | <span data-ttu-id="03e58-119">媒體類型不相容。</span><span class="sxs-lookup"><span data-stu-id="03e58-119">The media types are not compatible.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="03e58-120">備註</span><span class="sxs-lookup"><span data-stu-id="03e58-120">Remarks</span></span>

<span data-ttu-id="03e58-121">衍生的類別必須執行此方法。</span><span class="sxs-lookup"><span data-stu-id="03e58-121">The derived class must implement this method.</span></span> <span data-ttu-id="03e58-122">\_如果篩選器可以接受兩個指定的媒體類型，則傳回 [確定]，否則傳回錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="03e58-122">Return S\_OK if the filter can accept both of the specified media types, or an error code otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="03e58-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="03e58-123">Requirements</span></span>



| <span data-ttu-id="03e58-124">需求</span><span class="sxs-lookup"><span data-stu-id="03e58-124">Requirement</span></span> | <span data-ttu-id="03e58-125">值</span><span class="sxs-lookup"><span data-stu-id="03e58-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03e58-126">標頭</span><span class="sxs-lookup"><span data-stu-id="03e58-126">Header</span></span><br/>  | <dl> <span data-ttu-id="03e58-127"><dt>Transfrm (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="03e58-127"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="03e58-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="03e58-128">Library</span></span><br/> | <dl> <span data-ttu-id="03e58-129"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="03e58-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




