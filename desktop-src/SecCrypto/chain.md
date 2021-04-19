---
description: 代表憑證信任鏈。
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Chain 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fa3432767ccfdb60a2e3bc0a50ddbbcf565e0aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982574"
---
# <a name="chain-object"></a>Chain 物件

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Chain 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1)。\]

**Chain** 物件代表憑證信任鏈。

此物件提供屬性和方法，以建立憑證信任鏈來檢查憑證的有效性。 此鏈是使用 [**CertificateStatus CheckFlag**](certificatestatus-checkflag.md) 屬性值和 [**CertificateStatus**](certificatestatus.md) 物件的原則設定所建立。

**Chain** 物件會公開下列介面：

-   **IChain2**：在 CAPICOM 2.0 中引進。
-   **IChain**：在 CAPICOM 1.0 中引進。

## <a name="when-to-use"></a>使用時機

**Chain** 物件是用來執行下列工作：

-   建立憑證信任鏈。
-   取得所有憑證的 Oid，以及對此鏈有效的應用程式原則。
-   確認鏈中的憑證狀態。
-   取得擴充的錯誤資訊。
-   取得鏈中的憑證集合。

## <a name="members"></a>成員

**Chain** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Chain** 物件具有這些方法。



| 方法                                                   | 描述                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationPolicies**](chain-applicationpolicies.md) | 傳回 [**oid**](oids.md) 集合，這個集合表示對鏈有效的應用程式原則 oid。<br/>  (繼承自 **ChainIChain2**)                                                                                                                                                           |
| [**組建**](chain-build.md)                             | 從終端憑證建立憑證驗證鏈至受信任的 [*根憑證*](../secgloss/r-gly.md)，並傳回布林值，指出鏈的整體有效性。<br/>  (繼承自 **ChainIChain2IChain**)  |
| [**CertificatePolicies**](chain-certificatepolicies.md) | 傳回 [**oid**](oids.md) 集合，這個集合表示對鏈有效的憑證原則 oid。<br/>  (繼承自 **ChainIChain2**)                                                                                                                                                           |
| [**ExtendedErrorInfo**](chain-extendederrorinfo.md)     | 傳回字串，其中包含有關已編制索引之專案的其他錯誤資訊。<br/>  (繼承自 **ChainIChain2**)                                                                                                                                                                                  |



 

### <a name="properties"></a>屬性

**Chain** 物件具有這些屬性。



| 屬性                                              | 存取類型          | Description                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**憑證**](chain-certificates.md)<br/> | 唯讀<br/> | 抓取代表鏈中憑證的 [**憑證**](certificates.md) 集合。 這是預設屬性。<br/>  (繼承自 **ChainIChain2IChain**)  |
| [**狀態**](chain-status.md)<br/>             | 唯讀<br/> | 抓取鏈的有效狀態或鏈中的特定憑證。<br/>  (繼承自 **ChainIChain2IChain**)                                                        |



 

## <a name="remarks"></a>備註

您可以建立 **Chain** 物件，並且可以安全地進行腳本處理。 **連鎖店** 物件的 ProgID 為 "CAPICOM。Chain 2」。

**CAPICOM 1。*x*：** **Chain** 物件的 ProgID 是 CAPICOM。Chain. 1。

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
</dt> </dl>

 

 
