---
description: Get 方法會抓取屬性集 GUID 和屬性識別碼所識別的屬性。
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'IKsPropertySet：： Get 方法 (Ksproxy .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 9c4461e8c5886d84bcf3b7faa6675b749bc0c37d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467702"
---
# <a name="ikspropertysetget-method"></a><span data-ttu-id="2b0a3-103">IKsPropertySet：： Get 方法</span><span class="sxs-lookup"><span data-stu-id="2b0a3-103">IKsPropertySet::Get method</span></span>

<span data-ttu-id="2b0a3-104">**Get** 方法會抓取屬性集 GUID 和屬性識別碼所識別的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-104">The **Get** method retrieves a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b0a3-105">語法</span><span class="sxs-lookup"><span data-stu-id="2b0a3-105">Syntax</span></span>


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
);
```



## <a name="parameters"></a><span data-ttu-id="2b0a3-106">參數</span><span class="sxs-lookup"><span data-stu-id="2b0a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b0a3-107">*guidPropSet* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b0a3-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0a3-108">屬性集的 GUID。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-108">The GUID of the property set .</span></span>

</dd> <dt>

<span data-ttu-id="2b0a3-109">*dwPropID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b0a3-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0a3-110">屬性集內屬性的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-110">The identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="2b0a3-111">*pInstanceData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b0a3-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0a3-112">位元組陣列的指標，其中包含屬性的實例資料。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-112">A pointer to an array of bytes that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="2b0a3-113">*cbInstanceData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b0a3-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0a3-114">*PInstanceData* 中指定的陣列大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-114">The size of the array given in *pInstanceData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2b0a3-115">*pPropData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2b0a3-115">*pPropData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0a3-116">接收屬性資料之位元組陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-116">A pointer to an array of bytes that receives the property data.</span></span>

</dd> <dt>

<span data-ttu-id="2b0a3-117">*cbPropData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2b0a3-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0a3-118">*PPropData* 中指定的陣列大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-118">The size of the array given in *pPropData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="2b0a3-119">*pcbReturned* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2b0a3-119">*pcbReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b0a3-120">接收方法複製到 *pPropData* 陣列的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-120">Receives the number of bytes the method copies to the *pPropData* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b0a3-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="2b0a3-121">Return value</span></span>

<span data-ttu-id="2b0a3-122">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="2b0a3-123">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-123">Possible values include the following.</span></span>



| <span data-ttu-id="2b0a3-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2b0a3-124">Return code</span></span>                                                                                              | <span data-ttu-id="2b0a3-125">Description</span><span class="sxs-lookup"><span data-stu-id="2b0a3-125">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2b0a3-126"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0a3-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="2b0a3-127">成功。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-127">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="2b0a3-128"><dt>**E \_ \_ 設定 \_ 不支援的設定**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0a3-128"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="2b0a3-129">不支援屬性集。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-129">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="2b0a3-130"><dt>**E \_ \_ \_ 不支援的識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="2b0a3-130"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="2b0a3-131">指定的屬性集不支援屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-131">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2b0a3-132">備註</span><span class="sxs-lookup"><span data-stu-id="2b0a3-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2b0a3-133">這個名稱的另一個介面存在於 dsound .h 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-133">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="2b0a3-134">這兩個介面不相容。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-134">The two interfaces are not compatible.</span></span> <span data-ttu-id="2b0a3-135">[IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol)介面（記載于 DirectShow DDK）現在是在 WDM 驅動程式和使用者模式元件之間傳遞屬性集的建議介面。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-135">The [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="2b0a3-136">若要抓取屬性，請配置此方法將填入的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-136">To retrieve a property, allocate a buffer which this method will then fill in.</span></span> <span data-ttu-id="2b0a3-137">若要判斷所需的緩衝區大小，請針對 *pPropData* 指定 **Null** ，並為 *cbPropData* 指定零 (0) 。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-137">To determine the necessary buffer size, specify **NULL** for *pPropData* and zero (0) for *cbPropData*.</span></span> <span data-ttu-id="2b0a3-138">這個方法會在 *pcbReturned* 中傳回所需的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-138">This method returns the necessary buffer size in *pcbReturned*.</span></span>

<span data-ttu-id="2b0a3-139">您必須在 Ksproxy 之前包含 Ks。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-139">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="2b0a3-140">範例</span><span class="sxs-lookup"><span data-stu-id="2b0a3-140">Examples</span></span>

<span data-ttu-id="2b0a3-141">下列範例會藉由取出 **AMPROPERTY \_ 釘選 \_ 類別目錄** 屬性，查詢其釘選類別的 pin。</span><span class="sxs-lookup"><span data-stu-id="2b0a3-141">The following example queries a pin for its pin category, by retrieving the **AMPROPERTY\_PIN\_CATEGORY** property.</span></span> <span data-ttu-id="2b0a3-142"> (參閱 [釘選屬性集](pin-property-set.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="2b0a3-142">(See [Pin Property Set](pin-property-set.md).)</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="2b0a3-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b0a3-143">Requirements</span></span>



| <span data-ttu-id="2b0a3-144">需求</span><span class="sxs-lookup"><span data-stu-id="2b0a3-144">Requirement</span></span> | <span data-ttu-id="2b0a3-145">值</span><span class="sxs-lookup"><span data-stu-id="2b0a3-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b0a3-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b0a3-146">Minimum supported client</span></span><br/> | <span data-ttu-id="2b0a3-147">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b0a3-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2b0a3-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b0a3-148">Minimum supported server</span></span><br/> | <span data-ttu-id="2b0a3-149">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b0a3-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b0a3-150">標頭</span><span class="sxs-lookup"><span data-stu-id="2b0a3-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b0a3-151"><dt>Ksproxy。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b0a3-151"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="2b0a3-152">程式庫</span><span class="sxs-lookup"><span data-stu-id="2b0a3-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b0a3-153"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b0a3-153"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b0a3-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b0a3-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b0a3-155">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="2b0a3-155">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="2b0a3-156">**IKsPropertySet 介面**</span><span class="sxs-lookup"><span data-stu-id="2b0a3-156">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="2b0a3-157">屬性集</span><span class="sxs-lookup"><span data-stu-id="2b0a3-157">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
