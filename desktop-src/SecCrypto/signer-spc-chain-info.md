---
description: 指定軟體發行者憑證 (SPC) ，以及用來簽署檔的憑證鏈。
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: SIGNER_SPC_CHAIN_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SPC_CHAIN_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60279a60e6cdfbf43a1e2d9c45735b885d97a055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115533"
---
# <a name="signer_spc_chain_info-structure"></a>簽署者 \_ SPC \_ 連鎖 \_ 資訊結構

**簽署者的 \_ spc \_ 鏈 \_ 資訊** 結構會指定 [*軟體發行者憑證*](../secgloss/s-gly.md) (SPC) ，以及用來簽署檔的憑證鏈。

> [!Note]  
> 此結構未定義于任何標頭檔中。 若要使用這個結構，您必須自行定義，如本主題所示。

 

## <a name="syntax"></a>語法


```C++
typedef struct _SIGNER_SPC_CHAIN_INFO {
  DWORD      cbSize;
  LPCWSTR    pwszSpcFile;
  DWORD      dwCertPolicy;
  HCERTSTORE hCertStore;
} SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

結構的大小（以位元組為單位）。

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

用來簽署檔的 SPC 檔案名稱。

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

 

 
