---
description: 指定在串流處理時，MFT 編碼器支援接收 MEEncodingParameter 事件。
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: 'MFT_ENCODER_SUPPORTS_CONFIG_EVENT 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a528da44d59077c8445616f8fe344cba5497ced8b33be75e33be71bf9b5d76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113038"
---
# <a name="mft_encoder_supports_config_event-attribute"></a>MFT \_ 編碼器 \_ 支援 \_ CONFIG \_ 事件屬性

指定在串流處理時，MFT 編碼器支援接收 [MEEncodingParameter](meencodingparameters.md) 事件。

## <a name="data-type"></a>資料類型

**Bool** 儲存為 **UINT32**

## <a name="remarks"></a>備註

由 MFT 編碼器透過 IMFTransform 傳送 [**：:P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012R2 \[ desktop apps \| UWP 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Mftransform .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFTransform：:P rocessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




