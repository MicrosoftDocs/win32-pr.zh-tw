---
title: TLSKeyPackEnumEnd 函式
description: 從先前的 TLSKeyPackEnumBegin 函式呼叫繼續，然後終止列舉。
ms.assetid: 3434e18d-54c9-46ed-b6a5-bc174b63a152
ms.tgt_platform: multiple
keywords:
- TLSKeyPackEnumEnd 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSKeyPackEnumEnd
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04723318b29adff7a647fe2cab39fb0b16f3f5a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685851"
---
# <a name="tlskeypackenumend-function"></a>TLSKeyPackEnumEnd 函式

從先前的 [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) 函式呼叫繼續，然後終止列舉。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。

 

## <a name="syntax"></a>語法


```C++
DWORD WINAPI TLSKeyPackEnumEnd(
  _In_  TLS_HANDLE hHandle,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hHandle* \[在\]
</dt> <dd>

遠端桌面授權伺服器的控制碼。 指定 [**TLSConnectToLsServer**](tlsconnecttolsserver.md) 函式所開啟的控制碼。

</dd> <dt>

*pdwErrCode* \[擴展\]
</dt> <dd>

變數的指標，此變數會在傳回時接收下列其中一個錯誤碼。

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER \_S \_ 成功** (0) 


</dt> <dd>

呼叫成功。

</dd> <dt>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>

<span id="LSERVER_E_INVALID_HANDLE"></span><span id="lserver_e_invalid_handle"></span>**LSERVER \_E \_ 不正確 \_ 控制碼** (5005) 


</dt> <dd>

控制碼無效。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

此函數會傳回下列可能的傳回值。

<dl> <dt>

**RPC \_ S \_ 確定**
</dt> <dd>

呼叫成功。 檢查 *pdwErrCode* 參數的值，以取得呼叫的傳回碼。

</dd> <dt>

**RPC \_ S \_ 不正確 \_ ARG**
</dt> <dd>

引數無效。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> </dl>

 

