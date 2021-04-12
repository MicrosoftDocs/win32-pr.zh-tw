---
description: 指定媒體基礎轉換 (MFT) 的分類。
ms.assetid: cebd64ea-b20f-4ccc-805f-0deab3096bc3
title: 'MF_TRANSFORM_CATEGORY_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3c64fd5e19bba10646957e7c247294b6d82a97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191621"
---
# <a name="mf_transform_category_attribute-attribute"></a>MF \_ 轉換 \_ 類別目錄 \_ 屬性屬性

指定媒體基礎轉換 (MFT) 的分類。

## <a name="data-type"></a>資料類型

**GUID**

如需可能值的清單，請參閱 [**MFT \_ 類別目錄**](mft-category.md)。

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)。

## <a name="remarks"></a>備註

這個屬性是在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函數所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定的。

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

 

 




