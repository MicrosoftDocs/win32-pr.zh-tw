---
description: GetEffect 方法會在指定的優先權層級上抓取效果。
ms.assetid: 8606c457-1c4d-4a20-b674-aaf82abeb451
title: 'IAMTimelineEffectable：： GetEffect 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineEffectable.GetEffect
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7a769fca28ea1f8f698b23de7df6b7c15f05234
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001021"
---
# <a name="iamtimelineeffectablegeteffect-method"></a><span data-ttu-id="42dbc-103">IAMTimelineEffectable：： GetEffect 方法</span><span class="sxs-lookup"><span data-stu-id="42dbc-103">IAMTimelineEffectable::GetEffect method</span></span>

> [!Note]  
> <span data-ttu-id="42dbc-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="42dbc-104">\[Deprecated.</span></span> <span data-ttu-id="42dbc-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="42dbc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="42dbc-106">**GetEffect** 方法會在指定的優先權層級上抓取效果。</span><span class="sxs-lookup"><span data-stu-id="42dbc-106">The **GetEffect** method retrieves the effect at the specified priority level.</span></span>

## <a name="syntax"></a><span data-ttu-id="42dbc-107">語法</span><span class="sxs-lookup"><span data-stu-id="42dbc-107">Syntax</span></span>


```C++
HRESULT GetEffect(
  [out] IAMTimelineObj **ppFX,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="42dbc-108">參數</span><span class="sxs-lookup"><span data-stu-id="42dbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42dbc-109">*ppFX* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="42dbc-109">*ppFX* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42dbc-110">接收效果的 [**IAMTimelineObj**](iamtimelineobj.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="42dbc-110">Receives the effect's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="42dbc-111">*頻率*</span><span class="sxs-lookup"><span data-stu-id="42dbc-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="42dbc-112">要取得之效果的優先權層級。</span><span class="sxs-lookup"><span data-stu-id="42dbc-112">Priority level of the effect to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42dbc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="42dbc-113">Return value</span></span>

<span data-ttu-id="42dbc-114">傳回 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="42dbc-114">Returns an HRESULT value.</span></span> <span data-ttu-id="42dbc-115">可能的值如下：</span><span class="sxs-lookup"><span data-stu-id="42dbc-115">Possible values include the following:</span></span>



| <span data-ttu-id="42dbc-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="42dbc-116">Return code</span></span>                                                                               | <span data-ttu-id="42dbc-117">Description</span><span class="sxs-lookup"><span data-stu-id="42dbc-117">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="42dbc-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="42dbc-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="42dbc-119">沒有任何作用於指定的優先順序，</span><span class="sxs-lookup"><span data-stu-id="42dbc-119">No effect at the specified priority,</span></span><br/> |
| <dl> <span data-ttu-id="42dbc-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="42dbc-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="42dbc-121">成功。</span><span class="sxs-lookup"><span data-stu-id="42dbc-121">Success.</span></span><br/>                             |
| <dl> <span data-ttu-id="42dbc-122"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="42dbc-122"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="42dbc-123">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="42dbc-123">**NULL** pointer argument.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="42dbc-124">備註</span><span class="sxs-lookup"><span data-stu-id="42dbc-124">Remarks</span></span>

<span data-ttu-id="42dbc-125">如果方法傳回 S \_ OK，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="42dbc-125">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="42dbc-126">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="42dbc-126">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="42dbc-127">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="42dbc-127">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="42dbc-128">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="42dbc-128">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="42dbc-129">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="42dbc-129">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="42dbc-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="42dbc-130">Requirements</span></span>



| <span data-ttu-id="42dbc-131">需求</span><span class="sxs-lookup"><span data-stu-id="42dbc-131">Requirement</span></span> | <span data-ttu-id="42dbc-132">值</span><span class="sxs-lookup"><span data-stu-id="42dbc-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="42dbc-133">標頭</span><span class="sxs-lookup"><span data-stu-id="42dbc-133">Header</span></span><br/>  | <dl> <span data-ttu-id="42dbc-134"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="42dbc-134"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="42dbc-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="42dbc-135">Library</span></span><br/> | <dl> <span data-ttu-id="42dbc-136"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="42dbc-136"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42dbc-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42dbc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42dbc-138">**IAMTimelineEffectable 介面**</span><span class="sxs-lookup"><span data-stu-id="42dbc-138">**IAMTimelineEffectable Interface**</span></span>](iamtimelineeffectable.md)
</dt> <dt>

[<span data-ttu-id="42dbc-139">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="42dbc-139">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




