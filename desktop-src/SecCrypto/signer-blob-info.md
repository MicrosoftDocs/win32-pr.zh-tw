---
description: 指定要簽署的 BLOB。
ms.assetid: 214c9c05-5c95-4803-8993-23a87266f991
title: SIGNER_BLOB_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_BLOB_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: a865a65b5fd9a1ec658dcc86b1eb2b3dd255804308f04bebf4fffdb0650d71e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898925"
---
# <a name="signer_blob_info-structure"></a>簽署者 \_ BLOB \_ 資訊結構

\[您可以在 [需求] 區段中指定的作業系統中使用 **簽署者 \_ BLOB \_ 資訊** 結構。 它在後續版本中可能會變更或無法使用。\]

**簽署者 \_ BLOB \_ 資訊** 結構會指定要簽署的 [*blob*](../secgloss/b-gly.md) 。

> [!Note]  
> 此結構未定義于任何標頭檔中。 若要使用這個結構，您必須自行定義，如本主題所示。

 

## <a name="syntax"></a>語法


```C++
typedef struct _SIGNER_BLOB_INFO {
  DWORD   cbSize;
  GUID    *pGuidSubject;
  DWORD   cbBlob;
  BYTE    *pbBlob;
  LPCWSTR pwszDisplayName;
} SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

結構的大小（以位元組為單位）。

</dd> <dt>

**pGuidSubject**
</dt> <dd>

**GUID** 的指標，指定要載入 (SIP) 的主體介面套件。

</dd> <dt>

**cbBlob**
</dt> <dd>

要簽署之 BLOB 的大小（以位元組為單位）。

</dd> <dt>

**pbBlob**
</dt> <dd>

要簽署之 BLOB 的指標。

</dd> <dt>

**pwszDisplayName**
</dt> <dd>

BLOB 的顯示名稱。 這個成員可以設定為 **Null**。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)
</dt> </dl>

 

 
