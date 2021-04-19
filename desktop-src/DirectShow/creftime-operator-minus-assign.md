---
description: -= 運算子會減去另一個參考時間。
ms.assetid: 5b0ec72e-87d8-4562-96b1-40e4f5036fd4
title: 'CRefTime. operator-= 方法 (Reftime .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator-=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bf66abe11d5c61edbb70118020d882c82b08847
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998853"
---
# <a name="creftimeoperator--method"></a><span data-ttu-id="4d203-103">CRefTime. operator-= 方法</span><span class="sxs-lookup"><span data-stu-id="4d203-103">CRefTime.operator-= method</span></span>

<span data-ttu-id="4d203-104">-= 運算子會減去另一個參考時間。</span><span class="sxs-lookup"><span data-stu-id="4d203-104">The -= operator subtracts one reference time from another.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d203-105">語法</span><span class="sxs-lookup"><span data-stu-id="4d203-105">Syntax</span></span>


```C++
CRefTime& operator-=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="4d203-106">參數</span><span class="sxs-lookup"><span data-stu-id="4d203-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d203-107">*rt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="4d203-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="4d203-108">**CRefTime** 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="4d203-108">Reference to a **CRefTime** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d203-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d203-109">Return value</span></span>

<span data-ttu-id="4d203-110">傳回物件的參考。</span><span class="sxs-lookup"><span data-stu-id="4d203-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d203-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d203-111">Requirements</span></span>



| <span data-ttu-id="4d203-112">需求</span><span class="sxs-lookup"><span data-stu-id="4d203-112">Requirement</span></span> | <span data-ttu-id="4d203-113">值</span><span class="sxs-lookup"><span data-stu-id="4d203-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d203-114">標頭</span><span class="sxs-lookup"><span data-stu-id="4d203-114">Header</span></span><br/>  | <dl> <span data-ttu-id="4d203-115"><dt>Reftime (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="4d203-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4d203-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="4d203-116">Library</span></span><br/> | <dl> <span data-ttu-id="4d203-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="4d203-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




