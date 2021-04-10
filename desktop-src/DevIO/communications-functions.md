---
description: 下列函式會搭配通訊資源使用。
ms.assetid: ba7d1a9e-6906-4923-a8eb-db58050ba699
title: 通訊功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64853bf2b0c42d4e7ca607fbbe624995cfe1a249
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187723"
---
# <a name="communications-functions"></a>通訊功能

下列函式會搭配通訊資源使用。



| 函式                                                   | 描述                                                                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**BuildCommDCB**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcba)                       | 以裝置控制字元串中指定的值填滿指定的 [**DCB**](/windows/desktop/api/Winbase/ns-winbase-dcb) 結構。                           |
| [**BuildCommDCBAndTimeouts**](/windows/desktop/api/Winbase/nf-winbase-buildcommdcbandtimeoutsa) | 將裝置定義字串轉譯為適當的裝置控制區塊代碼，並將其放入裝置控制區塊。 |
| [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak)                   | 還原指定通訊裝置的字元傳輸，並將傳輸行置於 nonbreak 狀態。    |
| [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror)                   | 捕獲通訊錯誤的相關資訊，並報告通訊裝置的目前狀態。                  |
| [**CommConfigDialog**](/windows/desktop/api/Winbase/nf-winbase-commconfigdialoga)               | 顯示驅動程式提供的設定對話方塊。                                                                           |
| [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction)           | 指示指定的通訊裝置執行擴充功能。                                                     |
| [**GetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getcommconfig)                     | 抓取通訊裝置目前的設定。                                                                |
| [**GetCommMask**](/windows/desktop/api/Winbase/nf-winbase-getcommmask)                         | 抓取指定通訊裝置的事件遮罩值。                                                   |
| [**GetCommModemStatus**](/windows/desktop/api/Winbase/nf-winbase-getcommmodemstatus)           | 抓取數據機控制暫存器值。                                                                                       |
| [**GetCommProperties**](/windows/desktop/api/Winbase/nf-winbase-getcommproperties)             | 抓取指定通訊裝置的通訊屬性相關資訊。                               |
| [**GetCommState**](/windows/desktop/api/Winbase/nf-winbase-getcommstate)                       | 抓取指定通訊裝置的目前控制項設定。                                                  |
| [**GetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-getcommtimeouts)                 | 針對指定的通訊裝置上的所有讀取和寫入作業，捕獲超時參數。                      |
| [**GetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-getdefaultcommconfiga)       | 抓取指定通訊裝置的預設設定。                                                   |
| [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm)                             | 捨棄指定通訊資源的輸出或輸入緩衝區中的所有字元。                                |
| [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak)                       | 暫停指定通訊裝置的字元傳輸，並將傳輸行置於中斷狀態。       |
| [**SetCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setcommconfig)                     | 設定通訊裝置的目前設定。                                                                     |
| [**SetCommMask**](/windows/desktop/api/Winbase/nf-winbase-setcommmask)                         | 指定要針對通訊裝置監視的一組事件。                                                         |
| [**SetCommState**](/windows/desktop/api/Winbase/nf-winbase-setcommstate)                       | 根據裝置控制區塊中的規格設定通訊裝置。                                  |
| [**SetCommTimeouts**](/windows/desktop/api/Winbase/nf-winbase-setcommtimeouts)                 | 針對指定的通訊裝置上的所有讀取和寫入作業設定超時參數。                           |
| [**SetDefaultCommConfig**](/windows/desktop/api/Winbase/nf-winbase-setdefaultcommconfiga)       | 設定通訊裝置的預設設定。                                                                    |
| [**SetupComm**](/windows/desktop/api/Winbase/nf-winbase-setupcomm)                             | 初始化指定通訊裝置的通訊參數。                                               |
| [**TransmitCommChar**](/windows/desktop/api/Winbase/nf-winbase-transmitcommchar)               | 在指定通訊裝置的輸出緩衝區中，將指定的字元前移至任何擱置中的資料。         |
| [**WaitCommEvent**](/windows/desktop/api/Winbase/nf-winbase-waitcommevent)                     | 等候指定的通訊裝置發生事件。                                                             |



 

 

 



