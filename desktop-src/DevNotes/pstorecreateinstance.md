---
description: 抓取儲存提供者的介面指標。
ms.assetid: 22b5b003-82fa-48f1-96db-a8d6dd70d6d1
title: 'PStoreCreateInstance 函式 (Pstore) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreCreateInstance
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: 2e32319e9585f5d1a80d0473c6ce27167f0ec181b81b974c526371b29c018b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955687"
---
# <a name="pstorecreateinstance-function"></a>PStoreCreateInstance 函式

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

\[在 Windows 的未來版本中，此函式可能會變更或無法使用。 使用 **CryptProtectData** 和 **CryptUnprotectData** 函式，而不是此函數。\]

抓取儲存提供者的介面指標。

## <a name="syntax"></a>語法


```C++
HRESULT __stdcall PStoreCreateInstance(
  _Out_ IPStore        **ppProvider,
  _In_  PST_PROVIDERID *pProviderID,
  _In_  void           *pReserved,
  _In_  DWORD          dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppProvider* \[擴展\]
</dt> <dd>

儲存提供者之已抓取介面指標的指標。 當您使用完介面之後，請呼叫其 [**IUnknown：： Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 方法來遞減其參考計數。 此參數不可以是 **Null**。

</dd> <dt>

*pProviderID* \[在\]
</dt> <dd>

識別儲存提供者之 **GUID** 的指標。 如果此參數為 **Null**，則會使用基底儲存提供者。

</dd> <dt>

*保留* \[在\]
</dt> <dd>

保護必須是 **Null**。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

保護必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是 **HRESULT**。 值為 **S \_ OK** 表示函式已成功。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata)
</dt> <dt>

[**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)
</dt> </dl>

 

 
