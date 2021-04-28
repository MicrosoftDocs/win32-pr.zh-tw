---
description: IAMTimeline：： SetInsertMode 方法-未執行。
ms.assetid: 31ff6e32-e8e7-45b4-af62-b6a84e061c94
title: 'IAMTimeline：： SetInsertMode 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.SetInsertMode
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c3d89e779d1941b23e30c3f96314dd99058c4cf8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098666"
---
# <a name="iamtimelinesetinsertmode-method"></a><span data-ttu-id="b37fc-103">IAMTimeline：： SetInsertMode 方法</span><span class="sxs-lookup"><span data-stu-id="b37fc-103">IAMTimeline::SetInsertMode method</span></span>

> [!Note]  
> <span data-ttu-id="b37fc-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="b37fc-104">\[Deprecated.</span></span> <span data-ttu-id="b37fc-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="b37fc-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b37fc-106">未實作。</span><span class="sxs-lookup"><span data-stu-id="b37fc-106">Not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="b37fc-107">語法</span><span class="sxs-lookup"><span data-stu-id="b37fc-107">Syntax</span></span>


```C++
HRESULT SetInsertMode(
   long Mode
);
```



## <a name="parameters"></a><span data-ttu-id="b37fc-108">參數</span><span class="sxs-lookup"><span data-stu-id="b37fc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b37fc-109">*模式*</span><span class="sxs-lookup"><span data-stu-id="b37fc-109">*Mode*</span></span> 
</dt> <dd>

<span data-ttu-id="b37fc-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="b37fc-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b37fc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b37fc-111">Return value</span></span>

<span data-ttu-id="b37fc-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="b37fc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b37fc-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="b37fc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b37fc-114">備註</span><span class="sxs-lookup"><span data-stu-id="b37fc-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b37fc-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="b37fc-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b37fc-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b37fc-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b37fc-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="b37fc-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b37fc-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="b37fc-118">Requirements</span></span>



| <span data-ttu-id="b37fc-119">需求</span><span class="sxs-lookup"><span data-stu-id="b37fc-119">Requirement</span></span> | <span data-ttu-id="b37fc-120">值</span><span class="sxs-lookup"><span data-stu-id="b37fc-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b37fc-121">標頭</span><span class="sxs-lookup"><span data-stu-id="b37fc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b37fc-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="b37fc-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b37fc-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="b37fc-123">Library</span></span><br/> | <dl> <span data-ttu-id="b37fc-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b37fc-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b37fc-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b37fc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b37fc-126">**IAMTimeline 介面**</span><span class="sxs-lookup"><span data-stu-id="b37fc-126">**IAMTimeline Interface**</span></span>](iamtimeline.md)
</dt> </dl>

 

 




