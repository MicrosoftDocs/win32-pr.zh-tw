---
description: GetNextTrans 方法會抓取在指定時間或之後出現的第一個轉換。
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'IAMTimelineTransable：： GetNextTrans 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992366"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a><span data-ttu-id="229a7-103">IAMTimelineTransable：： GetNextTrans 方法</span><span class="sxs-lookup"><span data-stu-id="229a7-103">IAMTimelineTransable::GetNextTrans method</span></span>

> [!Note]  
> <span data-ttu-id="229a7-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="229a7-104">\[Deprecated.</span></span> <span data-ttu-id="229a7-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="229a7-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="229a7-106">`GetNextTrans`方法會抓取在指定時間或之後出現的第一個轉換。</span><span class="sxs-lookup"><span data-stu-id="229a7-106">The `GetNextTrans` method retrieves the first transition that appears at the specified time or later.</span></span>

## <a name="syntax"></a><span data-ttu-id="229a7-107">語法</span><span class="sxs-lookup"><span data-stu-id="229a7-107">Syntax</span></span>


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="229a7-108">參數</span><span class="sxs-lookup"><span data-stu-id="229a7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="229a7-109">*ppTrans* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="229a7-109">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="229a7-110">接收轉換物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="229a7-110">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="229a7-111">*接腳*</span><span class="sxs-lookup"><span data-stu-id="229a7-111">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="229a7-112">變數的指標，此變數會以 100-毫微秒單位來指定時間。</span><span class="sxs-lookup"><span data-stu-id="229a7-112">Pointer to a variable that specifies the time in 100-nanosecond units.</span></span> <span data-ttu-id="229a7-113">在輸入時，這個值會指定要從中尋找轉換的時間。</span><span class="sxs-lookup"><span data-stu-id="229a7-113">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="229a7-114">在輸出時，如果已抓取轉換，此值會設定為轉換的停止時間。</span><span class="sxs-lookup"><span data-stu-id="229a7-114">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="229a7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="229a7-115">Return value</span></span>

<span data-ttu-id="229a7-116">\_如果方法會抓取轉換，則傳回 [確定]， \_ 如果找不到轉換，則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="229a7-116">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="229a7-117">否則，會傳回 **HRESULT** 值，指出失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="229a7-117">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="229a7-118">備註</span><span class="sxs-lookup"><span data-stu-id="229a7-118">Remarks</span></span>

<span data-ttu-id="229a7-119">如果轉換跨越指定的時間，轉換的開始時間可能會小於您在外接 *引線* 中指定的時間。</span><span class="sxs-lookup"><span data-stu-id="229a7-119">The start time of the transition might be less than the time that you specify in *pInOut*, if the transition spans the specified time.</span></span>

<span data-ttu-id="229a7-120">如果方法傳回 S \_ OK，則傳回的 [**IAMTimelineObj**](iamtimelineobj.md) 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="229a7-120">If the method returns S\_OK, the [**IAMTimelineObj**](iamtimelineobj.md) interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="229a7-121">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="229a7-121">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="229a7-122">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="229a7-122">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="229a7-123">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="229a7-123">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="229a7-124">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="229a7-124">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="229a7-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="229a7-125">Requirements</span></span>



| <span data-ttu-id="229a7-126">需求</span><span class="sxs-lookup"><span data-stu-id="229a7-126">Requirement</span></span> | <span data-ttu-id="229a7-127">值</span><span class="sxs-lookup"><span data-stu-id="229a7-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="229a7-128">標頭</span><span class="sxs-lookup"><span data-stu-id="229a7-128">Header</span></span><br/>  | <dl> <span data-ttu-id="229a7-129"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="229a7-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="229a7-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="229a7-130">Library</span></span><br/> | <dl> <span data-ttu-id="229a7-131"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="229a7-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="229a7-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="229a7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229a7-133">**IAMTimelineTransable 介面**</span><span class="sxs-lookup"><span data-stu-id="229a7-133">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="229a7-134">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="229a7-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




