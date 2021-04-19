---
description: 當觸發程式事件發生時，可以註冊以啟動或停止服務。
ms.assetid: ca02a3ae-b16a-4427-b6db-b935c9cf23b3
title: 服務觸發程式事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdefd94b7896936f7ab4fc014647b08470611573
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980018"
---
# <a name="service-trigger-events"></a>服務觸發程式事件

當觸發程式事件發生時，可以註冊以啟動或停止服務。 這樣就不需要在系統啟動時啟動服務，或讓服務輪詢或主動等候事件;服務可以在需要時啟動，而不是在是否有要執行的工作時自動啟動。 預先定義的觸發程式事件範例包括抵達指定裝置介面類別別的裝置，或特定防火牆埠的可用性。 服務也可以註冊 Windows (ETW) 提供者的 [事件追蹤](../etw/event-tracing-portal.md) 所產生的自訂觸發程式事件。

**Windows server 2008、Windows Vista、Windows server 2003 和 WINDOWS XP：** 在 Windows Server 2008 R2 和 Windows 7 之前，不支援服務觸發程式事件。

觸發程式是由觸發程式事件類型、觸發程式事件子類型、為了回應觸發程式事件所採取的動作，以及特定觸發程式事件類型的 () 一個或多個觸發程式特定資料項目。 子類型和觸發程式特定的資料項目會一起指定通知服務事件的條件。 資料項目的格式取決於觸發程式事件類型。資料項目可以是二進位資料、字串或 multistring。 字串必須是 Unicode;不支援 ANSI 字串。

為了註冊觸發程式事件，服務會使用服務設定 **\_ 觸發程式 \_ \_ 資訊** 來呼叫 [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) ，並提供 [**服務觸發程式 \_ \_ 資訊**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info)結構。 **服務 \_ 觸發程式 \_ 資訊** 結構會指向 [**服務 \_ 觸發**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger)程式結構的陣列，每個結構都指定一個觸發程式。

如果在系統啟動時觸發條件為 true，或當系統正在執行時觸發條件變成 true，就會執行指定的觸發程式動作。 例如，如果服務註冊要在特定裝置可用時啟動，則在系統啟動時啟動服務（如果裝置已經插入電腦）。如果使用者在系統執行時插入裝置，則會在裝置抵達時啟動服務。

如果觸發程式具有觸發程式特定的資料項目，則只有在伴隨觸發程式事件的資料項目符合服務以觸發程式指定的其中一個資料項目時，才會執行觸發程式動作。 二進位資料比對是透過位比較來完成。 字串比對不區分大小寫。 如果資料項目是 multistring，則 multistring 中的所有字串都必須相符。

當服務啟動以回應觸發程式事件時，服務會在其 ServiceMain 回呼函式中，以 argv 1 的形式接收 **服務觸發程式啟動的 \_ \_ \_ 引數** \[ \] 。 [](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) *Argv* \[0 \] 一律是服務的簡短名稱。

當服務沒有要執行的工作時，註冊要啟動以回應觸發程式事件的服務，可能會在閒置的閒置時間之後停止本身。 停止本身的服務必須做好準備，以便處理 **服務 \_ 控制 \_ TRIGGEREVENT** 控制要求，該要求會在服務停止時抵達。 每當服務處於執行中狀態時，如果發生新的觸發程式事件，SCM 就會傳送 **服務 \_ 控制 \_ TRIGGEREVENT** 控制項要求。 為了避免遺失觸發程式事件，服務應該會在服務從執行轉換為已停止的任何 **服務 \_ 控制 \_ TRIGGEREVENT** 控制項要求時，傳回 **錯誤的 \_ 關閉 \_ \_** 。 這會指示 SCM 將觸發程式事件排入佇列，並等候服務進入已停止狀態。 SCM 接著會採用與佇列觸發程式事件相關聯的動作，例如啟動服務。

當服務已準備好要再次處理觸發程式事件時，它會在 [**>setservicestatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)的呼叫中，將 **服務 \_ 接受 \_ TRIGGEREVENT** 設定為其控制項接受的遮罩。 這通常是在服務呼叫 **>setservicestatus** ，且 **服務 \_ 正在** 執行時進行。 SCM 接著會發出每個佇列觸發程式事件的 **服務 \_ 控制 \_ TRIGGEREVENT** 要求，直到佇列是空的。

具有正在執行之相依服務的服務，無法停止以回應觸發程式事件。

觸發程式-啟動和觸發程式-停止要求在記憶體不足的情況下無法保證。

使用 [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) 函式來取得服務的觸發程式事件設定。

SC 工具 (sc.exe) 可以在命令提示字元中用來設定或查詢服務的觸發程式事件。 使用 **triggerinfo** 選項，將服務設定為啟動或停止，以回應觸發程式事件。 使用 **qtriggerinfo** 選項來查詢服務的觸發程式設定。

下列範例會查詢 W32time 服務的觸發程式設定，此設定會在電腦加入網域時啟動，並在電腦離開網域時停止。

``` syntax
C:\>sc qtriggerinfo w32time
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: w32time

        START SERVICE
          DOMAIN JOINED STATUS         : 1ce20aba-9851-4421-9430-1ddeb766e809 [DOMAIN JOINED]
        STOP SERVICE
          DOMAIN JOINED STATUS         : ddaf516e-58c2-4866-9574-c3b615d42ea1 [NOT DOMAIN JOINED]
```

下列範例會查詢平板電腦輸入服務的觸發程式設定，此設定會在具有 **GUID** {4d1e55b2-f16f-11cf-88cb-001111000030} 的 HID 裝置和任何指定的 HID 裝置識別碼抵達時啟動。

``` syntax
C:\>sc qtriggerinfo tabletinputservice
[SC] QueryServiceConfig2 SUCCESS

SERVICE_NAME: tabletinputservice

        START SERVICE
          DEVICE INTERFACE ARRIVAL     : 4d1e55b2-f16f-11cf-88cb-001111000030 [INTERFACE CLASS GUID]
            DATA                       : HID_DEVICE_UP:000D_U:0001
            DATA                       : HID_DEVICE_UP:000D_U:0002
            DATA                       : HID_DEVICE_UP:000D_U:0003
            DATA                       : HID_DEVICE_UP:000D_U:0004
```

 

 
