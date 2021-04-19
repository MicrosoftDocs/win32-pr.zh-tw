---
description: IsStreamTime 方法會指定是否要在資料流程時間或呈現時間執行命令。
ms.assetid: 4fb315a4-1bc6-49c8-a47f-0a8a46f3f790
title: 'CDeferredCommand. IsStreamTime 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDeferredCommand.IsStreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e15b579f911f6461df30c6b5ae9d3fc29f6fa1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976283"
---
# <a name="cdeferredcommandisstreamtime-method"></a><span data-ttu-id="c6d2c-103">CDeferredCommand. IsStreamTime 方法</span><span class="sxs-lookup"><span data-stu-id="c6d2c-103">CDeferredCommand.IsStreamTime method</span></span>

<span data-ttu-id="c6d2c-104">`IsStreamTime`方法會指定是否要在資料流程時間或呈現時間執行命令。</span><span class="sxs-lookup"><span data-stu-id="c6d2c-104">The `IsStreamTime` method specifies whether the command is to be run at stream time or presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6d2c-105">語法</span><span class="sxs-lookup"><span data-stu-id="c6d2c-105">Syntax</span></span>


```C++
BOOL IsStreamTime();
```



## <a name="parameters"></a><span data-ttu-id="c6d2c-106">參數</span><span class="sxs-lookup"><span data-stu-id="c6d2c-106">Parameters</span></span>

<span data-ttu-id="c6d2c-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c6d2c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c6d2c-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="c6d2c-108">Return value</span></span>

<span data-ttu-id="c6d2c-109">如果設定為數據流時間，則傳回 **TRUE** ;否則，會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c6d2c-109">Returns **TRUE** if set to stream time; otherwise, returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6d2c-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6d2c-110">Requirements</span></span>



| <span data-ttu-id="c6d2c-111">需求</span><span class="sxs-lookup"><span data-stu-id="c6d2c-111">Requirement</span></span> | <span data-ttu-id="c6d2c-112">值</span><span class="sxs-lookup"><span data-stu-id="c6d2c-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6d2c-113">標頭</span><span class="sxs-lookup"><span data-stu-id="c6d2c-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c6d2c-114"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="c6d2c-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c6d2c-115">程式庫</span><span class="sxs-lookup"><span data-stu-id="c6d2c-115">Library</span></span><br/> | <dl> <span data-ttu-id="c6d2c-116"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="c6d2c-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6d2c-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6d2c-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6d2c-118">**CDeferredCommand 類別**</span><span class="sxs-lookup"><span data-stu-id="c6d2c-118">**CDeferredCommand Class**</span></span>](cdeferredcommand.md)
</dt> </dl>

 

 




