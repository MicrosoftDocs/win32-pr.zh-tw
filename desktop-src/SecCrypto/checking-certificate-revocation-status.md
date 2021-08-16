---
description: 根據預設，CAPICOM 不會啟用憑證撤銷檢查。
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: 檢查憑證撤銷狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf1ce98e392da94fd800316fe63c5b79c8572a319c6db4246e7907eb80966d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769537"
---
# <a name="checking-certificate-revocation-status"></a>檢查憑證撤銷狀態

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]

根據預設，CAPICOM 不會啟用憑證撤銷檢查。 不過，您可以透過憑證物件的 **IsValid. CheckFlag** 屬性，以程式設計的方式為特定的憑證啟用憑證撤銷檢查。 設定適當的 **CheckFlag** 值之後，存取憑證物件的 **IsValid. Result** 屬性，或使用連鎖物件的組建方法建立憑證的驗證路徑，會強制執行撤銷檢查。

在下列範例中，cert 已具現化為有效的 CAPICOM 憑證。


```VB
Dim cert As Certificate
Dim LocalStore As New Store

' Open the My store.
LocalStore.Open LocalStore.Open CAPICOM_CURRENT_USER_STORE, _
    CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_WRITE

' Get the first certificate in the My store.
set cert = LocalStore.Certificates.Item(1)

cert.IsValid.CheckFlag = CAPICOM_CHECK_TRUSTED_ROOT Or _ 
   CAPICOM_CHECK_TIME_VALIDITY Or _ 
   CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
   CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
If cert.IsValid.Result Then
'CERTIFICATE IS VALID!
Else
Dim chain As New Chain
     chain.Build (cert)
     If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
     End If
     If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
'THE REVOCATION STATUS COULD NOT BE DETERMINED
     End If
End If

```



上述內容適用于個別憑證，不論取得的方式為何。 對 [**SignedData**](signeddata.md) 物件中的憑證執行撤銷檢查並無不同，因為 **SignedData** 物件的 [**Verify**](signeddata-verify.md) 方法無法用於此用途，因為啟用 CAPICOM 驗證簽 \_ 章 \_ \_ 和 \_ 憑證不會造成 CRL 檢查。

相反地，您必須為每個簽署者的憑證設定 **CheckFlag** 。 請考慮下列範例，其中已將 .Sdata 具現化為有效的 CAPICOM [**SignedData**](signeddata.md) 物件。


```VB
Dim cert As Certificate
Dim chain As New Chain

' sData is an existing SignedData object.

For I = 1 To sData.Certificates.Count
   set cert = sData.Certificates(I) 
   cert.IsValid.CheckFlag = _ 
       CAPICOM_CHECK_TRUSTED_ROOT Or _ 
       CAPICOM_CHECK_TIME_VALIDITY Or _ 
       CAPICOM_CHECK_SIGNATURE_VALIDITY Or _ 
       CAPICOM_CHECK_ONLINE_REVOCATION_STATUS
   If cert.IsValid.Result Then
      'THE CERTIFICATE IS VALID!
   Else
      chain.Build cert
      If CAPICOM_TRUST_IS_REVOKED And chain.Status Then
         'AT LEAST ONE CERTIFICATE IN THE CHAIN HAS BEEN REVOKED
      End If
      If CAPICOM_TRUST_REVOCATION_STATUS_UNKNOWN And chain.Status Then
         'THE REVOCATION STATUS COULD NOT BE DETERMINED
      End If
   End If
Next I
```



另一個範例是 [**SignedData**](signeddata.md) 物件中所有憑證的迴圈。

 

 



