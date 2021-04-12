---
description: 下列清單包含 TAPI MSP 支援的功能。
ms.assetid: e36bba94-1fa7-4514-9f8a-bcd690b04d73
title: 支援的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d10fd9ac787483b8dfa6e15046a733992adb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191368"
---
# <a name="features-supported"></a>支援的功能

下列清單包含 TAPI MSP 支援的功能。

-   執行 MSP，以處理每個 MSP 實例的單一位址。 多個類似的位址是藉由具現化 MSP 多次來處理。 這可大幅簡化 MSP 和基類的執行。
-   會實 MSPI 介面，包括 [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)、 [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)、 [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)和 [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)。
-   針對音訊和影片執行立即可用的靜態終端機。
-   實作為泛型終端基類。 上述的靜態終端機和 Termmgr.dll 中找到的動態終端機，都使用這些終端基類。 MSP 也可以使用它們來執行額外的終端機。
-   使用終端機管理員來處理動態終端。 使用訊息泵 (在背景工作執行緒上建立動態終端機，讓主控台應用程式不必處理影片轉譯終端機的視窗訊息，也可以簡化) 的同步處理問題。
-   支援針對每個資料流程使用篩選圖形的呼叫。
-   實行圖形事件的處理。
-   會搭配本身的背景工作執行緒使用執行緒共用 Api 來處理事件。
-   使用原本針對路由) 專案開發的 Windows 2000 (追蹤 Api，以及額外的邏輯來提供有彈性的一般記錄機制，可同時登入下列任何組合：使用者或核心模式的偵錯工具;以元件分隔記錄訊息的個別主控台視窗;記錄檔。
-   執行無限制執行緒。

 

 
