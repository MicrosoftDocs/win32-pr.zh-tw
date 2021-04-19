---
description: AreYouBlank 方法會判斷追蹤是否為空白 (不會) 包含任何來源物件。
ms.assetid: 05d02753-6e40-4307-9445-c3cbc835f75e
title: 'IAMTimelineTrack：： AreYouBlank 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.AreYouBlank
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 289fac360f989504d3eb5108f8c2388ac4a06b09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991552"
---
# <a name="iamtimelinetrackareyoublank-method"></a><span data-ttu-id="381c0-103">IAMTimelineTrack：： AreYouBlank 方法</span><span class="sxs-lookup"><span data-stu-id="381c0-103">IAMTimelineTrack::AreYouBlank method</span></span>

> [!Note]  
> <span data-ttu-id="381c0-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="381c0-104">\[Deprecated.</span></span> <span data-ttu-id="381c0-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="381c0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="381c0-106">`AreYouBlank`方法會判斷此追蹤是否為空白 (不會) 包含任何來源物件。</span><span class="sxs-lookup"><span data-stu-id="381c0-106">The `AreYouBlank` method determines whether the track is blank (contains no source objects).</span></span>

## <a name="syntax"></a><span data-ttu-id="381c0-107">語法</span><span class="sxs-lookup"><span data-stu-id="381c0-107">Syntax</span></span>


```C++
HRESULT AreYouBlank(
   long *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="381c0-108">參數</span><span class="sxs-lookup"><span data-stu-id="381c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="381c0-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="381c0-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="381c0-110">接收布林值，指定此曲目是否為空白。</span><span class="sxs-lookup"><span data-stu-id="381c0-110">Receives a Boolean value specifying whether the track is blank.</span></span> <span data-ttu-id="381c0-111">如果值為 **TRUE**，表示追蹤是空白的，且不包含任何來源物件。</span><span class="sxs-lookup"><span data-stu-id="381c0-111">If the value is **TRUE**, the track is blank and contains no source objects.</span></span> <span data-ttu-id="381c0-112">如果 **為 FALSE**，則表示播放軌不是空白的。</span><span class="sxs-lookup"><span data-stu-id="381c0-112">If **FALSE**, the track is not blank.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="381c0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="381c0-113">Return value</span></span>

<span data-ttu-id="381c0-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="381c0-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="381c0-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="381c0-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="381c0-116">備註</span><span class="sxs-lookup"><span data-stu-id="381c0-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="381c0-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="381c0-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="381c0-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="381c0-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="381c0-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="381c0-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="381c0-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="381c0-120">Requirements</span></span>



| <span data-ttu-id="381c0-121">需求</span><span class="sxs-lookup"><span data-stu-id="381c0-121">Requirement</span></span> | <span data-ttu-id="381c0-122">值</span><span class="sxs-lookup"><span data-stu-id="381c0-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="381c0-123">標頭</span><span class="sxs-lookup"><span data-stu-id="381c0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="381c0-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="381c0-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="381c0-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="381c0-125">Library</span></span><br/> | <dl> <span data-ttu-id="381c0-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="381c0-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="381c0-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="381c0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="381c0-128">**IAMTimelineTrack 介面**</span><span class="sxs-lookup"><span data-stu-id="381c0-128">**IAMTimelineTrack Interface**</span></span>](iamtimelinetrack.md)
</dt> <dt>

[<span data-ttu-id="381c0-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="381c0-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




