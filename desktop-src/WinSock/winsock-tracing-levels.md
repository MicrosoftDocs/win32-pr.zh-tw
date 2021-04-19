---
description: 深入瞭解： Winsock 追蹤層級
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Winsock 追蹤層級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975818"
---
# <a name="winsock-tracing-levels"></a>Winsock 追蹤層級

## <a name="levels-of-winsock-tracing"></a>Winsock 追蹤的層級

Winsock 追蹤有兩種可能的記錄層級：

-   資訊
-   「詳細資訊」

資訊層級會追蹤通訊端建立和關閉事件，以及任何發生在通訊端上的錯誤。

詳細資訊層級包含資訊層級的事件，並新增了傳送和接收事件的額外追蹤。 詳細資訊記錄會用來捕捉緩衝區損毀問題以及寫入不良的應用程式。

[資訊] 或 [詳細資訊] 層級可以與 Winsock 網路事件追蹤一起使用。 Winsock 類別目錄變更追蹤只支援資訊層級。

## <a name="information-event-tracing"></a>資訊事件追蹤

下列清單詳細說明在資訊層級追蹤的 Winsock 網路事件通訊端作業：

-   通訊端建立

    系統會在建立通訊端時記錄事件，可用來追蹤通訊端的存留期。 這些事件也包含在接聽通訊端上接受連接所建立的通訊端。

-   繫結

    系統會記錄本機 IP 位址，以協助將 Winsock 追蹤資訊與應用程式的通訊端呼叫產生關聯。

-   連線

    系統會記錄已連接通訊端的遠端 IP 位址，以協助將 Winsock 追蹤資訊與應用程式的通訊端呼叫產生關聯。

-   Winsock 起始的中止和取消

    每當 Winsock 主動中止或取消要求時，就會記錄事件。

-   傳輸起始的重設

    當基礎傳輸表示連接已重設時，會記錄事件。

-   傳送和接收錯誤

    每當基礎傳輸的傳送或接收呼叫失敗時，就會記錄事件。

-   通訊端中斷連線和關閉

    當通訊端控制碼關閉時，就會記錄事件。

## <a name="verbose-event-tracing"></a>詳細資訊事件追蹤

所有資訊事件都是在詳細資訊層級進行追蹤。 下列清單詳細說明在詳細資訊層級追蹤的額外 Winsock 網路事件通訊端作業：

-   傳送和接收緩衝區

    當傳送和接收呼叫張貼到 Winsock，以及完成這些呼叫時，會記錄使用者緩衝區位址和長度的事件。 這對於診斷緩衝區重複使用問題以及無效率的緩衝區使用來說很有用。

-   通訊端選項

    當應用程式變更特定通訊端選項值時，就會記錄事件。 記錄的部分選項包含 \_ SNDBUF，因此 \_ RCVBUF、SIO \_ 啟用 \_ 迴圈 \_ 佇列和 FIONBIO。

-   WSAPoll 並選取

    系統會記錄應用程式使用 [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) 的事件，並 [**選取**](/windows/desktop/api/Winsock2/nf-winsock2-select) 可用於尋找效能瓶頸的呼叫。

-   Winsock 起始的中止和取消

    每當 Winsock 主動中止或取消要求時，就會記錄事件。

-   事件遮罩

    事件是由應用程式註冊以使用 [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) 函式的事件遮罩來記錄。

-   資料包

    每當資料包抵達且沒有可複製的緩衝區空間時，就會記錄事件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Winsock 追蹤的控制權](control-of-winsock-tracing.md)
</dt> <dt>

[Winsock 追蹤](winsock-tracing.md)
</dt> <dt>

[Winsock 目錄變更追蹤詳細資料](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Winsock 網路事件追蹤詳細資料](winsock-tracing-event-details.md)
</dt> </dl>

 

 
