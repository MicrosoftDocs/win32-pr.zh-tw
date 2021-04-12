---
description: 指定媒體基礎轉換 (MFT) 是否支援 Microsoft Direct3D 11。
ms.assetid: 23482B8A-58F3-4B39-9C6D-54EC27D36C01
title: 'MF_SA_D3D11_AWARE 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d90f560e3d31b80c1b3fbcbb5c25c4e20815f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318647"
---
# <a name="mf_sa_d3d11_aware-attribute"></a>MF \_ SA \_ D3D11 \_ 感知屬性

指定媒體基礎轉換 (MFT) 是否支援 Microsoft Direct3D 11。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

這個屬性只適用于影片 MFTs。 若要查詢這個屬性，請呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 MFT 屬性存放區。 如果 **GetAttributes** 成功，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

-   如果屬性為非零，用戶端可以在串流處理開始之前，為 MFT 提供 [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) 介面的指標。 若要這樣做，用戶端會將 [**mft \_ 訊息 \_ 集 \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md) 訊息傳送到 mft。 用戶端不需要傳送此訊息。
-   如果此屬性為零 (**FALSE**) ，則 MFT 不支援 Direct3D 11，而且用戶端不應該將 [**mft \_ 訊息集的 \_ \_ D3D \_ 管理員**](mft-message-set-d3d-manager.md) 訊息傳送到 mft。

這個屬性的預設值為 **FALSE**。 將此屬性視為唯讀。 請勿變更值;MFT 會忽略值的任何變更。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[ desktop app \| UWP 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[支援媒體基礎中的 Direct3D 11 影片解碼](supporting-direct3d-11-video-decoding-in-media-foundation.md)
</dt> </dl>

 

 




