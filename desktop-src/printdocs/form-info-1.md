---
description: FORM_INFO_1 結構包含列印表單的相關資訊。 此資訊包括列印表單來源、其名稱、其尺寸，以及其可列印範圍的尺寸。
ms.assetid: 1c42ea6c-82cf-463c-bc67-44a8d8c4a1e7
title: 'FORM_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FORM_INFO_1
- _FORM_INFO_1A
- _FORM_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: b6f620d8bd2ed4ef39fc868c91068e10a7ff43f57d98510ecfbae1dbe2ae7c54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949258"
---
# <a name="form_info_1-structure"></a>FORM_INFO_1 結構

**FORM_INFO_1** 結構包含列印表單的相關資訊。 此資訊包括列印表單的原始來源、其名稱、其尺寸，以及其可列印範圍的尺寸。

## <a name="syntax"></a>語法


```C++
typedef struct _FORM_INFO_1 {
  DWORD  Flags;
  LPTSTR pName;
  SIZEL  Size;
  RECTL  ImageableArea;
} FORM_INFO_1, *PFORM_INFO_1;
```



## <a name="members"></a>成員

<dl> <dt>

**旗標**
</dt> <dd>

表單內容。 以下是定義的值。



| 值         | 意義                                                                                                                      |
|---------------|------------------------------------------------------------------------------------------------------------------------------|
| FORM_USER    | 如果設定此位旗標，使用者就會定義表單。 具有此旗標集合的表單是在登錄中定義。        |
| FORM_BUILTIN | 如果設定此位旗標，則表單是多工緩衝處理器的一部分。 具有此旗標設定的表單定義不會出現在登錄中。 |
| FORM_PRINTER | 如果設定了這個位旗標，表單就會與特定的印表機相關聯，而且其定義會出現在登錄中。          |



 

</dd> <dt>

**pName**
</dt> <dd>

指定表單名稱之以 null 結束的字串指標。 表單名稱不能超過31個字元。

</dd> <dt>

**大小**
</dt> <dd>

表單的寬度和高度（以千為單位）。

</dd> <dt>

**ImageableArea**
</dt> <dd>

表單的寬度和高度（以千為單位）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **_FORM_INFO_1W** (Unicode) 和 **_FORM_INFO_1A** (ANSI) <br/>                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**AddForm**](addform.md)
</dt> <dt>

[**GetForm**](getform.md)
</dt> <dt>

[**SetForm**](setform.md)
</dt> </dl>

 

 




