---
description: 包含以硬體為基礎的媒體基礎轉換 (MFT) 的符號連結。
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: 'MFT_ENUM_HARDWARE_URL_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192161"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a>MFT \_ 列舉 \_ 硬體 \_ URL \_ 屬性屬性

包含以硬體為基礎的媒體基礎轉換 (MFT) 的符號連結。

## <a name="data-type"></a>資料類型

**WCHAR \** _

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。

## <a name="remarks"></a>備註

以硬體為基礎的 MFTs 支援此屬性。 屬性的值是設備磁碟機的符號連結。 當這些指標代表以硬體為基礎的 MFTs 時，也會在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函數所配置的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定這個屬性。

符號連結應該視為不透明的字串。 若要取得裝置的顯示名稱，請查詢 [ [MFT \_ 易記 \_ 名稱](mft-friendly-name-attribute.md) ] 屬性。

軟體 MFTs 不應設定此屬性。

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

[硬體 MFTs](hardware-mfts.md)
</dt> <dt>

[轉換屬性](transform-attributes.md)
</dt> </dl>

 

 




