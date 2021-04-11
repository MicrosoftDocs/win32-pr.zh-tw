---
description: 指定媒體基礎轉換 (MFT) 是否執行非同步處理。
ms.assetid: fcc70282-cfac-487c-b9ff-39e62c836f8b
title: 'MF_TRANSFORM_ASYNC 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89622bd7bb7fa3e8306c94b02f90217b6367d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691252"
---
# <a name="mf_transform_async-attribute"></a><span data-ttu-id="50c32-103">MF \_ 轉換 \_ 非同步屬性</span><span class="sxs-lookup"><span data-stu-id="50c32-103">MF\_TRANSFORM\_ASYNC attribute</span></span>

<span data-ttu-id="50c32-104">指定媒體基礎轉換 (MFT) 是否執行非同步處理。</span><span class="sxs-lookup"><span data-stu-id="50c32-104">Specifies whether a Media Foundation transform (MFT) performs asynchronous processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="50c32-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="50c32-105">Data type</span></span>

<span data-ttu-id="50c32-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="50c32-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="50c32-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="50c32-107">Get/set</span></span>

<span data-ttu-id="50c32-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="50c32-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="50c32-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="50c32-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="50c32-110">備註</span><span class="sxs-lookup"><span data-stu-id="50c32-110">Remarks</span></span>

<span data-ttu-id="50c32-111">屬性是布林值：</span><span class="sxs-lookup"><span data-stu-id="50c32-111">The attribute is a Boolean value:</span></span>

-   <span data-ttu-id="50c32-112">如果屬性為非零，則 MFT 會執行非同步處理。</span><span class="sxs-lookup"><span data-stu-id="50c32-112">If the attribute is nonzero, the MFT performs asynchronous processing.</span></span>
-   <span data-ttu-id="50c32-113">如果屬性為0或未設定，則 MFT 為同步。</span><span class="sxs-lookup"><span data-stu-id="50c32-113">If the attribute is 0 or not set, the MFT is synchronous.</span></span>

<span data-ttu-id="50c32-114">若要取得這個屬性，請先呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 MFT 的屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="50c32-114">To get this attribute, first call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the MFT's attribute store.</span></span> <span data-ttu-id="50c32-115">如果該方法成功，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 來取得屬性值。</span><span class="sxs-lookup"><span data-stu-id="50c32-115">If that method succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute value.</span></span> <span data-ttu-id="50c32-116">如果這兩種方法中的任一個失敗，則 MFT 是同步的。</span><span class="sxs-lookup"><span data-stu-id="50c32-116">If either of the two methods fails, the MFT is synchronous.</span></span>

<span data-ttu-id="50c32-117">若為非同步 MFTs，這個屬性必須設定為非零值。</span><span class="sxs-lookup"><span data-stu-id="50c32-117">For asynchronous MFTs, this attribute must be set to a nonzero value.</span></span> <span data-ttu-id="50c32-118">針對同步 MFTs，這個屬性是選擇性的，但如果存在，則必須設定為0。</span><span class="sxs-lookup"><span data-stu-id="50c32-118">For synchronous MFTs, this attribute is optional, but must be set to 0 if present.</span></span>

<span data-ttu-id="50c32-119">非同步 MFTs 與舊版媒體基礎不相容。</span><span class="sxs-lookup"><span data-stu-id="50c32-119">Asynchronous MFTs are not compatible with earlier versions of Media Foundation.</span></span> <span data-ttu-id="50c32-120">若要使用非同步 MFT，用戶端必須在 MFT 上設定 [**MF \_ 轉換 \_ 非同步 \_ 解除鎖定**](mf-transform-async-unlock.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="50c32-120">To use an asynchronous MFT, the client must set the [**MF\_TRANSFORM\_ASYNC\_UNLOCK**](mf-transform-async-unlock.md) attribute on the MFT.</span></span> <span data-ttu-id="50c32-121"> (Microsoft 媒體基礎管線會自動執行此步驟。 ) </span><span class="sxs-lookup"><span data-stu-id="50c32-121">(The Microsoft Media Foundation pipeline performs this step automatically.)</span></span>

## <a name="examples"></a><span data-ttu-id="50c32-122">範例</span><span class="sxs-lookup"><span data-stu-id="50c32-122">Examples</span></span>

<span data-ttu-id="50c32-123">下列程式碼會測試 MFT 是否執行非同步處理。</span><span class="sxs-lookup"><span data-stu-id="50c32-123">The following code tests whether an MFT performs asynchronous processing.</span></span>


```C++
BOOL IsTransformAsync(IMFTransform *pMFT)
{
    BOOL bAsync = FALSE;
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bAsync = MFGetAttributeUINT32(pAttributes, MF_TRANSFORM_ASYNC, FALSE);
        pAttributes->Release();
    }

    return (bAsync != FALSE);
}
```



## <a name="requirements"></a><span data-ttu-id="50c32-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="50c32-124">Requirements</span></span>



| <span data-ttu-id="50c32-125">需求</span><span class="sxs-lookup"><span data-stu-id="50c32-125">Requirement</span></span> | <span data-ttu-id="50c32-126">值</span><span class="sxs-lookup"><span data-stu-id="50c32-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="50c32-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="50c32-127">Minimum supported client</span></span><br/> | <span data-ttu-id="50c32-128">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50c32-128">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="50c32-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="50c32-129">Minimum supported server</span></span><br/> | <span data-ttu-id="50c32-130">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="50c32-130">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="50c32-131">標頭</span><span class="sxs-lookup"><span data-stu-id="50c32-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="50c32-132"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="50c32-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50c32-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50c32-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50c32-134">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="50c32-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="50c32-135">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="50c32-135">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="50c32-136">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="50c32-136">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="50c32-137">**MF \_ 轉換 \_ 非同步 \_ 解除鎖定**</span><span class="sxs-lookup"><span data-stu-id="50c32-137">**MF\_TRANSFORM\_ASYNC\_UNLOCK**</span></span>](mf-transform-async-unlock.md)
</dt> </dl>

 

 




