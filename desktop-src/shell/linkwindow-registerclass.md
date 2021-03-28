---
description: 註冊視窗類別，讓 SysLink 通用控制項可以在視窗中使用。
ms.assetid: 1e6dd741-81be-40bb-a8b5-d565f593c4e9
title: LinkWindow_RegisterClass 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_RegisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 7b5bfd2e1a45ff3f65df7cf3d3cae41bf4926aaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973384"
---
# <a name="linkwindow_registerclass-function"></a>LinkWindow \_ RegisterClass 函式

\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。 它可能會在後續版本的 Windows 中改變或無法使用。 請改用 [**InitCommonControlsEx**](/windows/win32/api/commctrl/nf-commctrl-initcommoncontrolsex) 。\]

註冊視窗類別，讓 [SysLink](../controls/syslink-overview.md) 通用控制項可以在視窗中使用。

## <a name="syntax"></a>語法


```C++
BOOL LinkWindow_RegisterClass(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

類型： **BOOL**

如果註冊成功，則傳回 **TRUE** ;否則 **為 FALSE** 。

## <a name="remarks"></a>備註

此函式沒有相關聯的標頭或程式庫檔案，因此必須由序數值來呼叫。 使用 Shell32.dll 的 DLL 名稱呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。 然後使用該模組控制碼呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，並使用序號258來使用此函數。

使用 [**LinkWindow \_ UnregisterClass**](linkwindow-unregisterclass.md) 在使用後取消註冊類別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[SysLink 控制項總覽](../controls/syslink-overview.md)
</dt> </dl>

 

 
