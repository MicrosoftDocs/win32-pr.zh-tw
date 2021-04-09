---
description: KsQueryMediums 方法會抓取釘選所支援的媒體。
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
title: 'IKsPin：： KsQueryMediums 方法 (Ksproxy .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin.KsQueryMediums
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: f037317b49bc54f5ea9db5b7a4ae039ec0a9970d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687964"
---
# <a name="ikspinksquerymediums-method"></a><span data-ttu-id="73be6-103">IKsPin：： KsQueryMediums 方法</span><span class="sxs-lookup"><span data-stu-id="73be6-103">IKsPin::KsQueryMediums method</span></span>

<span data-ttu-id="73be6-104">方法會抓取 `KsQueryMediums` pin 所支援的媒體。</span><span class="sxs-lookup"><span data-stu-id="73be6-104">The `KsQueryMediums` method retrieves the mediums supported by a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="73be6-105">語法</span><span class="sxs-lookup"><span data-stu-id="73be6-105">Syntax</span></span>


```C++
HRESULT KsQueryMediums(
  [out] KSMULTIPLE_ITEM **ppmi
);
```



## <a name="parameters"></a><span data-ttu-id="73be6-106">參數</span><span class="sxs-lookup"><span data-stu-id="73be6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73be6-107">*ppmi* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="73be6-107">*ppmi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="73be6-108">指向 [**KSMULTIPLE \_ 專案**](ksmultiple-item.md) 結構之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="73be6-108">Address of a pointer to a [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73be6-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="73be6-109">Return value</span></span>

<span data-ttu-id="73be6-110">如果方法成功，它會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="73be6-110">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="73be6-111">如果失敗，則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="73be6-111">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="73be6-112">備註</span><span class="sxs-lookup"><span data-stu-id="73be6-112">Remarks</span></span>

<span data-ttu-id="73be6-113">這個方法會傳回工作配置的 [**KSMULTIPLE \_ 專案**](ksmultiple-item.md) 結構，後面接著零或多個 [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) 結構。</span><span class="sxs-lookup"><span data-stu-id="73be6-113">This method returns a task-allocated [**KSMULTIPLE\_ITEM**](ksmultiple-item.md) structure, which is followed by zero or more [**REGPINMEDIUM**](/windows/desktop/api/strmif/ns-strmif-regpinmedium) structures.</span></span> <span data-ttu-id="73be6-114">**KSMULTIPLE \_ 專案** 結構的 **Count** 成員會指定 **REGPINMEDIUM** 結構的數目。</span><span class="sxs-lookup"><span data-stu-id="73be6-114">The **Count** member of the **KSMULTIPLE\_ITEM** structure specifies the number of **REGPINMEDIUM** structures.</span></span> <span data-ttu-id="73be6-115">每個 **REGPINMEDIUM** 結構都會定義釘選所支援的媒體。</span><span class="sxs-lookup"><span data-stu-id="73be6-115">Each **REGPINMEDIUM** structure defines a medium supported by the pin.</span></span>

<span data-ttu-id="73be6-116">呼叫端必須使用 **CoTaskMemFree** 函數釋放傳回的結構。</span><span class="sxs-lookup"><span data-stu-id="73be6-116">The caller must free the returned structures, using the **CoTaskMemFree** function.</span></span>

<span data-ttu-id="73be6-117">您必須在 Ksproxy 之前包含 Ks。</span><span class="sxs-lookup"><span data-stu-id="73be6-117">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="73be6-118">範例</span><span class="sxs-lookup"><span data-stu-id="73be6-118">Examples</span></span>

<span data-ttu-id="73be6-119">下列 helper 函式會嘗試比對指定媒體的釘選。</span><span class="sxs-lookup"><span data-stu-id="73be6-119">The following helper function attempts to match a pin against a specified medium.</span></span>


```C++
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin->QueryInterface(IID_IKsPin, (void **)&pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin->KsQueryMediums(&pmi);
    pKsPin->Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi->Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i < pmi->Count; i++, pTemp++) 
        {
            if (pMedium->clsMedium == pTemp->clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
```



## <a name="requirements"></a><span data-ttu-id="73be6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="73be6-120">Requirements</span></span>



| <span data-ttu-id="73be6-121">需求</span><span class="sxs-lookup"><span data-stu-id="73be6-121">Requirement</span></span> | <span data-ttu-id="73be6-122">值</span><span class="sxs-lookup"><span data-stu-id="73be6-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="73be6-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73be6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="73be6-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73be6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="73be6-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73be6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="73be6-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73be6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="73be6-127">標頭</span><span class="sxs-lookup"><span data-stu-id="73be6-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="73be6-128"><dt>Ksproxy。h</dt></span><span class="sxs-lookup"><span data-stu-id="73be6-128"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="73be6-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="73be6-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="73be6-130"><dt>Strmiids .lib</dt></span><span class="sxs-lookup"><span data-stu-id="73be6-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73be6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73be6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73be6-132">錯誤和成功碼</span><span class="sxs-lookup"><span data-stu-id="73be6-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="73be6-133">**IKsPin 介面**</span><span class="sxs-lookup"><span data-stu-id="73be6-133">**IKsPin Interface**</span></span>](ikspin.md)
</dt> <dt>

[<span data-ttu-id="73be6-134">WDM 類別驅動程式篩選</span><span class="sxs-lookup"><span data-stu-id="73be6-134">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
</dt> </dl>

 

 




