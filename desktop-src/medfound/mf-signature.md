---
description: 包含 (GRL) 簽章的全域撤銷清單。
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: MF_SIGNATURE 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194861"
---
# <a name="mf_signature-structure"></a>MF \_ 簽名結構

包含 (GRL) 簽章的全域撤銷清單。

## <a name="syntax"></a>語法


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a>成員

<dl> <dt>

**dwSignVer**
</dt> <dd>

簽章版本號碼。

</dd> <dt>

**cbSign**
</dt> <dd>

簽章的大小（以位元組為單位）。

</dd> <dt>

**rgSign**
</dt> <dd>

**CbSign** 大小的位元組陣列，其中包含簽章。 實際的陣列大小大於結構宣告中指定的大小。

</dd> </dl>

## <a name="remarks"></a>備註

SDK 標頭中未宣告此結構。 若要使用此結構，請將此處顯示的宣告新增至您的原始程式碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[OPM 憑證撤銷](opm-certificate-revocation.md)
</dt> <dt>

[OPM 結構](opm-structures.md)
</dt> </dl>

 

 




