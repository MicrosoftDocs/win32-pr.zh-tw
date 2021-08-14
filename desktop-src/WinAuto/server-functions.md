---
title: '伺服器函式 (Windows 的協助工具功能) '
description: 伺服器函數
ms.assetid: 3cfa42c4-3d8b-44a1-9b8e-19248da12334
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2eb449e81371a1c0c9e230610de97b8abdefb41429c5753059540e45f921d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118828066"
---
# <a name="server-functions-windows-accessibility-features"></a>伺服器函式 (Windows 的協助工具功能) 

本章節包含與 Microsoft Active Accessibility 搭配使用之伺服器函數的相關資訊。

## <a name="in-this-section"></a>本節內容



| 主題                                                                     | 描述                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccNotifyTouchInteraction**](/windows/desktop/api/Oleacc/nf-oleacc-accnotifytouchinteraction)<br/> | 允許) 應用程式上的輔助技術 (，以透過 Windows 自動化 (API （例如 Microsoft 消費者介面自動化) 作為使用者觸控手勢的結果，來通知系統它正在與 UI 互動。 這可讓輔助技術通知目標應用程式，以及使用者要與觸控互動的系統。<br/> |
| [**AccSetRunningUtilityState**](/windows/desktop/api/Oleacc/nf-oleacc-accsetrunningutilitystate)<br/> | 設定系統值，指出在) 應用程式目前狀態 (的輔助技術是否會影響通常由系統提供的功能。 <br/>                                                                                                                                                                                 |
| [**CreateStdAccessibleObject**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleobject)<br/> | 使用指定之系統提供的使用者介面元素類型的方法和屬性，建立可存取的物件。<br/>                                                                                                                                                                                                                      |
| [**CreateStdAccessibleProxy**](/windows/desktop/api/Oleacc/nf-oleacc-createstdaccessibleproxya)<br/>   | 建立可存取的物件，這個物件具有系統提供之使用者介面專案之指定類別的屬性和方法。<br/>                                                                                                                                                                                                                 |
| [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject)<br/>                 | 傳回指定之物件的參考，與控制碼類似。 伺服器會在處理 [**WM \_ GETOBJECT**](wm-getobject.md)時傳回此參考。<br/>                                                                                                                                                                                              |
| [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult)<br/>                 | 根據先前產生的物件參考，抓取可存取物件的要求介面指標。<br/> 此函式是專為 Microsoft Active Accessibility 的內部使用所設計，而且只記載給資訊參考之用。 用戶端和伺服器都不應該呼叫此函式。<br/>                               |
| [**IsWinEventHookInstalled**](/windows/desktop/api/Winuser/nf-winuser-iswineventhookinstalled)<br/>     | 判斷是否有已安裝的 New-winevent 勾點，可能會收到指定事件的通知。<br/>                                                                                                                                                                                                                                                |
| [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)<br/>                       | 表示發生預先定義之事件的系統。 如果有任何用戶端應用程式已為事件註冊攔截函式，系統會呼叫用戶端的攔截函式。<br/>                                                                                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Active Accessibility 消費者介面服務](active-accessibility-user-interface-services-ref.md)
</dt> </dl>

 

 





