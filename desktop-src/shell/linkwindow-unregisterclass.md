---
description: 取消註冊 LinkWindow RegisterClass 所註冊的視窗類別 \_ 。
ms.assetid: 9e5c4326-efd1-43ca-a087-a436fe3f9bbd
title: LinkWindow_UnregisterClass 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LinkWindow_UnregisterClass
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 05a50d5f3af72c31ee04a1a9e8264acb22327c38f79f765ce2ad7a740086747e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968937"
---
# <a name="linkwindow_unregisterclass-function"></a>LinkWindow \_ UnregisterClass 函式

\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。 它可能會在 Windows 的後續版本中變更或無法使用。\]

取消註冊 [**LinkWindow \_ RegisterClass**](linkwindow-registerclass.md)所註冊的視窗類別。

## <a name="syntax"></a>語法


```C++
BOOL LinkWindow_UnregisterClass(void);
```



## <a name="parameters"></a>參數

此函式沒有參數。

## <a name="return-value"></a>傳回值

類型： **BOOL**

如果作業成功，則傳回 **TRUE** ;否則 **為 FALSE** 。

## <a name="remarks"></a>備註

此函式沒有相關聯的標頭或程式庫檔案，因此必須由序數值來呼叫。 使用 Shell32.dll 的 DLL 名稱呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ，以取得模組控制碼。 然後使用該模組控制碼呼叫 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ，並使用序號259來使用此函數。

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

 

 
