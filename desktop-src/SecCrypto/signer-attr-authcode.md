---
description: 指定 Authenticode 簽章的屬性。
ms.assetid: 1c1052c3-c5c5-48ae-8266-0b367800a84a
title: SIGNER_ATTR_AUTHCODE 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_ATTR_AUTHCODE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 952ed0f55a185d9a7ef9eeed3366f64c84423ddd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945394"
---
# <a name="signer_attr_authcode-structure"></a>簽署者 \_ ATTR \_ AUTHCODE 結構

**簽署者的 \_ ATTR \_ AUTHCODE** 結構會指定 [*Authenticode*](../secgloss/a-gly.md)簽章的屬性。

> [!Note]  
> 此結構未定義于任何標頭檔中。 若要使用這個結構，您必須自行定義，如本主題所示。

 

## <a name="syntax"></a>語法


```C++
typedef struct _SIGNER_ATTR_AUTHCODE {
  DWORD   cbSize;
  BOOL    fCommercial;
  BOOL    fIndividual;
  LPCWSTR pwszName;
  LPCWSTR pwszInfo;
} SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

結構的大小（以位元組為單位）。

</dd> <dt>

**fCommercial**
</dt> <dd>

**TRUE** 表示將主體簽署為商業發行者;否則 **為 FALSE**。

</dd> <dt>

**fIndividual**
</dt> <dd>

**TRUE** 表示以個別發行者的形式簽署主體;否則 **為 FALSE**。

</dd> <dt>

**pwszName**
</dt> <dd>

下載時檔案的顯示名稱。

</dd> <dt>

**pwszInfo**
</dt> <dd>

下載時檔案的 URL 顯示名稱。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**簽署人 \_ 簽名 \_ 資訊**](signer-signature-info.md)
</dt> </dl>

 

 
