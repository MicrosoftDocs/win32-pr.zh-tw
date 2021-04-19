---
description: = 運算子會指派新的參考時間。
ms.assetid: 0b11e2ea-23dc-4c75-88c6-94215a4b14b6
title: 'CRefTime： operator = 方法 (Reftime .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b87e6517946c64cb2a60e95912aba423a1880215
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998663"
---
# <a name="creftimeoperator-method-reftimeh"></a><span data-ttu-id="d265a-103">CRefTime： operator = 方法 (Reftime .h) </span><span class="sxs-lookup"><span data-stu-id="d265a-103">CRefTime.operator= method (Reftime.h)</span></span>

<span data-ttu-id="d265a-104">= 運算子會指派新的參考時間。</span><span class="sxs-lookup"><span data-stu-id="d265a-104">The = operator assigns a new reference time.</span></span>

## <a name="syntax"></a><span data-ttu-id="d265a-105">語法</span><span class="sxs-lookup"><span data-stu-id="d265a-105">Syntax</span></span>


```C++
CRefTime& operator=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="d265a-106">參數</span><span class="sxs-lookup"><span data-stu-id="d265a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d265a-107">*rt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="d265a-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="d265a-108">**CRefTime** 物件的參考，該物件會指定新的參考時間。</span><span class="sxs-lookup"><span data-stu-id="d265a-108">Reference to a **CRefTime** object that specifies the new reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d265a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="d265a-109">Return value</span></span>

<span data-ttu-id="d265a-110">傳回物件的參考。</span><span class="sxs-lookup"><span data-stu-id="d265a-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d265a-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d265a-111">Requirements</span></span>



| <span data-ttu-id="d265a-112">需求</span><span class="sxs-lookup"><span data-stu-id="d265a-112">Requirement</span></span> | <span data-ttu-id="d265a-113">值</span><span class="sxs-lookup"><span data-stu-id="d265a-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d265a-114">標頭</span><span class="sxs-lookup"><span data-stu-id="d265a-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d265a-115"><dt>Reftime (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d265a-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d265a-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="d265a-116">Library</span></span><br/> | <dl> <span data-ttu-id="d265a-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d265a-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




