---
description: CMediaType. CMediaType (Mtype. h) -函式方法。
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: CMediaType. CMediaType (Mtype. h) -cmtype 和 phr 參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dd91252920c74d45e4218be3c3d03249a116bfcf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095416"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a><span data-ttu-id="345a6-103">CMediaType. CMediaType (Mtype. h) </span><span class="sxs-lookup"><span data-stu-id="345a6-103">CMediaType.CMediaType constructor (Mtype.h)</span></span>

<span data-ttu-id="345a6-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="345a6-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="345a6-105">語法</span><span class="sxs-lookup"><span data-stu-id="345a6-105">Syntax</span></span>


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="345a6-106">參數</span><span class="sxs-lookup"><span data-stu-id="345a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="345a6-107">*cmtype* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="345a6-107">*cmtype* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="345a6-108">物件的參考 `CMediaType` 。</span><span class="sxs-lookup"><span data-stu-id="345a6-108">Reference to a `CMediaType` object.</span></span> <span data-ttu-id="345a6-109">此函式會將媒體類型複製到新的物件，包括格式區塊（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="345a6-109">The constructor copies the media type to the new object, including the format block, if any.</span></span>

</dd> <dt>

<span data-ttu-id="345a6-110">*phr*</span><span class="sxs-lookup"><span data-stu-id="345a6-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="345a6-111">接收 HRESULT 值之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="345a6-111">Pointer to a variable that receives an HRESULT value.</span></span> <span data-ttu-id="345a6-112">這個參數可以是 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="345a6-112">This parameter can be a **NULL** pointer.</span></span> <span data-ttu-id="345a6-113">否則，呼叫端必須在呼叫此函式之前，將值設定為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="345a6-113">Otherwise, the caller must set the value to S\_OK before calling the constructor.</span></span> <span data-ttu-id="345a6-114">如果此函式失敗，則會將值設定為失敗碼。</span><span class="sxs-lookup"><span data-stu-id="345a6-114">If the constructor fails, it sets the value to a failure code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="345a6-115">備註</span><span class="sxs-lookup"><span data-stu-id="345a6-115">Remarks</span></span>

<span data-ttu-id="345a6-116">此函式會呼叫 [**CMediaType：： InitMediaType**](cmediatype-initmediatype.md) 方法來初始化媒體類型。</span><span class="sxs-lookup"><span data-stu-id="345a6-116">The constructor calls the [**CMediaType::InitMediaType**](cmediatype-initmediatype.md) method to initialize the media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="345a6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="345a6-117">Requirements</span></span>



| <span data-ttu-id="345a6-118">需求</span><span class="sxs-lookup"><span data-stu-id="345a6-118">Requirement</span></span> | <span data-ttu-id="345a6-119">值</span><span class="sxs-lookup"><span data-stu-id="345a6-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="345a6-120">標頭</span><span class="sxs-lookup"><span data-stu-id="345a6-120">Header</span></span><br/>  | <dl> <span data-ttu-id="345a6-121"><dt>Mtype (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="345a6-121"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="345a6-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="345a6-122">Library</span></span><br/> | <dl> <span data-ttu-id="345a6-123"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="345a6-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="345a6-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="345a6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345a6-125">**CMediaType 類別**</span><span class="sxs-lookup"><span data-stu-id="345a6-125">**CMediaType Class**</span></span>](cmediatype.md)
</dt> </dl>

 

 




