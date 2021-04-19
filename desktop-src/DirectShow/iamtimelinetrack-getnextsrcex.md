---
description: GetNextSrcEx 方法會在指定的來源之後，抓取下一個來源。
ms.assetid: cda3d079-eeb5-42a9-8854-5c90ae0e2c07
title: 'IAMTimelineTrack：： GetNextSrcEx 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrcEx
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 274a4f6800d995e2b456dbd55adf81cf82aa84a9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994609"
---
# <a name="iamtimelinetrackgetnextsrcex-method"></a><span data-ttu-id="fc8a9-103">IAMTimelineTrack：： GetNextSrcEx 方法</span><span class="sxs-lookup"><span data-stu-id="fc8a9-103">IAMTimelineTrack::GetNextSrcEx method</span></span>

> [!Note]  
> <span data-ttu-id="fc8a9-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="fc8a9-104">\[Deprecated.</span></span> <span data-ttu-id="fc8a9-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="fc8a9-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fc8a9-106">方法會在 `GetNextSrcEx` 指定的來源之後，抓取下一個來源。</span><span class="sxs-lookup"><span data-stu-id="fc8a9-106">The `GetNextSrcEx` method retrieves the next source after the specified source.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8a9-107">語法</span><span class="sxs-lookup"><span data-stu-id="fc8a9-107">Syntax</span></span>


```C++
HRESULT GetNextSrcEx(
        IAMTimelineObj *pLast,
  [out] IAMTimelineObj **ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="fc8a9-108">參數</span><span class="sxs-lookup"><span data-stu-id="fc8a9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc8a9-109">*pLast*</span><span class="sxs-lookup"><span data-stu-id="fc8a9-109">*pLast*</span></span> 
</dt> <dd>

<span data-ttu-id="fc8a9-110">先前來源物件的指標，或為 **Null** ，以抓取曲目中的第一個來源。</span><span class="sxs-lookup"><span data-stu-id="fc8a9-110">Pointer to the previous source object, or **NULL** to retrieve the first source in the track.</span></span>

</dd> <dt>

<span data-ttu-id="fc8a9-111">*ppNext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fc8a9-111">*ppNext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc8a9-112">接收下一個來源物件之 [**IAMTimelineObj**](iamtimelineobj.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="fc8a9-112">Receives a pointer to the next source object's [**IAMTimelineObj**](iamtimelineobj.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc8a9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc8a9-113">Return value</span></span>

<span data-ttu-id="fc8a9-114">\_如果方法會抓取來源，則傳回 [確定]， \_ 否則傳回 FALSE。</span><span class="sxs-lookup"><span data-stu-id="fc8a9-114">Returns S\_OK if the method retrieves a source, or S\_FALSE otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc8a9-115">備註</span><span class="sxs-lookup"><span data-stu-id="fc8a9-115">Remarks</span></span>

<span data-ttu-id="fc8a9-116">如果方法傳回 S \_ OK，則傳回的 **IAMTimelineObj** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="fc8a9-116">If the method returns S\_OK, the **IAMTimelineObj** interface that it returns has an outstanding reference count.</span></span> <span data-ttu-id="fc8a9-117">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="fc8a9-117">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="fc8a9-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="fc8a9-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fc8a9-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fc8a9-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fc8a9-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="fc8a9-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fc8a9-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc8a9-121">Requirements</span></span>



| <span data-ttu-id="fc8a9-122">需求</span><span class="sxs-lookup"><span data-stu-id="fc8a9-122">Requirement</span></span> | <span data-ttu-id="fc8a9-123">值</span><span class="sxs-lookup"><span data-stu-id="fc8a9-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8a9-124">標頭</span><span class="sxs-lookup"><span data-stu-id="fc8a9-124">Header</span></span><br/>  | <dl> <span data-ttu-id="fc8a9-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fc8a9-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fc8a9-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="fc8a9-126">Library</span></span><br/> | <dl> <span data-ttu-id="fc8a9-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc8a9-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc8a9-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc8a9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc8a9-129">**IAMTimelineTrack 介面**</span><span class="sxs-lookup"><span data-stu-id="fc8a9-129">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="fc8a9-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="fc8a9-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




