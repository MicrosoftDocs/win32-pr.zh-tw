---
description: 設定或清除適用于 DirectX Video Accereration (DXVA) 的 Direct3D 裝置管理員。
ms.assetid: fd346d56-1f80-488a-94c8-4e4e36d72890
title: 'MFT_MESSAGE_SET_D3D_MANAGER (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef8ecb5db474935bb25138a960b6df1c2109c16c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977256"
---
# <a name="mft_message_set_d3d_manager"></a><span data-ttu-id="99dcd-103">MFT \_ 訊息 \_ 集 \_ D3D \_ 管理員</span><span class="sxs-lookup"><span data-stu-id="99dcd-103">MFT\_MESSAGE\_SET\_D3D\_MANAGER</span></span>

<span data-ttu-id="99dcd-104">設定或清除適用于 DirectX Video Accereration (DXVA) 的 [Direct3D 裝置管理員](direct3d-device-manager.md) 。</span><span class="sxs-lookup"><span data-stu-id="99dcd-104">Sets or clears the [Direct3D Device Manager](direct3d-device-manager.md) for DirectX Video Accereration (DXVA).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="99dcd-105">Message 參數</span><span class="sxs-lookup"><span data-stu-id="99dcd-105">Message Parameter</span></span>

<span data-ttu-id="99dcd-106">串流處理開始時， *ulParam* 參數會包含 **IUnknown** 指標。</span><span class="sxs-lookup"><span data-stu-id="99dcd-106">When streaming begins, the *ulParam* parameter contains an **IUnknown** pointer.</span></span> <span data-ttu-id="99dcd-107">此 MFT 會針對 Direct3D 9 的 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面以及 direct3d 11 的 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 介面查詢此指標。</span><span class="sxs-lookup"><span data-stu-id="99dcd-107">The MFT will query this pointer for the [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) interface for Direct3D 9 and the [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) interface for Direct3D 11.</span></span> <span data-ttu-id="99dcd-108">當串流停止時， *ulParameter* 會包含 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="99dcd-108">When streaming stops, the *ulParameter* contains the value **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="99dcd-109">備註</span><span class="sxs-lookup"><span data-stu-id="99dcd-109">Remarks</span></span>

<span data-ttu-id="99dcd-110">若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。</span><span class="sxs-lookup"><span data-stu-id="99dcd-110">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="99dcd-111">此訊息只適用于影片轉換。</span><span class="sxs-lookup"><span data-stu-id="99dcd-111">This message applies only to video transforms.</span></span> <span data-ttu-id="99dcd-112">除非 ([mf \_ sa \_ D3D11 \_ 感知](mf-sa-d3d11-aware.md)Direct3D 11) 的 [**mf \_ sa \_ D3D \_ 感知**](mf-sa-d3d-aware-attribute.md)屬性，否則用戶端不應傳送此訊息。 </span><span class="sxs-lookup"><span data-stu-id="99dcd-112">The client should not send this message unless the MFT returns **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute ([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span>

<span data-ttu-id="99dcd-113">請勿將此訊息傳送至具有多個輸出的 MFT。</span><span class="sxs-lookup"><span data-stu-id="99dcd-113">Do not send this message to an MFT with multiple ouputs.</span></span>

### <a name="implementation"></a><span data-ttu-id="99dcd-114">實作</span><span class="sxs-lookup"><span data-stu-id="99dcd-114">Implementation</span></span>

<span data-ttu-id="99dcd-115">只有在 MFT 使用 DirectX Video 加速進行影片處理或解碼時，MFT 才應支援此訊息。</span><span class="sxs-lookup"><span data-stu-id="99dcd-115">An MFT should support this message only if the MFT uses DirectX Video Acceleration for video processing or decoding.</span></span>

<span data-ttu-id="99dcd-116">如果 MFT 支援此訊息，它也應該執行 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)方法，並針對 ( ([mf \_ sa \_ D3D11 \_ 感知](mf-sa-d3d11-aware.md)) 的 mf [**\_ sa \_ D3D \_ 感知**](mf-sa-d3d-aware-attribute.md)屬性傳回 **TRUE** 值。</span><span class="sxs-lookup"><span data-stu-id="99dcd-116">If an MFT supports this message, it should also implement the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method and return the value **TRUE** for the [**MF\_SA\_D3D\_AWARE**](mf-sa-d3d-aware-attribute.md) attribute (([MF\_SA\_D3D11\_AWARE](mf-sa-d3d11-aware.md) for Direct3D 11).</span></span> <span data-ttu-id="99dcd-117">這個屬性會通知用戶端，用戶端應該在串流處理開始之前，將 **mft \_ 訊息 \_ 集 \_ D3D \_ 管理員** 訊息傳送到 mft。</span><span class="sxs-lookup"><span data-stu-id="99dcd-117">This attribute informs the client that the client should send the **MFT\_MESSAGE\_SET\_D3D\_MANAGER** message to the MFT before streaming begins.</span></span>

<span data-ttu-id="99dcd-118">如果 MFT 不支援此訊息，它應該會傳回來自 [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)的 **E \_ >notimpl** 。</span><span class="sxs-lookup"><span data-stu-id="99dcd-118">If an MFT does not support this message, it should return **E\_NOTIMPL** from [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span> <span data-ttu-id="99dcd-119">這是一個例外狀況，也就是 MFT 可以從其所忽略的任何訊息傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="99dcd-119">This is an exception to the general rule that an MFT can return **S\_OK** from any message it ignores.</span></span>

<span data-ttu-id="99dcd-120">如需詳細資訊，請參閱 [Direct3D 感知 MFTs](direct3d-aware-mfts.md)。</span><span class="sxs-lookup"><span data-stu-id="99dcd-120">For more information, see [Direct3D-Aware MFTs](direct3d-aware-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="99dcd-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="99dcd-121">Requirements</span></span>



| <span data-ttu-id="99dcd-122">需求</span><span class="sxs-lookup"><span data-stu-id="99dcd-122">Requirement</span></span> | <span data-ttu-id="99dcd-123">值</span><span class="sxs-lookup"><span data-stu-id="99dcd-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="99dcd-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="99dcd-124">Minimum supported client</span></span><br/> | <span data-ttu-id="99dcd-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99dcd-125">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="99dcd-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="99dcd-126">Minimum supported server</span></span><br/> | <span data-ttu-id="99dcd-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="99dcd-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="99dcd-128">標頭</span><span class="sxs-lookup"><span data-stu-id="99dcd-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="99dcd-129"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="99dcd-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99dcd-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99dcd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99dcd-131">Direct3D 感知 MFTs</span><span class="sxs-lookup"><span data-stu-id="99dcd-131">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
</dt> <dt>

[<span data-ttu-id="99dcd-132">媒體基礎中支援 DXVA 2。0</span><span class="sxs-lookup"><span data-stu-id="99dcd-132">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="99dcd-133">支援媒體基礎中的 Direct3D 11 影片解碼</span><span class="sxs-lookup"><span data-stu-id="99dcd-133">Supporting Direct3D 11 Video Decoding in Media Foundation</span></span>](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="99dcd-134">**MFT \_ 訊息 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="99dcd-134">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




