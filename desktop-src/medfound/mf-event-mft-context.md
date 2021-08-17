---
description: 包含 METransformMarker 事件的呼叫端定義值。
ms.assetid: c6ab20d9-c2bc-43ba-a018-2c6682bf0485
title: 'MF_EVENT_MFT_CONTEXT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9518853030ec52a687f02ac0288c3fd3ffcf55b676be56c7036b349e1dec9aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104844"
---
# <a name="mf_event_mft_context-attribute"></a>MF \_ 事件 \_ MFT \_ 內容屬性

包含 [METransformMarker](metransformmarker.md) 事件的呼叫端定義值。

## <a name="data-type"></a>資料類型

**ULONG \_** 以 **UINT64** 形式儲存的 PTR

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)。

## <a name="applies-to"></a>適用於

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)

## <a name="remarks"></a>備註

這個屬性會與 [METransformMarker](metransformmarker.md) 事件一起使用。 屬性的值取自 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)方法的 *ulParam* 參數。

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

 

 




