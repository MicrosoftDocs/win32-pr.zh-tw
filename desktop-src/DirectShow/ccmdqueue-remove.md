---
description: Remove 方法會從佇列中移除 CDeferredCommand 物件。
ms.assetid: b3cff57d-9625-40db-b815-9529ac706f45
title: 'CCmdQueue： Remove 方法 (Winutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Remove
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef9f45c8176645c5937b5ad74045130ff8cd8c06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996478"
---
# <a name="ccmdqueueremove-method"></a><span data-ttu-id="d6e4e-103">CCmdQueue 方法</span><span class="sxs-lookup"><span data-stu-id="d6e4e-103">CCmdQueue.Remove method</span></span>

<span data-ttu-id="d6e4e-104">`Remove`方法會從佇列中移除 [**CDeferredCommand**](cdeferredcommand.md)物件。</span><span class="sxs-lookup"><span data-stu-id="d6e4e-104">The `Remove` method removes the [**CDeferredCommand**](cdeferredcommand.md) object from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6e4e-105">語法</span><span class="sxs-lookup"><span data-stu-id="d6e4e-105">Syntax</span></span>


```C++
virtual HRESULT Remove(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="d6e4e-106">參數</span><span class="sxs-lookup"><span data-stu-id="d6e4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6e4e-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="d6e4e-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="d6e4e-108">要從佇列中移除之 **CDeferredCommand** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="d6e4e-108">Pointer to the **CDeferredCommand** object to remove from the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6e4e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6e4e-109">Return value</span></span>

<span data-ttu-id="d6e4e-110">如果在 \_ \_ \_ 佇列中找不到物件，則會傳回 VFW E （找不到）。</span><span class="sxs-lookup"><span data-stu-id="d6e4e-110">Returns VFW\_E\_NOT\_FOUND if the object is not found in the queue.</span></span> <span data-ttu-id="d6e4e-111">否則，會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d6e4e-111">Otherwise, returns S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6e4e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6e4e-112">Requirements</span></span>



| <span data-ttu-id="d6e4e-113">需求</span><span class="sxs-lookup"><span data-stu-id="d6e4e-113">Requirement</span></span> | <span data-ttu-id="d6e4e-114">值</span><span class="sxs-lookup"><span data-stu-id="d6e4e-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6e4e-115">標頭</span><span class="sxs-lookup"><span data-stu-id="d6e4e-115">Header</span></span><br/>  | <dl> <span data-ttu-id="d6e4e-116"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="d6e4e-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d6e4e-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="d6e4e-117">Library</span></span><br/> | <dl> <span data-ttu-id="d6e4e-118"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="d6e4e-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6e4e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d6e4e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6e4e-120">**CCmdQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="d6e4e-120">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




