---
description: 包含如何建立憑證信任鏈的相關資訊。
ms.assetid: 120cd79e-7c9b-45f3-8596-091b674e73d8
title: CertificateStatus 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c0c228a06da9d0a4dd93491908af0c0a2d0693125be57b675ca64e10378f253
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769995"
---
# <a name="certificatestatus-object"></a>CertificateStatus 物件

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]

**CertificateStatus** 物件包含如何建立憑證信任鏈的相關資訊。

## <a name="members"></a>成員

**CertificateStatus** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**CertificateStatus** 物件有這些方法。



| 方法                                                               | 描述                                                                                                                                  |
|:---------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationPolicies**](certificatestatus-applicationpolicies.md) | 傳回 [**oid**](oids.md) 集合，表示應用程式原則 oid。<br/>                                           |
| [**CertificatePolicies**](certificatestatus-certificatepolicies.md) | 傳回 [**oid**](oids.md) 集合，這個集合表示在鏈大樓期間使用的憑證原則 oid。<br/>                |
| [**EKU**](certificatestatus-eku.md)                                 | 傳回 [**eku**](eku.md) 物件，用來設定要檢查的 eku 元素，以建立憑證的有效狀態。<br/> |



 

### <a name="properties"></a>屬性

**CertificateStatus** 物件具有這些屬性。



| 屬性                                                                        | 存取類型           | Description                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**憑證**](certificatestatus-certificates.md)<br/>               | 讀取/寫入<br/> | 設定或抓取可以用來建立憑證鏈的憑證集合。<br/> **CAPICOM 2.0.0.3 和更早版本：** 不支援 [ [**憑證**](certificatestatus-certificates.md) ] 屬性。<br/>                    |
| [**CheckFlag**](certificatestatus-checkflag.md)<br/>                     | 讀取/寫入<br/> | 有效性檢查旗標。 您可以使用邏輯 **OR** 運算子來聯結值。 預設核取旗標為 [ [**\_ \_ 線上 \_ 所有的 CAPICOM 檢查**](capicom-check-flag.md)]。<br/>                                                                                     |
| [**結果**](certificatestatus-result.md)<br/>                           | 唯讀<br/>  | 指出憑證是否有效。 使用 [**CheckFlag**](certificatestatus-checkflag.md) 屬性的目前設定和憑證的原則設定，檢查憑證的有效性。 這是預設屬性。<br/> |
| [**UrlRetrievalTimeout**](certificatestatus-urlretrievaltimeout.md)<br/> | 讀取/寫入<br/> | 設定或抓取 URL 判定為無法存取之前的時間長度。<br/>                                                                                                                                                                     |
| [**VerificationTime**](certificatestatus-verificationtime.md)<br/>       | 讀取/寫入<br/> | 設定或抓取憑證驗證的時間。<br/>                                                                                                                                                                                          |



 

## <a name="remarks"></a>備註

無法建立 **CertificateStatus** 物件。

**CertificateStatus** 物件是由 [**Certificate. IsValid**](certificate-isvalid.md)方法傳回。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> <dt>

[**鏈**](chain.md)
</dt> </dl>

 

 
