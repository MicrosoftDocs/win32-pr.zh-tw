---
description: 包含媒體基礎轉換 (MFT) 的已註冊輸入類型。
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: 'MFT_INPUT_TYPES_Attributes 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c42a051c124cdb96e57ea239c02ebaa47f22e0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512605"
---
# <a name="mft_input_types_attributes-attribute"></a>MFT \_ 輸入 \_ 類型 \_ 屬性屬性

包含媒體基礎轉換 (MFT) 的已註冊輸入類型。

## <a name="data-type"></a>資料類型

**MFT \_儲存 \_ 為 \_ \[ \]** **位元組 \[ 的註冊類型 \]** 資訊

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。

## <a name="remarks"></a>備註

這個屬性是在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函數所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定的。

此屬性包含 [**mft 登錄 \_ \_ 類型 \_ 資訊**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) 結構的陣列，其描述 mft 所支援的一或多個輸入格式。 這些值會從登錄中取得，並作為應用程式的提示。 MFT 可能會支援其他格式。 若要設定實際的輸入格式，您必須建立 MFT 並呼叫 [**IMFTransform：： SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)。

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

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 




