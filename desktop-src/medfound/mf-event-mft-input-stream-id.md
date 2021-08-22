---
description: 指定媒體基礎轉換 (MFT) 的輸入資料流程。
ms.assetid: 2922af62-3fcc-4153-a26a-aba3c4121a0b
title: 'MF_EVENT_MFT_INPUT_STREAM_ID 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d211eb30280e6b7390df8509795d49567c7f8a8c9016b2825786858fe888b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973807"
---
# <a name="mf_event_mft_input_stream_id-attribute"></a>MF \_ 事件 \_ MFT \_ 輸入 \_ 資料流程 \_ 識別碼屬性

指定媒體基礎轉換 (MFT) 的輸入資料流程。

## <a name="data-type"></a>資料類型

**UINT32**

此值為輸入資料流程識別碼。

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>備註

這個屬性會搭配下列事件使用：

-   [METransformDrainComplete](metransformdraincomplete.md)
-   [METransformNeedInput](metransformneedinput.md)

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[非同步 MFTs](asynchronous-mfts.md)
</dt> <dt>

[事件屬性](event-attributes.md)
</dt> </dl>

 

 




