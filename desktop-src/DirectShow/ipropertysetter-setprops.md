---
description: SetProps 方法會在指定的時間內，將目標物件的屬性設定為適當的狀態。
ms.assetid: 65e701c9-d3a1-4396-9cba-a7830757701f
title: 'IPropertySetter：： SetProps 方法 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.SetProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6a36b1735ea5b8261c37bee66ac90b9a186a55f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999273"
---
# <a name="ipropertysettersetprops-method"></a><span data-ttu-id="2d532-103">IPropertySetter：： SetProps 方法</span><span class="sxs-lookup"><span data-stu-id="2d532-103">IPropertySetter::SetProps method</span></span>

> [!Note]  
> <span data-ttu-id="2d532-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="2d532-104">\[Deprecated.</span></span> <span data-ttu-id="2d532-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="2d532-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="2d532-106">`SetProps`方法會將目標物件的屬性設定為指定時間的適當狀態。</span><span class="sxs-lookup"><span data-stu-id="2d532-106">The `SetProps` method sets the properties of the target object to the appropriate state for the specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d532-107">語法</span><span class="sxs-lookup"><span data-stu-id="2d532-107">Syntax</span></span>


```C++
HRESULT SetProps(
  [in] IUnknown       *pTarget,
  [in] REFERENCE_TIME rtNow
);
```



## <a name="parameters"></a><span data-ttu-id="2d532-108">參數</span><span class="sxs-lookup"><span data-stu-id="2d532-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d532-109">*pTarget* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d532-109">*pTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d532-110">要設定屬性的目標物件指標。</span><span class="sxs-lookup"><span data-stu-id="2d532-110">Pointer to the target object for which to set the properties.</span></span>

</dd> <dt>

<span data-ttu-id="2d532-111">*rtNow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2d532-111">*rtNow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2d532-112">設定屬性的時間，以 100-毫微秒為單位，或-1 表示設定靜態屬性 (不會隨時間變化的) 。</span><span class="sxs-lookup"><span data-stu-id="2d532-112">Time at which to set the properties, in 100-nanosecond units, or –1 to set static properties (those that do not vary over time).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d532-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2d532-113">Return value</span></span>

<span data-ttu-id="2d532-114">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="2d532-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2d532-115">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2d532-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d532-116">備註</span><span class="sxs-lookup"><span data-stu-id="2d532-116">Remarks</span></span>

<span data-ttu-id="2d532-117">DES 會呼叫這個方法來設定轉換或效果的屬性。</span><span class="sxs-lookup"><span data-stu-id="2d532-117">This method is called by DES to set the properties on a transition or effect.</span></span> <span data-ttu-id="2d532-118">應用程式通常不會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="2d532-118">An application will not normally call this method.</span></span>

<span data-ttu-id="2d532-119">*PTarget* 所指定的物件必須執行 **IDispatch** 介面。</span><span class="sxs-lookup"><span data-stu-id="2d532-119">The object specified by *pTarget* must implement the **IDispatch** interface.</span></span>

> [!Note]  
> <span data-ttu-id="2d532-120">標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。</span><span class="sxs-lookup"><span data-stu-id="2d532-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="2d532-121">若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。</span><span class="sxs-lookup"><span data-stu-id="2d532-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="2d532-122">在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。</span><span class="sxs-lookup"><span data-stu-id="2d532-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2d532-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="2d532-123">Requirements</span></span>



| <span data-ttu-id="2d532-124">需求</span><span class="sxs-lookup"><span data-stu-id="2d532-124">Requirement</span></span> | <span data-ttu-id="2d532-125">值</span><span class="sxs-lookup"><span data-stu-id="2d532-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d532-126">標頭</span><span class="sxs-lookup"><span data-stu-id="2d532-126">Header</span></span><br/>  | <dl> <span data-ttu-id="2d532-127"><dt>Qedit。h</dt></span><span class="sxs-lookup"><span data-stu-id="2d532-127"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="2d532-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="2d532-128">Library</span></span><br/> | <dl> <span data-ttu-id="2d532-129"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2d532-129"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d532-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2d532-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d532-131">**IPropertySetter 介面**</span><span class="sxs-lookup"><span data-stu-id="2d532-131">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="2d532-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="2d532-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




