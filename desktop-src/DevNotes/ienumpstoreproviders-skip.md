---
description: IEnumPStoreProviders：： Skip 方法-略過列舉順序中的下一個指定專案數目。
ms.assetid: bf9ea700-3f44-48a7-8ea0-ee66dea61836
title: 'IEnumPStoreProviders：： Skip 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders.Skip
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 2f74c44de172d9235d9768b8f484405b5e8fb7fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096746"
---
# <a name="ienumpstoreprovidersskip-method"></a>IEnumPStoreProviders：： Skip 方法

\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

略過列舉順序中的下一個指定專案數目。

## <a name="syntax"></a>語法


```C++
HRESULT Skip(
  [in] DWORD celt
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*celt* \[在\]
</dt> <dd>

要略過的提供者類型數目。

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

 

 
