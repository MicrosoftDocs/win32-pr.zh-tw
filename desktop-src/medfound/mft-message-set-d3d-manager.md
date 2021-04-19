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
# <a name="mft_message_set_d3d_manager"></a>MFT \_ 訊息 \_ 集 \_ D3D \_ 管理員

設定或清除適用于 DirectX Video Accereration (DXVA) 的 [Direct3D 裝置管理員](direct3d-device-manager.md) 。

## <a name="message-parameter"></a>Message 參數

串流處理開始時， *ulParam* 參數會包含 **IUnknown** 指標。 此 MFT 會針對 Direct3D 9 的 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面以及 direct3d 11 的 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 介面查詢此指標。 當串流停止時， *ulParameter* 會包含 **Null** 值。

## <a name="remarks"></a>備註

若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。

此訊息只適用于影片轉換。 除非 ([mf \_ sa \_ D3D11 \_ 感知](mf-sa-d3d11-aware.md)Direct3D 11) 的 [**mf \_ sa \_ D3D \_ 感知**](mf-sa-d3d-aware-attribute.md)屬性，否則用戶端不應傳送此訊息。 

請勿將此訊息傳送至具有多個輸出的 MFT。

### <a name="implementation"></a>實作

只有在 MFT 使用 DirectX Video 加速進行影片處理或解碼時，MFT 才應支援此訊息。

如果 MFT 支援此訊息，它也應該執行 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)方法，並針對 ( ([mf \_ sa \_ D3D11 \_ 感知](mf-sa-d3d11-aware.md)) 的 mf [**\_ sa \_ D3D \_ 感知**](mf-sa-d3d-aware-attribute.md)屬性傳回 **TRUE** 值。 這個屬性會通知用戶端，用戶端應該在串流處理開始之前，將 **mft \_ 訊息 \_ 集 \_ D3D \_ 管理員** 訊息傳送到 mft。

如果 MFT 不支援此訊息，它應該會傳回來自 [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)的 **E \_ >notimpl** 。 這是一個例外狀況，也就是 MFT 可以從其所忽略的任何訊息傳回 **S \_ OK** 。

如需詳細資訊，請參閱 [Direct3D 感知 MFTs](direct3d-aware-mfts.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 感知 MFTs](direct3d-aware-mfts.md)
</dt> <dt>

[媒體基礎中支援 DXVA 2。0](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[支援媒體基礎中的 Direct3D 11 影片解碼](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> <dt>

[**MFT \_ 訊息 \_ 類型**](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




