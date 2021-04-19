---
description: GetSubObject 方法會抓取與這個物件相關聯的子物件。
ms.assetid: 478597d6-ae13-4fa9-a928-19893f378f1a
title: 'IAMTimelineObj：： GetSubObject 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 74f14658db5ffbaf100925f26573a08b592f6510
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001889"
---
# <a name="iamtimelineobjgetsubobject-method"></a><span data-ttu-id="4ea4c-103">IAMTimelineObj：： GetSubObject 方法</span><span class="sxs-lookup"><span data-stu-id="4ea4c-103">IAMTimelineObj::GetSubObject method</span></span>

> [!Note]  
> <span data-ttu-id="4ea4c-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="4ea4c-104">\[Deprecated.</span></span> <span data-ttu-id="4ea4c-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="4ea4c-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="4ea4c-106">方法會抓取 `GetSubObject` 與這個物件相關聯的子物件。</span><span class="sxs-lookup"><span data-stu-id="4ea4c-106">The `GetSubObject` method retrieves the subobject associated with this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ea4c-107">語法</span><span class="sxs-lookup"><span data-stu-id="4ea4c-107">Syntax</span></span>


```C++
HRESULT GetSubObject(
  [out, retval] IUnknown **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="4ea4c-108">參數</span><span class="sxs-lookup"><span data-stu-id="4ea4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ea4c-109">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="4ea4c-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="4ea4c-110">接收物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="4ea4c-110">Receives a pointer to the subobject's **IUnknown** interface.</span></span> <span data-ttu-id="4ea4c-111">如果物件沒有子物件，此值會設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4ea4c-111">If the object does not have a subobject, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ea4c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ea4c-112">Return value</span></span>

<span data-ttu-id="4ea4c-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="4ea4c-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4ea4c-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="4ea4c-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ea4c-115">備註</span><span class="sxs-lookup"><span data-stu-id="4ea4c-115">Remarks</span></span>

<span data-ttu-id="4ea4c-116">每個時間軸物件都可以保留關聯子物件的指標。</span><span class="sxs-lookup"><span data-stu-id="4ea4c-116">Every timeline object can hold a pointer to an associated subobject.</span></span>

<span data-ttu-id="4ea4c-117">如果 *pVal* 中傳回的值不是 **Null**，則 **IUnknown** 介面具有未處理的參考計數。</span><span class="sxs-lookup"><span data-stu-id="4ea4c-117">If the value returned in *pVal* is not **NULL**, the **IUnknown** interface has an outstanding reference count.</span></span> <span data-ttu-id="4ea4c-118">使用完畢後，請務必釋放介面。</span><span class="sxs-lookup"><span data-stu-id="4ea4c-118">Be sure to release the interface when you are finished using it.</span></span>

> [!Note]  
> <span data-ttu-id="4ea4c-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="4ea4c-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="4ea4c-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="4ea4c-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="4ea4c-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="4ea4c-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4ea4c-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ea4c-122">Requirements</span></span>



| <span data-ttu-id="4ea4c-123">需求</span><span class="sxs-lookup"><span data-stu-id="4ea4c-123">Requirement</span></span> | <span data-ttu-id="4ea4c-124">值</span><span class="sxs-lookup"><span data-stu-id="4ea4c-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea4c-125">標頭</span><span class="sxs-lookup"><span data-stu-id="4ea4c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4ea4c-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ea4c-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="4ea4c-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="4ea4c-127">Library</span></span><br/> | <dl> <span data-ttu-id="4ea4c-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4ea4c-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ea4c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ea4c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea4c-130">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="4ea4c-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="4ea4c-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="4ea4c-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




