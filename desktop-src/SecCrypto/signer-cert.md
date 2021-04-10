---
description: 指定用來簽署檔的憑證。 憑證可以儲存在軟體發行者憑證 (SPC) 檔或憑證存放區中。
ms.assetid: 9a99ce98-237d-4223-ab3d-0576041038e3
title: SIGNER_CERT 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CERT
api_type:
- NA
api_location: ''
ms.openlocfilehash: a14f955749e98ca34cda0be2c57a3d5c546afc41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194363"
---
# <a name="signer_cert-structure"></a>簽署者 \_ CERT 結構

**簽署者 \_ CERT** 結構會指定 [*用來*](../secgloss/c-gly.md)簽署檔的憑證。 憑證可以儲存在 [*軟體發行者憑證*](../secgloss/s-gly.md) (SPC) 檔或 [*憑證存放區*](../secgloss/c-gly.md)中。

> [!Note]  
> 此結構未定義于任何標頭檔中。 若要使用這個結構，您必須自行定義，如本主題所示。

 

## <a name="syntax"></a>語法


```C++
typedef struct _SIGNER_CERT {
  DWORD cbSize;
  DWORD dwCertChoice;
  union {
    LPCWSTR                pwszSpcFile;
    SIGNER_CERT_STORE_INFO *pCertStoreInfo;
    SIGNER_SPC_CHAIN_INFO  *pSpcChainInfo;
  };
  HWND  hwnd;
} SIGNER_CERT, *PSIGNER_CERT;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

結構的大小（以位元組為單位）。

</dd> <dt>

**dwCertChoice**
</dt> <dd>

指定憑證的儲存方式。 這個成員可以是下列一或多個值。



| 值                                                                                                                                                                                                                                          | 意義                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_SPC_FILE"></span><span id="signer_cert_spc_file"></span><dl> <dt>**簽署者 \_CERT \_ SPC \_ FILE**</dt> <dt>1</dt> </dl>    | 憑證會儲存在 SPC 檔案中。 **PwszSpcFile** 成員包含 SPC 檔案的路徑和檔案名。<br/>                                                                                                                                                  |
| <span id="SIGNER_CERT_STORE"></span><span id="signer_cert_store"></span><dl> <dt>**簽署者 \_證書 \_ 存儲**</dt> <dt>2</dt> </dl>              | 憑證會儲存在憑證存放區中。 **PCertStoreInfo** 成員包含 [**簽署者 \_ 證書 \_ 存儲 \_ 資訊**](signer-cert-store-info.md)結構的指標，此結構會指定儲存憑證的憑證存放區。<br/>                 |
| <span id="SIGNER_CERT_SPC_CHAIN"></span><span id="signer_cert_spc_chain"></span><dl> <dt>**簽署者 \_CERT \_ SPC \_ CHAIN**</dt> <dt>3</dt> </dl> | 憑證會儲存在 SPC 檔案中，並與憑證鏈相關聯。 **PSpcChainInfo** 成員包含 [**簽署者 \_ SPC \_ 連鎖 \_ 資訊**](signer-spc-chain-info.md)結構的指標，其中包含憑證的連鎖資訊。<br/> |



 

</dd> <dt>

**pwszSpcFile**
</dt> <dd>

以 null 終止的 Unicode 字串指標，其中包含儲存憑證之 SPC 檔案的路徑和檔案名。 只有當 **dwCertChoice** 成員包含 **簽署者憑證 \_ \_ SPC \_** 檔案時，才會使用這個成員。

</dd> <dt>

**pCertStoreInfo**
</dt> <dd>

[**簽署者 \_ 證書 \_ 存儲 \_ 資訊**](signer-cert-store-info.md)結構的指標，指定儲存憑證的憑證存放區。 只有當 **dwCertChoice** 成員包含「 **簽署人」 \_ 證書 \_ 存儲** 時，才會使用這個成員。

</dd> <dt>

**pSpcChainInfo**
</dt> <dd>

[**簽署者的 \_ SPC \_ 連鎖 \_ 資訊**](signer-spc-chain-info.md)結構的指標，其中包含憑證的鏈資訊。 只有在 **dwCertChoice** 成員包含 **簽署者憑證 \_ \_ SPC \_ 鏈** 時，才會使用這個成員。

</dd> <dt>

**hwnd**
</dt> <dd>

要做為顯示之任何對話方塊擁有者使用的視窗控制碼。 目前未使用這個成員，所以會忽略。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
