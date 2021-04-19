---
description: GetLocked 方法會將物件的編輯狀態 (鎖定或解除鎖定) 。
ms.assetid: ecd258db-36bf-41b6-9bdf-537efcf0a46a
title: 'IAMTimelineObj：： GetLocked 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetLocked
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 472b7dedbdbd879d4fa49fe874fb9178d0ccdee4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984806"
---
# <a name="iamtimelineobjgetlocked-method"></a><span data-ttu-id="fba3a-103">IAMTimelineObj：： GetLocked 方法</span><span class="sxs-lookup"><span data-stu-id="fba3a-103">IAMTimelineObj::GetLocked method</span></span>

> [!Note]  
> <span data-ttu-id="fba3a-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="fba3a-104">\[Deprecated.</span></span> <span data-ttu-id="fba3a-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="fba3a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fba3a-106">`GetLocked`方法會將物件的編輯狀態 (鎖定或解除鎖定) 。</span><span class="sxs-lookup"><span data-stu-id="fba3a-106">The `GetLocked` method retrieves the object's editing state (locked or unlocked).</span></span> <span data-ttu-id="fba3a-107">鎖定狀態表示不應編輯物件;解除鎖定狀態表示可以編輯物件。</span><span class="sxs-lookup"><span data-stu-id="fba3a-107">A locked state indicates that the object should not be edited; an unlocked state indicates that the object can be edited.</span></span> <span data-ttu-id="fba3a-108">時間軸不會強制執行鎖定。</span><span class="sxs-lookup"><span data-stu-id="fba3a-108">The timeline does not enforce the lock.</span></span> <span data-ttu-id="fba3a-109">鎖定的設定只存在於應用程式的便利性。</span><span class="sxs-lookup"><span data-stu-id="fba3a-109">The locked setting exists only for the convenience of the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="fba3a-110">語法</span><span class="sxs-lookup"><span data-stu-id="fba3a-110">Syntax</span></span>


```C++
 GetLocked(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="fba3a-111">參數</span><span class="sxs-lookup"><span data-stu-id="fba3a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fba3a-112">*pVal*</span><span class="sxs-lookup"><span data-stu-id="fba3a-112">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="fba3a-113">接收物件的編輯狀態。</span><span class="sxs-lookup"><span data-stu-id="fba3a-113">Receives the object's editing state.</span></span> <span data-ttu-id="fba3a-114">如果值為 **TRUE**，表示物件已鎖定，且不應該編輯。</span><span class="sxs-lookup"><span data-stu-id="fba3a-114">If the value is **TRUE**, the object is locked and should not be edited.</span></span> <span data-ttu-id="fba3a-115">如果 **為 FALSE**，則表示物件已解除鎖定，而且可以進行編輯。</span><span class="sxs-lookup"><span data-stu-id="fba3a-115">If **FALSE**, the object is unlocked and can be edited.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fba3a-116">備註</span><span class="sxs-lookup"><span data-stu-id="fba3a-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fba3a-117">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="fba3a-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fba3a-118">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="fba3a-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fba3a-119">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="fba3a-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fba3a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="fba3a-120">Requirements</span></span>



| <span data-ttu-id="fba3a-121">需求</span><span class="sxs-lookup"><span data-stu-id="fba3a-121">Requirement</span></span> | <span data-ttu-id="fba3a-122">值</span><span class="sxs-lookup"><span data-stu-id="fba3a-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fba3a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="fba3a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fba3a-124"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="fba3a-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fba3a-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="fba3a-125">Library</span></span><br/> | <dl> <span data-ttu-id="fba3a-126"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="fba3a-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fba3a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fba3a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fba3a-128">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="fba3a-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="fba3a-129">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="fba3a-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




