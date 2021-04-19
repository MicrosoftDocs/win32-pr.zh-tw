---
description: 指定媒體基礎轉換 (MFT) 是否支援 (DXVA) 的 DirectX Video 加速。 這個屬性只適用于影片 MFTs。
ms.assetid: db6a8b20-fda0-4ffe-b1b5-a77b7604d290
title: 'MF_SA_D3D_AWARE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eb0de8c5a66eaa89f66becf6770f69e6449c1c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979807"
---
# <a name="mf_sa_d3d_aware-attribute"></a><span data-ttu-id="4c537-104">MF \_ SA \_ D3D \_ 感知屬性</span><span class="sxs-lookup"><span data-stu-id="4c537-104">MF\_SA\_D3D\_AWARE attribute</span></span>

<span data-ttu-id="4c537-105">指定媒體基礎轉換 (MFT) 是否支援 (DXVA) 的 DirectX Video 加速。</span><span class="sxs-lookup"><span data-stu-id="4c537-105">Specifies whether a Media Foundation transform (MFT) supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="4c537-106">這個屬性只適用于影片 MFTs。</span><span class="sxs-lookup"><span data-stu-id="4c537-106">This attribute applies only to video MFTs.</span></span>

## <a name="data-type"></a><span data-ttu-id="4c537-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="4c537-107">Data type</span></span>

<span data-ttu-id="4c537-108">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="4c537-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4c537-109">備註</span><span class="sxs-lookup"><span data-stu-id="4c537-109">Remarks</span></span>

<span data-ttu-id="4c537-110">若要查詢這個屬性，請呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 MFT 的全域屬性存放區。</span><span class="sxs-lookup"><span data-stu-id="4c537-110">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="4c537-111">如果 **GetAttributes** 成功，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="4c537-111">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="4c537-112">這個屬性會告知用戶端是否可以使用 Direct3D 9 影片：</span><span class="sxs-lookup"><span data-stu-id="4c537-112">This attribute tells the client whether the MFT can use Direct3D 9 video:</span></span>

-   <span data-ttu-id="4c537-113">如果屬性為非零，用戶端可以在串流處理開始之前，為 MFT 提供 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="4c537-113">If the attribute is nonzero, the client can give the MFT a pointer to the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface before streaming starts.</span></span> <span data-ttu-id="4c537-114">若要這樣做，用戶端會將 [**mft \_ 訊息 \_ 集 \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md) 訊息傳送到 mft。</span><span class="sxs-lookup"><span data-stu-id="4c537-114">To do so, the client sends the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span> <span data-ttu-id="4c537-115">用戶端不需要傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="4c537-115">The client is not required to send this message.</span></span>
-   <span data-ttu-id="4c537-116">如果此屬性為零 (**FALSE**) ，則 MFT 不支援 Direct3D 9 video，而且用戶端不應將 [**mft \_ 訊息集的 \_ \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md) 訊息傳送到 mft。</span><span class="sxs-lookup"><span data-stu-id="4c537-116">If this attribute is zero (**FALSE**), the MFT does not support Direct3D 9 video, and the client should not send the [**MFT\_MESSAGE\_SET\_D3D\_MANAGER**](mft-message-set-d3d-manager.md) message to the MFT.</span></span>

<span data-ttu-id="4c537-117">這個屬性的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="4c537-117">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="4c537-118">將此屬性視為唯讀。</span><span class="sxs-lookup"><span data-stu-id="4c537-118">Treat this attribute as read-only.</span></span> <span data-ttu-id="4c537-119">請勿變更值;MFT 會忽略值的任何變更。</span><span class="sxs-lookup"><span data-stu-id="4c537-119">Do not change the value; the MFT will ignore any changes to the value.</span></span>

<span data-ttu-id="4c537-120">如需在自訂 MFT 中執行此屬性的詳細資訊，請參閱 [Direct3D 感知 MFTs](direct3d-aware-mfts.md)。</span><span class="sxs-lookup"><span data-stu-id="4c537-120">For more information about implementing this attribute in a custom MFT, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

<span data-ttu-id="4c537-121">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="4c537-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="4c537-122">範例</span><span class="sxs-lookup"><span data-stu-id="4c537-122">Examples</span></span>

<span data-ttu-id="4c537-123">下列程式碼會測試 MFT 是否支援 DXVA。</span><span class="sxs-lookup"><span data-stu-id="4c537-123">The following code tests whether an MFT supports DXVA.</span></span>


```C++
// Returns TRUE is an MFT supports DirectX Video Acceleration.

BOOL IsTransformD3DAware(IMFTransform *pMFT)
{
    BOOL bD3DAware = FALSE;
    
    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMFT->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        bD3DAware = MFGetAttributeUINT32(pAttributes, MF_SA_D3D_AWARE, FALSE);
        pAttributes->Release();
    }
    return bD3DAware;
}
```



## <a name="requirements"></a><span data-ttu-id="4c537-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c537-124">Requirements</span></span>



| <span data-ttu-id="4c537-125">需求</span><span class="sxs-lookup"><span data-stu-id="4c537-125">Requirement</span></span> | <span data-ttu-id="4c537-126">值</span><span class="sxs-lookup"><span data-stu-id="4c537-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c537-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c537-127">Minimum supported client</span></span><br/> | <span data-ttu-id="4c537-128">Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c537-128">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                    |
| <span data-ttu-id="4c537-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c537-129">Minimum supported server</span></span><br/> | <span data-ttu-id="4c537-130">Windows Server 2008 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4c537-130">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="4c537-131">標頭</span><span class="sxs-lookup"><span data-stu-id="4c537-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c537-132"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="4c537-132"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c537-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c537-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c537-134">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="4c537-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c537-135">Direct3D 感知 MFTs</span><span class="sxs-lookup"><span data-stu-id="4c537-135">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="4c537-136">媒體基礎中支援 DXVA 2。0</span><span class="sxs-lookup"><span data-stu-id="4c537-136">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="4c537-137">媒體基礎轉換</span><span class="sxs-lookup"><span data-stu-id="4c537-137">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="4c537-138">轉換屬性</span><span class="sxs-lookup"><span data-stu-id="4c537-138">Transform Attributes</span></span>](transform-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c537-139">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4c537-139">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4c537-140">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4c537-140">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="4c537-141">MF \_ 拓撲 \_ DXVA \_ 模式</span><span class="sxs-lookup"><span data-stu-id="4c537-141">MF\_TOPOLOGY\_DXVA\_MODE</span></span>](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




