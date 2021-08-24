---
title: 視窗工作站和桌上型電腦功能
description: 應用程式可以搭配使用下列功能與視窗站物件。
ms.assetid: 6214c28f-1035-446c-8c79-5d1dd638af2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccda67841508081444f7025e457c9a778195b99d0ab67ebb585362d7a3b22cd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810398"
---
# <a name="window-station-and-desktop-functions"></a>視窗工作站和桌上型電腦功能

應用程式可以搭配使用下列功能與 [視窗站](window-stations.md) 物件。



| 函式                                                     | 描述                                                                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**CloseWindowStation**](/windows/win32/api/winuser/nf-winuser-closewindowstation)             | 關閉開啟的視窗工作站控制碼。                                                                           |
| [**CreateWindowStation**](/windows/win32/api/winuser/nf-winuser-createwindowstationa)           | 建立視窗站物件、將它與目前的進程產生關聯，並將它指派給目前的會話。 |
| [**EnumWindowStations**](/windows/win32/api/winuser/nf-winuser-enumwindowstationsa)             | 列舉目前會話中的所有視窗電臺。                                                          |
| [**GetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-getprocesswindowstation)   | 針對呼叫進程，抓取目前視窗工作站的控制碼。                                       |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | 抓取指定之視窗工作站或桌面物件的相關資訊。                                     |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | 抓取指定之視窗工作站或桌面物件的安全性資訊。                              |
| [**OpenWindowStation**](/windows/win32/api/winuser/nf-winuser-openwindowstationa)               | 開啟指定的視窗站。                                                                             |
| [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)   | 將指定的視窗站指派給呼叫進程。                                                    |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | 設定指定之視窗工作站或桌面物件的相關資訊。                                          |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | 設定指定之視窗工作站或桌面物件的安全性資訊。                                   |



 

應用程式可以搭配使用下列功能與 [桌面](desktops.md) 物件。



| 函式                                                     | 描述                                                                                                                        |
|--------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**CloseDesktop**](/windows/win32/api/winuser/nf-winuser-closedesktop)                         | 關閉桌面物件的開啟控制碼。                                                                                         |
| [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa)                       | 建立新的桌面、將它與目前呼叫進程的視窗站產生關聯，並將它指派給呼叫執行緒。 |
| [**CreateDesktopEx**](/windows/win32/api/winuser/nf-winuser-createdesktopexa)                   | 建立新的桌面、將它與目前呼叫進程的視窗站產生關聯，並將它指派給呼叫執行緒。 |
| [**EnumDesktops**](/windows/win32/api/winuser/nf-winuser-enumdesktopsa)                         | 列舉與呼叫進程目前視窗工作站相關聯的所有桌面。                                         |
| [**EnumDesktopWindows**](/windows/win32/api/winuser/nf-winuser-enumdesktopwindows)             | 列舉與指定桌面相關聯的所有最上層視窗。                                                            |
| [**GetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-getthreaddesktop)                 | 抓取指派給指定執行緒之桌面的控制碼。                                                                |
| [**GetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-getuserobjectinformationa) | 取得視窗工作站或桌面物件的相關資訊。                                                                         |
| [**GetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-getuserobjectsecurity)  | 取得視窗工作站或桌面物件的安全性資訊。                                                                  |
| [**OpenDesktop**](/windows/win32/api/winuser/nf-winuser-opendesktopa)                           | 開啟指定的桌面物件。                                                                                                |
| [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop)                 | 開啟接收使用者輸入的桌面。                                                                                        |
| [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)                 | 將指定的桌面指派給呼叫的執行緒。                                                                               |
| [**SetUserObjectInformation**](/windows/win32/api/winuser/nf-winuser-setuserobjectinformationa) | 設定視窗工作站或桌面物件的相關資訊。                                                                         |
| [**SetUserObjectSecurity**](/windows/desktop/api/winuser/nf-winuser-setuserobjectsecurity)  | 設定視窗工作站或桌面物件的安全性資訊。                                                                  |
| [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop)                       | 讓桌面成為可見的，並啟用它。 這可讓桌面接收來自使用者的輸入。                                 |



 

 

 