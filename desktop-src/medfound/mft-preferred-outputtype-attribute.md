---
description: 指定編碼器慣用的輸出格式。
ms.assetid: 36a09696-3fe7-41a0-93f1-712220f88b04
title: 'MFT_PREFERRED_OUTPUTTYPE_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13cd079bee65f5324987d9b38dca845ec5b85f83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848710"
---
# <a name="mft_preferred_outputtype_attribute-attribute"></a>MFT \_ 慣用 \_ OUTPUTTYPE \_ 屬性屬性

指定編碼器慣用的輸出格式。

## <a name="data-type"></a>資料類型

**[](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) IMFAttributes \** _ 儲存為 _*IUnknown \**_

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。

## <a name="applies-to"></a>適用於

[**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)

## <a name="remarks"></a>備註

這個屬性可以在 [**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate) 函數所傳回的啟用物件上設定。 只有在啟用物件設定為建立編碼器時，才會套用此屬性。 屬性的值是媒體類型。 啟用物件會在編碼器上設定此輸出類型。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**MFCreateTransformActivate**](/windows/desktop/api/mftransform/nf-mftransform-mfcreatetransformactivate)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 




