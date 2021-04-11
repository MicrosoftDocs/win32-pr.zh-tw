---
title: OP_JOINPROV2_PART
description: OP_JOINPROV2_PART IDL 定義
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "104093480"
---
# <a name="op_joinprov2_part-structure"></a>OP_JOINPROV2_PART 結構

包含用來設定加入網域之用戶端的其他資訊。

## <a name="syntax"></a>語法

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a>成員

### <a name="dwflags"></a>dwFlags

必須設定為零或下列其中一個值：

|值|意義|
| --- | --- |
|OP_JP2_FLAG_PERSISTENTSITE (0x00000001) |在 lpSiteName 中指定的網站必須被視為用戶端的永久網站。|

### <a name="lpnetbiosname"></a>lpNetbiosName

包含 Unicode 格式之電腦帳戶的 Netbios 名稱。

### <a name="lpsitename"></a>lpSiteName

包含用戶端應使用之 Active Directory 網站的名稱。

### <a name="lpprimarydnsdomain"></a>lpPrimaryDNSDomain

包含用戶端應使用的主要 DNS 功能變數名稱。

### <a name="dwreserved"></a>>dwreserved

保留供日後使用，且必須設定為0。

### <a name="lpreserved"></a>lpReserved

保留供日後使用，且必須設定為 Null。

## <a name="see-also"></a>另請參閱

[**離線網域加入 IDL 定義**](odj-idl.md)
