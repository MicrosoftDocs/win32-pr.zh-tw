---
title: EAPHost 和舊版架構
description: 描述用於建立設定 XML 和認證 XML 的 EAPHost 架構和舊版架構。
ms.assetid: d4572866-7e2b-4e7c-afe1-66394b549bc4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4eb9f09a0f1380ad0373ec1171b0b0ea9101af87335d25287969d9a5f7f2da9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984228"
---
# <a name="eaphost-and-legacy-schema"></a>EAPHost 和舊版架構

本主題說明用來建立設定 XML 和認證 XML 的 EAPHost 架構和舊版架構。

## <a name="about-eaphost-and-legacy-schema"></a>關於 EAPHost 和舊版架構

建立具有 [eaphostconfig](eaphostconfigschema-schema.md) 架構的設定 XML建立具有 [eaphostusercredentials](eaphostusercredentialsschema-schema.md) 架構的認證 XML。

有幾個原生和舊版架構包含通用的架構元素。 方法設定和方法認證中所使用的通用元素會抽象化成單一架構檔案，稱為「一般架構」。

"Method configuration" 和 "connection properties" 這兩個詞彙可交換使用。 同樣地，「方法認證」和「使用者屬性」等詞彙也會交替使用。

## <a name="eaphost-schema"></a>EAPHost 架構



| 結構描述                                                                        | 描述                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------|
| [baseeapmethodconfig](baseeapmethodconfigschema-schema.md)                   | 包含一般設定架構元素。     |
| [baseeapmethodusercredentials](baseeapmethodusercredentialsschema-schema.md) | 包含一般的認證架構元素。        |
| [eapcommon](eapcommonschema-schema.md)                                       | 包含 **EapMethodType** 元素定義。 |
| [eaphostconfig](eaphostconfigschema-schema.md)                               | 包含 EAPHost 設定架構。             |
| [eaphostusercredentials](eaphostusercredentialsschema-schema.md)             | 包含 EAPHost 認證架構。                |



 

## <a name="legacy-schema"></a>舊版架構



| 結構描述                                                                            | 描述                                                                                  |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md)   | 包含一般設定架構元素。                                               |
| [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md)               | 包含一般的認證架構元素。                                                  |
| [eapconnectionpropertiesv1](eapconnectionpropertiesv1schema-schema.md)           | 包含一般設定架構元素。                                               |
| [eapuserpropertiesv1](eapuserpropertiesv1schema-schema.md)                       | 包含一般的認證架構元素。                                                  |
| [eaptlsconnectionpropertiesv1](eaptlsconnectionpropertiesv1schema-schema.md)     | 使用 EAP-TLS 來描述驗證設定資料。                          |
| [eaptlsconnectionpropertiesv2](eaptlsconnectionpropertiesv2schema-schema.md)     | 使用 eap-tls 來描述從 Windows 7 開始的驗證設定資料。 |
| [eaptlsuserpropertiesv1](eaptlsuserpropertiesv1schema-schema.md)                 | 使用 EAP-TLS 來描述驗證認證和認證選項。          |
| [mschapv2connectionpropertiesv1](mschapv2connectionpropertiesv1schema-schema.md) | 可搭配 MS-CHAPv2 用來描述驗證設定資料。                        |
| [mschapv2userpropertiesv1](mschapv2userpropertiesv1schema-schema.md)             | 搭配 MS-CHAPv2 使用，以描述驗證認證和認證選項。        |
| [mspeapconnectionpropertiesv1](mspeapconnectionpropertiesv1schema-schema.md)     | 可搭配 PEAPv0 用來描述驗證設定資料。                           |
| [mspeapconnectionpropertiesv2](mspeapconnectionpropertiesv2schema-schema.md)     | 與 PEAPv0 搭配使用，以描述從 Windows 7 開始的驗證設定資料。  |
| [mspeapuserpropertiesv1](mspeapuserpropertiesv1schema-schema.md)                 | 與 PEAPv0 搭配使用，以描述驗證認證和認證選項。           |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[查看 EAPHost 和舊版架構範例](eaphost-schemas.md)
</dt> </dl>

 

 




