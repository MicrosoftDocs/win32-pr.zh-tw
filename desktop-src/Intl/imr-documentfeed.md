---
description: 當選取的輸入法需要應用程式的轉換字串時，通知應用程式。 應用程式會透過 WM \_ IME 要求訊息接收此命令 \_ ，並使用如下所示的參數設定。
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: 'IMR_DOCUMENTFEED 通知碼 (Imm) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbef4c83d35fa02e2c879d76b9520df6d01588c07cb725b13e66888e9dd27722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948775"
---
# <a name="imr_documentfeed-notification-code"></a>IMR \_ DOCUMENTFEED 通知碼

當選取的輸入法需要應用程式的轉換字串時，通知應用程式。 應用程式會透過 [**WM \_ IME \_ 要求**](wm-ime-request.md) 訊息接收此命令，並使用如下所示的參數設定。


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a>參數

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

設定為 IMR \_ DOCUMENTFEED。

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

包含 [**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring) 結構之緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回目前的漢字重組字串結構。 如果 *lParam* 設定為 **Null**，則應用程式會傳回緩衝區所需的大小以保存結構。 如果不成功，此命令會傳回0。

## <a name="remarks"></a>備註

IME 會快取已轉換的字串，以提升轉換的精確度。 輸入法的一個快取限制是在下列情況下，它會遺失轉換的字串：

-   應用程式的插入號位置是由按鍵（例如，資料指標索引鍵）移動。
-   滑鼠會移動應用程式的插入號位置。
-   新檔會開啟。

使用 **IMR \_ DOCUMENTFEED** 命令，IME 隨時都可以重新整理其快取字串。 使用這個命令可改善轉換的精確度。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>Imm (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[輸入方法管理員](input-method-manager.md)
</dt> <dt>

[輸入方法管理員命令](input-method-manager-commands.md)
</dt> <dt>

[**RECONVERTSTRING**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**WM \_ IME \_ 要求**](wm-ime-request.md)
</dt> </dl>

 

 




