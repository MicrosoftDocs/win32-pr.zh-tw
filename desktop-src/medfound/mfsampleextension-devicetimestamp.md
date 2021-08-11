---
description: 包含設備磁碟機的時間戳記。
ms.assetid: 8904d104-ebcc-474d-b6b5-b262b6f62ee9
title: 'MFSampleExtension_DeviceTimestamp 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3322f295908ae2bbdc095a21ab57ee2e0f2ed10dd2267eaea227b9248ddc226b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241123"
---
# <a name="mfsampleextension_devicetimestamp-attribute"></a>MFSampleExtension \_ DeviceTimestamp 屬性

包含設備磁碟機的時間戳記。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)。

## <a name="applies-to"></a>適用於

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>備註

這個屬性是在由捕獲裝置的媒體來源所建立的媒體範例上設定的。 這個屬性的值是在 [**MFTIME**](mftime.md) 網域中，與 query 效能計數器共用 EPOCH (QPC) 時間，而且一律以100ns 單位表示。 這個屬性可用於插入至 capture 管線的 MFTs。

若要取得相對於資料流程開頭的時間戳記，請呼叫 [**IMFSample：： GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) 方法。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體基礎中的音訊/影片捕獲](audio-video-capture-in-media-foundation.md)
</dt> <dt>

[範例屬性](sample-attributes.md)
</dt> </dl>

 

 




