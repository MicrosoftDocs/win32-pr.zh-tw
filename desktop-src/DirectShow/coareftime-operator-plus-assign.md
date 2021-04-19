---
description: 這個運算子會新增兩個參考時間，並將此物件設定為結果。
ms.assetid: 6d29014b-0e31-497e-8326-e3fefc022227
title: 'COARefTime. operator + = 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a6a03d9e98c3c2f2ca09c3f90f2cb0867d976e02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999418"
---
# <a name="coareftimeoperator-method"></a><span data-ttu-id="93bb1-103">COARefTime. operator + = 方法</span><span class="sxs-lookup"><span data-stu-id="93bb1-103">COARefTime.operator+= method</span></span>

<span data-ttu-id="93bb1-104">這個運算子會新增兩個參考時間，並將此物件設定為結果。</span><span class="sxs-lookup"><span data-stu-id="93bb1-104">This operator adds two reference times, and sets this object to the result.</span></span>

## <a name="syntax"></a><span data-ttu-id="93bb1-105">語法</span><span class="sxs-lookup"><span data-stu-id="93bb1-105">Syntax</span></span>


```C++
COARefTime& operator+=(
  [ref] const COARefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="93bb1-106">參數</span><span class="sxs-lookup"><span data-stu-id="93bb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93bb1-107">*rt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="93bb1-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="93bb1-108">要加入之 **COARefTime** 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="93bb1-108">Reference to the **COARefTime** object to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93bb1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="93bb1-109">Return value</span></span>

<span data-ttu-id="93bb1-110">傳回物件的參考。</span><span class="sxs-lookup"><span data-stu-id="93bb1-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="93bb1-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="93bb1-111">Requirements</span></span>



| <span data-ttu-id="93bb1-112">需求</span><span class="sxs-lookup"><span data-stu-id="93bb1-112">Requirement</span></span> | <span data-ttu-id="93bb1-113">值</span><span class="sxs-lookup"><span data-stu-id="93bb1-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93bb1-114">標頭</span><span class="sxs-lookup"><span data-stu-id="93bb1-114">Header</span></span><br/>  | <dl> <span data-ttu-id="93bb1-115"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="93bb1-115"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="93bb1-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="93bb1-116">Library</span></span><br/> | <dl> <span data-ttu-id="93bb1-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="93bb1-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93bb1-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93bb1-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93bb1-119">**COARefTime 類別**</span><span class="sxs-lookup"><span data-stu-id="93bb1-119">**COARefTime Class**</span></span>](coareftime.md)
</dt> </dl>

 

 




