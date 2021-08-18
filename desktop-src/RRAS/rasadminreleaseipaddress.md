---
title: RasAdminReleaseIpAddress 回呼函式
description: RasAdminReleaseIpAddress 函式是由協力廠商 RAS 伺服器管理 DLL 匯出的應用程式定義函數。
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- RasAdminReleaseIpAddress 回呼函式 RAS
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 102c9af7a8e38ccbbb4a7e67b2734588857ddca93da862be211fd1223133f80d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788860"
---
# <a name="rasadminreleaseipaddress-callback-function"></a>RasAdminReleaseIpAddress 回呼函式

\[**RasAdminReleaseIpAddress** 函式可用於 Windows NT 4.0，並在後續版本中無法使用。 相反地，請使用 [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)。\]

**RasAdminReleaseIpAddress** 函式是由協力廠商 RAS 伺服器管理 DLL 匯出的應用程式定義函數。 RAS 會呼叫此函式，以通知 DLL 遠端用戶端已中斷連線，而且應該釋放 IP 位址。

## <a name="syntax"></a>語法


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszUserName* \[在\]
</dt> <dd>

指定以 null 終止之 Unicode 字串的指標，此字串會指定先前使用 [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) 函式取得 IP 位址之遠端使用者的名稱。

</dd> <dt>

*lpszPortName* \[在\]
</dt> <dd>

以 null 結束的 Unicode 字串指標，指定 *lpszUserName* 指定之使用者所連接的埠名稱。

</dd> <dt>

*pipAddress* \[在\]
</dt> <dd>

**IPADDR** 變數的指標，此變數會指定在先前呼叫 [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)時為此使用者傳回的 IP 位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函數沒有任何延伸的錯誤資訊;不要呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

只有當應用 **程式在先前** 呼叫 *lpszUserName* 參數所指定的 [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) *時，才* 會呼叫 **RasAdminReleaseIpAddress** 函式。

協力廠商 RAS 管理 DLL 的安裝程式必須在登錄中的下列機碼底下提供資訊，向 RAS 註冊 DLL：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

若要註冊 DLL，請在此機碼下設定下列值。



| 值名稱    | 值資料                                                                    |
|---------------|-------------------------------------------------------------------------------|
| *DisplayName* | **REG \_ SZ** 字串，其中包含 DLL 的使用者易記顯示名稱。 |
| *DLLPath*     | **REG \_ SZ** 字串，其中包含 DLL 的完整路徑。                  |



 

例如，名為 ProElectron，Inc. 之虛構公司的 RAS 管理 DLL 的登錄專案可能是：

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

*DisplayName*： **reg \_ Sz** ： ProElectron RAS 管理 DLL *DLLPath*： **reg \_ sz** ： C： \\ nt \\ system32 \\ntwkadm.dll

RAS 系統管理 DLL 的安裝程式也應該提供移除/卸載功能。 如果使用者移除 DLL，安裝程式應該刪除 DLL 的登錄專案。

 

 