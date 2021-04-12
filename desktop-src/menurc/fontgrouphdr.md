---
title: FONTGROUPHDR 結構
description: 包含應用程式存取特定字型所需的資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: 180b3dfd-3f20-4100-b45b-2f253b7c0582
keywords:
- FONTGROUPHDR 結構功能表和其他資源
topic_type:
- apiref
api_name:
- FONTGROUPHDR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1d67d9ecfa451970422f21d05817f26170a9c8eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104187303"
---
# <a name="fontgrouphdr-structure"></a>FONTGROUPHDR 結構

包含應用程式存取特定字型所需的資訊。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD     NumberOfFonts;
  DIRENTRY DE;
} FONTGROUPHDR;
```



## <a name="members"></a>成員

<dl> <dt>

**NumberOfFonts**
</dt> <dd>

類型： **WORD**

</dd> <dd>

與此資源相關聯的個別字型數目。

</dd> <dt>

**德**
</dt> <dd>

類型： **[ **DIRENTRY**](direntry.md)**

</dd> <dd>

結構，其中包含資源中每個字型的唯一序數識別碼。 **DE** 成員是 [**DIRENTRY**](direntry.md)結構的可變長度陣列的預留位置。

</dd> </dl>

## <a name="remarks"></a>備註

**FONTGROUPHDR** 結構會遵循中個別字型的資料。Res 檔。 資源編譯器會自動新增 **FONTGROUPHDR** 結構，通常是檔案中的最後一個專案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**DIRENTRY**](direntry.md)
</dt> <dt>

[**FONTDIRENTRY**](fontdirentry.md)
</dt> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> </dl>

 

 





