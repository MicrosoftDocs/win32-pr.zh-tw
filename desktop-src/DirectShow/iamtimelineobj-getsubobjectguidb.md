---
description: GetSubObjectGUIDB 方法會抓取與這個時間軸物件相關聯的子物件的 GUID。 這個方法相當於 IAMTimelineObj：： GetSubObjectGUID，但會接收 BSTR 值。
ms.assetid: 693cafda-78c8-4ba4-90d7-23fedcd1fc52
title: 'IAMTimelineObj：： GetSubObjectGUIDB 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 903c6638eececd635af2facd964adabe26f0c106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001811"
---
# <a name="iamtimelineobjgetsubobjectguidb-method"></a><span data-ttu-id="5f6bf-104">IAMTimelineObj：： GetSubObjectGUIDB 方法</span><span class="sxs-lookup"><span data-stu-id="5f6bf-104">IAMTimelineObj::GetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="5f6bf-105">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="5f6bf-105">\[Deprecated.</span></span> <span data-ttu-id="5f6bf-106">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="5f6bf-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="5f6bf-107">方法會抓取 `GetSubObjectGUIDB` 與這個時間軸物件相關聯的子物件的 GUID。</span><span class="sxs-lookup"><span data-stu-id="5f6bf-107">The `GetSubObjectGUIDB` method retrieves the GUID of the subobject associated with this timeline object.</span></span> <span data-ttu-id="5f6bf-108">這個方法相當於 [**IAMTimelineObj：： GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md)，但會接收 **BSTR** 值。</span><span class="sxs-lookup"><span data-stu-id="5f6bf-108">This method is equivalent to [**IAMTimelineObj::GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), but receives a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f6bf-109">語法</span><span class="sxs-lookup"><span data-stu-id="5f6bf-109">Syntax</span></span>


```C++
HRESULT GetSubObjectGUIDB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="5f6bf-110">參數</span><span class="sxs-lookup"><span data-stu-id="5f6bf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f6bf-111">*pVal* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="5f6bf-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5f6bf-112">接收表示子物件 GUID 的字串。</span><span class="sxs-lookup"><span data-stu-id="5f6bf-112">Receives a string representing the subobject GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5f6bf-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5f6bf-113">Return value</span></span>

<span data-ttu-id="5f6bf-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5f6bf-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5f6bf-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5f6bf-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f6bf-116">備註</span><span class="sxs-lookup"><span data-stu-id="5f6bf-116">Remarks</span></span>

<span data-ttu-id="5f6bf-117">方法會配置字串的記憶體。</span><span class="sxs-lookup"><span data-stu-id="5f6bf-117">The method allocates memory for the string.</span></span> <span data-ttu-id="5f6bf-118">應用程式必須呼叫 **SysFreeString** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="5f6bf-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="5f6bf-119">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="5f6bf-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="5f6bf-120">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="5f6bf-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="5f6bf-121">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="5f6bf-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5f6bf-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f6bf-122">Requirements</span></span>



| <span data-ttu-id="5f6bf-123">需求</span><span class="sxs-lookup"><span data-stu-id="5f6bf-123">Requirement</span></span> | <span data-ttu-id="5f6bf-124">值</span><span class="sxs-lookup"><span data-stu-id="5f6bf-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f6bf-125">標頭</span><span class="sxs-lookup"><span data-stu-id="5f6bf-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5f6bf-126"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="5f6bf-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="5f6bf-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="5f6bf-127">Library</span></span><br/> | <dl> <span data-ttu-id="5f6bf-128"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5f6bf-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f6bf-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f6bf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f6bf-130">**IAMTimelineObj 介面**</span><span class="sxs-lookup"><span data-stu-id="5f6bf-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="5f6bf-131">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="5f6bf-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




