---
title: '物件識別碼 (Winuser .h) '
description: 本主題說明 Microsoft Active Accessibility 物件識別碼、32位值，以識別視窗內可存取物件的類別。
ms.assetid: dc1603f8-29e5-4acd-817a-c6957feaff6c
topic_type:
- apiref
api_name:
- OBJID_ALERT
- OBJID_CARET
- OBJID_CLIENT
- OBJID_CURSOR
- OBJID_HSCROLL
- OBJID_NATIVEOM
- OBJID_MENU
- OBJID_QUERYCLASSNAMEIDX
- OBJID_SIZEGRIP
- OBJID_SOUND
- OBJID_SYSMENU
- OBJID_TITLEBAR
- OBJID_VSCROLL
- OBJID_WINDOW
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa2cf2099c5177be6f295ef6455646762525b26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984039"
---
# <a name="object-identifiers-winuserh"></a>物件識別碼 (Winuser .h) 

本主題說明 Microsoft Active Accessibility 物件識別碼、32位值，以識別視窗內可存取物件的 *類別* 。 Microsoft Active Accessibility 伺服器和 Microsoft 消費者介面自動化提供者會使用物件識別碼來判斷由 [**WM \_ GETOBJECT**](wm-getobject.md) message 要求所參考的物件。

用戶端會在其 [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) 回呼函式中接收這些值，並使用它們來識別視窗的部分。 伺服器會在呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) 或回應 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息時，使用這些值來識別視窗的對應部分。

伺服器可以定義自訂物件識別碼，以識別其應用程式內的其他物件類別。 自訂物件識別碼必須指派為正值，因為 Microsoft Active Accessibility 保留下列標準物件識別碼的零和所有負數值。

下列常數定義于 winuser 中：



| 常數                                                                                                                                                                                    | 描述                                                                                                                                                                                                                                                                                                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OBJID_ALERT"></span><span id="objid_alert"></span><dl> <dt>**OBJID \_ 警示**</dt> </dl>                                     | 與視窗或應用程式相關聯的警示。 系統提供的訊息方塊是以這個物件識別碼傳送事件的唯一 UI 元素。 伺服器應用程式無法使用 **AccessibleObjectFrom**_X_ 函數搭配此物件識別碼。 這是 Microsoft Active Accessibility 的已知問題。<br/>          |
| <span id="OBJID_CARET"></span><span id="objid_caret"></span><dl> <dt>**OBJID \_ 插入號**</dt> </dl>                                     | 文字插入列 (視窗中的插入號) 。<br/>                                                                                                                                                                                                                                                                                               |
| <span id="OBJID_CLIENT"></span><span id="objid_client"></span><dl> <dt>**OBJID \_ 用戶端**</dt> </dl>                                  | 視窗的工作區。 在大部分的情況下，作業系統會控制框架元素，而用戶端物件則包含應用程式所控制的所有元素。 伺服器只會處理 *lParam* 為 OBJID 用戶端、OBJID [**\_**](wm-getobject.md) \_ \_ 視窗或自訂物件識別碼的 WM GETOBJECT 訊息。<br/> |
| <span id="OBJID_CURSOR"></span><span id="objid_cursor"></span><dl> <dt>**OBJID 資料 \_ 指標**</dt> </dl>                                  | 滑鼠指標。 系統中只有一個滑鼠指標，且它不是任何視窗的子指標。<br/>                                                                                                                                                                                                                                      |
| <span id="OBJID_HSCROLL"></span><span id="objid_hscroll"></span><dl> <dt>**OBJID \_ HSCROLL**</dt> </dl>                               | 視窗的水準捲軸。<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="OBJID_NATIVEOM"></span><span id="objid_nativeom"></span><dl> <dt>**OBJID \_ NATIVEOM**</dt> </dl>                            | 為了回應此物件識別碼，協力廠商應用程式可以公開自己的物件模型。 協力廠商應用程式可以傳回任何 COM 介面，以回應此物件識別碼。<br/>                                                                                                                                             |
| <span id="OBJID_MENU"></span><span id="objid_menu"></span><dl> <dt>**OBJID \_ 功能表**</dt> </dl>                                        | 視窗的功能表列。<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="OBJID_QUERYCLASSNAMEIDX"></span><span id="objid_queryclassnameidx"></span><dl> <dt>**OBJID \_ QUERYCLASSNAMEIDX**</dt> </dl> | Oleacc.dll 在內部使用的物件識別碼。 如需詳細資訊，請參閱 [附錄 F： OBJID \_ QUERYCLASSNAMEIDX 的物件識別碼值](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md)。<br/>                                                                                                                  |
| <span id="OBJID_SIZEGRIP"></span><span id="objid_sizegrip"></span><dl> <dt>**OBJID \_ SIZEGRIP**</dt> </dl>                            | 視窗的大小底圖：選用的框架元件，位於視窗框架的右下角。<br/>                                                                                                                                                                                                                                  |
| <span id="OBJID_SOUND"></span><span id="objid_sound"></span><dl> <dt>**OBJID \_ 音效**</dt> </dl>                                     | 音效物件。 音效物件沒有螢幕位置或子系，但有名稱和狀態屬性。 它們是播放音效的應用程式子系。<br/>                                                                                                                                                         |
| <span id="OBJID_SYSMENU"></span><span id="objid_sysmenu"></span><dl> <dt>**OBJID \_ SYSMENU**</dt> </dl>                               | 視窗的系統功能表。<br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="OBJID_TITLEBAR"></span><span id="objid_titlebar"></span><dl> <dt>**OBJID \_ 標題列**</dt> </dl>                            | 視窗的標題列。<br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="OBJID_VSCROLL"></span><span id="objid_vscroll"></span><dl> <dt>**OBJID \_ VSCROLL**</dt> </dl>                               | 視窗的垂直捲動條。<br/>                                                                                                                                                                                                                                                                                                           |
| <span id="OBJID_WINDOW"></span><span id="objid_window"></span><dl> <dt>**OBJID \_ 視窗**</dt> </dl>                                  | 視窗本身，而非子物件。<br/>                                                                                                                                                                                                                                                                                               |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Winuser (包含) 的 Windows。h </dt> </dl> |



 

 





