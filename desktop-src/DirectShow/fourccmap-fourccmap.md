---
description: 提供舊樣式多媒體格式 DWORD 型別和 GUID 子類型之間對應的方法。 這個方法不會使用任何參數。
ms.assetid: 2152803c-f45f-43b0-9207-4eaeddf5eeb6
title: FOURCCMap：： FOURCCMap (Fourcc .h) -沒有參數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.FOURCCMap
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd37ac842ab46c0d46fb3db1567d42274a026c47
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106986556"
---
# <a name="fourccmapfourccmap-constructor-fourcch---no-parameters"></a><span data-ttu-id="f9c2c-104">FOURCCMap：： FOURCCMap (Fourcc .h) -沒有參數</span><span class="sxs-lookup"><span data-stu-id="f9c2c-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - No parameters</span></span>

<span data-ttu-id="f9c2c-105">函式方法。</span><span class="sxs-lookup"><span data-stu-id="f9c2c-105">Constructor method.</span></span> <span data-ttu-id="f9c2c-106">建構會提供舊樣式的多媒體格式 **DWORD** 類型與 **GUID** 子類型之間的對應。</span><span class="sxs-lookup"><span data-stu-id="f9c2c-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c2c-107">語法</span><span class="sxs-lookup"><span data-stu-id="f9c2c-107">Syntax</span></span>


```C++
FOURCCMap();
```



## <a name="parameters"></a><span data-ttu-id="f9c2c-108">參數</span><span class="sxs-lookup"><span data-stu-id="f9c2c-108">Parameters</span></span>

<span data-ttu-id="f9c2c-109">這個函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="f9c2c-109">This constructor has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9c2c-110">備註</span><span class="sxs-lookup"><span data-stu-id="f9c2c-110">Remarks</span></span>

<span data-ttu-id="f9c2c-111">如果使用 **FOURCC** 程式碼來建立此物件，則會建立 **GUID** 以與其相符。</span><span class="sxs-lookup"><span data-stu-id="f9c2c-111">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="f9c2c-112">如果此物件是使用現有的 **GUID** 建立的，則物件的 **FOURCC** 值會設定為零。</span><span class="sxs-lookup"><span data-stu-id="f9c2c-112">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="f9c2c-113">之後，您可以分別使用 [**SetFOURCC**](fourccmap-setfourcc.md)和 [**GetFOURCC**](fourccmap-getfourcc.md)成員函式來設定或取出 **FOURCC** 值。</span><span class="sxs-lookup"><span data-stu-id="f9c2c-113">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9c2c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f9c2c-114">Requirements</span></span>


| <span data-ttu-id="f9c2c-115">需求</span><span class="sxs-lookup"><span data-stu-id="f9c2c-115">Requirement</span></span> | <span data-ttu-id="f9c2c-116">值</span><span class="sxs-lookup"><span data-stu-id="f9c2c-116">Value</span></span> |
|-|-|
| <span data-ttu-id="f9c2c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="f9c2c-117">Header</span></span>  | <span data-ttu-id="f9c2c-118">Fourcc (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="f9c2c-118">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="f9c2c-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="f9c2c-119">Library</span></span> | <span data-ttu-id="f9c2c-120"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="f9c2c-120">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |



## <a name="see-also"></a><span data-ttu-id="f9c2c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f9c2c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c2c-122">**FOURCCMap 類別**</span><span class="sxs-lookup"><span data-stu-id="f9c2c-122">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




