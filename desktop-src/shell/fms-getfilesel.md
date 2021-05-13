---
description: 在 [active 檔案管理員] 視窗中， ([目錄] 視窗或 [搜尋結果] 視窗) ，包含所選取檔案的相關資訊。
title: 'FMS_GETFILESEL 結構 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_GETFILESEL
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: d8339f87-ba05-40bf-b7d1-a9de29eb15a4
ms.openlocfilehash: b1188840299a101081c5c29d0e5658963ca7a72e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842219"
---
# <a name="fms_getfilesel-structure"></a>FMS \_ GETFILESEL 結構

在 [active 檔案管理員] 視窗中， ([目錄] 視窗或 [搜尋結果] 視窗) ，包含所選取檔案的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _FMS_GETFILESEL {
  FILETIME ftTime;
  DWORD    dwSize;
  BYTE     bAttr;
  TCHAR    szName;
} FMS_GETFILESEL;
```



## <a name="members"></a>成員

<dl> <dt>

**ftTime**
</dt> <dd>

類型： **FILETIME**

</dd> <dd>

建立檔案的時間和日期。

</dd> <dt>

**dwSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

檔案的大小（以位元組為單位）。

</dd> <dt>

**bAttr**
</dt> <dd>

類型： **位元組**

</dd> <dd>

檔案的屬性。

</dd> <dt>

**szName**
</dt> <dd>

類型： **TCHAR**

</dd> <dd>

以 null 結束的完整路徑和所選取檔案的檔案名。

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
</dt> </dl>

 

 




