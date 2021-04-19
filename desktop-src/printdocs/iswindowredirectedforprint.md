---
description: IsWindowRedirectedForPrint 函式會判斷指定的視窗目前是否重新導向以進行列印。
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: IsWindowRedirectedForPrint 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983895"
---
# <a name="iswindowredirectedforprint-function"></a>IsWindowRedirectedForPrint 函式

**IsWindowRedirectedForPrint** 函式會判斷指定的視窗目前是否重新導向以進行列印。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hWnd* \[在\]
</dt> <dd>

視窗控制代碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果視窗目前重新導向以進行列印，則函式會傳回非零值。否則，它會傳回零。

## <a name="remarks"></a>備註

當視窗處理 [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)的呼叫時，會將視窗重新導向以進行列印。 在 **PrintWindow** 的呼叫中，視窗會將其內容轉譯為螢幕上的裝置內容。

此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>User32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**WM \_ 列印**](/windows/desktop/gdi/wm-print)
</dt> <dt>

[**WM \_ PRINTCLIENT**](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

