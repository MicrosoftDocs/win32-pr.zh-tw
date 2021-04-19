---
description: + = 運算子會新增兩個參考時間。
ms.assetid: 016d3dac-4d7c-490a-83aa-1d88a2080748
title: 'CRefTime. operator + = 方法 (Reftime .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime.operator+=
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b5e0d9a5a16a963b67643823e5e3b547a1076fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000453"
---
# <a name="creftimeoperator-method"></a><span data-ttu-id="39eea-103">CRefTime. operator + = 方法</span><span class="sxs-lookup"><span data-stu-id="39eea-103">CRefTime.operator+= method</span></span>

<span data-ttu-id="39eea-104">+ = 運算子會新增兩個參考時間。</span><span class="sxs-lookup"><span data-stu-id="39eea-104">The += operator adds two reference times.</span></span>

## <a name="syntax"></a><span data-ttu-id="39eea-105">語法</span><span class="sxs-lookup"><span data-stu-id="39eea-105">Syntax</span></span>


```C++
CRefTime& operator+=(
  [ref] const CRefTime &rt
);
```



## <a name="parameters"></a><span data-ttu-id="39eea-106">參數</span><span class="sxs-lookup"><span data-stu-id="39eea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39eea-107">*rt* \[裁判\]</span><span class="sxs-lookup"><span data-stu-id="39eea-107">*rt* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="39eea-108">**CRefTime** 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="39eea-108">Reference to a **CRefTime** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39eea-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="39eea-109">Return value</span></span>

<span data-ttu-id="39eea-110">傳回物件的參考。</span><span class="sxs-lookup"><span data-stu-id="39eea-110">Returns a reference to the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="39eea-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="39eea-111">Requirements</span></span>



| <span data-ttu-id="39eea-112">需求</span><span class="sxs-lookup"><span data-stu-id="39eea-112">Requirement</span></span> | <span data-ttu-id="39eea-113">值</span><span class="sxs-lookup"><span data-stu-id="39eea-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39eea-114">標頭</span><span class="sxs-lookup"><span data-stu-id="39eea-114">Header</span></span><br/>  | <dl> <span data-ttu-id="39eea-115"><dt>Reftime (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="39eea-115"><dt>Reftime.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="39eea-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="39eea-116">Library</span></span><br/> | <dl> <span data-ttu-id="39eea-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="39eea-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




