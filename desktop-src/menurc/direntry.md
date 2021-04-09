---
title: DIRENTRY 結構
description: 包含識別字型資源群組中個別字型的唯一序數。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 4afc561e-bc98-4968-9a00-5002870b0c5e
keywords:
- DIRENTRY 結構功能表和其他資源
topic_type:
- apiref
api_name:
- DIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caed8f05a92abbeda39084b99b6806c2e28777a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686040"
---
# <a name="direntry-structure"></a>DIRENTRY 結構

包含識別字型資源群組中個別字型的唯一序數。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD fontOrdinal;
} DIRENTRY;
```



## <a name="members"></a>成員

<dl> <dt>

**fontOrdinal**
</dt> <dd>

類型： **WORD**

</dd> <dd>

字型資源群組中個別字型的唯一序數識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

指定字型的 [**FONTDIRENTRY**](fontdirentry.md) 結構會直接遵循該字型的 **DIRENTRY** 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> </dl>

 

 





