---
description: 包含檔管理員用來加入功能表或工具列命令專案之說明字串的資訊。
title: 'FMS_HELPSTRING 結構 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: b3ae7f86-5d58-47fa-87bd-e4e6a3541a93
ms.openlocfilehash: 4e9521df91619d108c7a03b6574926147fc2b04a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842209"
---
# <a name="fms_helpstring-structure"></a>FMS \_ HELPSTRING 結構

包含檔管理員用來加入功能表或工具列命令專案之說明字串的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _FMS_HELPSTRING {
  INT       idCommand;
  HMENU     hMenu;
  __wchar_t szHelp[128];
} FMS_HELPSTRING;
```



## <a name="members"></a>成員

<dl> <dt>

**idCommand**
</dt> <dd>

類型： **INT**

</dd> <dd>

命令專案的識別碼。

</dd> <dt>

**hMenu**
</dt> <dd>

類型： **HMENU**

</dd> <dd>

功能表列的識別碼。

</dd> <dt>

**szHelp**
</dt> <dd>

類型： **\_ \_ wchar \_ t \[ 128 \]**

</dd> <dd>

以 null 終止的字串，此字串會接收解說文字。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wfext。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FMExtensionProc**](fmextensionproc.md)
</dt> <dt>

[**FMEVENT \_ HELPMENUITEM**](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




