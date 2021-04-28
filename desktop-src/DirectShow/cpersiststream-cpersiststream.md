---
description: CPersistStream。 CPersistStream 函式-函數方法。
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
ms.openlocfilehash: 9e3be9233d76929ebfcb79121c60ef6c1af35b56
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085606"
---
# <a name="cpersiststreamcpersiststream-constructor"></a><span data-ttu-id="81763-103">CPersistStream. CPersistStream 函數</span><span class="sxs-lookup"><span data-stu-id="81763-103">CPersistStream.CPersistStream constructor</span></span>

<span data-ttu-id="81763-104">函式方法。</span><span class="sxs-lookup"><span data-stu-id="81763-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="81763-105">語法</span><span class="sxs-lookup"><span data-stu-id="81763-105">Syntax</span></span>


```C++
CPersistStream(
   IUnknown *pUnk,
   HRESULT  *phr
);
```



## <a name="parameters"></a><span data-ttu-id="81763-106">參數</span><span class="sxs-lookup"><span data-stu-id="81763-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81763-107">*朋 克*</span><span class="sxs-lookup"><span data-stu-id="81763-107">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="81763-108">委派物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="81763-108">Pointer to the **IUnknown** interface of the delegating object.</span></span>

</dd> <dt>

<span data-ttu-id="81763-109">*phr*</span><span class="sxs-lookup"><span data-stu-id="81763-109">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="81763-110">一般 COM 傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="81763-110">Pointer to the general COM return value.</span></span> <span data-ttu-id="81763-111">只有當此函式失敗時，才會變更此值。</span><span class="sxs-lookup"><span data-stu-id="81763-111">This value is changed only if this function fails.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81763-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="81763-112">Requirements</span></span>



| <span data-ttu-id="81763-113">需求</span><span class="sxs-lookup"><span data-stu-id="81763-113">Requirement</span></span> | <span data-ttu-id="81763-114">值</span><span class="sxs-lookup"><span data-stu-id="81763-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="81763-115">標頭</span><span class="sxs-lookup"><span data-stu-id="81763-115">Header</span></span><br/>  | <dl> <span data-ttu-id="81763-116"><dt>Pstream (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="81763-116"><dt>Pstream.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="81763-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="81763-117">Library</span></span><br/> | <dl> <span data-ttu-id="81763-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="81763-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81763-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81763-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81763-120">**CPersistStream 類別**</span><span class="sxs-lookup"><span data-stu-id="81763-120">**CPersistStream Class**</span></span>](cpersiststream.md)
</dt> </dl>

 

 




