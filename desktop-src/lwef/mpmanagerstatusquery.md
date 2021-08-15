---
title: 'MpManagerStatusQuery 函式 (MpClient) '
description: '傳回惡意程式碼防護管理員各元件的相關狀態資訊。 |MpManagerStatusQuery 函式 (MpClient) '
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- MpManagerStatusQuery 函式舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d05751f30e1579ef8b12e31a4f858469b1c997cf9c29d7643c0600a133840fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883373"
---
# <a name="mpmanagerstatusquery-function"></a>MpManagerStatusQuery 函式

\[**MpManagerStatusQuery** 不受支援，未來可能會變更或無法使用。 相反地，請使用 [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)。\]

傳回惡意程式碼防護管理員各元件的相關狀態資訊。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
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
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**MPSTATUS \_ 資訊**](mpstatus-info.md)
</dt> </dl>

 

 





