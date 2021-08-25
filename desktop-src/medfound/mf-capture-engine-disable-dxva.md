---
description: 指定捕捉引擎是否使用 DirectX Video 加速 (DXVA) 進行影片解碼。
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: 'MF_CAPTURE_ENGINE_DISABLE_DXVA 屬性 (Mfcaptureengine) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c722b70e1707e6ad5d14b7afca0da2c8d1a63b3a132345e727de1f37023916a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941008"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>MF \_ 捕獲 \_ 引擎 \_ 停用 \_ DXVA 屬性

指定捕捉引擎是否使用 DirectX Video 加速 (DXVA) 進行影片解碼。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="remarks"></a>備註

如果下列條件成立，則適用此屬性：

-   捕獲引擎會從捕獲裝置解碼壓縮的影片串流 (例如，如果捕捉裝置輸出 h.264 video) 。
-   影片解碼支援使用 DXVA 進行硬體加速解碼。
-   應用程式會使用「 [MF \_ 捕捉引擎」 \_ \_ D3D \_ 管理員](mf-capture-engine-d3d-manager.md) 屬性，在「捕獲引擎」上設定 DXGI 裝置管理員。

否則，會忽略這個屬性。

這個屬性可讓應用程式停用 DXVA，同時仍在對 Direct3D 介面進行解碼。

這個屬性的預設值為 **FALSE**，表示 DXVA 解碼會在可用時啟用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                         |
| 標頭<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Capture 引擎屬性](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine：： Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




