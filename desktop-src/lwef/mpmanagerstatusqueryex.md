---
title: 'MpManagerStatusQueryEx 函式 (MpClient) '
description: '傳回惡意程式碼防護管理員各元件的相關狀態資訊。 |MpManagerStatusQueryEx 函式 (MpClient) '
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- MpManagerStatusQueryEx 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106989177"
---
# <a name="mpmanagerstatusqueryex-function"></a>MpManagerStatusQueryEx 函式

傳回惡意程式碼防護管理員各元件的相關狀態資訊。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hMpHandle* \[在\]
</dt> <dd>

類型： **MPHANDLE**

惡意程式碼防護管理員介面的控制碼。 [**MpManagerOpen**](mpmanageropen.md)函數會傳回這個控制碼。

</dd> <dt>

*>dwflag* \[在\]
</dt> <dd>

類型： **DWORD**

控制傳回的查詢資訊。 某些資訊的成本很高，而且可能不需要。



| 值                                                                                                                                                                                                         | 意義                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <dt>**MP \_ STATUS \_ 查詢 \_ 旗標 \_ 無**</dt> </dl>       | 預設值。<br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <dt>**MP \_ STATUS \_ 查詢 \_ 旗標 \_ NOSTATE**</dt> </dl> | 請勿查詢狀態資訊。<br/> |



 

</dd> <dt>

*pStatusInfo* \[擴展\]
</dt> <dd>

類型： **PMPSTATUS \_ 資訊**

結構的指標，此結構會傳回有關上次掃描、作用中威脅和各種元件狀態的狀態資訊。 請參閱 [**MPSTATUS \_ 資訊**](mpstatus-info.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果函式成功，則傳回值為 **S \_ OK**。 即使反惡意程式碼服務不在執行中，此函式呼叫仍會成功。

如果函式失敗，則傳回值會是失敗的 **HRESULT** 程式碼。 呼叫端可以使用 [**MpErrorMessageFormat**](mperrormessageformat.md) 函數來取得錯誤訊息的一般描述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MPSTATUS \_ 資訊**](mpstatus-info.md)
</dt> </dl>

 

 





