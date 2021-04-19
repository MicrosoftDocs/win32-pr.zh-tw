---
description: Get \_ CurrentPosition 方法會抓取目前的位置，相對於資料流程的總持續時間。 這個方法會實 IMediaPosition：： get \_ CurrentPosition 方法。
ms.assetid: 6e68af98-440d-4ecc-b1aa-d5e241de4999
title: 'CPosPassThru.get_CurrentPosition 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.get_CurrentPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c146eb1ee3d0a48da90973ab181a4bd02182331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994052"
---
# <a name="cpospassthruget_currentposition-method"></a><span data-ttu-id="a5187-104">CPosPassThru. 取得 \_ CurrentPosition 方法</span><span class="sxs-lookup"><span data-stu-id="a5187-104">CPosPassThru.get\_CurrentPosition method</span></span>

<span data-ttu-id="a5187-105">方法會抓取 `get_CurrentPosition` 目前的位置，相對於資料流程的總持續時間。</span><span class="sxs-lookup"><span data-stu-id="a5187-105">The `get_CurrentPosition` method retrieves the current position, relative to the total duration of the stream.</span></span> <span data-ttu-id="a5187-106">這個方法會實 [**IMediaPosition：： get \_ CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) 方法。</span><span class="sxs-lookup"><span data-stu-id="a5187-106">This method implements the [**IMediaPosition::get\_CurrentPosition**](/windows/desktop/api/Control/nf-control-imediaposition-get_currentposition) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5187-107">語法</span><span class="sxs-lookup"><span data-stu-id="a5187-107">Syntax</span></span>


```C++
HRESULT get_CurrentPosition(
   REFTIME *pllTime
);
```



## <a name="parameters"></a><span data-ttu-id="a5187-108">參數</span><span class="sxs-lookup"><span data-stu-id="a5187-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5187-109">*pllTime*</span><span class="sxs-lookup"><span data-stu-id="a5187-109">*pllTime*</span></span> 
</dt> <dd>

<span data-ttu-id="a5187-110">接收目前位置之變數的指標（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="a5187-110">Pointer to a variable that receives the current position, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5187-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5187-111">Return value</span></span>

<span data-ttu-id="a5187-112">從連接的 pin 傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="a5187-112">Returns the **HRESULT** value from the connected pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5187-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5187-113">Requirements</span></span>



| <span data-ttu-id="a5187-114">需求</span><span class="sxs-lookup"><span data-stu-id="a5187-114">Requirement</span></span> | <span data-ttu-id="a5187-115">值</span><span class="sxs-lookup"><span data-stu-id="a5187-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5187-116">標頭</span><span class="sxs-lookup"><span data-stu-id="a5187-116">Header</span></span><br/>  | <dl> <span data-ttu-id="a5187-117"><dt>Ctlutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a5187-117"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a5187-118">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5187-118">Library</span></span><br/> | <dl> <span data-ttu-id="a5187-119"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="a5187-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a5187-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5187-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5187-121">**CPosPassThru 類別**</span><span class="sxs-lookup"><span data-stu-id="a5187-121">**CPosPassThru Class**</span></span>](cpospassthru.md)
</dt> </dl>

 

 




