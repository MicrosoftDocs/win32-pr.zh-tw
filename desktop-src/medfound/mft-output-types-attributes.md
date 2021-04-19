---
description: 包含媒體基礎轉換 (MFT) 的已註冊輸出類型。
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: 'MFT_OUTPUT_TYPES_Attributes 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973708"
---
# <a name="mft_output_types_attributes-attribute"></a>MFT \_ 輸出 \_ 類型 \_ 屬性屬性

包含媒體基礎轉換 (MFT) 的已註冊輸出類型。

## <a name="data-type"></a>資料類型

**MFT \_儲存 \_ 為 \_ \[ \]** **位元組 \[ 的註冊類型 \]** 資訊

## <a name="remarks"></a>備註

這個屬性是在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函數所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定的。

此屬性包含 [**mft 登錄 \_ \_ 類型 \_ 資訊**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) 結構的陣列，其描述 mft 所支援的一或多個輸出格式。 這些值會從登錄中取得，並作為應用程式的提示。 MFT 可能會支援其他格式。 若要設定實際的輸出格式，您必須建立 MFT 並呼叫 [**IMFTransform：： SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)。

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

 

 




