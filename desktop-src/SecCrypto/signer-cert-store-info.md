---
description: 指定用來簽署檔的憑證存放區。
ms.assetid: aabad010-6fa3-4677-bd73-b8c52d68dbc8
title: SIGNER_CERT_STORE_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT_STORE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 197bd4855a7d2afec4c0b23662365e5f9197e302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998464"
---
# <a name="signer_cert_store_info-structure"></a>簽署者 \_ 證書 \_ 存儲 \_ 資訊結構

**簽署者 \_ 證書 \_ 存儲 \_ 資訊** 結構會指定用來簽署檔的憑證存放區。

> [!Note]  
> 此結構未定義于任何標頭檔中。 若要使用這個結構，您必須自行定義，如本主題所示。

 

## <a name="syntax"></a>語法


```C++
typedef struct _SIGNER_CERT_STORE_INFO {
  DWORD          cbSize;
  PCCERT_CONTEXT pSigningCert;
  DWORD          dwCertPolicy;
  HCERTSTORE     hCertStore;
} SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

結構的大小（以位元組為單位）。

</dd> <dt>

**pSigningCert**
</dt> <dd>

簽署憑證之憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 結構的指標。

</dd> <dt>

**dwCertPolicy**
</dt> <dd>

指定如何將憑證加入至簽章。 若要尋找憑證鏈，除了 **hCertStore** 成員所指定的存放區之外，還會檢查「我的」、「CA」、「根」和「SPC」存放區。 這個成員可以是下列一或多個值。



| 值                                                                                                                                                                                                                                                                                   | 意義                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <dt>**簽署者 \_CERT \_ POLICY \_ CHAIN**</dt> <dt>2 (0x2)</dt> </dl>                           | 只新增憑證鏈中的憑證。<br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <dt>**簽署者 \_CERT \_ POLICY \_ CHAIN \_ NO \_ ROOT**</dt> <dt>8 (0x8)</dt> </dl> | 只新增憑證鏈中的憑證，但不包含根憑證。<br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <dt>**簽署者 \_CERT \_ POLICY \_ STORE**</dt> <dt>1 (0x1)</dt> </dl>                           | 新增 **hCertStore** 成員所指定之存放區中的所有憑證。 此旗標可以是與此成員的任何其他可能值的位 **or** 組合。<br/> |



 

</dd> <dt>

**hCertStore**
</dt> <dd>

選擇性。 其他憑證存放區的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**簽署 \_ 者憑證**](signer-cert.md)
</dt> </dl>

 

 




