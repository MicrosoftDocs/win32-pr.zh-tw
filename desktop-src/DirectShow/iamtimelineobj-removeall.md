---
description: RemoveAll 方法會從時間軸中永久移除這個物件，包括子物件和子系。
ms.assetid: 9596cf47-63fe-4839-a6d5-3685fc91a935
title: 'IAMTimelineObj：： RemoveAll 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.RemoveAll
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1888b89773253285036c89e20332d92555b6db2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978432"
---
# <a name="iamtimelineobjremoveall-method"></a><span data-ttu-id="98b10-103">IAMTimelineObj：： RemoveAll 方法</span><span class="sxs-lookup"><span data-stu-id="98b10-103">IAMTimelineObj::RemoveAll method</span></span>

> [!Note]  
> <span data-ttu-id="98b10-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="98b10-104">\[Deprecated.</span></span> <span data-ttu-id="98b10-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="98b10-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="98b10-106">`RemoveAll`方法會從時間軸中永久移除這個物件，包括子物件和子系。</span><span class="sxs-lookup"><span data-stu-id="98b10-106">The `RemoveAll` method permanently removes this object from the timeline, including subobjects and children.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b10-107">語法</span><span class="sxs-lookup"><span data-stu-id="98b10-107">Syntax</span></span>


```C++
HRESULT RemoveAll();
```



## <a name="parameters"></a><span data-ttu-id="98b10-108">參數</span><span class="sxs-lookup"><span data-stu-id="98b10-108">Parameters</span></span>

<span data-ttu-id="98b10-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="98b10-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98b10-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="98b10-110">Return value</span></span>

<span data-ttu-id="98b10-111">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="98b10-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="98b10-112">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="98b10-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="98b10-113">備註</span><span class="sxs-lookup"><span data-stu-id="98b10-113">Remarks</span></span>

<span data-ttu-id="98b10-114">若要移除物件以在時間軸中的其他位置重新插入物件，請呼叫 [**IAMTimelineObj：： remove**](iamtimelineobj-remove.md)。</span><span class="sxs-lookup"><span data-stu-id="98b10-114">To remove an object for the purpose of reinserting it elsewhere in the timeline, call [**IAMTimelineObj::Remove**](iamtimelineobj-remove.md).</span></span>

> [!Note]  
> <span data-ttu-id="98b10-115">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="98b10-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="98b10-116">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="98b10-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="98b10-117">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="98b10-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="98b10-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="98b10-118">Requirements</span></span>



| <span data-ttu-id="98b10-119">需求</span><span class="sxs-lookup"><span data-stu-id="98b10-119">Requirement</span></span> | <span data-ttu-id="98b10-120">值</span><span class="sxs-lookup"><span data-stu-id="98b10-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98b10-121">標頭</span><span class="sxs-lookup"><span data-stu-id="98b10-121">Header</span></span><br/>  | <dl> <span data-ttu-id="98b10-122"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="98b10-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="98b10-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="98b10-123">Library</span></span><br/> | <dl> <span data-ttu-id="98b10-124"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="98b10-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98b10-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="98b10-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98b10-126">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="98b10-126">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="98b10-127">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="98b10-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




