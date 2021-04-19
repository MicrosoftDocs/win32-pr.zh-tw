---
description: 函式方法。
ms.assetid: 48143a61-5ba7-4bf9-bffa-244f2769144d
title: 'CPersistStream. CPersistStream (Pstream. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.CPersistStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7cdb736a191f64099b8c0310a5b3ac3dad3cbe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989638"
---
# <a name="cpersiststreamcpersiststream-constructor"></a><span data-ttu-id="1362d-103">CPersistStream. CPersistStream 函數</span><span class="sxs-lookup"><span data-stu-id="1362d-103">CPersistStream.CPersistStream constructor</span></span>

<span data-ttu-id="1362d-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="1362d-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1362d-105">語法</span><span class="sxs-lookup"><span data-stu-id="1362d-105">Syntax</span></span>


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a><span data-ttu-id="1362d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1362d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1362d-107">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="1362d-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="1362d-108">委派物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="1362d-108">Pointer to the **IUnknown** interface of the delegating object.</span></span>

</dd> <dt>

<span data-ttu-id="1362d-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="1362d-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="1362d-110">一般 COM 傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="1362d-110">Pointer to the general COM return value.</span></span> <span data-ttu-id="1362d-111">只有當此函式失敗時，才會變更此值。</span><span class="sxs-lookup"><span data-stu-id="1362d-111">This value is changed only if this function fails.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1362d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="1362d-112">Requirements</span></span>



| <span data-ttu-id="1362d-113">需求</span><span class="sxs-lookup"><span data-stu-id="1362d-113">Requirement</span></span> | <span data-ttu-id="1362d-114">值</span><span class="sxs-lookup"><span data-stu-id="1362d-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1362d-115">標頭</span><span class="sxs-lookup"><span data-stu-id="1362d-115">Header</span></span><br/>  | <dl> <span data-ttu-id="1362d-116"><dt>Pstream (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="1362d-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="1362d-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="1362d-117">Library</span></span><br/> | <dl> <span data-ttu-id="1362d-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="1362d-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1362d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1362d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1362d-120">**CPersistStream 類別**</span><span class="sxs-lookup"><span data-stu-id="1362d-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




