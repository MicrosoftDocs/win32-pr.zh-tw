---
title: " (網路管理) 的訊息函數"
description: 網路管理訊息功能會傳送訊息並維護訊息別名。 訊息函數如下所示。
ms.assetid: 9face737-3472-4a53-97b6-e861a60ee96a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3629a281637fe4ecd0c937ce0c7504beac8e11d2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383706"
---
# <a name="message-functions-network-management"></a> (網路管理) 的訊息函數

\[由於不支援「警報器」和「messenger」服務，因此 Windows Vista 不支援訊息功能。\]

網路管理訊息功能會傳送訊息並維護訊息別名。 訊息函數如下所示。

**Windows Server 2003：** 預設會停用警報器和 messenger 服務。 您必須重新啟用服務，才能呼叫網路管理 [警示功能](alert-functions.md) 或網路管理訊息功能。



| 函式                                               | 描述                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [**NetMessageBufferSend**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | 將訊息傳送至已註冊的訊息別名。                                  |
| [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | 在訊息名稱資料表中註冊訊息別名。                            |
| [**NetMessageNameDel**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | 從訊息名稱資料表刪除訊息別名。                            |
| [**NetMessageNameEnum**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | 列出儲存在訊息名稱資料表中的所有訊息別名。                 |
| [**NetMessageNameGetInfo**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | 傳回訊息名稱資料表中特定訊息別名的相關資訊。 |



 

*訊息* 是傳送給網路上的使用者或應用程式之文字資料的緩衝區。 若要接收訊息，使用者或應用程式必須在電腦的訊息名稱表格中註冊訊息別名。 預設會註冊下列別名：「使用者」、「電腦」、「網域」或「」 \* (電腦) 的目前網域。 "Domain" 別名指定一組電腦，這些電腦的功能變數名稱定義為其網域或其工作組，並接聽相同子網的廣播。 針對 NetBIOS over TCP/IP，如果名稱伺服器解析功能變數名稱，或在路由器之間轉送 NetBIOS 資料包廣播，則指定 "domain" 別名也可以跨子網成功。 因此，傳送至網域的訊息無法保證傳遞至網域的所有成員。 如果某些網域成員已安裝多個支援 NetBIOS 的傳輸，也可能會多次接收訊息。

您也可以藉由呼叫 [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) 函數來註冊訊息別名。 *訊息名稱表* 包含已註冊的訊息別名清單 (使用者和應用程式) 允許接收訊息。 在訊息名稱表格中註冊的別名不區分大小寫。

接收端電腦上必須執行 messenger 服務，才能在接收到訊息時顯示快顯視窗訊息。 此外，工作站服務必須在本機電腦上執行。 NetBIOS 是在傳送者與接收者之間使用的傳輸機制。

訊息函數可在兩個資訊層級取得：

-   [**MSG \_ 資訊 \_ 0**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_0)
-   [**MSG \_ 資訊 \_ 1**](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_1)

**MSG \_ INFO \_ 1** 資訊層級只存在於相容性。 Messenger 服務不會轉寄名稱或允許名稱轉寄給它。

 

 




