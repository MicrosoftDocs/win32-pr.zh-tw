---
title: 用戶端函數
description: 用戶端函數
ms.assetid: c6d3577c-6975-4708-a1bd-ee70992f851d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3d5a2c8b20008dd179c12d3f81eb9d40e70cb9639e0d90dd9b3532ad5cba15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052826"
---
# <a name="client-functions"></a>用戶端函數

本章節包含與 Microsoft Active Accessibility 搭配使用之用戶端函式的相關資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)<br/>                       | 抓取可存取容器物件內每個子系的子系識別碼或 [**IDispatch**](idispatch-interface.md) 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)<br/>         | 抓取物件的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面位址，此物件會產生用戶端事件攔截函式目前正在處理的事件。<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)<br/>         | 針對顯示于螢幕上指定點的物件，抓取 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標的位址。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)<br/>       | 針對與指定之視窗相關聯的物件，抓取指定介面的位址。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**GetOleaccVersionInfo**](/windows/desktop/api/Oleacc/nf-oleacc-getoleaccversioninfo)<br/>                   | 抓取 Microsoft Active Accessibility 檔 Oleacc.dll 的版本號碼和組建編號。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**GetProcessHandleFromHwnd**](getprocesshandlefromhwnd.md)<br/>           | 從視窗控制碼抓取進程控制碼。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**GetRoleText**](/windows/desktop/api/Oleacc/nf-oleacc-getroletexta)<br/>                                     | 針對指定的角色值，抓取描述物件角色的當地語系化字串。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**GetStateText**](/windows/desktop/api/Oleacc/nf-oleacc-getstatetexta)<br/>                                   | 抓取當地語系化的字串，這個字串會描述單一預先定義之狀態位旗標的物件狀態。 由於狀態值是一或多個位旗標的組合，因此用戶端會多次呼叫此函式，以取得所有狀態字串。<br/>                                                                                                                                                                                                                                                                                                                      |
| [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)<br/>                             | 設定事件範圍的事件攔截函式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UnhookWinEvent**](/windows/desktop/api/Winuser/nf-winuser-unhookwinevent)<br/>                               | 移除先前呼叫 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)所建立的事件攔截函式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**WindowFromAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-windowfromaccessibleobject)<br/>       | 抓取對應于 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面之特定實例的視窗控制碼。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [*WinEventProc 回呼函式*](/windows/desktop/api/Winuser/nc-winuser-wineventproc)<br/> | 應用程式定義的回呼 (或攔截) 函式，系統會呼叫此函式以回應可存取物件所產生的事件。 攔截函式會視需要處理事件通知。 用戶端會藉由呼叫 [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook)來安裝攔截函式和要求特定類型的事件通知。<br/> [**WINEVENTPROC**](/previous-versions/windows/desktop/legacy/dd373882(v=vs.85))型別定義此回呼函數的指標。 [*WinEventProc*](/windows/desktop/api/winuser/nc-winuser-wineventproc) 是應用程式定義函數名稱的預留位置。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Active Accessibility 消費者介面服務](active-accessibility-user-interface-services-ref.md)
</dt> </dl>

 

