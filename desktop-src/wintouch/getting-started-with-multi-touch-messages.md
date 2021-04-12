---
title: 具有 Windows Touch 訊息的開始使用
description: 本節說明在應用程式中取得函式 Windows Touch 輸入相關聯的工作。
ms.assetid: cd4e140e-a0b8-494f-82d9-bc0bfba55ecd
keywords:
- Windows Touch，訊息
- Windows Touch，註冊觸控輸入
- Windows Touch，測試輸入數位板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39048a4f9d643026396328093ae554c0eaa5d08
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375592"
---
# <a name="getting-started-with-windows-touch-messages"></a>具有 Windows Touch 訊息的開始使用

本節說明在應用程式中取得函式 Windows Touch 輸入相關聯的工作。

使用 Windows Touch 訊息時，通常會執行下列步驟：

1.  測試輸入數位板的功能。
2.  註冊以接收 Windows Touch 的訊息。
3.  處理訊息。

用於 Windows Touch 的訊息為 [**WM \_ 觸控**](wm-touchdown.md)。 此訊息表示與數位板聯繫的各種狀態。

## <a name="testing-the-capabilities-of-the-input-digitizer"></a>測試輸入數位板的功能

[GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics)函式可用來查詢輸入數位板的功能，方法是傳入 **SM \_ 數位化** 器的 *nIndex* 值。 [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) 會傳回位欄位，指出裝置是否就緒、裝置是否支援畫筆或觸控、輸入裝置是否為整合式或外部，以及裝置是否支援多個輸入 (Windows Touch) 。 下表顯示各種欄位的位。



| bit   | 8           | 7           | 6        | 5        | 4            | 3              | 2              | 1                |
|-------|-------------|-------------|----------|----------|--------------|----------------|----------------|------------------|
| 值 | 堆疊就緒 | 多重輸入 | 保留 | 保留 | 外部畫筆 | 整合式畫筆 | 外部觸控 | 整合式觸控 |



 

若要測試特定功能的命令結果，您可以使用位 & 運算子和您要測試的特定位。 例如，若要測試 Windows Touch，您會測試第七個順序位是否設定為十六進位)  (0x40。 下列程式碼範例顯示如何測試這些值。


```C++
#include <windows.h>
```




```C++
// test for touch
int value = GetSystemMetrics(SM_DIGITIZER);
if (value & NID_READY){ /* stack ready */}
if (value  & NID_MULTI_INPUT){
    /* digitizer is multitouch */ 
    MessageBoxW(hWnd, L"Multitouch found", L"IsMulti!", MB_OK);
}
if (value & NID_INTEGRATED_TOUCH){ /* Integrated touch */}
```



下表列出用來測試輸入數位板之觸控功能的 windows. h 中定義的常數。



| Name                   | 值      | 描述                                                                                                                                                                                   |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TABLET \_ 設定 \_ 無   | 0x00000000 | 輸入數位板沒有觸控功能。                                                                                                                                         |
| NID \_ 整合式 \_ 觸控 | 0x00000001 | 整合式觸控數位板用於輸入。                                                                                                                                              |
| NID \_ 外部 \_ 觸控   | 0x00000002 | 外部觸控數位板用於輸入。                                                                                                                                                |
| NID \_ 整合式 \_ 畫筆   | 0x00000004 | 整合式畫筆數位板用於輸入。                                                                                                                                                |
| NID \_ 外部 \_ 畫筆     | 0x00000008 | 外部畫筆數位板用於輸入。                                                                                                                                                  |
| NID \_ 多重 \_ 輸入      | 0x00000040 | 輸入支援多個輸入的數位板會用於輸入。                                                                                                                        |
| NID \_ 就緒             | 0x00000080 | 輸入數位板已備妥可供輸入。 如果未設定此值，可能表示 tablet 服務已停止、不支援數位板，或尚未安裝數位板驅動程式。 |



 

檢查 NID \_ \* 值是檢查使用者電腦功能以設定觸控、畫筆或非平板電腦輸入之應用程式的實用方式。 例如，如果您有動態使用者介面 (UI) 並且想要自動設定它，您可以檢查 NID \_ 整合式 \_ 觸控、NID \_ 多點觸控，並且可以在使用者第一次執行應用程式時取得最大的潤色數目。

> [!Note]  
> SM GETSYSTEMMETRICS 有一些固有的限制 \_ 。 例如，不支援隨插即用。 基於這個理由，使用此函式作為永久設定的方法時，請特別小心。

 

## <a name="registering-to-receive-windows-touch-input"></a>註冊接收 Windows Touch 輸入

在接收 Windows Touch 輸入之前，應用程式必須先註冊才能接收 Windows Touch 輸入。 藉由註冊應用程式視窗，應用程式會指出它具有觸控相容性。 應用程式註冊其視窗之後，就會在視窗上進行輸入時，將來自 Windows Touch 驅動程式的通知轉送到應用程式。 當應用程式關閉時，它會取消註冊其視窗以停用通知。

> [!Note]  
> [**WM \_觸控**](wm-touchdown.md) 訊息目前是「貪心的」。 在視窗上收到第一個觸控訊息之後，所有觸控訊息都會傳送到該視窗，直到另一個視窗獲得焦點為止。

 

> [!Note]  
> 根據預設，您會收到 [**wm \_ 手勢**](wm-gesture.md) 訊息，而非 [**wm \_ 觸控**](wm-touchdown.md) 訊息。 如果您呼叫 [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow)，就會停止接收 **WM \_ 手勢** 訊息。

 

下列程式碼示範如何註冊應用程式，以接收 Win32 應用程式中的 Windows Touch 訊息。


```C++
RegisterTouchWindow(hWnd, 0);
```



## <a name="handling-windows-touch-messages"></a>處理 Windows Touch 訊息

您可以透過許多方式，在 Windows 作業系統中處理來自應用程式的 Windows Touch 訊息。 如果您正在設計 GUI 應用程式，請在函式內新增程式碼 `WndProc` 以處理感興趣的訊息。 如果您要在 MFC) 或 managed 應用程式的 MFC (程式設計，您可以為感興趣的訊息加入處理常式。 下列程式碼範例示範如何在 Windows 應用程式中從 WndProc 處理觸控訊息。


```C++
  LRESULT OnTouch(HWND hWnd, WPARAM wParam, LPARAM lParam ){
    BOOL bHandled = FALSE;
    UINT cInputs = LOWORD(wParam);
    PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
    if (pInputs){
        if (GetTouchInputInfo((HTOUCHINPUT)lParam, cInputs, pInputs, sizeof(TOUCHINPUT))){
            for (UINT i=0; i < cInputs; i++){
                TOUCHINPUT ti = pInputs[i];
                //do something with each touch input entry
            }            
            bHandled = TRUE;
        }else{
             /* handle the error here */
        }
        delete [] pInputs;
    }else{
        /* handle the error here, probably out of memory */
    }
    if (bHandled){
        // if you handled the message, close the touch input handle and return
        CloseTouchInputHandle((HTOUCHINPUT)lParam);
        return 0;
    }else{
        // if you didn't handle the message, let DefWindowProc handle it
        return DefWindowProc(hWnd, WM_TOUCH, wParam, lParam);
    }
  }


LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
      // pass touch messages to the touch handler 
      case WM_TOUCH:
        OnTouch(hWnd, wParam, lParam);
        break;
```





下列程式碼會示範如何執行訊息對應和訊息處理常式。 請注意，訊息必須在訊息對應中宣告，然後才能執行訊息的處理常式。 例如，在 MFC 應用程式中，可以在對話方塊程式碼中宣告這項功能。 另請注意，交談視窗的函式 `OnInitDialog` 必須包含對 [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) 的呼叫，例如 `RegisterTouchWindow(m_hWnd, 0)` 。


```C++
  // Class implementations within a dialog
  LRESULT TestDlg::OnTouch( WPARAM wParam, LPARAM lParam ){
    //Insert handler code here to do something with the message or uncomment the following line to test
    //MessageBox(L"touch!", L"touch!", MB_OK);
    return 0;
  }
  // The message map
  BEGIN_MESSAGE_MAP()
    ON_WM_CREATE()
    ... ... ...
    ON_MESSAGE(WM_TOUCH, OnTouch)
  END_MESSAGE_MAP()  
 
  BOOL TestDlg::OnInitDialog()
  {
    CDialog::OnInitDialog();    

    RegisterTouchWindow(m_hWnd, 0);
     ... ... ...
  }  
  
```



觸碰視窗將表示從快顯視窗中的觸控。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Touch 輸入](guide-multi-touch-input.md)
</dt> </dl>

 

 