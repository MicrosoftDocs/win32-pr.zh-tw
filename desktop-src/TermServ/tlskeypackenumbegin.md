---
title: TLSKeyPackEnumBegin 函式
description: 根據搜尋準則，在遠端桌面授權伺服器上安裝的所有金鑰套件開始列舉。
ms.assetid: 2d847fe4-66ab-42df-8213-651e14257590
ms.tgt_platform: multiple
keywords:
- TLSKeyPackEnumBegin 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSKeyPackEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 469e4e255f3bdd64749060fcb712df480a8a1f6fc3683ebb25916be44856e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869328"
---
# <a name="tlskeypackenumbegin-function"></a>TLSKeyPackEnumBegin 函式

根據搜尋準則，在遠端桌面授權伺服器上安裝的所有金鑰套件開始列舉。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。

 

## <a name="syntax"></a>語法


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hHandle* \[在\]
</dt> <dd>

遠端桌面授權伺服器的控制碼。 指定 [**TLSConnectToLsServer**](tlsconnecttolsserver.md) 函式所開啟的控制碼。

</dd> <dt>

*dwSearchParm* \[在\]
</dt> <dd>

指定搜尋準則。 此參數會保留供日後使用，且必須包含0xFFFFFFFF。

</dd> <dt>

*bMatchAll* \[在\]
</dt> <dd>

指定是否要符合所有搜尋值。

</dd> <dt>

*lpSearchParm* \[在\]
</dt> <dd>

[**LSKeyPack**](lskeypack.md)結構的指標，指定要尋找的搜尋參數。

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

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER \_E \_ 內部 \_ 錯誤** (5001) 


</dt> <dd>

授權伺服器發生內部錯誤。

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER \_E \_ 不正確 \_ 序列** (5006) 


</dt> <dd>

呼叫順序無效。 最可能的情況是先前的列舉尚未結束。

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

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER \_E \_ 不正確 \_ 資料** (5009) 


</dt> <dd>

搜尋參數中的資料無效。

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

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

