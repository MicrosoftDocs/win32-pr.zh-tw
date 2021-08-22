---
description: 指定密碼編譯服務提供者 (CSP) ，以及用來建立數位簽章的私密金鑰資訊。
ms.assetid: 85dc6a06-365a-4591-9d1d-117556a4417d
title: SIGNER_PROVIDER_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_PROVIDER_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 45ab23e4a568082de7e7fb4d23364ac6ba15c0f61378d54735cbc398e7e0e8ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898685"
---
# <a name="signer_provider_info-structure"></a>簽署者 \_ 提供者 \_ 資訊結構

**簽署者 \_ 提供者 \_ 資訊** 結構會指定 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) ，以及用來建立數位簽章的私密金鑰資訊。

> [!Note]  
> 此結構未定義于任何標頭檔中。 若要使用這個結構，您必須自行定義，如本主題所示。

 

## <a name="syntax"></a>語法


```C++
typedef struct _SIGNER_PROVIDER_INFO {
  DWORD   cbSize;
  LPCWSTR pwszProviderName;
  DWORD   dwProviderType;
  DWORD   dwKeySpec;
  DWORD   dwPvkChoice;
  union {
    LPWSTR pwszPvkFileName;
    LPWSTR pwszKeyContainer;
  };
} SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

結構的大小（以位元組為單位）。

</dd> <dt>

**pwszProviderName**
</dt> <dd>

用來建立數位簽章的 CSP 名稱。 如果這個成員的值為 **Null**，則會使用預設提供者。

</dd> <dt>

**dwProviderType**
</dt> <dd>

**PwszProviderName** 成員所指定之 CSP 的型別。

</dd> <dt>

**dwKeySpec**
</dt> <dd>

金鑰規格。 如果這個成員設定為零，則會使用 **pwszPvkFileName** 或 **pwszKeyContainer** 成員中的金鑰規格。 如果 **pwszKeyContainer** 成員中有一個 **以上的索引鍵規格，則會 \_** 使用簽章。 如果失敗，則會使用 **\_ KEYEXCHANGE** 。

</dd> <dt>

**dwPvkChoice**
</dt> <dd>

指定私用金鑰資訊的類型。 這個成員可以是下列一或多個值。



| 值                                                                                                                                                                                                                                               | 意義                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="PVK_TYPE_FILE_NAME"></span><span id="pvk_type_file_name"></span><dl> <dt>**PVK \_輸入 \_ 檔案名 \_**</dt> <dt>1 (0x1)</dt> </dl>         | 私密金鑰資訊是檔案名。<br/>     |
| <span id="PVK_TYPE_KEYCONTAINER"></span><span id="pvk_type_keycontainer"></span><dl> <dt>**PVK \_輸入 \_ KEYCONTAINER**</dt> <dt>2 (0x2)</dt> </dl> | 私密金鑰資訊是金鑰容器。<br/> |



 

</dd> <dt>

**pwszPvkFileName**
</dt> <dd>

包含私用金鑰資訊的檔案名。

</dd> <dt>

**pwszKeyContainer**
</dt> <dd>

包含私密金鑰資訊的金鑰容器名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
