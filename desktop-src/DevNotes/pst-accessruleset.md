---
description: 識別受保護儲存體資料的存取規則集。
ms.assetid: 0eee34c2-b832-41b3-80f5-b03fdddf75cc
title: 'PST_ACCESSRULESET 結構 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_ACCESSRULESET
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: b4c339ea0866ad872d5d0a2f8eaff6be947adc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995027"
---
# <a name="pst_accessruleset-structure"></a>PST \_ ACCESSRULESET 結構

\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

識別受保護儲存體資料的存取規則集。

## <a name="syntax"></a>語法


```C++
typedef struct {
  DWORD          cbSize;
  DWORD          cRules;
  PST_ACCESSRULE *rgRules;
} PST_ACCESSRULESET, *PPST_ACCESSRULESET;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

此結構的大小。

</dd> <dt>

**cRules**
</dt> <dd>

**RgRules** 陣列中的規則數目。

</dd> <dt>

**rgRules**
</dt> <dd>

[**PST \_ ACCESSRULE**](pst-accessrule.md)結構陣列的指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PST \_ ACCESSRULE**](pst-accessrule.md)
</dt> <dt>

[**CreateSubtype**](ipstore-createsubtype.md)
</dt> </dl>

 

 
