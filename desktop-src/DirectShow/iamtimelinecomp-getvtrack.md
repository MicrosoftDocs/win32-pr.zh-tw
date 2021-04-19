---
description: GetVTrack 方法會依指定的優先順序抓取虛擬追蹤。
ms.assetid: e866064b-a511-4f0c-8cb1-62e4f1c42347
title: 'IAMTimelineComp：： GetVTrack 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp.GetVTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 06c205f700cbdb98fdc5f45bdd2ca7727e2456f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998639"
---
# <a name="iamtimelinecompgetvtrack-method"></a><span data-ttu-id="39fbc-103">IAMTimelineComp：： GetVTrack 方法</span><span class="sxs-lookup"><span data-stu-id="39fbc-103">IAMTimelineComp::GetVTrack method</span></span>

> [!Note]  
> <span data-ttu-id="39fbc-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="39fbc-104">\[Deprecated.</span></span> <span data-ttu-id="39fbc-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="39fbc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="39fbc-106">方法會依 `GetVTrack` 指定的優先順序抓取虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="39fbc-106">The `GetVTrack` method retrieves the virtual track at the specified priority.</span></span>

## <a name="syntax"></a><span data-ttu-id="39fbc-107">語法</span><span class="sxs-lookup"><span data-stu-id="39fbc-107">Syntax</span></span>


```C++
HRESULT GetVTrack(
  [out] IAMTimelineObj **ppVirtualTrack,
        long           Which
);
```



## <a name="parameters"></a><span data-ttu-id="39fbc-108">參數</span><span class="sxs-lookup"><span data-stu-id="39fbc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39fbc-109">*ppVirtualTrack* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="39fbc-109">*ppVirtualTrack* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39fbc-110">接收虛擬軌的 [**IAMTimelineObj**](iamtimelineobj.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="39fbc-110">Receives the virtual track's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="39fbc-111">*頻率*</span><span class="sxs-lookup"><span data-stu-id="39fbc-111">*Which*</span></span> 
</dt> <dd>

<span data-ttu-id="39fbc-112">要抓取的虛擬追蹤優先權。</span><span class="sxs-lookup"><span data-stu-id="39fbc-112">Priority of the virtual track to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39fbc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="39fbc-113">Return value</span></span>

<span data-ttu-id="39fbc-114">傳回下列其中一個 **HRESULT** 值：</span><span class="sxs-lookup"><span data-stu-id="39fbc-114">Returns one of the following **HRESULT** values:</span></span>



| <span data-ttu-id="39fbc-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="39fbc-115">Return code</span></span>                                                                                  | <span data-ttu-id="39fbc-116">Description</span><span class="sxs-lookup"><span data-stu-id="39fbc-116">Description</span></span>                                              |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="39fbc-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="39fbc-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="39fbc-118">成功。</span><span class="sxs-lookup"><span data-stu-id="39fbc-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="39fbc-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="39fbc-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="39fbc-120">沒有具有指定優先權的虛擬追蹤。</span><span class="sxs-lookup"><span data-stu-id="39fbc-120">No virtual track with the specified priority.</span></span><br/> |
| <dl> <span data-ttu-id="39fbc-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="39fbc-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="39fbc-122">**Null** 指標引數。</span><span class="sxs-lookup"><span data-stu-id="39fbc-122">**NULL** pointer argument.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="39fbc-123">備註</span><span class="sxs-lookup"><span data-stu-id="39fbc-123">Remarks</span></span>

<span data-ttu-id="39fbc-124">如果方法成功，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="39fbc-124">If the method succeeds, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="39fbc-125">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="39fbc-125">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="39fbc-126">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="39fbc-126">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="39fbc-127">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="39fbc-127">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="39fbc-128">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="39fbc-128">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="39fbc-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="39fbc-129">Requirements</span></span>



| <span data-ttu-id="39fbc-130">需求</span><span class="sxs-lookup"><span data-stu-id="39fbc-130">Requirement</span></span> | <span data-ttu-id="39fbc-131">值</span><span class="sxs-lookup"><span data-stu-id="39fbc-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39fbc-132">標頭</span><span class="sxs-lookup"><span data-stu-id="39fbc-132">Header</span></span><br/>  | <dl> <span data-ttu-id="39fbc-133"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="39fbc-133"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="39fbc-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="39fbc-134">Library</span></span><br/> | <dl> <span data-ttu-id="39fbc-135"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="39fbc-135"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39fbc-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39fbc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39fbc-137">**IAMTimelineComp 介面**</span><span class="sxs-lookup"><span data-stu-id="39fbc-137">**IAMTimelineComp Interface**</span></span>](iamtimelinecomp.md)
</dt> <dt>

[<span data-ttu-id="39fbc-138">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="39fbc-138">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




