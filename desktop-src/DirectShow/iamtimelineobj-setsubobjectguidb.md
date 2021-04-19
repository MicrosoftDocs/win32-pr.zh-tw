---
description: SetSubObjectGUIDB 方法會指定與這個物件相關聯的子物件的 GUID。 這個方法相當於 IAMTimelineObj：： SetSubObjectGUID，但會採用 BSTR 值。
ms.assetid: b2523b17-1df3-4be5-8bbb-6b67815f9349
title: 'IAMTimelineObj：： SetSubObjectGUIDB 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8df74249f061321ccd710822b8c2e0b76d5c3582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000397"
---
# <a name="iamtimelineobjsetsubobjectguidb-method"></a><span data-ttu-id="81e6e-104">IAMTimelineObj：： SetSubObjectGUIDB 方法</span><span class="sxs-lookup"><span data-stu-id="81e6e-104">IAMTimelineObj::SetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="81e6e-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="81e6e-105">\[Deprecated.</span></span> <span data-ttu-id="81e6e-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="81e6e-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="81e6e-107">`SetSubObjectGUIDB`方法會指定與這個物件相關聯之子物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="81e6e-107">The `SetSubObjectGUIDB` method specifies the GUID of the subobject associated with this object.</span></span> <span data-ttu-id="81e6e-108">這個方法相當於 [**IAMTimelineObj：： SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) ，但會採用 **BSTR** 值。</span><span class="sxs-lookup"><span data-stu-id="81e6e-108">This method is equivalent to [**IAMTimelineObj::SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md) but takes a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e6e-109">語法</span><span class="sxs-lookup"><span data-stu-id="81e6e-109">Syntax</span></span>


```C++
HRESULT SetSubObjectGUIDB(
   BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="81e6e-110">參數</span><span class="sxs-lookup"><span data-stu-id="81e6e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81e6e-111">*newVal*</span><span class="sxs-lookup"><span data-stu-id="81e6e-111">*newVal*</span></span> 
</dt> <dd>

<span data-ttu-id="81e6e-112">表示子物件 GUID 的 **BSTR** 。</span><span class="sxs-lookup"><span data-stu-id="81e6e-112">**BSTR** representing the GUID of the subobject.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81e6e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="81e6e-113">Return value</span></span>

<span data-ttu-id="81e6e-114">\_如果成功，則傳回，否則會傳回表示錯誤原因的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="81e6e-114">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="81e6e-115">備註</span><span class="sxs-lookup"><span data-stu-id="81e6e-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="81e6e-116">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="81e6e-116">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="81e6e-117">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="81e6e-117">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="81e6e-118">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="81e6e-118">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="81e6e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="81e6e-119">Requirements</span></span>



| <span data-ttu-id="81e6e-120">需求</span><span class="sxs-lookup"><span data-stu-id="81e6e-120">Requirement</span></span> | <span data-ttu-id="81e6e-121">值</span><span class="sxs-lookup"><span data-stu-id="81e6e-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81e6e-122">標頭</span><span class="sxs-lookup"><span data-stu-id="81e6e-122">Header</span></span><br/>  | <dl> <span data-ttu-id="81e6e-123"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="81e6e-123"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="81e6e-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="81e6e-124">Library</span></span><br/> | <dl> <span data-ttu-id="81e6e-125"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="81e6e-125"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81e6e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="81e6e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81e6e-127">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="81e6e-127">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="81e6e-128">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="81e6e-128">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




