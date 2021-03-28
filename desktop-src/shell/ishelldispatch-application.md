---
description: 包含代表應用程式的物件。
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: 'IShellDispatch： Application 屬性 (Shldisp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5adeb5663220309310c7cccb323be877de909516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512232"
---
# <a name="ishelldispatchapplication-property"></a>IShellDispatch。應用程式屬性

包含代表應用程式的物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a>屬性值

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)型別的變數，會接收應用程式物件。

## <a name="remarks"></a>備註

這個屬性是透過 [**EjectPC**](shell-ejectpc.md) 屬性來執行和存取。

如果可以存取該物件， **應用程式** 屬性會傳回包含 WebBrowser 控制項之應用程式所支援的 automation 物件。 否則，此屬性會傳回 WebBrowser 控制項的 automation 物件。

使用這個屬性搭配 **Set** 和 **CreateObject** 命令，或使用 **GetObject** 命令來建立和操作 Windows Internet Explorer 應用程式的實例。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| 標頭<br/>                   | <dl> <dt>Shldisp。h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp .idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



 

 
