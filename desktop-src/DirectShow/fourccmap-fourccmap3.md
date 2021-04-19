---
description: 提供舊樣式多媒體格式 DWORD 型別和 GUID 子類型之間對應的方法。 這個方法會使用 ' pguid ' 參數。
ms.assetid: 4de6cb49-938e-42f8-8687-dc60a0f23e87
title: FOURCCMap：： FOURCCMap (Fourcc .h) -pguid 參數
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
ms.openlocfilehash: 3e36f0ea58c99930d4c6c2e0929f27a43184c6be
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/19/2021
ms.locfileid: "106986557"
---
# <a name="fourccmapfourccmap-constructor-fourcch---pguid-parameter"></a><span data-ttu-id="31ff0-104">FOURCCMap：： FOURCCMap (Fourcc .h) -pguid 參數</span><span class="sxs-lookup"><span data-stu-id="31ff0-104">FOURCCMap::FOURCCMap constructor (Fourcc.h) - pguid parameter</span></span>

<span data-ttu-id="31ff0-105">函式方法。</span><span class="sxs-lookup"><span data-stu-id="31ff0-105">Constructor method.</span></span> <span data-ttu-id="31ff0-106">建構會提供舊樣式的多媒體格式 **DWORD** 類型與 **GUID** 子類型之間的對應。</span><span class="sxs-lookup"><span data-stu-id="31ff0-106">The constuctor provides the mapping between old-style multimedia format **DWORD** types and **GUID** subtypes.</span></span>

## <a name="syntax"></a><span data-ttu-id="31ff0-107">語法</span><span class="sxs-lookup"><span data-stu-id="31ff0-107">Syntax</span></span>


```C++
FOURCCMap(
   const GUID *pguid
);
```



## <a name="parameters"></a><span data-ttu-id="31ff0-108">參數</span><span class="sxs-lookup"><span data-stu-id="31ff0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31ff0-109">*pguid*</span><span class="sxs-lookup"><span data-stu-id="31ff0-109">*pguid*</span></span> 
</dt> <dd>

<span data-ttu-id="31ff0-110">全域唯一識別碼 (**GUID**) 的指標。</span><span class="sxs-lookup"><span data-stu-id="31ff0-110">Pointer to the globally unique identifier (**GUID**).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31ff0-111">備註</span><span class="sxs-lookup"><span data-stu-id="31ff0-111">Remarks</span></span>

<span data-ttu-id="31ff0-112">如果使用 **FOURCC** 程式碼來建立此物件，則會建立 **GUID** 以與其相符。</span><span class="sxs-lookup"><span data-stu-id="31ff0-112">If this object is constructed with the **FOURCC** code, a **GUID** is created to match it.</span></span> <span data-ttu-id="31ff0-113">如果此物件是使用現有的 **GUID** 建立的，則物件的 **FOURCC** 值會設定為零。</span><span class="sxs-lookup"><span data-stu-id="31ff0-113">If this object is created with an existing **GUID**, the **FOURCC** value of the object is set to zero.</span></span> <span data-ttu-id="31ff0-114">之後，您可以分別使用 [**SetFOURCC**](fourccmap-setfourcc.md)和 [**GetFOURCC**](fourccmap-getfourcc.md)成員函式來設定或取出 **FOURCC** 值。</span><span class="sxs-lookup"><span data-stu-id="31ff0-114">Thereafter, the **FOURCC** value can be set or retrieved using the [**SetFOURCC**](fourccmap-setfourcc.md) and [**GetFOURCC**](fourccmap-getfourcc.md) member functions, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="31ff0-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="31ff0-115">Requirements</span></span>

| <span data-ttu-id="31ff0-116">需求</span><span class="sxs-lookup"><span data-stu-id="31ff0-116">Requirement</span></span> | <span data-ttu-id="31ff0-117">值</span><span class="sxs-lookup"><span data-stu-id="31ff0-117">Value</span></span> |
|-|-|
| <span data-ttu-id="31ff0-118">標頭</span><span class="sxs-lookup"><span data-stu-id="31ff0-118">Header</span></span>  | <span data-ttu-id="31ff0-119">Fourcc (包含： .h) </span><span class="sxs-lookup"><span data-stu-id="31ff0-119">Fourcc.h (include Streams.h)</span></span> |
| <span data-ttu-id="31ff0-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="31ff0-120">Library</span></span> | <span data-ttu-id="31ff0-121"> (零售組建的 Strmbase .lib) ;Strmbasd (debug 組建) </span><span class="sxs-lookup"><span data-stu-id="31ff0-121">Strmbase.lib (retail builds); Strmbasd.lib (debug builds)</span></span> |

## <a name="see-also"></a><span data-ttu-id="31ff0-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31ff0-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31ff0-123">**FOURCCMap 類別**</span><span class="sxs-lookup"><span data-stu-id="31ff0-123">**FOURCCMap Class**</span></span>](fourccmap.md)
</dt> </dl>

 

 




