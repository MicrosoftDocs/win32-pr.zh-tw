---
description: GetNextTrans2 方法會抓取在指定時間或之後出現的第一個轉換。 這個方法相當於 IAMTimelineTransable：： GetNextTrans，但會接受 REFTIME 值。
ms.assetid: e6910e94-f289-4a5d-9976-1e8f7373c882
title: 'IAMTimelineTransable：： GetNextTrans2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c5f79ff20507247fbcac3badceaf2c3e28f0303
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997035"
---
# <a name="iamtimelinetransablegetnexttrans2-method"></a><span data-ttu-id="88f53-104">IAMTimelineTransable：： GetNextTrans2 方法</span><span class="sxs-lookup"><span data-stu-id="88f53-104">IAMTimelineTransable::GetNextTrans2 method</span></span>

> [!Note]  
> <span data-ttu-id="88f53-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="88f53-105">\[Deprecated.</span></span> <span data-ttu-id="88f53-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="88f53-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="88f53-107">`GetNextTrans2`方法會抓取在指定時間或之後出現的第一個轉換。</span><span class="sxs-lookup"><span data-stu-id="88f53-107">The `GetNextTrans2` method retrieves the first transition that appears at the specified time or later.</span></span> <span data-ttu-id="88f53-108">這個方法相當於 [**IAMTimelineTransable：： GetNextTrans**](iamtimelinetransable-getnexttrans.md)，但會接受 [**REFTIME**](reftime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="88f53-108">This method is equivalent to [**IAMTimelineTransable::GetNextTrans**](iamtimelinetransable-getnexttrans.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="88f53-109">語法</span><span class="sxs-lookup"><span data-stu-id="88f53-109">Syntax</span></span>


```C++
HRESULT GetNextTrans2(
  [out] IAMTimelineObj **ppTrans,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a><span data-ttu-id="88f53-110">參數</span><span class="sxs-lookup"><span data-stu-id="88f53-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88f53-111">*ppTrans* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="88f53-111">*ppTrans* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88f53-112">接收轉換物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="88f53-112">Receives a pointer to the transition object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="88f53-113">*接腳*</span><span class="sxs-lookup"><span data-stu-id="88f53-113">*pInOut*</span></span> 
</dt> <dd>

<span data-ttu-id="88f53-114">指定時間（以秒為單位）之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="88f53-114">Pointer to a variable that specifies the time in seconds.</span></span> <span data-ttu-id="88f53-115">在輸入時，這個值會指定要從中尋找轉換的時間。</span><span class="sxs-lookup"><span data-stu-id="88f53-115">On input, this value specifies the time from which to find the transition.</span></span> <span data-ttu-id="88f53-116">在輸出時，如果已抓取轉換，此值會設定為轉換的停止時間。</span><span class="sxs-lookup"><span data-stu-id="88f53-116">On output, if a transition is retrieved, this value is set to the stop time of the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88f53-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="88f53-117">Return value</span></span>

<span data-ttu-id="88f53-118">\_如果方法會抓取轉換，則傳回 [確定]， \_ 如果找不到轉換，則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="88f53-118">Returns S\_OK if the method retrieves a transition, or S\_FALSE if it does not find a transition.</span></span> <span data-ttu-id="88f53-119">否則，會傳回 **HRESULT** 值，指出失敗的原因。</span><span class="sxs-lookup"><span data-stu-id="88f53-119">Otherwise, returns an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="88f53-120">備註</span><span class="sxs-lookup"><span data-stu-id="88f53-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="88f53-121">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="88f53-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="88f53-122">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="88f53-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="88f53-123">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="88f53-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="88f53-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="88f53-124">Requirements</span></span>



| <span data-ttu-id="88f53-125">需求</span><span class="sxs-lookup"><span data-stu-id="88f53-125">Requirement</span></span> | <span data-ttu-id="88f53-126">值</span><span class="sxs-lookup"><span data-stu-id="88f53-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88f53-127">標頭</span><span class="sxs-lookup"><span data-stu-id="88f53-127">Header</span></span><br/>  | <dl> <span data-ttu-id="88f53-128"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="88f53-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="88f53-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="88f53-129">Library</span></span><br/> | <dl> <span data-ttu-id="88f53-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="88f53-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88f53-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88f53-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88f53-132">**IAMTimelineTransable 介面**</span><span class="sxs-lookup"><span data-stu-id="88f53-132">**IAMTimelineTransable Interface**</span></span>](iamtimelinetransable.md)
</dt> <dt>

[<span data-ttu-id="88f53-133">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="88f53-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




