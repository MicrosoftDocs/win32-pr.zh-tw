---
title: IWMDRMLicense 介面
description: IWMDRMLicense 介面代表一或多個授權的清單。
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- IWMDRMLicense 介面 windows 媒體格式
- IWMDRMLicense 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 38aadbda7a0ab6e899e4100adb5ff03873a4dd683fcb8f5893c506033545d558
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847125"
---
# <a name="iwmdrmlicense-interface"></a>IWMDRMLicense 介面

**IWMDRMLicense** 介面代表一或多個授權的清單。

## <a name="members"></a>成員

**IWMDRMLicense** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IWMDRMLicense** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IWMDRMLicense** 介面具有這些方法。



| 方法                                                                                   | 描述                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPersist**](iwmdrmlicense-canpersist.md)                                           | 查詢授權是否可保存在本機授權存放區中。<br/>                                                                                                                                               |
| [**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)                                 | 使用目前授權的設定建立解密程式物件。<br/>                                                                                                                                                   |
| [**CreateEncryptor**](iwmdrmlicense-createencryptor.md)                                 | 使用目前授權的設定建立加密程式物件。<br/>                                                                                                                                                  |
| [**CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md)                     | 建立安全的解密子物件。 安全解密程式與一般解密程式不同，因為它會解密內容，然後根據此方法的參數中指定的設定重新加密。<br/> |
| [**GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md) | 抓取目前授權所設定的所有類比影片限制。<br/>                                                                                                                                                     |
| [**GetInclusionList**](iwmdrmlicense-getinclusionlist.md)                               | 抓取目前授權或授權鏈的整個包含清單。<br/>                                                                                                                                           |
| [**GetLicense**](iwmdrmlicense-getlicense.md)                                           | 以可延伸標記語言 (XML)  (XML) 或可延伸媒體許可權 (XMR) 資料的形式抓取授權。<br/>                                                                                                                        |
| [**GetLicenseProperty**](iwmdrmlicense-getlicenseproperty.md)                           | 從目前的授權抓取屬性。<br/>                                                                                                                                                                          |
| [**GetNext**](iwmdrmlicense-getnext.md)                                                 | 載入清單中下一個授權的相關資訊。<br/>                                                                                                                                                               |
| [**GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md)             | 抓取指派給授權 (OPLs) 之所有輸出保護層級的相關資訊。<br/>                                                                                                                                |
| [**PersistLicense**](iwmdrmlicense-persistlicense.md)                                   | 將目前的授權從暫時存放區儲存到永久本機授權存放區。<br/>                                                                                                                              |
| [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md)                               | 將授權清單重設為其原始狀態。<br/>                                                                                                                                                                          |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](drm-interfaces.md)
</dt> </dl>

 

