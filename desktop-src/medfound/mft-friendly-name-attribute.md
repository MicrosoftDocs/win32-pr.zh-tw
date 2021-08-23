---
description: 包含以硬體為基礎的媒體基礎轉換 (MFT) 的顯示名稱。
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: 'MFT_FRIENDLY_NAME_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b867db021c43679fef026022bf95bda1186a679eb544465393562b0a51d5d7af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554918"
---
# <a name="mft_friendly_name_attribute-attribute"></a>MFT \_ 易記 \_ 名稱 \_ 屬性屬性

包含以硬體為基礎的媒體基礎轉換 (MFT) 的顯示名稱。

## <a name="data-type"></a>資料類型

**WCHAR\***

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。

## <a name="remarks"></a>備註

以硬體為基礎的 MFTs 支援此屬性。 當這些指標代表以硬體為基礎的 MFTs 時，也會在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函式所配置的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定它。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 




