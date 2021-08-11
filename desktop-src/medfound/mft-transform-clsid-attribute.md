---
description: 包含 (MFT) 之媒體基礎轉換 (CLSID) 的類別識別碼。
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: 'MFT_TRANSFORM_CLSID_Attribute 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0122b783d8b321aa2a5c7788a589e19625b6a2bde8e37b0b659b0a1192f8c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240196"
---
# <a name="mft_transform_clsid_attribute-attribute"></a>MFT \_ 轉換 \_ CLSID \_ 屬性屬性

包含 (MFT) 之媒體基礎轉換 (CLSID) 的類別識別碼。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)。

## <a name="remarks"></a>備註

這個屬性是在 [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)函數所傳回的 [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)指標上設定的。

這個屬性會在建立 MFT 時由啟用物件在內部使用。 應用程式不應直接使用此 CLSID 來建立 MFT，因為啟用物件可能需要初始化 MFT。 因此，若要建立此 MFT 的實例，請在啟用物件上呼叫 [**IMFActivate：： ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) 。

請注意， [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) 函式的行為與此方面的 [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) 函式不同。 **MFTEnum** 函式會傳回 clsid，讓應用程式傳遞至 **CoCreateInstance** 函數。 **MFTEnumEx** 函式會傳回啟用物件而非 clsid。

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

 

 




