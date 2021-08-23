---
description: 提供憑證的金鑰使用方式屬性的唯讀存取。
ms.assetid: 8b8e9076-1a4f-4383-ac4b-1322d52949f0
title: KeyUsage 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 37b1e33ccb92b2d46effa9f0575f0331fa064e79d172715b8746355d5e99d2b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622268"
---
# <a name="keyusage-object"></a>KeyUsage 物件

\[**KeyUsage** 物件可用於 [需求] 區段中指定的作業系統。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]

**KeyUsage** 物件提供對憑證的金鑰使用方式屬性的唯讀存取。

## <a name="members"></a>成員

**KeyUsage** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**KeyUsage** 物件具有這些屬性。



| 屬性                                                                           | 存取類型          | 描述                                                                                                                                 |
|:-----------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCritical**](keyusage-iscritical.md)<br/>                               | 唯讀<br/> | 抓取布林值，指出 **KeyUsage** 延伸模組是否標記為重大。<br/>                                  |
| [**IsCRLSignEnabled**](keyusage-iscrlsignenabled.md)<br/>                   | 唯讀<br/> | 抓取布林值，指出是否已設定 CRLSign 位。<br/>                                                         |
| [**IsDataEnciphermentEnabled**](keyusage-isdataenciphermentenabled.md)<br/> | 唯讀<br/> | 抓取布林值，指出是否已設定 dataEncipherment 位。<br/>                                                |
| [**IsDecipherOnlyEnabled**](keyusage-isdecipheronlyenabled.md)<br/>         | 唯讀<br/> | 抓取布林值，指出是否已設定 decipherOnly 位。<br/>                                                    |
| [**IsDigitalSignatureEnabled**](keyusage-isdigitalsignatureenabled.md)<br/> | 唯讀<br/> | 抓取布林值，指出是否已設定 digitalSignature 位。<br/>                                                |
| [**IsEncipherOnlyEnabled**](keyusage-isencipheronlyenabled.md)<br/>         | 唯讀<br/> | 抓取布林值，指出是否已設定 encipherOnly 位。<br/>                                                    |
| [**IsKeyAgreementEnabled**](keyusage-iskeyagreementenabled.md)<br/>         | 唯讀<br/> | 抓取布林值，指出是否已設定 keyAgreement 位。<br/>                                                    |
| [**IsKeyCertSignEnabled**](keyusage-iskeycertsignenabled.md)<br/>           | 唯讀<br/> | 抓取布林值，指出是否已設定 keyCertSign 位。<br/>                                                     |
| [**IsKeyEnciphermentEnabled**](keyusage-iskeyenciphermentenabled.md)<br/>   | 唯讀<br/> | 抓取布林值，指出是否已設定 keyEncipherment 位。<br/>                                                 |
| [**IsNonRepudiationEnabled**](keyusage-isnonrepudiationenabled.md)<br/>     | 唯讀<br/> | 抓取布林值，指出是否已設定 nonRepudiationEnabled 位。<br/>                                           |
| [**IsPresent**](keyusage-ispresent.md)<br/>                                 | 唯讀<br/> | 抓取布林值，指出 **KeyUsage** 延伸是否存在。<br/> 這是預設屬性。<br/> |



 

## <a name="remarks"></a>備註

無法建立 **KeyUsage** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
