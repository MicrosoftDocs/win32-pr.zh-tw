---
description: 指定要簽署的主旨。
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: SIGNER_SUBJECT_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989357"
---
# <a name="signer_subject_info-structure"></a>簽署者 \_ 主體 \_ 資訊結構

**簽署者 \_ 主體 \_ 資訊** 結構會指定要簽署的主旨。

> [!Note]  
> 此結構未定義于任何標頭檔中。 若要使用這個結構，您必須自行定義，如本主題所示。

 

## <a name="syntax"></a>語法


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

結構的大小（以位元組為單位）。

</dd> <dt>

**pdwIndex**
</dt> <dd>

這個成員是保留的。 它必須設定為零。

</dd> <dt>

**dwSubjectChoice**
</dt> <dd>

指定主體是否為檔案或 [*BLOB*](../secgloss/b-gly.md)。 這個成員可以是下列一或多個值。



| 值                                                                                                                                                                                                                                         | 意義                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <dt>**簽署者 \_主體 \_ BLOB**</dt> <dt>2 (0x2)</dt> </dl> | 主體是 BLOB。<br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <dt>**簽署者 \_主題 \_**</dt>檔案 <dt>1 (0x1)</dt> </dl> | 主體是一個檔案。<br/> |



 

</dd> <dt>

**pSignerFileInfo**
</dt> <dd>

[**簽署者檔案 \_ \_ 資訊**](signer-file-info.md)結構的指標，指定要簽署的檔案。

</dd> <dt>

**pSignerBlobInfo**
</dt> <dd>

[**簽署者 \_ BLOB \_ 資訊**](signer-blob-info.md)結構的指標，指定要簽署的 blob。

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

 

 
