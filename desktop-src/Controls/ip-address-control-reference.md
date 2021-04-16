---
title: IP 位址控制
description: 本章節包含與 IP 位址控制項搭配使用之程式設計項目的相關資訊。
ms.assetid: vs|controls|~\controls\ipaddress\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c80fc87a12ce49038f4c1836e684fa0f8895bd0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462121"
---
# <a name="ip-address-control"></a>IP 位址控制

本章節包含與 IP 位址控制項搭配使用之程式設計項目的相關資訊。

### <a name="overviews"></a>概觀



| 主題                                          | 目錄                                                                                                                    |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| [IP 位址控制項](ip-address-controls.md) | 網際網路通訊協定 (IP) 位址控制可讓使用者以容易理解的格式輸入 IP 位址。<br/> |



 

### <a name="macros"></a>巨集



| 主題                                         | 目錄                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**第一個 \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)   | 從以 [**IPM \_ GETADDRESS**](ipm-getaddress.md) 訊息取出的已壓縮 IP 位址中，解壓縮 [欄位 0] 值。 <br/> |
| [**第四個 \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) | 從以 [**IPM \_ GETADDRESS**](ipm-getaddress.md) 訊息取出的已壓縮 IP 位址中，解壓縮 [欄位 3] 值。 <br/> |
| [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress)        | 將四個位元組值封裝成適合與 [**IPM \_ SETADDRESS**](ipm-setaddress.md) 訊息搭配使用的單一 LPARAM。 <br/>  |
| [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange)            | 將兩個位元組值封裝成適合與 [**IPM \_ SETRANGE**](ipm-setrange.md) 訊息搭配使用的單一 LPARAM。 <br/>       |
| [**第二個 \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress) | 從以 [**IPM \_ GETADDRESS**](ipm-getaddress.md) 訊息取出的已壓縮 IP 位址中，解壓縮欄位1值。 <br/> |
| [**第三個 \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)   | 從以 [**IPM \_ GETADDRESS**](ipm-getaddress.md) 訊息抓取的封裝 IP 位址中，解壓縮 [欄位 2] 值。 <br/> |



 

### <a name="messages"></a>訊息



| 主題                                         | 目錄                                                                                                                              |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**IPM \_ CLEARADDRESS**](ipm-clearaddress.md) | 清除 IP 位址控制項的內容。 <br/>                                                                            |
| [**IPM \_ GETADDRESS**](ipm-getaddress.md)     | 取得 IP 位址控制項中所有四個欄位的位址值。 <br/>                                                    |
| [**IPM \_ ISBLANK**](ipm-isblank.md)           | 判斷 IP 位址控制項中的所有欄位是否為空白。 <br/>                                                             |
| [**IPM \_ SETADDRESS**](ipm-setaddress.md)     | 在 IP 位址控制項中設定所有四個欄位的位址值。 <br/>                                                    |
| [**IPM \_ SETFOCUS**](ipm-setfocus.md)         | 將鍵盤焦點設定為 IP 位址控制項中的指定欄位。 將會選取該欄位中的所有文字。 <br/> |
| [**IPM \_ SETRANGE**](ipm-setrange.md)         | 在 IP 位址控制項中，設定指定之欄位的有效範圍。 <br/>                                                   |



 

### <a name="notifications"></a>通知



| 主題                                     | 目錄                                                                                                                                                                                   |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) | 當使用者變更控制項中的欄位，或從某個欄位移至另一個欄位時傳送。 此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。 <br/> |



 

### <a name="structures"></a>結構



| 主題                              | 目錄                                                                                              |
|------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**NMIPADDRESS**](/windows/win32/api/commctrl/ns-commctrl-nmipaddress) | 包含 [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) 通知碼的資訊。 <br/> |



 

 

 





