---
description: SetLocked 方法會將物件的編輯狀態設定為 [已鎖定] 或 [已解除鎖定]。
ms.assetid: 801b8bf0-5c7a-4122-9038-6b0d8bdc5da3
title: 'IAMTimelineObj：： SetLocked 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b8707aa86b651553dde2f9f9b57c84169a9969b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998658"
---
# <a name="iamtimelineobjsetlocked-method"></a><span data-ttu-id="5d131-103">IAMTimelineObj：： SetLocked 方法</span><span class="sxs-lookup"><span data-stu-id="5d131-103">IAMTimelineObj::SetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="5d131-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="5d131-104">\[Deprecated.</span></span> <span data-ttu-id="5d131-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="5d131-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5d131-106">`SetLocked`方法會將物件的編輯狀態設定為 [已鎖定] 或 [已解除鎖定]。</span><span class="sxs-lookup"><span data-stu-id="5d131-106">The `SetLocked` method sets the object's editing state to locked or unlocked.</span></span>

<span data-ttu-id="5d131-107">鎖定狀態表示不應編輯物件;解除鎖定狀態表示可以編輯物件。</span><span class="sxs-lookup"><span data-stu-id="5d131-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="5d131-108">時間軸不會強制執行鎖定。</span><span class="sxs-lookup"><span data-stu-id="5d131-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="5d131-109">鎖定的設定只存在於應用程式的便利性。</span><span class="sxs-lookup"><span data-stu-id="5d131-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d131-110">語法</span><span class="sxs-lookup"><span data-stu-id="5d131-110">Syntax</span></span>


```C++
HRESULT SetLocked(
   BOOL newVal
);
```



## <a name="parameters"></a><span data-ttu-id="5d131-111">參數</span><span class="sxs-lookup"><span data-stu-id="5d131-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d131-112">*newVal*</span><span class="sxs-lookup"><span data-stu-id="5d131-112">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="5d131-113">指定物件之編輯狀態的布林值。</span><span class="sxs-lookup"><span data-stu-id="5d131-113">Boolean value that specifies the object's editing state.</span></span> <span data-ttu-id="5d131-114">若 **為 TRUE**，則物件已鎖定，不應該編輯。</span><span class="sxs-lookup"><span data-stu-id="5d131-114">If **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="5d131-115">如果 **為 FALSE**，則表示物件已解除鎖定，而且可以進行編輯。</span><span class="sxs-lookup"><span data-stu-id="5d131-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d131-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d131-116">Return value</span></span>

<span data-ttu-id="5d131-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5d131-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d131-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5d131-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d131-119">備註</span><span class="sxs-lookup"><span data-stu-id="5d131-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5d131-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="5d131-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5d131-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5d131-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5d131-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="5d131-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d131-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d131-123">Requirements</span></span>



| <span data-ttu-id="5d131-124">需求</span><span class="sxs-lookup"><span data-stu-id="5d131-124">Requirement</span></span> | <span data-ttu-id="5d131-125">值</span><span class="sxs-lookup"><span data-stu-id="5d131-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d131-126">標頭</span><span class="sxs-lookup"><span data-stu-id="5d131-126">Header</span></span><br/>  | <dl> <span data-ttu-id="5d131-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5d131-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5d131-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="5d131-128">Library</span></span><br/> | <dl> <span data-ttu-id="5d131-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5d131-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d131-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d131-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d131-131">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="5d131-131">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="5d131-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="5d131-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




