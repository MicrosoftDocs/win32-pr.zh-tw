---
description: Insert 方法會將 CDeferredCommand 物件新增至佇列。
ms.assetid: 41f9c30c-6267-435a-9089-eb34ae606896
title: 'CCmdQueue： Insert 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.Insert
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6bad004641258e29ed42d7142a5b0ab2c0ceb78d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979897"
---
# <a name="ccmdqueueinsert-method"></a><span data-ttu-id="aaf36-103">CCmdQueue. Insert 方法</span><span class="sxs-lookup"><span data-stu-id="aaf36-103">CCmdQueue.Insert method</span></span>

<span data-ttu-id="aaf36-104">`Insert`方法會將 [**CDeferredCommand**](cdeferredcommand.md)物件新增至佇列。</span><span class="sxs-lookup"><span data-stu-id="aaf36-104">The `Insert` method adds a [**CDeferredCommand**](cdeferredcommand.md) object to the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaf36-105">語法</span><span class="sxs-lookup"><span data-stu-id="aaf36-105">Syntax</span></span>


```C++
virtual HRESULT Insert(
   CDeferredCommand *pCmd
);
```



## <a name="parameters"></a><span data-ttu-id="aaf36-106">參數</span><span class="sxs-lookup"><span data-stu-id="aaf36-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaf36-107">*pCmd*</span><span class="sxs-lookup"><span data-stu-id="aaf36-107">*pCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="aaf36-108">要加入至佇列之 **CDeferredCommand** 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="aaf36-108">Pointer to the **CDeferredCommand** object to add to the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaf36-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="aaf36-109">Return value</span></span>

<span data-ttu-id="aaf36-110">\_在預設的執行中傳回 S OK。</span><span class="sxs-lookup"><span data-stu-id="aaf36-110">Returns S\_OK in the default implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaf36-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="aaf36-111">Requirements</span></span>



| <span data-ttu-id="aaf36-112">需求</span><span class="sxs-lookup"><span data-stu-id="aaf36-112">Requirement</span></span> | <span data-ttu-id="aaf36-113">值</span><span class="sxs-lookup"><span data-stu-id="aaf36-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaf36-114">標頭</span><span class="sxs-lookup"><span data-stu-id="aaf36-114">Header</span></span><br/>  | <dl> <span data-ttu-id="aaf36-115"><dt>Winutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="aaf36-115"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aaf36-116">程式庫</span><span class="sxs-lookup"><span data-stu-id="aaf36-116">Library</span></span><br/> | <dl> <span data-ttu-id="aaf36-117"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="aaf36-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaf36-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aaf36-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaf36-119">**CCmdQueue 類別**</span><span class="sxs-lookup"><span data-stu-id="aaf36-119">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




