---
description: GetCurrentSample 方法不會實作為。
ms.assetid: 0c903498-3c1d-4e95-a797-ca8cfded25f2
title: 'ISampleGrabber：： GetCurrentSample 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISampleGrabber.GetCurrentSample
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9a21f50f84f030502cfd3243d36595e465e1b85b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993443"
---
# <a name="isamplegrabbergetcurrentsample-method"></a><span data-ttu-id="26bb0-103">ISampleGrabber：： GetCurrentSample 方法</span><span class="sxs-lookup"><span data-stu-id="26bb0-103">ISampleGrabber::GetCurrentSample method</span></span>

> [!Note]  
> <span data-ttu-id="26bb0-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="26bb0-104">\[Deprecated.</span></span> <span data-ttu-id="26bb0-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="26bb0-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="26bb0-106">`GetCurrentSample` 方法尚未實作。</span><span class="sxs-lookup"><span data-stu-id="26bb0-106">The `GetCurrentSample` method is not implemented.</span></span>

## <a name="syntax"></a><span data-ttu-id="26bb0-107">語法</span><span class="sxs-lookup"><span data-stu-id="26bb0-107">Syntax</span></span>


```C++
HRESULT GetCurrentSample(
   IMediaSample **ppSample
);
```



## <a name="parameters"></a><span data-ttu-id="26bb0-108">參數</span><span class="sxs-lookup"><span data-stu-id="26bb0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26bb0-109">*ppSample*</span><span class="sxs-lookup"><span data-stu-id="26bb0-109">*ppSample*</span></span> 
</dt> <dd>

<span data-ttu-id="26bb0-110">保留的。</span><span class="sxs-lookup"><span data-stu-id="26bb0-110">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26bb0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="26bb0-111">Return value</span></span>

<span data-ttu-id="26bb0-112">傳回 E \_ >notimpl。</span><span class="sxs-lookup"><span data-stu-id="26bb0-112">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="26bb0-113">備註</span><span class="sxs-lookup"><span data-stu-id="26bb0-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="26bb0-114">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="26bb0-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="26bb0-115">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="26bb0-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="26bb0-116">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="26bb0-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="26bb0-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="26bb0-117">Requirements</span></span>



| <span data-ttu-id="26bb0-118">需求</span><span class="sxs-lookup"><span data-stu-id="26bb0-118">Requirement</span></span> | <span data-ttu-id="26bb0-119">值</span><span class="sxs-lookup"><span data-stu-id="26bb0-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26bb0-120">標頭</span><span class="sxs-lookup"><span data-stu-id="26bb0-120">Header</span></span><br/>  | <dl> <span data-ttu-id="26bb0-121"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="26bb0-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="26bb0-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="26bb0-122">Library</span></span><br/> | <dl> <span data-ttu-id="26bb0-123"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="26bb0-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26bb0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26bb0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26bb0-125">使用範例捕獲</span><span class="sxs-lookup"><span data-stu-id="26bb0-125">Using the Sample Grabber</span></span>](using-the-sample-grabber.md)
</dt> <dt>

[<span data-ttu-id="26bb0-126">**ISampleGrabber 介面**</span><span class="sxs-lookup"><span data-stu-id="26bb0-126">**ISampleGrabber Interface**</span></span>](isamplegrabber.md)
</dt> </dl>

 

 




