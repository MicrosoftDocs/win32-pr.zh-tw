---
description: 指定虛擬攝影機設定應用程式的應用程式套件系列名稱。
title: 'MF_VIRTUALCAMERA_APP_PACKAGE_FAMILY_NAME 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/24/2021
ms.openlocfilehash: e821a273c44b1d5c9e654e34bbfb928ea707cdc0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691845"
---
# <a name="mf_virtualcamera_app_package_family_name-attribute"></a>MF \_ VIRTUALCAMERA \_ 應用程式 \_ 套件 \_ 系列 \_ 名稱屬性

指定虛擬攝影機設定應用程式的應用程式套件系列名稱。 提供時，管線會將設定應用程式與虛擬攝影機建立關聯，並在相機設定頁面中提供啟動點。

## <a name="data-type"></a>資料類型

[MF_ATTRIBUTE_STRING](/windows/win32/api/mfobjects/ne-mfobjects-mf_attribute_type)

## <a name="remarks"></a>備註

虛擬攝影機自訂媒體來源會從媒體來源屬性存放區 [IMFMediaSourceEx：： GetSourceAttributes](/windows/win32/api/mfvirtualcamera/nf-mfvirtualcamera-imfvirtualcamera-getmediasource)公開此屬性。  

如果電腦上還沒有安裝設定應用程式，則會啟動存放區應用程式，並流覽至套件系列名稱所指定的應用程式頁面。 否則，系統會為使用者啟動已安裝的應用程式。


## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows組建22000<br/>                          |
| 最低支援的伺服器<br/> | Windows組建22000<br/>                      |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes：： SetString**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> 
</dl>
 




