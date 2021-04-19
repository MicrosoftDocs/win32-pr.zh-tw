---
description: GetCutPoint2 方法會抓取剪下點。 這個方法相當於 IAMTimelineTrans：： GetCutPoint，但會接受 REFTIME 值。
ms.assetid: bf2b7cac-6740-44d8-a889-8c745a23db19
title: 'IAMTimelineTrans：： GetCutPoint2 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 68712da95da2f5c21d5e370c688002aa14a8a166
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990833"
---
# <a name="iamtimelinetransgetcutpoint2-method"></a><span data-ttu-id="3e77f-104">IAMTimelineTrans：： GetCutPoint2 方法</span><span class="sxs-lookup"><span data-stu-id="3e77f-104">IAMTimelineTrans::GetCutPoint2 method</span></span>

> [!Note]  
> <span data-ttu-id="3e77f-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="3e77f-105">\[Deprecated.</span></span> <span data-ttu-id="3e77f-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="3e77f-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3e77f-107">方法會抓取 `GetCutPoint2` 剪下點。</span><span class="sxs-lookup"><span data-stu-id="3e77f-107">The `GetCutPoint2` method retrieves the cut point.</span></span> <span data-ttu-id="3e77f-108">這個方法相當於 [**IAMTimelineTrans：： GetCutPoint**](iamtimelinetrans-getcutpoint.md)，但會接受 [**REFTIME**](reftime.md) 值。</span><span class="sxs-lookup"><span data-stu-id="3e77f-108">This method is equivalent to [**IAMTimelineTrans::GetCutPoint**](iamtimelinetrans-getcutpoint.md), but takes a [**REFTIME**](reftime.md) value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e77f-109">語法</span><span class="sxs-lookup"><span data-stu-id="3e77f-109">Syntax</span></span>


```C++
HRESULT GetCutPoint2(
   REFTIME *pTLTime
);
```



## <a name="parameters"></a><span data-ttu-id="3e77f-110">參數</span><span class="sxs-lookup"><span data-stu-id="3e77f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e77f-111">*pTLTime*</span><span class="sxs-lookup"><span data-stu-id="3e77f-111">*pTLTime*</span></span> 
</dt> <dd>

<span data-ttu-id="3e77f-112">接收相對於轉換開始時間的切割點（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3e77f-112">Receives the cut point, relative to the start time of the transition, in seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e77f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="3e77f-113">Return value</span></span>

<span data-ttu-id="3e77f-114">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="3e77f-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="3e77f-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3e77f-115">Return code</span></span>                                                                               | <span data-ttu-id="3e77f-116">Description</span><span class="sxs-lookup"><span data-stu-id="3e77f-116">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3e77f-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="3e77f-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="3e77f-118">未設定剪下點。</span><span class="sxs-lookup"><span data-stu-id="3e77f-118">The cut point was not set.</span></span> <span data-ttu-id="3e77f-119">傳回的值是預設值。</span><span class="sxs-lookup"><span data-stu-id="3e77f-119">The value returned is the default value.</span></span><br/> |
| <dl> <span data-ttu-id="3e77f-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3e77f-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="3e77f-121">剪下點已設定為預設值以外的值。</span><span class="sxs-lookup"><span data-stu-id="3e77f-121">The cut point was set to a value other than the default.</span></span><br/>            |
| <dl> <span data-ttu-id="3e77f-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="3e77f-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="3e77f-123">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="3e77f-123">**NULL** pointer argument.</span></span><br/>                                          |



 

## <a name="remarks"></a><span data-ttu-id="3e77f-124">備註</span><span class="sxs-lookup"><span data-stu-id="3e77f-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3e77f-125">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="3e77f-125">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3e77f-126">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="3e77f-126">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3e77f-127">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="3e77f-127">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3e77f-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e77f-128">Requirements</span></span>



| <span data-ttu-id="3e77f-129">需求</span><span class="sxs-lookup"><span data-stu-id="3e77f-129">Requirement</span></span> | <span data-ttu-id="3e77f-130">值</span><span class="sxs-lookup"><span data-stu-id="3e77f-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e77f-131">標頭</span><span class="sxs-lookup"><span data-stu-id="3e77f-131">Header</span></span><br/>  | <dl> <span data-ttu-id="3e77f-132"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="3e77f-132"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3e77f-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="3e77f-133">Library</span></span><br/> | <dl> <span data-ttu-id="3e77f-134"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3e77f-134"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e77f-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e77f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e77f-136">**IAMTimelineTrans 介面**</span><span class="sxs-lookup"><span data-stu-id="3e77f-136">**IAMTimelineTrans Interface**</span></span>](iamtimelinetrans.md)
</dt> <dt>

[<span data-ttu-id="3e77f-137">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="3e77f-137">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




