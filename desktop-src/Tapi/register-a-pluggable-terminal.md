---
description: 可將插入式終端機的註冊，呼叫至實終端機組件的 DllRegisterServer 函式。 下列程式碼範例可以放入 DllRegisterServer 的程式碼中。
ms.assetid: d88a8d2c-4b05-4c31-928f-0baf1dbc218c
title: 註冊可插入的終端機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7be84d9e2063c28a320c49d5249ea6434094b9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985159"
---
# <a name="register-a-pluggable-terminal"></a>註冊可插入的終端機

可將插入式終端機的註冊，呼叫至實終端機組件的 **DllRegisterServer** 函式。 下列程式碼範例可以放入 **DllRegisterServer** 的程式碼中。

``` syntax
ITPluggableTerminalClassRegistration* pTerminal;
BSTR bstrTerminalSuperclass = SysAllocString(L"{F7438990-D6EB-11d0-82A6-00AA00B5CA1B}");

// If (NULL == bstrTerminalSuperclass) process the error here.

BSTR bstrTerminalClass = SysAllocString(L"{AED6483E-3304-11d2-86F1-006008B0E5D2}");

// If (NULL == bstrTerminalClass) process the error here.

BSTR bstrTerminalCLSID = SysAllocString(L"{E2F7AEF7-4971-11D1-A671-006097C9A2E8}");

// If (NULL == bstrTerminalCLSID) process the error here.

HRESULT hr;
hr = CoCreateInstance( 
    CLSID_PluggableTerminalRegistration,
    NULL,
    CLSCTX_INPROC_SERVER,
    IID_ITPluggableTerminalClassRegistration,
    (void**)&pTerminal);

hr = pTerminal->put_TerminalClass( bstrTerminalClass );
// If (hr != S_OK) process the error here. 
pTerminal->put_CLSID( bstrTerminalCLSID );
// If (hr != S_OK) process the error here.
pTerminal->put_Name( ... );
// If (hr != S_OK) process the error here.
pTerminal->put_Company( ... );
// If (hr != S_OK) process the error here.
pTerminal->put_Version( ... );
// If (hr != S_OK) process the error here.
pTerminal->put_Direction( ... );
// If (hr != S_OK) process the error here.
pTerminal->put_MediaTypes( ... );
// If (hr != S_OK) process the error here.
pTerminal->Add( bstrTerminalSuperclass );
// If (hr != S_OK) process the error here.

// Free the memory created by SysAllocString().
SysFreeString(bstrTerminalSuperclass);
SysFreeString(bstrTerminalClass);
SysFreeString(bstrTerminalCLSID);
```

 

 



