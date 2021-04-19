---
description: 延期方法會為先前佇列的命令指定新的呈現時間。
ms.assetid: 6201eb18-8180-445c-8d29-980511748fe4
title: CDeferredCommand) 延後方法 (Ctlutil
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.Postpone
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9ce19c5391541336f52dd872b44bb9f3a447c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987985"
---
# <a name="cdeferredcommandpostpone-method"></a><span data-ttu-id="8e166-103">CDeferredCommand. 延遲方法</span><span class="sxs-lookup"><span data-stu-id="8e166-103">CDeferredCommand.Postpone method</span></span>

<span data-ttu-id="8e166-104">`Postpone`方法會為先前已排入佇列的命令指定新的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="8e166-104">The `Postpone` method specifies a new presentation time for a previously queued command.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e166-105">語法</span><span class="sxs-lookup"><span data-stu-id="8e166-105">Syntax</span></span>


```C++
HRESULT Postpone(
   REFTIME newtime
);
```



## <a name="parameters"></a><span data-ttu-id="8e166-106">參數</span><span class="sxs-lookup"><span data-stu-id="8e166-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e166-107">*newtime*</span><span class="sxs-lookup"><span data-stu-id="8e166-107">*newtime*</span></span> 
</dt> <dd>

<span data-ttu-id="8e166-108">新的呈現時間。</span><span class="sxs-lookup"><span data-stu-id="8e166-108">New presentation time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e166-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e166-109">Return value</span></span>

<span data-ttu-id="8e166-110">\_ \_ \_ \_ 如果已通過 *newtime* ，則傳回已通過的 VFW E 時間。</span><span class="sxs-lookup"><span data-stu-id="8e166-110">Returns VFW\_E\_TIME\_ALREADY\_PASSED if *newtime* is already passed.</span></span> <span data-ttu-id="8e166-111">否則，從清單中解壓縮時，會傳回 [**CCmdQueue：： Remove**](ccmdqueue-remove.md) (的 **HRESULT** ，) 或 [**CCmdQueue：： Insert**](ccmdqueue-insert.md) (當重新插入時) 的變更時間。</span><span class="sxs-lookup"><span data-stu-id="8e166-111">Otherwise, returns an **HRESULT** resulting from a call to [**CCmdQueue::Remove**](ccmdqueue-remove.md) (when extracting from the list) or [**CCmdQueue::Insert**](ccmdqueue-insert.md) (when reinserting with the changed time).</span></span>

## <a name="remarks"></a><span data-ttu-id="8e166-112">備註</span><span class="sxs-lookup"><span data-stu-id="8e166-112">Remarks</span></span>

<span data-ttu-id="8e166-113">此成員函式會實 [**IDeferredCommand：:P ostpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) 方法。</span><span class="sxs-lookup"><span data-stu-id="8e166-113">This member function implements the [**IDeferredCommand::Postpone**](/windows/desktop/api/Control/nf-control-ideferredcommand-postpone) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e166-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e166-114">Requirements</span></span>



| <span data-ttu-id="8e166-115">需求</span><span class="sxs-lookup"><span data-stu-id="8e166-115">Requirement</span></span> | <span data-ttu-id="8e166-116">值</span><span class="sxs-lookup"><span data-stu-id="8e166-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e166-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8e166-117">Header</span></span><br/>  | <dl> <span data-ttu-id="8e166-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="8e166-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8e166-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="8e166-119">Library</span></span><br/> | <dl> <span data-ttu-id="8e166-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="8e166-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e166-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e166-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e166-122">**CDeferredCommand 類別**</span><span class="sxs-lookup"><span data-stu-id="8e166-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




