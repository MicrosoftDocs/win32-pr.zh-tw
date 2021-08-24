---
description: 讀取指定類型的存取規則。
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: 'IPStore：： ReadAccessRuleSet 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadAccessRuleSet
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: d22f56c14df4d11a8979065ede81ab8418909033ffd816a233a18c51af7f66c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749748"
---
# <a name="ipstorereadaccessruleset-method"></a>IPStore：： ReadAccessRuleSet 方法

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

\[這個方法尚未實作。\]

讀取指定類型的存取規則。

## <a name="syntax"></a>語法


```C++
HRESULT ReadAccessRuleSet(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET **ppRules,
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

*ppRules* \[在\]
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

 

 
