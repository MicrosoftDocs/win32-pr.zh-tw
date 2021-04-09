---
description: 指定媒體基礎轉換 (MFT) 是否將屬性從輸入範例複製到輸出範例。
ms.assetid: 039ecb35-9aa9-4e8a-bbbc-042b9c4c874c
title: 'MFPKEY_EXATTRIBUTE_SUPPORTED 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33017111eba95f54e88671cbcf026b3f40812a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848812"
---
# <a name="mfpkey_exattribute_supported-property"></a><span data-ttu-id="a41c2-103">MFPKEY \_ EXATTRIBUTE \_ 支援的屬性</span><span class="sxs-lookup"><span data-stu-id="a41c2-103">MFPKEY\_EXATTRIBUTE\_SUPPORTED property</span></span>

<span data-ttu-id="a41c2-104">指定媒體基礎轉換 (MFT) 是否將屬性從輸入範例複製到輸出範例。</span><span class="sxs-lookup"><span data-stu-id="a41c2-104">Specifies whether a Media Foundation transform (MFT) copies attributes from input samples to output samples.</span></span>



<span data-ttu-id="a41c2-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="a41c2-105">Data type</span></span>

<span data-ttu-id="a41c2-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="a41c2-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a41c2-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="a41c2-107">PROPVARIANT member</span></span>

<span data-ttu-id="a41c2-108">**VARIANT \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="a41c2-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="a41c2-109">VT \_ BOOL</span><span class="sxs-lookup"><span data-stu-id="a41c2-109">VT\_BOOL</span></span>

<span data-ttu-id="a41c2-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="a41c2-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a41c2-111">備註</span><span class="sxs-lookup"><span data-stu-id="a41c2-111">Remarks</span></span>

<span data-ttu-id="a41c2-112">這個屬性可以具有下列值。</span><span class="sxs-lookup"><span data-stu-id="a41c2-112">This attribute can have the following values.</span></span>



| <span data-ttu-id="a41c2-113">值</span><span class="sxs-lookup"><span data-stu-id="a41c2-113">Value</span></span>              | <span data-ttu-id="a41c2-114">描述</span><span class="sxs-lookup"><span data-stu-id="a41c2-114">Description</span></span>                                                                                                                                             |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a41c2-115">**VARIANT \_ TRUE**</span><span class="sxs-lookup"><span data-stu-id="a41c2-115">**VARIANT\_TRUE**</span></span>  | <span data-ttu-id="a41c2-116">MFT 會將屬性從輸入範例複製到輸出範例。</span><span class="sxs-lookup"><span data-stu-id="a41c2-116">The MFT copies attributes from the input samples to the output samples.</span></span>                                                                                 |
| <span data-ttu-id="a41c2-117">**VARIANT \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="a41c2-117">**VARIANT\_FALSE**</span></span> | <span data-ttu-id="a41c2-118">媒體會話會將屬性從輸入範例複製到輸出範例。</span><span class="sxs-lookup"><span data-stu-id="a41c2-118">The Media Session copies attributes from input samples to output samples.</span></span> <span data-ttu-id="a41c2-119">它不會覆寫 MFT 在輸出範例上設定的任何屬性。</span><span class="sxs-lookup"><span data-stu-id="a41c2-119">It does not overwrite any attributes that the MFT sets on the output samples.</span></span> |



 

<span data-ttu-id="a41c2-120">若要取得這個屬性，請針對 **IPropertyStore** 介面呼叫 MFT 上的 **QueryInterface** 。</span><span class="sxs-lookup"><span data-stu-id="a41c2-120">To get this attribute, call **QueryInterface** on the MFT for the **IPropertyStore** interface.</span></span>

<span data-ttu-id="a41c2-121">預設值為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a41c2-121">The default value is **VARIANT\_FALSE**.</span></span> <span data-ttu-id="a41c2-122">如果 MFT 未公開 **IPropertyStore** 介面，或未設定此屬性，則會將值視為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a41c2-122">If the MFT does not expose the **IPropertyStore** interface, or if this property is not set, treat the value as **VARIANT\_FALSE**.</span></span>

<span data-ttu-id="a41c2-123">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="a41c2-123">This property is read-only.</span></span>

> [!NOTE] 
> <span data-ttu-id="a41c2-124">這個屬性不會套用到非同步 MFTs。</span><span class="sxs-lookup"><span data-stu-id="a41c2-124">This attribute does not apply to asynchronous MFTs.</span></span> <span data-ttu-id="a41c2-125">無論這個屬性的值為何，都不會將屬性從輸入範例複製到非同步 MFTs 的輸出範例。</span><span class="sxs-lookup"><span data-stu-id="a41c2-125">Attributes will not be copied from the input samples to the output samples for asynchronous MFTs, regardless of the value of this attribute.</span></span>

## <a name="examples"></a><span data-ttu-id="a41c2-126">範例</span><span class="sxs-lookup"><span data-stu-id="a41c2-126">Examples</span></span>

<span data-ttu-id="a41c2-127">如果 MFT 複製範例屬性，則下列範例會傳回 VARIANT \_ TRUE。</span><span class="sxs-lookup"><span data-stu-id="a41c2-127">The following example returns VARIANT\_TRUE if an MFT copies sample attributes.</span></span>


```C++
BOOL TransformCopiesSampleAttributes(IMFTransform *pMFT)
{
    BOOL bCopiesAttributes = FALSE;

    IPropertyStore *pProps = NULL;

    HRESULT hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    
    if (SUCCEEDED(hr))
    {
        PROPVARIANT var;
        hr = pProps->GetValue(MFPKEY_EXATTRIBUTE_SUPPORTED, &var);

        if (SUCCEEDED(hr))
        {
            bCopiesAttributes = 
                (var.vt == VT_BOOL && var.boolVal == VARIANT_TRUE);

            PropVariantClear(&var);
        }
        pProps->Release();
    }
    return bCopiesAttributes;
}
```



## <a name="requirements"></a><span data-ttu-id="a41c2-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="a41c2-128">Requirements</span></span>



| <span data-ttu-id="a41c2-129">需求</span><span class="sxs-lookup"><span data-stu-id="a41c2-129">Requirement</span></span> | <span data-ttu-id="a41c2-130">值</span><span class="sxs-lookup"><span data-stu-id="a41c2-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a41c2-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a41c2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a41c2-132">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a41c2-132">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a41c2-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a41c2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a41c2-134">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a41c2-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a41c2-135">標頭</span><span class="sxs-lookup"><span data-stu-id="a41c2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="a41c2-136"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="a41c2-136"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a41c2-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a41c2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a41c2-138">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="a41c2-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a41c2-139">範例屬性</span><span class="sxs-lookup"><span data-stu-id="a41c2-139">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="a41c2-140">**IMFTransform：:P rocessOutput**</span><span class="sxs-lookup"><span data-stu-id="a41c2-140">**IMFTransform::ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
</dt> </dl>

 

 




