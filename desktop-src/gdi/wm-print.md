---
description: 會將 WM \_ 列印訊息傳送至視窗，要求它在指定的裝置內容中（最常用於印表機裝置內容）繪製自身。
ms.assetid: e6be2ecd-603a-405f-8a48-68d971e1f6de
title: 'WM_PRINT 訊息 (Winuser .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09d3cb7dbb3b4a4fca7a2af4272f1b4175aa26e911d1def909c97ba35f3d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964848"
---
# <a name="wm_print-message"></a>WM \_ 列印訊息

會將 **WM \_ 列印** 訊息傳送至視窗，要求它在指定的裝置內容中（最常用於印表機裝置內容）繪製自身。

視窗會透過其 [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) 函數接收此訊息。


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要在其中繪製的裝置內容控制碼。

</dd> <dt>

*lParam* 
</dt> <dd>

繪圖選項。 這個參數可以是下列一或多個值。



| 值                                                                                                                                                                  | 意義                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="PRF_CHECKVISIBLE"></span><span id="prf_checkvisible"></span><dl> <dt>**PRF \_ CHECKVISIBLE**</dt> </dl> | 只有當視窗可見時，才會繪製視窗。<br/>          |
| <span id="PRF_CHILDREN"></span><span id="prf_children"></span><dl> <dt>**PRF \_ 子系**</dt> </dl>             | 繪製所有可見的子系視窗。<br/>              |
| <span id="PRF_CLIENT"></span><span id="prf_client"></span><dl> <dt>**PRF \_ 用戶端**</dt> </dl>                   | 繪製視窗的工作區。<br/>             |
| <span id="PRF_ERASEBKGND"></span><span id="prf_erasebkgnd"></span><dl> <dt>**PRF \_ ERASEBKGND**</dt> </dl>       | 在繪製視窗之前清除背景。<br/> |
| <span id="PRF_NONCLIENT"></span><span id="prf_nonclient"></span><dl> <dt>**PRF \_ 非工作區**</dt> </dl>          | 繪製視窗的非工作區。<br/>          |
| <span id="PRF_OWNED"></span><span id="prf_owned"></span><dl> <dt>**\_所擁有的 PRF**</dt> </dl>                      | 繪製所有擁有的視窗。<br/>                         |



 

</dd> </dl>

## <a name="remarks"></a>備註

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)函式會根據指定的繪圖選項來處理此訊息：如果指定了 PRF \_ CHECKVISIBLE，而且不會顯示視窗，則不執行任何動作。如果指定了 prf 非工作區，請 \_ 在指定的裝置內容中繪製非工作區，如果指定了 prf \_ ERASEBKGND，請傳送一個 [**wm \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md)訊息給視窗，如果 \_ 指定了 prf 用戶端 [**\_**](wm-printclient.md) ，請傳送一個 wm PRINTCLIENT 訊息給視窗，如果設定了 prf 子系，請將 \_ 每個可見的子 **\_** \_ **\_** 視窗傳送至 wm 列印訊息。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Winuser (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[繪製和繪製總覽](painting-and-drawing.md)
</dt> <dt>

[繪製和繪製訊息](painting-and-drawing-messages.md)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md)
</dt> <dt>

[**WM \_ PRINTCLIENT**](wm-printclient.md)
</dt> </dl>

 

 
