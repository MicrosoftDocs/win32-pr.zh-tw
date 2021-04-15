---
description: 啟用使用非同步媒體基礎轉換 (MFT) 。
ms.assetid: e12ab57e-ebc2-46af-afdf-d78d4db16fcf
title: 'MF_TRANSFORM_ASYNC_UNLOCK 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e7876b3f1fca80e881414399d40e69112a64d8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512261"
---
# <a name="mf_transform_async_unlock-attribute"></a><span data-ttu-id="d7250-103">MF \_ 轉換 \_ 非同步 \_ 解除鎖定屬性</span><span class="sxs-lookup"><span data-stu-id="d7250-103">MF\_TRANSFORM\_ASYNC\_UNLOCK attribute</span></span>

<span data-ttu-id="d7250-104">啟用使用非同步媒體基礎轉換 (MFT) 。</span><span class="sxs-lookup"><span data-stu-id="d7250-104">Enables the use of an asynchronous Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="d7250-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="d7250-105">Data type</span></span>

<span data-ttu-id="d7250-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d7250-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="d7250-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="d7250-107">Get/set</span></span>

<span data-ttu-id="d7250-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="d7250-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="d7250-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="d7250-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7250-110">備註</span><span class="sxs-lookup"><span data-stu-id="d7250-110">Remarks</span></span>

<span data-ttu-id="d7250-111">非同步 MFTs 與舊版 Microsoft 媒體基礎不相容。</span><span class="sxs-lookup"><span data-stu-id="d7250-111">Asynchronous MFTs are not compatible with earlier versions of Microsoft Media Foundation.</span></span> <span data-ttu-id="d7250-112">若要防止現有的應用程式不小心使用非同步 MFT，必須先將此屬性設定為非零值，才能使用非同步 MFT。</span><span class="sxs-lookup"><span data-stu-id="d7250-112">To prevent existing applications from accidentally using an asynchronous MFT, this attribute must be set to a nonzero value before an asynchronous MFT can be used.</span></span> <span data-ttu-id="d7250-113">媒體基礎管線會自動設定屬性，因此大部分的應用程式不需要使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="d7250-113">The Media Foundation pipeline automatically sets the attribute, so that most applications do not need to use this attribute.</span></span> <span data-ttu-id="d7250-114">但是，如果應用程式使用媒體基礎管線以外的非同步 MFT，則應用程式必須設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d7250-114">However, if an application uses an asynchronous MFT outside of the Media Foundation pipeline, the application must set this attribute.</span></span>

<span data-ttu-id="d7250-115">同步 MFTs 不需要此屬性。</span><span class="sxs-lookup"><span data-stu-id="d7250-115">Synchronous MFTs do not require this attribute.</span></span>

<span data-ttu-id="d7250-116">若要測試 MFT 是否為非同步，請在 MFT 上取得 [MF \_ 轉換 \_ ASYNC](mf-transform-async.md) 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="d7250-116">To test whether an MFT is asynchronous, get the value of the [MF\_TRANSFORM\_ASYNC](mf-transform-async.md) attribute on the MFT.</span></span>

## <a name="examples"></a><span data-ttu-id="d7250-117">範例</span><span class="sxs-lookup"><span data-stu-id="d7250-117">Examples</span></span>

<span data-ttu-id="d7250-118">下列程式碼會解除鎖定非同步 MFT。</span><span class="sxs-lookup"><span data-stu-id="d7250-118">The following code unlocks an asynchronous MFT.</span></span>


```C++
HRESULT UnlockAsyncMFT(IMFTransform *pMFT)
{
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = hr = pMFT->GetAttributes(&pAttributes);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_TRANSFORM_ASYNC_UNLOCK, TRUE);
        pAttributes->Release();
    }
    
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="d7250-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7250-119">Requirements</span></span>



| <span data-ttu-id="d7250-120">需求</span><span class="sxs-lookup"><span data-stu-id="d7250-120">Requirement</span></span> | <span data-ttu-id="d7250-121">值</span><span class="sxs-lookup"><span data-stu-id="d7250-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7250-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7250-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7250-123">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7250-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d7250-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7250-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7250-125">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7250-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d7250-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d7250-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7250-127"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7250-127"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7250-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7250-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7250-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="d7250-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d7250-130">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="d7250-130">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="d7250-131">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="d7250-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




