---
description: QuerySupported 方法會判斷物件是否支援指定的屬性集。
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'IKsPropertySet：： QuerySupported 方法 (Ks. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: a13c8523d45278ad403ee08d0822fb853b301520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187472"
---
# <a name="ikspropertysetquerysupported-method"></a><span data-ttu-id="4279b-103">IKsPropertySet：： QuerySupported 方法</span><span class="sxs-lookup"><span data-stu-id="4279b-103">IKsPropertySet::QuerySupported method</span></span>

<span data-ttu-id="4279b-104">`QuerySupported`方法會判斷物件是否支援指定的屬性集。</span><span class="sxs-lookup"><span data-stu-id="4279b-104">The `QuerySupported` method determines whether an object supports a specified property set.</span></span>

## <a name="syntax"></a><span data-ttu-id="4279b-105">語法</span><span class="sxs-lookup"><span data-stu-id="4279b-105">Syntax</span></span>


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a><span data-ttu-id="4279b-106">參數</span><span class="sxs-lookup"><span data-stu-id="4279b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4279b-107">*guidPropSet* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4279b-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4279b-108">屬性集 GUID。</span><span class="sxs-lookup"><span data-stu-id="4279b-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="4279b-109">*dwPropID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4279b-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4279b-110">屬性集內屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4279b-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="4279b-111">*pTypeSupport* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4279b-111">*pTypeSupport* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4279b-112">用來儲存旗標的值指標，指出驅動程式所提供的支援。</span><span class="sxs-lookup"><span data-stu-id="4279b-112">Pointer to a value in which to store flags indicating the support provided by the driver.</span></span> <span data-ttu-id="4279b-113">支援的旗標包含下列各項。</span><span class="sxs-lookup"><span data-stu-id="4279b-113">Supported flags include the following.</span></span>



| <span data-ttu-id="4279b-114">值</span><span class="sxs-lookup"><span data-stu-id="4279b-114">Value</span></span>                    | <span data-ttu-id="4279b-115">描述</span><span class="sxs-lookup"><span data-stu-id="4279b-115">Description</span></span>                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4279b-116">KSPROPERTY \_ 支援 \_ 取得</span><span class="sxs-lookup"><span data-stu-id="4279b-116">KSPROPERTY\_SUPPORT\_GET</span></span> | <span data-ttu-id="4279b-117">您可以藉由呼叫 [**IKsPropertySet：： Get**](ikspropertyset-get.md) 方法來取得屬性。</span><span class="sxs-lookup"><span data-stu-id="4279b-117">You can retrieve the property by calling the [**IKsPropertySet::Get**](ikspropertyset-get.md) method.</span></span> |
| <span data-ttu-id="4279b-118">KSPROPERTY \_ 支援 \_ 集</span><span class="sxs-lookup"><span data-stu-id="4279b-118">KSPROPERTY\_SUPPORT\_SET</span></span> | <span data-ttu-id="4279b-119">您可以藉由呼叫 [**IKsPropertySet：： Set**](ikspropertyset-set.md)來變更屬性。</span><span class="sxs-lookup"><span data-stu-id="4279b-119">You can change the property by calling [**IKsPropertySet::Set**](ikspropertyset-set.md).</span></span>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4279b-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="4279b-120">Return value</span></span>

<span data-ttu-id="4279b-121">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4279b-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="4279b-122">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="4279b-122">Possible values include the following.</span></span>



| <span data-ttu-id="4279b-123">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4279b-123">Return code</span></span>                                                                                              | <span data-ttu-id="4279b-124">Description</span><span class="sxs-lookup"><span data-stu-id="4279b-124">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4279b-125"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4279b-125"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="4279b-126">支援指定的屬性集和屬性 ID 組合。</span><span class="sxs-lookup"><span data-stu-id="4279b-126">The specified property set and property ID combination is supported.</span></span><br/> |
| <dl> <span data-ttu-id="4279b-127"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="4279b-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                | <span data-ttu-id="4279b-128">不支援屬性集。</span><span class="sxs-lookup"><span data-stu-id="4279b-128">Property set is not supported.</span></span><br/>                                       |
| <dl> <span data-ttu-id="4279b-129"><dt>**E \_ \_ \_ 不支援的識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="4279b-129"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="4279b-130">指定的屬性集不支援屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="4279b-130">Property ID is not supported for the specified property set.</span></span><br/>         |
| <dl> <span data-ttu-id="4279b-131"><dt>**E \_ \_ 設定 \_ 不支援的設定**</dt></span><span class="sxs-lookup"><span data-stu-id="4279b-131"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="4279b-132">不支援屬性集。</span><span class="sxs-lookup"><span data-stu-id="4279b-132">Property set is not supported.</span></span><br/>                                       |



 

## <a name="remarks"></a><span data-ttu-id="4279b-133">備註</span><span class="sxs-lookup"><span data-stu-id="4279b-133">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4279b-134">這個名稱的另一個介面存在於 dsound .h 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="4279b-134">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="4279b-135">這兩個介面不相容。</span><span class="sxs-lookup"><span data-stu-id="4279b-135">The two interfaces are not compatible.</span></span> <span data-ttu-id="4279b-136">**IKsControl** 介面（記載于 DirectShow DDK）現在是在 WDM 驅動程式和使用者模式元件之間傳遞屬性集的建議介面。</span><span class="sxs-lookup"><span data-stu-id="4279b-136">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="4279b-137">您必須在 Ksproxy 之前包含 Ks。</span><span class="sxs-lookup"><span data-stu-id="4279b-137">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="4279b-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="4279b-138">Requirements</span></span>



| <span data-ttu-id="4279b-139">需求</span><span class="sxs-lookup"><span data-stu-id="4279b-139">Requirement</span></span> | <span data-ttu-id="4279b-140">值</span><span class="sxs-lookup"><span data-stu-id="4279b-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4279b-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4279b-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4279b-142">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4279b-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                       |
| <span data-ttu-id="4279b-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4279b-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4279b-144">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4279b-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="4279b-145">標頭</span><span class="sxs-lookup"><span data-stu-id="4279b-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="4279b-146"><dt>Ks. h;</dt><dt>Ksproxy .h</dt></span><span class="sxs-lookup"><span data-stu-id="4279b-146"><dt>Ks.h; </dt> <dt>Ksproxy.h</dt></span></span> </dl> |
| <span data-ttu-id="4279b-147">程式庫</span><span class="sxs-lookup"><span data-stu-id="4279b-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="4279b-148"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4279b-148"><dt>Strmiids.lib</dt></span></span> </dl>                                                          |



## <a name="see-also"></a><span data-ttu-id="4279b-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4279b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4279b-150">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="4279b-150">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="4279b-151">**IKsPropertySet 介面**</span><span class="sxs-lookup"><span data-stu-id="4279b-151">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="4279b-152">屬性集</span><span class="sxs-lookup"><span data-stu-id="4279b-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




