---
title: 原始輸入
description: 本節說明系統如何提供原始輸入給您的應用程式，以及應用程式如何接收和處理該輸入。
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Windows消費者介面，使用者輸入
- Windows消費者介面，原始輸入
- 使用者輸入，原始輸入
- 捕獲使用者輸入，原始輸入
- 原始輸入
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e26d67f2b014ce22c2d01cb4738cca4e041c59e417a216f0d75ffef6e6e4b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118482754"
---
# <a name="raw-input"></a>原始輸入

本節說明系統如何提供原始輸入給您的應用程式，以及應用程式如何接收和處理該輸入。 原始輸入有時稱為一般輸入。

### <a name="in-this-section"></a>本節內容



| Name                                           | 描述                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [關於原始輸入](about-raw-input.md)         | 討論裝置的使用者輸入，例如操縱杆、觸控式螢幕和麥克風。<br/> |
| [使用原始輸入](using-raw-input.md)         | 提供與原始輸入相關之工作的範例程式碼。<br/>                                |
| [原始輸入參考](raw-input-reference.md) | 包含 API 參考。<br/>                                                          |



 

### <a name="functions"></a>函式



| Name                                                                 | 描述                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | 呼叫預設的原始輸入程式，以提供應用程式未處理之任何原始輸入訊息的預設處理。 這個函式可確保處理每個訊息。 呼叫 [**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc)時所使用的參數，與視窗程式所收到的參數相同。 <br/> |
| [**GetRawInputBuffer**](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | 執行原始輸入資料的緩衝讀取。<br/>                                                                                                                                                                                                                                                              |
| [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | 從指定的裝置取得原始輸入。<br/>                                                                                                                                                                                                                                                                |
| [**GetRawInputDeviceInfo**](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | 取得原始輸入裝置的相關資訊。<br/>                                                                                                                                                                                                                                                                 |
| [**GetRawInputDeviceList**](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | 列舉附加至系統的原始輸入裝置。 <br/>                                                                                                                                                                                                                                                    |
| [**GetRegisteredRawInputDevices**](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | 取得目前應用程式之原始輸入裝置的相關資訊。<br/>                                                                                                                                                                                                                                |
| [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | 註冊提供原始輸入資料的裝置。<br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a>巨集



| Name                                                            | 描述                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**取得 \_ RAWINPUT 程式 \_ 代碼 \_ WPARAM**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | 從 [**WM \_ 輸入**](wm-input.md)中的 *wParam* 取得輸入碼。<br/>                              |
| [**NEXTRAWINPUTBLOCK**](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | 取得 [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) 結構陣列中下一個結構的位置。 <br/> |



 

### <a name="notifications"></a>通知



| Name                                                        | 描述                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [**WM \_ 輸入**](wm-input.md)                               | 傳送至正在取得原始輸入的視窗。 <br/>            |
| [**WM \_ 輸入 \_ 設備 \_ 變更**](wm-input-device-change.md) | 傳送至已註冊要接收原始輸入的視窗。 <br/> |



 

### <a name="structures"></a>結構



| Name                                                            | 描述                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**RAWHID**](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | 描述來自人體介面裝置 (HID) 的原始輸入格式。 <br/> |
| [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | 包含來自裝置的原始輸入。 <br/>                                      |
| [**RAWINPUTDEVICE**](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | 定義原始輸入裝置的資訊。 <br/>                             |
| [**RAWINPUTDEVICELIST**](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | 包含原始輸入裝置的相關資訊。<br/>                              |
| [**RAWINPUTHEADER**](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | 包含屬於原始輸入資料一部分的標頭資訊。 <br/>        |
| [**RAWKEYBOARD**](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | 包含鍵盤狀態的相關資訊。 <br/>                      |
| [**RAWMOUSE**](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | 包含滑鼠狀態的相關資訊。 <br/>                         |
| [**RID \_ 裝置 \_ 資訊**](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | 定義來自任何裝置的原始輸入資料。 <br/>                         |
| [**RID \_ 裝置 \_ 資訊 \_ 隱藏**](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | 定義來自指定之隱藏的原始輸入資料。 <br/>                  |
| [**RID \_ 裝置 \_ 資訊 \_ 鍵盤**](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | 定義來自指定鍵盤的原始輸入資料。 <br/>             |
| [**RID \_ 裝置 \_ 資訊 \_ 滑鼠**](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | 定義來自指定滑鼠的原始輸入資料。<br/>                 |



 

 

