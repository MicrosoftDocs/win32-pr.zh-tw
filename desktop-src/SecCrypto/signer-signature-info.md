---
description: 包含數位簽章的相關資訊。
ms.assetid: 0b86fdf9-533f-4640-8c70-c3c8f4ef2c68
title: SIGNER_SIGNATURE_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SIGNATURE_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8e2b1fa68da51a649a01d4356ebfb1519ceeffb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104192947"
---
# <a name="signer_signature_info-structure"></a>簽署人 \_ 簽名 \_ 資訊結構

**簽署者簽章 \_ \_ 資訊** 結構包含數位簽章的相關資訊。

> [!Note]  
> 此結構未定義于任何標頭檔中。 若要使用這個結構，您必須自行定義，如本主題所示。

 

## <a name="syntax"></a>語法


```C++
typedef struct _SIGNER_SIGNATURE_INFO {
  DWORD             cbSize;
  ALG_ID            algidHash;
  DWORD             dwAttrChoice;
  union {
    SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
  };
  PCRYPT_ATTRIBUTES psAuthenticated;
  PCRYPT_ATTRIBUTES psUnauthenticated;
} SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

結構的大小（以位元組為單位）。

</dd> <dt>

**algidHash**
</dt> <dd>

用於數位簽章的雜湊演算法。

</dd> <dt>

**dwAttrChoice**
</dt> <dd>

指定簽章是否有 [*Authenticode*](../secgloss/a-gly.md) 屬性。 這個成員可以是下列一或多個值。



| 值                                                                                                                                                                                                                                      | 意義                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_AUTHCODE_ATTR"></span><span id="signer_authcode_attr"></span><dl> <dt>**簽署者 \_AUTHCODE \_ ATTR**</dt> <dt>1</dt> </dl> | 簽名具有 [*Authenticode*](../secgloss/a-gly.md) 屬性。<br/>           |
| <span id="SIGNER_NO_ATTR"></span><span id="signer_no_attr"></span><dl> <dt>**簽署者 \_沒有 \_ ATTR**</dt> <dt>0</dt> </dl>                   | 簽章沒有 [*Authenticode*](../secgloss/a-gly.md) 屬性。<br/> |



 

</dd> <dt>

**pAttrAuthcode**
</dt> <dd>

指定 [*Authenticode*](../secgloss/a-gly.md) 簽章的屬性。 如果 **dwAttrChoice** 成員的值為 **簽署者 \_ AUTHCODE \_ ATTR**，則需要這個成員。

</dd> <dt>

**psAuthenticated**
</dt> <dd>

已驗證的使用者提供屬性已新增至數位簽章。

</dd> <dt>

**psUnauthenticated**
</dt> <dd>

未驗證的使用者提供屬性已新增至數位簽章。

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

 

 
