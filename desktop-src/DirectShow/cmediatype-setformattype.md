---
description: SetFormatType 方法會指定格式類型。
ms.assetid: e8ed9190-7169-4d51-ace7-597f43ff083e
title: 'CMediaType. SetFormatType 方法 (Mtype .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.SetFormatType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7843c5a9788545909ef4297accfa342c08b71e88
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984767"
---
# <a name="cmediatypesetformattype-method"></a><span data-ttu-id="703a8-103">CMediaType. SetFormatType 方法</span><span class="sxs-lookup"><span data-stu-id="703a8-103">CMediaType.SetFormatType method</span></span>

<span data-ttu-id="703a8-104">' ' SetFormatType 方法會指定格式類型。</span><span class="sxs-lookup"><span data-stu-id="703a8-104">The \`\`SetFormatType method specifies the format type.</span></span>

## <a name="syntax"></a><span data-ttu-id="703a8-105">語法</span><span class="sxs-lookup"><span data-stu-id="703a8-105">Syntax</span></span>


```C++
void SetFormatType(
   const GUID *pformattype
);
```



## <a name="parameters"></a><span data-ttu-id="703a8-106">參數</span><span class="sxs-lookup"><span data-stu-id="703a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="703a8-107">*pformattype*</span><span class="sxs-lookup"><span data-stu-id="703a8-107">*pformattype*</span></span> 
</dt> <dd>

<span data-ttu-id="703a8-108">指定格式類型之 **GUID** 的指標。</span><span class="sxs-lookup"><span data-stu-id="703a8-108">Pointer to a **GUID** that specifies the format type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="703a8-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="703a8-109">Return value</span></span>

<span data-ttu-id="703a8-110">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="703a8-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="703a8-111">備註</span><span class="sxs-lookup"><span data-stu-id="703a8-111">Remarks</span></span>

<span data-ttu-id="703a8-112">這個方法會設定 **formattype** 成員。</span><span class="sxs-lookup"><span data-stu-id="703a8-112">This method sets the **formattype** member.</span></span> <span data-ttu-id="703a8-113">格式類型會定義格式區塊的版面配置。</span><span class="sxs-lookup"><span data-stu-id="703a8-113">The format type defines the layout of the format block.</span></span> <span data-ttu-id="703a8-114">例如，如果格式類型為 \_ VIDEOINFO 格式，則格式區塊應該包含 **VIDEOINFOHEADER** 結構。</span><span class="sxs-lookup"><span data-stu-id="703a8-114">For example, if the format type is FORMAT\_VideoInfo, the format block should contain a **VIDEOINFOHEADER** structure.</span></span> <span data-ttu-id="703a8-115">若要設定格式區塊，請呼叫 [**CMediaType：： SetFormat**](cmediatype-setformat.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="703a8-115">To set the format block, call the [**CMediaType::SetFormat**](cmediatype-setformat.md) method.</span></span> <span data-ttu-id="703a8-116">呼叫端負責確定格式區塊符合格式類型。</span><span class="sxs-lookup"><span data-stu-id="703a8-116">The caller is responsible for making sure that the format block matches the format type.</span></span>

## <a name="requirements"></a><span data-ttu-id="703a8-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="703a8-117">Requirements</span></span>



| <span data-ttu-id="703a8-118">需求</span><span class="sxs-lookup"><span data-stu-id="703a8-118">Requirement</span></span> | <span data-ttu-id="703a8-119">值</span><span class="sxs-lookup"><span data-stu-id="703a8-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="703a8-120">標頭</span><span class="sxs-lookup"><span data-stu-id="703a8-120">Header</span></span><br/>  | <dl> <span data-ttu-id="703a8-121"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="703a8-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="703a8-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="703a8-122">Library</span></span><br/> | <dl> <span data-ttu-id="703a8-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="703a8-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="703a8-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="703a8-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="703a8-125">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="703a8-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 


``
