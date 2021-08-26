---
title: TLSConnectToLsServer 函式
description: 開啟指定之遠端桌面授權伺服器的控制碼。
ms.assetid: 9e90a8e8-9319-42ee-b541-a1d028b6ed4d
ms.tgt_platform: multiple
keywords:
- TLSConnectToLsServer 函式遠端桌面服務
topic_type:
- apiref
api_name:
- TLSConnectToLsServer
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbfc3c1e365a97b8199df34c2e55a8362f48b7f6a2a43e524e3c6e937de5cb0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986968"
---
# <a name="tlsconnecttolsserver-function"></a>TLSConnectToLsServer 函式

開啟指定之遠端桌面授權伺服器的控制碼。

> [!Note]  
> 此函數沒有相關聯的標頭檔或匯入程式庫。 若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mstlsapi.dll。

 

## <a name="syntax"></a>語法


```C++
TLS_HANDLE WINAPI TLSConnectToLsServer(
  _In_ LPTSTR pszLsServer
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszLsServer* \[在\]
</dt> <dd>

以 **null** 結束的字串指標，指定遠端桌面授權伺服器的 NetBIOS 名稱。 如果這個參數的值為 **Null**，指定的伺服器就是本機電腦。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值是指定之伺服器的控制碼。

如果函式失敗，則傳回值為 **Null**。 若要取得延伸錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。

## <a name="remarks"></a>備註

當您完成使用 **TLSConnectToLsServer** 函式所傳回的控制碼時，請呼叫 [**TLSDisconnectFromServer**](tlsdisconnectfromserver.md) 函數來釋放它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Mstlsapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TLS \_ 控制碼**](tls-handle.md)
</dt> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

