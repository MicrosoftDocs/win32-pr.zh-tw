---
description: GetFlags 方法會抓取與延後命令相關聯的內容旗標。
ms.assetid: 3a96299a-b157-419b-a23e-86241e10566f
title: 'CDeferredCommand. GetFlags 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetFlags
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec9b97e42534d34c5033b3b86edb9c33366d639
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987975"
---
# <a name="cdeferredcommandgetflags-method"></a><span data-ttu-id="cc3d7-103">CDeferredCommand. GetFlags 方法</span><span class="sxs-lookup"><span data-stu-id="cc3d7-103">CDeferredCommand.GetFlags method</span></span>

<span data-ttu-id="cc3d7-104">方法會抓取 `GetFlags` 與延後命令相關聯的內容旗標。</span><span class="sxs-lookup"><span data-stu-id="cc3d7-104">The `GetFlags` method retrieves the context flags associated with the deferred command.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc3d7-105">語法</span><span class="sxs-lookup"><span data-stu-id="cc3d7-105">Syntax</span></span>


```C++
short GetFlags();
```



## <a name="parameters"></a><span data-ttu-id="cc3d7-106">參數</span><span class="sxs-lookup"><span data-stu-id="cc3d7-106">Parameters</span></span>

<span data-ttu-id="cc3d7-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="cc3d7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cc3d7-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="cc3d7-108">Return value</span></span>

<span data-ttu-id="cc3d7-109">傳回下列項目之一：</span><span class="sxs-lookup"><span data-stu-id="cc3d7-109">Returns one of the following:</span></span>



| <span data-ttu-id="cc3d7-110">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cc3d7-110">Return code</span></span>                                                                                             | <span data-ttu-id="cc3d7-111">Description</span><span class="sxs-lookup"><span data-stu-id="cc3d7-111">Description</span></span>                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cc3d7-112"><dt>**分派 \_ 方法**</dt></span><span class="sxs-lookup"><span data-stu-id="cc3d7-112"><dt>**DISPATCH\_METHOD**</dt></span></span> </dl>         | <span data-ttu-id="cc3d7-113">以方法的形式執行成員。</span><span class="sxs-lookup"><span data-stu-id="cc3d7-113">Run the member as a method.</span></span> <span data-ttu-id="cc3d7-114">如果屬性具有相同的名稱，則可以設定此和分派 \_ PROPERTYGET 旗標。</span><span class="sxs-lookup"><span data-stu-id="cc3d7-114">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span><br/>                                               |
| <dl> <span data-ttu-id="cc3d7-115"><dt>**分派 \_ PROPERTYGET**</dt></span><span class="sxs-lookup"><span data-stu-id="cc3d7-115"><dt>**DISPATCH\_PROPERTYGET**</dt></span></span> </dl>    | <span data-ttu-id="cc3d7-116">正在將成員取出為屬性或資料成員。</span><span class="sxs-lookup"><span data-stu-id="cc3d7-116">The member is being retrieved as a property or data member.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="cc3d7-117"><dt>**分派 \_ PROPERTYPUT**</dt></span><span class="sxs-lookup"><span data-stu-id="cc3d7-117"><dt>**DISPATCH\_PROPERTYPUT**</dt></span></span> </dl>    | <span data-ttu-id="cc3d7-118">成員正變更為屬性或資料成員。</span><span class="sxs-lookup"><span data-stu-id="cc3d7-118">The member is being changed as a property or data member.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="cc3d7-119"><dt>**分派 \_ PROPERTYPUTREF**</dt></span><span class="sxs-lookup"><span data-stu-id="cc3d7-119"><dt>**DISPATCH\_PROPERTYPUTREF**</dt></span></span> </dl> | <span data-ttu-id="cc3d7-120">成員正在透過參考指派進行變更，而不是值指派。</span><span class="sxs-lookup"><span data-stu-id="cc3d7-120">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="cc3d7-121">只有當屬性接受物件的參考時，此旗標才會是有效的。</span><span class="sxs-lookup"><span data-stu-id="cc3d7-121">This flag is valid only when the property accepts a reference to an object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cc3d7-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="cc3d7-122">Requirements</span></span>



| <span data-ttu-id="cc3d7-123">需求</span><span class="sxs-lookup"><span data-stu-id="cc3d7-123">Requirement</span></span> | <span data-ttu-id="cc3d7-124">值</span><span class="sxs-lookup"><span data-stu-id="cc3d7-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc3d7-125">標頭</span><span class="sxs-lookup"><span data-stu-id="cc3d7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="cc3d7-126"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="cc3d7-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cc3d7-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="cc3d7-127">Library</span></span><br/> | <dl> <span data-ttu-id="cc3d7-128"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="cc3d7-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc3d7-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cc3d7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc3d7-130">**CDeferredCommand 類別**</span><span class="sxs-lookup"><span data-stu-id="cc3d7-130">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




