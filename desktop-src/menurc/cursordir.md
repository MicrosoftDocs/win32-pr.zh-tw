---
title: CURSORDIR 結構
description: 包含資源群組中個別資料指標影像的維度。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。
ms.assetid: bc826fd6-74a2-470b-8d19-437cdeb0727d
keywords:
- CURSORDIR 結構功能表和其他資源
topic_type:
- apiref
api_name:
- CURSORDIR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7194d6af764a9f66a2bf1a059f9c387cde13bb05728a7e96ccec470fa3650c81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602168"
---
# <a name="cursordir-structure"></a>CURSORDIR 結構

包含資源群組中個別資料指標影像的維度。 此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WORD Width;
  WORD Height;
} CURSORDIR;
```



## <a name="members"></a>成員

<dl> <dt>

**寬度**
</dt> <dd>

類型： **WORD**

</dd> <dd>

游標的寬度（以圖元為單位）。 可接受的值為16、32和64。

</dd> <dt>

**高度**
</dt> <dd>

類型： **WORD**

</dd> <dd>

資料指標的高度（以圖元為單位）。 可接受的值為16、32和64。

</dd> </dl>

## <a name="remarks"></a>備註

如果 **RESDIR** 結構描述資料指標，則會在 [**RESDIR**](resdir.md)結構中傳遞 **CURSORDIR** 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/> |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**RESDIR**](resdir.md)
</dt> <dt>

**概念**
</dt> <dt>

[資源](resources.md)
</dt> </dl>

 

 





