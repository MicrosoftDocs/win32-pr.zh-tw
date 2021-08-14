---
description: 安裝新的裝置。 系統會提示使用者選取裝置。
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: InstallNewDevice 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: cb12e87ceee4812ffc8c0e39d961ce631e26c4ab8ca7ae555785c8ad8381ca01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405304"
---
# <a name="installnewdevice-function"></a>InstallNewDevice 函式

安裝新的裝置。 系統會提示使用者選取裝置。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hwndParent* \[在\]
</dt> <dd>

最上層視窗的控制碼，可用於任何必要的使用者介面。

</dd> <dt>

*ClassGuid* \[在\]
</dt> <dd>

類別 **GUID** 的指標。 這是選擇性參數。 如果此參數為 **Null**，則使用者會在 [偵測選擇] 頁面上啟動。 如果此參數為 **guid \_ Null** 或 **guid \_ DEVCLASS \_ UNKNOWN**，則使用者會在 [類別選取] 頁面上啟動。

</dd> <dt>

*啟動* \[ 前擴展\]
</dt> <dd>

接收重新開機狀態之變數的指標。 此參數可以是 **di \_ NEEDRESTART** 或 **di \_ NEEDREBOOT**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回非零的值。

如果此函式失敗，則傳回值為零。 若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫。 您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 NewDev.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2003<br/>                                                        |
| DLL<br/>                      | <dl> <dt>NewDev.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[裝置管理函式](device-management-functions.md)
</dt> </dl>

 

