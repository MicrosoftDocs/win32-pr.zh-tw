---
description: GetHResult 方法會從叫用的命令抓取 HRESULT 值。
ms.assetid: 7e88a2bd-6b1b-4e59-b185-5dfd501fc37a
title: 'CDeferredCommand. GetHResult 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.GetHResult
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b09049bc443991dabe07a7626ffc42097feceee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996508"
---
# <a name="cdeferredcommandgethresult-method"></a><span data-ttu-id="b46e0-103">CDeferredCommand. GetHResult 方法</span><span class="sxs-lookup"><span data-stu-id="b46e0-103">CDeferredCommand.GetHResult method</span></span>

<span data-ttu-id="b46e0-104">`GetHResult`方法會從叫用的命令抓取 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="b46e0-104">The `GetHResult` method retrieves the **HRESULT** value from the invoked command.</span></span>

## <a name="syntax"></a><span data-ttu-id="b46e0-105">語法</span><span class="sxs-lookup"><span data-stu-id="b46e0-105">Syntax</span></span>


```C++
HRESULT GetHResult(
   HRESULT *phrResult
);
```



## <a name="parameters"></a><span data-ttu-id="b46e0-106">參數</span><span class="sxs-lookup"><span data-stu-id="b46e0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b46e0-107">*phrResult*</span><span class="sxs-lookup"><span data-stu-id="b46e0-107">*phrResult*</span></span> 
</dt> <dd>

<span data-ttu-id="b46e0-108">**HRESULT** 值的指標。</span><span class="sxs-lookup"><span data-stu-id="b46e0-108">Pointer to the **HRESULT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b46e0-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="b46e0-109">Return value</span></span>

<span data-ttu-id="b46e0-110">\_如果 **m \_ pQueue** 為 **Null**，則傳回 E ABORT。</span><span class="sxs-lookup"><span data-stu-id="b46e0-110">Returns E\_ABORT if **m\_pQueue** is **NULL**.</span></span> <span data-ttu-id="b46e0-111">否則，會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b46e0-111">Otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="b46e0-112">備註</span><span class="sxs-lookup"><span data-stu-id="b46e0-112">Remarks</span></span>

<span data-ttu-id="b46e0-113">此成員函式會實 [**IDeferredCommand：： GetHResult**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) 方法。</span><span class="sxs-lookup"><span data-stu-id="b46e0-113">This member function implements the [**IDeferredCommand::GetHResult**](/windows/desktop/api/Control/nf-control-ideferredcommand-gethresult) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b46e0-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b46e0-114">Requirements</span></span>



| <span data-ttu-id="b46e0-115">需求</span><span class="sxs-lookup"><span data-stu-id="b46e0-115">Requirement</span></span> | <span data-ttu-id="b46e0-116">值</span><span class="sxs-lookup"><span data-stu-id="b46e0-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b46e0-117">標頭</span><span class="sxs-lookup"><span data-stu-id="b46e0-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b46e0-118"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="b46e0-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b46e0-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="b46e0-119">Library</span></span><br/> | <dl> <span data-ttu-id="b46e0-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="b46e0-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b46e0-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b46e0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b46e0-122">**CDeferredCommand 類別**</span><span class="sxs-lookup"><span data-stu-id="b46e0-122">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




