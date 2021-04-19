---
description: 寫入指定類型的存取規則。
ms.assetid: d5cfd782-8d87-45ae-a574-0a294a30ca71
title: 'IPStore：： WriteAccessRuleset 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteAccessRuleset
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7399ff800087720d65cb45e80ccab080a7df9baf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995464"
---
# <a name="ipstorewriteaccessruleset-method"></a>IPStore：： WriteAccessRuleset 方法

\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

\[這個方法尚未實作。\]

寫入指定類型的存取規則。

## <a name="syntax"></a>語法


```C++
HRESULT WriteAccessRuleset(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

保留的。

</dd> <dt>

*pType* \[在\]
</dt> <dd>

保留的。

</dd> <dt>

*pSubtype* \[在\]
</dt> <dd>

保留的。

</dd> <dt>

*pInfo* \[在\]
</dt> <dd>

保留的。

</dd> <dt>

*pRules* \[在\]
</dt> <dd>

保留的。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

保留的。

</dd> </dl>

## <a name="return-value"></a>傳回值

呼叫這個方法一律會失敗。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IPStore**](ipstore.md)
</dt> </dl>

 

 
