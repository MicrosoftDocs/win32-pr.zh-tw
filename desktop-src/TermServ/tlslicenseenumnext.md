---
title: TLSLicenseEnumNext 函式
description: 繼續進行先前的 TLSLicenseEnumBegin 函式呼叫，並傳回與搜尋條件相符的遠端桌面授權伺服器上所安裝的下一個授權。
ms.assetid: 6932289b-b59c-493c-8dbc-03c0662e921e
ms.tgt_platform: multiple
keywords:
- TLSLicenseEnumNext 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSLicenseEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 945c0afb931770a36049342f32c71613bd8fb1a0a9b16142c1ffbc6a67ccc288
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986798"
---
# <a name="tlslicenseenumnext-function"></a>TLSLicenseEnumNext 函式

繼續進行先前的 [**TLSLicenseEnumBegin**](tlslicenseenumbegin.md) 函式呼叫，並傳回與搜尋條件相符的遠端桌面授權伺服器上所安裝的下一個授權。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。

 

## <a name="syntax"></a>語法


```C++
DWORD WINAPI TLSLicenseEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LSLicense  *lpLicense,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hHandle* \[在\]
</dt> <dd>

遠端桌面授權伺服器的控制碼。 指定 [**TLSConnectToLsServer**](tlsconnecttolsserver.md) 函式所開啟的控制碼。

</dd> <dt>

*lpLicense* \[在\]
</dt> <dd>

[**LSLicense**](lslicense.md)結構的指標，此結構會接收符合搜尋準則的下一個授權。

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

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER \_我 \_ 沒有 \_ 其他 \_ 資料** (4001) 


</dt> <dd>

沒有其他授權符合搜尋準則。

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_E \_ 內部 \_ 錯誤** (5001) 


</dt> <dd>

授權伺服器發生內部錯誤。

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_E \_ 不正確 \_ 序列** (5006) 


</dt> <dd>

呼叫順序無效。 必須先呼叫 [**TLSLicenseEnumBegin ()**](tlslicenseenumbegin.md) 函式，才能進行此工作。

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER \_E \_ SERVER \_ 忙碌** (5007) 


</dt> <dd>

授權伺服器太忙碌，無法處理要求。

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER \_E \_ OUTOFMEMORY** (5008) 


</dt> <dd>

因為記憶體不足，所以無法處理要求。

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

[**LSLicense**](lslicense.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

