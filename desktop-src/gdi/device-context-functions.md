---
description: 下列函式適用于裝置內容。
ms.assetid: 9ff68d16-0f27-4cc8-932a-b2063cfed135
title: 裝置內容函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c33eda03ce65a5873c4420f6675128243e30493dc75fa3055c8718f6826f4a94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966048"
---
# <a name="device-context-functions"></a>裝置內容函式

下列函式適用于裝置內容。



| 函式                                                   | 描述                                                                                                                               |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc)                               | 取消指定之裝置內容上的任何暫止作業。                                                                            |
| [**ChangeDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsa)     | 將預設顯示裝置的設定變更為指定的圖形模式。                                                        |
| [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) | 將指定之顯示裝置的設定變更為指定的圖形模式。                                                      |
| [**CreateCompatibleDC**](/windows/desktop/api/Wingdi/nf-wingdi-createcompatibledc)           | 建立與指定裝置相容的記憶體裝置內容。                                                                     |
| [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca)                               | 使用指定的名稱，建立裝置的裝置內容。                                                                           |
| [**CreateIC**](/windows/desktop/api/Wingdi/nf-wingdi-createica)                               | 建立指定裝置的資訊內容。                                                                                  |
| [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc)                               | 刪除指定的裝置內容。                                                                                                     |
| [**DeleteObject**](/windows/desktop/api/Wingdi/nf-wingdi-deleteobject)                       | 刪除邏輯畫筆、筆刷、字型、點陣圖、區域或調色板，釋出與物件相關聯的所有系統資源。                  |
| [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa)           | 抓取印表機設備磁碟機的功能。                                                                                    |
| [**DrawEscape**](/windows/desktop/api/Wingdi/nf-wingdi-drawescape)                           | 提供指定的影片顯示器的繪圖功能，而這些功能無法透過圖形裝置介面直接提供。       |
| [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa)           | 捕獲系統中顯示裝置的相關資訊。                                                                              |
| [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa)         | 抓取顯示裝置的其中一個圖形模式的相關資訊。                                                               |
| [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa)     | 抓取顯示裝置的其中一個圖形模式的相關資訊。                                                               |
| [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects)                         | 列舉適用于指定之裝置內容的畫筆或筆刷。                                                                |
| [**EnumObjectsProc**](/windows/win32/api/wingdi/nc-wingdi-gobjenumproc)                 | 搭配 [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) 函式使用的應用程式定義回呼函數。                                       |
| [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject)               | 抓取已在指定的裝置內容中選取之指定型別的物件控制碼。                           |
| [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc)                                     | 抓取所指定視窗的工作區或整個螢幕的顯示裝置內容控制碼。                        |
| [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor)                 | 抓取指定之裝置內容的目前筆刷色彩。                                                                       |
| [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex)                                 | 抓取所指定視窗的工作區或整個螢幕的顯示裝置內容控制碼。                        |
| [**GetDCOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getdcorgex)                           | 抓取指定之裝置內容的最終轉譯來源。                                                                    |
| [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor)                     | 抓取指定之裝置內容的目前畫筆色彩。                                                                         |
| [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps)                     | 抓取指定裝置的裝置特定資訊。                                                                           |
| [**GetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-getlayout)                             | 抓取裝置內容的版面配置。                                                                                                 |
| [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject)                             | 取得指定之繪圖物件的資訊。                                                                                  |
| [**GetObjectType**](/windows/desktop/api/Wingdi/nf-wingdi-getobjecttype)                     | 抓取指定之物件的類型。                                                                                               |
| [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject)                   | 抓取其中一個股票畫筆、筆刷、字型或調色板的控制碼。                                                                 |
| [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc)                             | 釋放裝置內容，釋出以供其他應用程式使用。                                                                      |
| [**ResetDC**](/windows/desktop/api/Wingdi/nf-wingdi-resetdca)                                 | 使用指定的資訊更新指定的印表機或繪圖器裝置內容。                                                  |
| [**RestoreDC**](/windows/desktop/api/Wingdi/nf-wingdi-restoredc)                             | 將裝置內容還原到指定的狀態。                                                                                         |
| [**SaveDC**](/windows/desktop/api/Wingdi/nf-wingdi-savedc)                                   | 將描述所選物件和圖形模式的資料複製到內容堆疊，以儲存指定之裝置內容的目前狀態。 |
| [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject)                       | 在指定的裝置內容中選取物件。                                                                                      |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | 將目前的裝置內容筆刷色彩設定為指定的色彩值。                                                                 |
| [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor)                     | 將目前的裝置內容畫筆色彩設定為指定的色彩值。                                                                   |
| [**SetLayout**](/windows/desktop/api/Wingdi/nf-wingdi-setlayout)                             | 設定裝置內容的版面配置。                                                                                                     |
| [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc)                       | 傳回與裝置內容相關聯的視窗控制碼。                                                                          |



 

 

 
