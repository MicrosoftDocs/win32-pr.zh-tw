---
description: 受保護儲存體方法的資料類型。
ms.assetid: 4d494326-6d0f-4a12-83a2-3c3dd3ca9c1b
title: 'PStore 類型 (Pstore) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6def89ea4beb5d27a98cb8e6f44fc12271de7d1642b236f31f4979ed26b54a44
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538448"
---
# <a name="pstore-types"></a>PStore 類型

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

受保護儲存體方法的資料類型。


```C++
typedef DWORD PST_ACCESSMODE;
typedef DWORD PST_ACCESSCLAUSETYPE;
typedef DWORD PST_KEY;
```



<dl> <dt>

**PST \_ ACCESSMODE**
</dt> <dd>

定義存取規則的讀取或寫入模式。

</dd> <dt>

**PST \_ ACCESSCLAUSETYPE**
</dt> <dd>

定義存取規則的子句類型。

</dd> <dt>

**PST \_ 金鑰**
</dt> <dd>

定義預存專案的索引鍵。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl> |



 

 
