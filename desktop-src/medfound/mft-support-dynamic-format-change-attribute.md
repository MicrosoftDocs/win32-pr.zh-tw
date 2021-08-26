---
description: 指定媒體基礎轉換 (MFT) 是否支援動態格式變更。
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: 'MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d9bfd2185006975cf128cc60f2b774eba6ba74229b3e290c743c4cde3930
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012608"
---
# <a name="mft_support_dynamic_format_change-attribute"></a>MFT \_ 支援 \_ 動態 \_ 格式 \_ 變更屬性

指定媒體基礎轉換 (MFT) 是否支援動態格式變更。

## <a name="data-type"></a>資料類型

**UINT32**

視為布林值。

## <a name="remarks"></a>備註

這個屬性可以具有下列值。



| 值     | 描述                                                            |
|-----------|------------------------------------------------------------------------|
| **TRUE**  | 用戶端可以在串流期間變更輸入格式。               |
| **FALSE** | 必須先清空 MFT，用戶端才能變更輸入格式。 |



 

若要取得這個屬性，請先呼叫 [**IMFTransform：： GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 來取得 MFT 的全域屬性存放區。 然後呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) 來取得屬性值。

如果 [**GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) 失敗或屬性不存在，則預設值為 **FALSE**。

[非同步 MFTs](asynchronous-mfts.md) 必須傳回 **TRUE** 值。

如需詳細資訊，請參閱 [處理資料流程變更](handling-stream-changes.md)。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[非同步 MFTs](asynchronous-mfts.md)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




