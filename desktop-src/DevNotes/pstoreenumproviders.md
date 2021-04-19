---
description: 取得枚舉器物件，這個物件可以用來列舉目前安裝在系統上的受保護儲存提供者。
ms.assetid: df162086-caeb-427f-9db8-9722855cfbbf
title: 'PStoreEnumProviders 函式 (Pstore) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PStoreEnumProviders
api_type:
- DllExport
api_location:
- Pstorec.dll
ms.openlocfilehash: f4f97bdae8646d3a4d683bb5b87bf72efb4c5a5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996421"
---
# <a name="pstoreenumproviders-function"></a>PStoreEnumProviders 函式

\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

取得枚舉器物件，這個物件可以用來列舉目前安裝在系統上的受保護儲存提供者。

## <a name="syntax"></a>語法


```C++
HRESULT PStoreEnumProviders(
   DWORD                dwFlags,
   IEnumPStoreProviders **ppenum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*dwFlags* 
</dt> <dd>

未使用此參數，且必須為零。

</dd> <dt>

*ppenum* 
</dt> <dd>

指向 [**IEnumPStoreProviders**](ienumpstoreproviders.md) 介面指標的指標，該介面可用來列舉已安裝的提供者。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數會傳回 **HRESULT**。

## <a name="remarks"></a>備註

受保護的儲存元件具有以提供者為基礎的架構。 使用受保護存放裝置的應用程式可以指定在儲存和抓取其資料時，所要使用的已安裝提供者。

**PStoreEnumProviders** 函式可用來列舉已安裝的受保護存放裝置提供者。 每個提供者都是以全域唯一識別碼 (GUID) 來識別。

目前為止，只寫入一個受保護的儲存提供者。 由於受保護的儲存體服務目前已被取代，因此不太可能會產生任何額外的提供者。 因此，此函式不應該用於任何用途。

此函數沒有相關聯的匯入程式庫;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumPStoreProviders**](ienumpstoreproviders.md)
</dt> </dl>

 

 
