---
description: 提供舊樣式多媒體格式 DWORD 型別和 GUID 子類型之間對應的方法。 這個方法會使用 ' Fourcc ' 參數。
ms.assetid: 35344aae-ed87-4e5e-8824-84f5482b332e
title: FOURCCMap：： FOURCCMap (Fourcc .h) -Fourcc 參數
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
ms.openlocfilehash: cbcd5e8a7c37d3265f508ac7632ffd4b18c8a00f
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106983939"
---
# <a name="fourccmapfourccmap-constructor-fourcch---fourcc-parameter"></a><span data-ttu-id="26f02-104">FOURCCMap：： FOURCCMap (Fourcc .h) -Fourcc 參數</span><span class="sxs-lookup"><span data-stu-id="26f02-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - Fourcc parameter</span></span>

<span data-ttu-id="26f02-105">函式方法。</span><span class="sxs-lookup"><span data-stu-id="26f02-105">Constructor method.</span></span> <span data-ttu-id="26f02-106">建構會提供舊樣式的多媒體格式 **DWORD** 類型與 **GUID** 子類型之間的對應。</span><span class="sxs-lookup"><span data-stu-id="26f02-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f02-107">語法</span><span class="sxs-lookup"><span data-stu-id="26f02-107">Syntax</span></span>


```C++
FOURCCMap(
   DWORD Fourcc
);
```



## <a name="parameters"></a><span data-ttu-id="26f02-108">參數</span><span class="sxs-lookup"><span data-stu-id="26f02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f02-109">*Fourcc*</span><span class="sxs-lookup"><span data-stu-id="26f02-109">*Fourcc*</span></span> 
</dt> <dd>

<span data-ttu-id="26f02-110">指定 FOURCC 的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="26f02-110">**DWORD** that specifies the FOURCC.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26f02-111">備註</span><span class="sxs-lookup"><span data-stu-id="26f02-111">Remarks</span></span>

<span data-ttu-id="26f02-112">如果使用 **FOURCC** 程式碼來建立此物件，則會建立 **GUID** 以與其相符。</span><span class="sxs-lookup"><span data-stu-id="26f02-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="26f02-113">如果此物件是使用現有的 **GUID** 建立的，則物件的 **FOURCC** 值會設定為零。</span><span class="sxs-lookup"><span data-stu-id="26f02-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="26f02-114">之後，您可以分別使用 [**SetFOURCC**](fourccmap-setfourcc.md)和 [**GetFOURCC**](fourccmap-getfourcc.md)成員函式來設定或取出 **FOURCC** 值。</span><span class="sxs-lookup"><span data-stu-id="26f02-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="26f02-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="26f02-115">Requirements</span></span>

| <span data-ttu-id="26f02-116">需求</span><span class="sxs-lookup"><span data-stu-id="26f02-116">Requirement</span></span> | <span data-ttu-id="26f02-117">值</span><span class="sxs-lookup"><span data-stu-id="26f02-117">Value</span></span> |
|-|-|
| <span data-ttu-id="26f02-118">標頭</span><span class="sxs-lookup"><span data-stu-id="26f02-118">Header</span></span>  | <span data-ttu-id="26f02-119">Fourcc (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="26f02-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="26f02-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="26f02-120">Library</span></span> | <span data-ttu-id="26f02-121"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="26f02-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="26f02-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26f02-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f02-123">**FOURCCMap 類別**</span><span class="sxs-lookup"><span data-stu-id="26f02-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




