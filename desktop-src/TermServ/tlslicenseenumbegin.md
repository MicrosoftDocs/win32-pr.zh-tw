---
title: TLSLicenseEnumBegin 函式
description: 根據搜尋準則開始列舉遠端桌面授權伺服器所發行的授權。
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- TLSLicenseEnumBegin 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSLicenseEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95913337de968d0b30780b5898b7f204d947dd4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686480"
---
# <a name="tlslicenseenumbegin-function"></a>TLSLicenseEnumBegin 函式

根據搜尋準則開始列舉遠端桌面授權伺服器所發行的授權。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。

 

## <a name="syntax"></a>語法


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
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

指定搜尋準則。 參數可以是下列清單所描述的一或多個值的組合。 參數指定金鑰套件的類型以及要搜尋的金鑰套件。

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE \_搜尋 \_ LICENSEID** (0x00000001) 


</dt> <dd>

依授權識別碼搜尋。

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE \_搜尋 \_ KEYPACKID** (0x00000002) 


</dt> <dd>

依金鑰套件識別碼搜尋。

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE \_搜尋 \_ MACHINENAME** (0x00000008) 


</dt> <dd>

依電腦名稱稱搜尋。

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE \_搜尋使用者 \_ 名稱** (0x00000010) 


</dt> <dd>

依使用者名稱搜尋。

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE \_搜尋 \_ ISSUEDATE** (0x00000080) 


</dt> <dd>

依發行日期搜尋。

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE \_搜尋 \_ EXPIREDATE** (0x00000100) 


</dt> <dd>

依到期日搜尋。

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE \_搜尋 \_ NUMLICENSES** (0x00000200) 


</dt> <dd>

依授權數目搜尋。

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE \_搜尋 \_ 輸入 \_ 狀態** (0x20000000) 


</dt> <dd>

依專案狀態搜尋。

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE \_EXSEARCH \_ LICENSESTATUS** (0x00100000) 


</dt> <dd>

依授權狀態搜尋。

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK \_搜尋 \_ 所有** (0xffffffff) 


</dt> <dd>

搜尋所有授權。

</dd> </dl> </dd> <dt>

*bMatchAll* \[在\]
</dt> <dd>

指定是否要符合所有搜尋值。

</dd> <dt>

*lpSearchParm* \[在\]
</dt> <dd>

[**LSLicense**](lslicense.md)結構的指標，指定要尋找的搜尋參數。

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

[**LSLicense**](lslicense.md)
</dt> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

