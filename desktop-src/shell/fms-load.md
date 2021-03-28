---
description: 包含檔管理員用來新增由檔管理程式延伸模組 DLL 提供之自訂功能表的資訊。 此結構也提供差異值，可供延伸模組 DLL 在檔案管理員載入功能表之後，用來操作自訂功能表。
title: 'FMS_LOAD 結構 (Wfext .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 0e76bcc5-76c2-4ec0-8ddb-4042cb5ffa7d
ms.openlocfilehash: 1745c4e34ac124e9990602350db6479ce287be8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971916"
---
# <a name="fms_load-structure"></a>FMS \_ 載入結構

包含檔管理員用來新增由檔管理程式延伸模組 DLL 提供之自訂功能表的資訊。 此結構也提供差異值，可供延伸模組 DLL 在檔案管理員載入功能表之後，用來操作自訂功能表。

## <a name="syntax"></a>語法


```C++
typedef struct _FMS_LOAD {
  DWORD dwSize;
  TCHAR szMenuName[MENU_TEXT_LEN];
  HMENU hMenu;
  UINT  wMenuDelta;
} FMS_LOAD;
```



## <a name="members"></a>成員

<dl> <dt>

**dwSize**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

結構的長度（以位元組為單位）。

</dd> <dt>

**szMenuName**
</dt> <dd>

類型： **TCHAR \[ 功能表 \_ 文字 \_ LEN \]**

</dd> <dd>

在 [檔案管理員] 中出現在功能表列上的功能表項目之以 null 結束的名稱。

</dd> <dt>

**hMenu**
</dt> <dd>

類型： **HMENU**

</dd> <dd>

已新增至 [檔案管理員] 功能表列之快顯功能表的識別碼。

</dd> <dt>

**wMenuDelta**
</dt> <dd>

類型： **UINT**

</dd> <dd>

功能表項目差異值。 為了避免與本身的功能表項目發生衝突，檔管理員會將此差異值新增至每個識別碼，以將 **hMenu** 成員所識別之快顯功能表中的功能表項目識別碼進行比對。 必須修改功能表項目的延伸模組 DLL 必須將 delta 值新增至功能表項目的識別碼，以識別專案。 此成員的值可能會因會話而異。

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

 

 




