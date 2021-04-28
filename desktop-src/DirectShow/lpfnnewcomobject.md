---
description: LPFNNewCOMObject 函式指標-函式的指標，該函式會建立物件的實例。
ms.assetid: 8c9dab82-a080-4733-8c62-d090b28306e0
title: 'LPFNNewCOMObject 函式指標 (Combase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LPFNNewCOMObject
api_type:
- UserDefined
api_location:
- Combase.h
ms.openlocfilehash: f3ea5bc172bc22f7aa9dce1f348bba552520565f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116526"
---
# <a name="lpfnnewcomobject-function-pointer"></a><span data-ttu-id="10420-103">LPFNNewCOMObject 函式指標</span><span class="sxs-lookup"><span data-stu-id="10420-103">LPFNNewCOMObject function pointer</span></span>

<span data-ttu-id="10420-104">函數的指標，該函式會建立物件的實例。</span><span class="sxs-lookup"><span data-stu-id="10420-104">Pointer to a function that creates an instance of the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="10420-105">語法</span><span class="sxs-lookup"><span data-stu-id="10420-105">Syntax</span></span>


```C++
typedef CUnknown* ( CALLBACK *LPFNNewCOMObject)(
   LPUNKNOWN pUnkOuter,
   HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="10420-106">參數</span><span class="sxs-lookup"><span data-stu-id="10420-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10420-107">*pUnkOuter*</span><span class="sxs-lookup"><span data-stu-id="10420-107">*pUnkOuter*</span></span> 
</dt> <dd>

<span data-ttu-id="10420-108">物件的 **IUnknown** 介面指標，該物件會匯總新物件（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="10420-108">Pointer to the **IUnknown** interface of the object that aggregates the new object, if any.</span></span> <span data-ttu-id="10420-109">此指標可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="10420-109">This pointer can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="10420-110">*phr*</span><span class="sxs-lookup"><span data-stu-id="10420-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="10420-111">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="10420-111">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="10420-112">如果函式失敗，此參數會收到錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="10420-112">If the constructor fails, this parameter receives an error code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10420-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="10420-113">Return value</span></span>

<span data-ttu-id="10420-114">傳回物件新實例的指標。</span><span class="sxs-lookup"><span data-stu-id="10420-114">Returns a pointer to a new instance of the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="10420-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="10420-115">Requirements</span></span>



| <span data-ttu-id="10420-116">需求</span><span class="sxs-lookup"><span data-stu-id="10420-116">Requirement</span></span> | <span data-ttu-id="10420-117">值</span><span class="sxs-lookup"><span data-stu-id="10420-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10420-118">標頭</span><span class="sxs-lookup"><span data-stu-id="10420-118">Header</span></span><br/> | <dl> <span data-ttu-id="10420-119"><dt>Combase (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="10420-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10420-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10420-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10420-121">**CFactoryTemplate 類別**</span><span class="sxs-lookup"><span data-stu-id="10420-121">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




