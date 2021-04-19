---
description: GetMuted 方法會抓取物件的已靜音狀態。
ms.assetid: e901af1f-1137-4708-a98b-c9f83edc5ab9
title: 'IAMTimelineObj：： GetMuted 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetMuted
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 8883b03f9070a017b8fa4788a7cfd795f46c5f3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991151"
---
# <a name="iamtimelineobjgetmuted-method"></a><span data-ttu-id="036ad-103">IAMTimelineObj：： GetMuted 方法</span><span class="sxs-lookup"><span data-stu-id="036ad-103">IAMTimelineObj::GetMuted method</span></span>

> [!Note]  
> <span data-ttu-id="036ad-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="036ad-104">\[Deprecated.</span></span> <span data-ttu-id="036ad-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="036ad-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="036ad-106">方法會抓取 `GetMuted` 物件的已靜音狀態。</span><span class="sxs-lookup"><span data-stu-id="036ad-106">The `GetMuted` method retrieves the object's muted state.</span></span>

## <a name="syntax"></a><span data-ttu-id="036ad-107">語法</span><span class="sxs-lookup"><span data-stu-id="036ad-107">Syntax</span></span>


```C++
HRESULT GetMuted(
   BOOL *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="036ad-108">參數</span><span class="sxs-lookup"><span data-stu-id="036ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="036ad-109">*pVal*</span><span class="sxs-lookup"><span data-stu-id="036ad-109">*pVal*</span></span> 
</dt> <dd>

<span data-ttu-id="036ad-110">接收指出靜音狀態的值。</span><span class="sxs-lookup"><span data-stu-id="036ad-110">Receives a value indicating the muted state.</span></span> <span data-ttu-id="036ad-111">如果值為 **TRUE**，則物件和其子系會靜音。</span><span class="sxs-lookup"><span data-stu-id="036ad-111">If the value is **TRUE**, the object and its children are muted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="036ad-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="036ad-112">Return value</span></span>

<span data-ttu-id="036ad-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="036ad-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="036ad-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="036ad-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="036ad-115">備註</span><span class="sxs-lookup"><span data-stu-id="036ad-115">Remarks</span></span>

<span data-ttu-id="036ad-116">如果物件的父系為靜音，則不論物件的靜音狀態為何，都會將物件靜音。</span><span class="sxs-lookup"><span data-stu-id="036ad-116">If an object's parent is muted, the object is muted regardless of its muted state.</span></span> <span data-ttu-id="036ad-117">當父系不再處於靜音狀態時，就會還原物件的先前已靜音狀態。</span><span class="sxs-lookup"><span data-stu-id="036ad-117">When the parent is no longer muted, the object's previous muted state is restored.</span></span>

> [!Note]  
> <span data-ttu-id="036ad-118">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="036ad-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="036ad-119">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="036ad-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="036ad-120">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="036ad-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="036ad-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="036ad-121">Requirements</span></span>



| <span data-ttu-id="036ad-122">需求</span><span class="sxs-lookup"><span data-stu-id="036ad-122">Requirement</span></span> | <span data-ttu-id="036ad-123">值</span><span class="sxs-lookup"><span data-stu-id="036ad-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="036ad-124">標頭</span><span class="sxs-lookup"><span data-stu-id="036ad-124">Header</span></span><br/>  | <dl> <span data-ttu-id="036ad-125"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="036ad-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="036ad-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="036ad-126">Library</span></span><br/> | <dl> <span data-ttu-id="036ad-127"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="036ad-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="036ad-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="036ad-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="036ad-129">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="036ad-129">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="036ad-130">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="036ad-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




