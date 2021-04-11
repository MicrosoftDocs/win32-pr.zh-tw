---
description: 根據預設，CAPICOM 不會啟用憑證撤銷檢查。
ms.assetid: c6e2724c-1802-4bc4-a0e4-3cb85427a445
title: 檢查憑證撤銷狀態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada134bbca88b1a875ff27add7566116cf7334bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194035"
---
# <a name="checking-certificate-revocation-status"></a><span data-ttu-id="6cf09-103">檢查憑證撤銷狀態</span><span class="sxs-lookup"><span data-stu-id="6cf09-103">Checking Certificate Revocation Status</span></span>

<span data-ttu-id="6cf09-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="6cf09-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6cf09-105">相反地，請使用 .NET Framework 來執行安全性功能。</span><span class="sxs-lookup"><span data-stu-id="6cf09-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="6cf09-106">如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]</span><span class="sxs-lookup"><span data-stu-id="6cf09-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="6cf09-107">根據預設，CAPICOM 不會啟用憑證撤銷檢查。</span><span class="sxs-lookup"><span data-stu-id="6cf09-107">CAPICOM does not enable certificate revocation checking by default.</span></span> <span data-ttu-id="6cf09-108">不過，您可以透過憑證物件的 **IsValid. CheckFlag** 屬性，以程式設計的方式為特定的憑證啟用憑證撤銷檢查。</span><span class="sxs-lookup"><span data-stu-id="6cf09-108">However, certificate revocation checking can be enabled programmatically for a particular certificate through the **IsValid.CheckFlag** property of a Certificate object.</span></span> <span data-ttu-id="6cf09-109">設定適當的 **CheckFlag** 值之後，存取憑證物件的 **IsValid. Result** 屬性，或使用連鎖物件的組建方法建立憑證的驗證路徑，會強制執行撤銷檢查。</span><span class="sxs-lookup"><span data-stu-id="6cf09-109">After the appropriate value of **CheckFlag** has been set, accessing the Certificate object's **IsValid.Result** property or building the certificate's verification path using a Chain object's Build method forces revocation checking.</span></span>

<span data-ttu-id="6cf09-110">在下列範例中，cert 已具現化為有效的 CAPICOM 憑證。</span><span class="sxs-lookup"><span data-stu-id="6cf09-110">In the following example, cert has been instantiated as a valid CAPICOM certificate.</span></span>


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



<span data-ttu-id="6cf09-111">上述內容適用于個別憑證，不論取得的方式為何。</span><span class="sxs-lookup"><span data-stu-id="6cf09-111">The preceding applies to an individual certificate, no matter how it was obtained.</span></span> <span data-ttu-id="6cf09-112">對 [**SignedData**](signeddata.md) 物件中的憑證執行撤銷檢查並無不同，因為 **SignedData** 物件的 [**Verify**](signeddata-verify.md) 方法無法用於此用途，因為啟用 CAPICOM 驗證簽 \_ 章 \_ \_ 和 \_ 憑證不會造成 CRL 檢查。</span><span class="sxs-lookup"><span data-stu-id="6cf09-112">Performing revocation checking on the certificates in a [**SignedData**](signeddata.md) object is no different because the **SignedData** object's [**Verify**](signeddata-verify.md) method cannot be used for this purpose because enabling CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE does not cause CRL checking.</span></span>

<span data-ttu-id="6cf09-113">相反地，您必須為每個簽署者的憑證設定 **CheckFlag** 。</span><span class="sxs-lookup"><span data-stu-id="6cf09-113">Instead, the **CheckFlag** must be set for each signer's certificate.</span></span> <span data-ttu-id="6cf09-114">請考慮下列範例，其中已將 .Sdata 具現化為有效的 CAPICOM [**SignedData**](signeddata.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="6cf09-114">Consider the following example where sData has been instantiated as a valid CAPICOM [**SignedData**](signeddata.md) object.</span></span>


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



<span data-ttu-id="6cf09-115">另一個範例是 [**SignedData**](signeddata.md) 物件中所有憑證的迴圈。</span><span class="sxs-lookup"><span data-stu-id="6cf09-115">The additional example is the loop over all the certificates in the [**SignedData**](signeddata.md) object.</span></span>

 

 



