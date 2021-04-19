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
# <a name="mf_sa_d3d_aware-attribute"></a>MF \_ SA \_ D3D \_ 感知屬性

指定媒體基礎轉換 (MFT) 是否支援 (DXVA) 的 DirectX Video 加速。 這個屬性只適用于影片 MFTs。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

若要查詢這個屬性，請呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 MFT 的全域屬性存放區。 如果 **GetAttributes** 成功，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

這個屬性會告知用戶端是否可以使用 Direct3D 9 影片：

-   如果屬性為非零，用戶端可以在串流處理開始之前，為 MFT 提供 [**IDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) 介面的指標。 若要這樣做，用戶端會將 [**mft \_ 訊息 \_ 集 \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md) 訊息傳送到 mft。 用戶端不需要傳送此訊息。
-   如果此屬性為零 (**FALSE**) ，則 MFT 不支援 Direct3D 9 video，而且用戶端不應將 [**mft \_ 訊息集的 \_ \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md) 訊息傳送到 mft。

這個屬性的預設值為 **FALSE**。 將此屬性視為唯讀。 請勿變更值;MFT 會忽略值的任何變更。

如需在自訂 MFT 中執行此屬性的詳細資訊，請參閱 [Direct3D 感知 MFTs](direct3d-aware-mfts.md)。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="examples"></a>範例

下列程式碼會測試 MFT 是否支援 DXVA。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                    |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Direct3D 感知 MFTs](direct3d-aware-mfts.md)
</dt> <dt>

[媒體基礎中支援 DXVA 2。0](supporting-dxva-2-0-in-media-foundation.md)
</dt> <dt>

[媒體基礎轉換](media-foundation-transforms.md)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[MF \_ 拓撲 \_ DXVA \_ 模式](mf-topology-dxva-mode.md)
</dt> </dl>

 

 




