---
description: 傳送至主控台應用程式的 CPlApplet 函式，以提示它執行全域初始化（尤其是記憶體配置）。
ms.assetid: 0e7e9b14-9f44-496e-a518-5d3ae92868c5
title: 'CPL_INIT 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be6acdf58822e6f10f35880a97a7b5bbb9ce0b7bbbf7556b4c18c3f7ad96f72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456368"
---
# <a name="cpl_init-message"></a>CPL \_ 初始訊息

傳送至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式，以提示它執行全域初始化（尤其是記憶體配置）。


```C++

                CPlApplet(

    hwndCPl,

    CPL_INIT,

    wParam,  // = 0; not used, must be zero

    lParam   // = 0; not used, must be zero 

);

            
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果初始化成功， [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函數應該會傳回非零值。 否則，它應該會傳回零。

如果 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 傳回零，控制應用程式就會結束通訊，並釋放包含主控台應用程式的 DLL。

## <a name="remarks"></a>備註

因為這是主控台的應用程式可以表示錯誤狀況的唯一方法，所以應用程式應該配置記憶體以回應這則訊息。

在載入包含應用程式的 DLL 之後，會立即傳送此訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Cpl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> </dl>

 

 
