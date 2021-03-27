---
description: 包含有關檔案管理員延伸模組 DLL 新增至 [檔案管理員] 工具列之按鈕的資訊。
title: 'EXT_BUTTON 結構 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXT_BUTTON
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 8cd29a06-0f38-4285-9092-647a391b72d7
ms.openlocfilehash: 5eabb9f5e958b1e0bd15a6412dfbfa276d23f255
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690184"
---
# <a name="ext_button-structure"></a>EXT \_ 按鈕結構

包含有關檔案管理員延伸模組 DLL 新增至 [檔案管理員] 工具列之按鈕的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagEXT_BUTTON {
  WORD idCommand;
  WORD idsHelp;
  WORD fsStyle;
} EXT_BUTTON, *LPEXT_BUTTON;
```



## <a name="members"></a>成員

<dl> <dt>

**idCommand**
</dt> <dd>

類型： **WORD**

</dd> <dd>

按鈕的命令識別碼。

</dd> <dt>

**idsHelp**
</dt> <dd>

類型： **WORD**

</dd> <dd>

按鈕的說明字串識別碼。

</dd> <dt>

**fsStyle**
</dt> <dd>

類型： **WORD**

</dd> <dd>

按鈕的樣式。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FMEVENT \_ TOOLBARLOAD**](fmevent-toolbarload.md)
</dt> <dt>

[**FMS \_ TOOLBARLOAD**](fms-toolbarload.md)
</dt> </dl>

 

 




