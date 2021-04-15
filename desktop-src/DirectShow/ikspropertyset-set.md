---
description: Set 方法會設定屬性集 GUID 和屬性識別碼所識別的屬性。
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'IKsPropertySet：： Set 方法 (Ksproxy .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: b233cea7e131919d94b00afeb5a6e2ea3703c738
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385697"
---
# <a name="ikspropertysetset-method"></a><span data-ttu-id="2f585-103">IKsPropertySet：： Set 方法</span><span class="sxs-lookup"><span data-stu-id="2f585-103">IKsPropertySet::Set method</span></span>

<span data-ttu-id="2f585-104">`Set`方法會設定屬性集 GUID 和屬性識別碼所識別的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f585-104">The `Set` method sets a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f585-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f585-105">Syntax</span></span>


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
);
```



## <a name="parameters"></a><span data-ttu-id="2f585-106">參數</span><span class="sxs-lookup"><span data-stu-id="2f585-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f585-107">*guidPropSet* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f585-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f585-108">屬性集 GUID。</span><span class="sxs-lookup"><span data-stu-id="2f585-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="2f585-109">*dwPropID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f585-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f585-110">屬性集內屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f585-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="2f585-111">*pInstanceData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f585-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f585-112">緩衝區的指標，此緩衝區包含屬性的實例資料。</span><span class="sxs-lookup"><span data-stu-id="2f585-112">Pointer to a buffer that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="2f585-113">*cbInstanceData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f585-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f585-114">*PInstanceData* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f585-114">Size of the *pInstanceData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2f585-115">*pPropData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f585-115">*pPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f585-116">包含屬性值之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="2f585-116">Pointer to a buffer that contains the value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="2f585-117">*cbPropData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f585-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f585-118">*PPropData* 緩衝區的 Sise （以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f585-118">Sise of the *pPropData* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f585-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f585-119">Return value</span></span>

<span data-ttu-id="2f585-120">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2f585-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2f585-121">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="2f585-121">Possible values include the following.</span></span>



| <span data-ttu-id="2f585-122">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2f585-122">Return code</span></span>                                                                                              | <span data-ttu-id="2f585-123">Description</span><span class="sxs-lookup"><span data-stu-id="2f585-123">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f585-124"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2f585-124"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="2f585-125">成功。</span><span class="sxs-lookup"><span data-stu-id="2f585-125">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="2f585-126"><dt>**E \_ \_ 設定 \_ 不支援的設定**</dt></span><span class="sxs-lookup"><span data-stu-id="2f585-126"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="2f585-127">不支援屬性集。</span><span class="sxs-lookup"><span data-stu-id="2f585-127">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="2f585-128"><dt>**E \_ \_ \_ 不支援的識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="2f585-128"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="2f585-129">指定的屬性集不支援屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f585-129">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f585-130">備註</span><span class="sxs-lookup"><span data-stu-id="2f585-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2f585-131">這個名稱的另一個介面存在於 dsound .h 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="2f585-131">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="2f585-132">這兩個介面不相容。</span><span class="sxs-lookup"><span data-stu-id="2f585-132">The two interfaces are not compatible.</span></span> <span data-ttu-id="2f585-133">**IKsControl** 介面（記載于 DirectShow DDK）現在是在 WDM 驅動程式和使用者模式元件之間傳遞屬性集的建議介面。</span><span class="sxs-lookup"><span data-stu-id="2f585-133">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="2f585-134">您必須在 Ksproxy 之前包含 Ks。</span><span class="sxs-lookup"><span data-stu-id="2f585-134">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f585-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f585-135">Requirements</span></span>



| <span data-ttu-id="2f585-136">需求</span><span class="sxs-lookup"><span data-stu-id="2f585-136">Requirement</span></span> | <span data-ttu-id="2f585-137">值</span><span class="sxs-lookup"><span data-stu-id="2f585-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f585-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f585-138">Minimum supported client</span></span><br/> | <span data-ttu-id="2f585-139">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f585-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2f585-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f585-140">Minimum supported server</span></span><br/> | <span data-ttu-id="2f585-141">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f585-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2f585-142">標頭</span><span class="sxs-lookup"><span data-stu-id="2f585-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f585-143"><dt>Ksproxy。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f585-143"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="2f585-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="2f585-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f585-145"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f585-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f585-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f585-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f585-147">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="2f585-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="2f585-148">**IKsPropertySet 介面**</span><span class="sxs-lookup"><span data-stu-id="2f585-148">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="2f585-149">屬性集</span><span class="sxs-lookup"><span data-stu-id="2f585-149">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




