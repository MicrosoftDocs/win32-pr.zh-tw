---
description: SetCutPoint2 方法會設定當轉換轉譯為剪下時，轉換從某個來源剪下的時間。 這個方法相當於 IAMTimelineTrans：： SetCutPoint，但會接受 REFTIME 值。
ms.assetid: d06d3ee7-04a2-4266-9995-bfabea24aef9
title: 'IAMTimelineTrans：： SetCutPoint2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 117ec522416f0d5722c8ef7aa17cd6e81720b4c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993962"
---
# <a name="iamtimelinetranssetcutpoint2-method"></a><span data-ttu-id="6b181-104">IAMTimelineTrans：： SetCutPoint2 方法</span><span class="sxs-lookup"><span data-stu-id="6b181-104">IAMTimelineTrans::SetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="6b181-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="6b181-105">\[Deprecated.</span></span> <span data-ttu-id="6b181-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="6b181-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6b181-107">`SetCutPoint2`如果轉換是轉譯為剪下，則方法會設定轉換從某個來源減少到下一個來源的時間。</span><span class="sxs-lookup"><span data-stu-id="6b181-107">The `SetCutPoint2` method sets the time at which the transition cuts from one source to the next, if the transition is rendered as a cut.</span></span> <span data-ttu-id="6b181-108">這個方法相當於 [**IAMTimelineTrans：： SetCutPoint**](iamtimelinetrans-setcutpoint.md)，但會接受 [**REFTIME**](reftime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="6b181-108">This method is equivalent to [**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b181-109">語法</span><span class="sxs-lookup"><span data-stu-id="6b181-109">Syntax</span></span>


```C++
HRESULT SetCutPoint2(
   REFTIME TLTime
);
```



## <a name="parameters"></a><span data-ttu-id="6b181-110">參數</span><span class="sxs-lookup"><span data-stu-id="6b181-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b181-111">*TLTime*</span><span class="sxs-lookup"><span data-stu-id="6b181-111">*TLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="6b181-112">相對於轉換開始的切割點（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="6b181-112">Cut point relative to the start of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b181-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6b181-113">Return value</span></span>

<span data-ttu-id="6b181-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6b181-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6b181-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6b181-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b181-116">備註</span><span class="sxs-lookup"><span data-stu-id="6b181-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6b181-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="6b181-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6b181-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="6b181-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6b181-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="6b181-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6b181-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b181-120">Requirements</span></span>



| <span data-ttu-id="6b181-121">需求</span><span class="sxs-lookup"><span data-stu-id="6b181-121">Requirement</span></span> | <span data-ttu-id="6b181-122">值</span><span class="sxs-lookup"><span data-stu-id="6b181-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b181-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6b181-123">Header</span></span><br/>  | <dl> <span data-ttu-id="6b181-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="6b181-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6b181-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="6b181-125">Library</span></span><br/> | <dl> <span data-ttu-id="6b181-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b181-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b181-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b181-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b181-128">**IAMTimelineTrans 介面**</span><span class="sxs-lookup"><span data-stu-id="6b181-128">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="6b181-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="6b181-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




