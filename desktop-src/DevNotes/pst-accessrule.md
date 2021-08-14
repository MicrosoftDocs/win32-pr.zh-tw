---
description: 描述存取儲存在受保護儲存體中之專案的規則。
ms.assetid: 22aebac3-46e9-4c66-bfaf-e82cf9d494cb
title: 'PST_ACCESSRULE 結構 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULE
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 26b4df38c5e5599c13cc52a75c58ea019d786eaa971c8ac3a67a7a8c15651075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667054"
---
# <a name="pst_accessrule-structure"></a>PST \_ ACCESSRULE 結構

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

描述存取儲存在受保護儲存體中之專案的規則。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD            cbSize;
  PST_ACCESSMODE   AccessModeFlags;
  DWORD            cClauses;
  PST_ACCESSCLAUSE *rgClauses;
} PST_ACCESSRULE, *PPST_ACCESSRULE;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

此結構的大小。

</dd> <dt>

**AccessModeFlags**
</dt> <dd>

一組指定之存取子句所屬的存取模式。



| 值                                                                                                                                                                                                         | 意義                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span id="PST_READ"></span><span id="pst_read"></span><dl> <dt>**PST \_讀取**</dt> <dt>0x0001</dt> </dl>    | 讀取存取模式。<br/>  |
| <span id="PST_WRITE"></span><span id="pst_write"></span><dl> <dt>**PST \_寫入**</dt> <dt>0x0002</dt> </dl> | 寫入存取模式。<br/> |



 

</dd> <dt>

**cClauses**
</dt> <dd>

**RgClauses** 陣列中的結構數目。

</dd> <dt>

**rgClauses**
</dt> <dd>

[**PST \_ ACCESSCLAUSE**](pst-accessclause.md)結構陣列的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PST \_ ACCESSCLAUSE**](pst-accessclause.md)
</dt> <dt>

[**PST \_ ACCESSRULESET**](pst-accessruleset.md)
</dt> </dl>

 

 
