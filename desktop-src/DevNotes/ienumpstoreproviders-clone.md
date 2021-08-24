---
description: IEnumPStoreProviders：： Clone 方法-建立另一個列舉值，其中包含與目前相同的列舉狀態。
ms.assetid: c9a53005-4bb2-4a07-8f58-28d51f22c9e8
title: 'IEnumPStoreProviders：： Clone 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Clone
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: a88a814d5052dea51bade8046392ecfe7530d43e368b10700c614d42baafe398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119542178"
---
# <a name="ienumpstoreprovidersclone-method"></a>IEnumPStoreProviders：： Clone 方法

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

建立另一個列舉值，其包含與目前列舉值相同的列舉型別狀態。

## <a name="syntax"></a>語法


```C++
HRESULT Clone(
  [out] IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppenum* \[擴展\]
</dt> <dd>

指向 [**IEnumPStoreProviders**](ienumpstoreproviders.md) 指標的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT** 值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
