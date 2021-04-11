---
title: IMsRdpClientNonScriptable4 LaunchedViaClientShellInterface 屬性
description: 指定使用者是否使用遠端桌面 Web 存取 (RD Web 存取) 介面啟動用戶端控制項。
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- LaunchedViaClientShellInterface 屬性遠端桌面服務
- LaunchedViaClientShellInterface 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，LaunchedViaClientShellInterface 屬性
- LaunchedViaClientShellInterface 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，LaunchedViaClientShellInterface 屬性
- LaunchedViaClientShellInterface 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、LaunchedViaClientShellInterface 屬性
- LaunchedViaClientShellInterface 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、LaunchedViaClientShellInterface 屬性
- LaunchedViaClientShellInterface 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、LaunchedViaClientShellInterface 屬性
- LaunchedViaClientShellInterface 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、LaunchedViaClientShellInterface 屬性
- LaunchedViaClientShellInterface 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、LaunchedViaClientShellInterface 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d5854a4e75be455035fd9a123418bd486932379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934580"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a>IMsRdpClientNonScriptable4：： LaunchedViaClientShellInterface 屬性

指定使用者是否使用遠端桌面 Web 存取 (RD Web 存取) 介面啟動用戶端控制項。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a>屬性值

設定 **LaunchedViaClientShellInterface** 屬性。

## <a name="error-codes"></a>錯誤碼

如果成功，則傳回 **S \_ OK** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                           |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





