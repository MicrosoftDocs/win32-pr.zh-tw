---
description: 裝置重新導向功能會重新導向標準 MS-DOS 裝置、磁碟機號和 LPT 埠。 這可讓在系統上執行的應用程式使用裝置，並以完全透明的方式存取網路。
ms.assetid: a61ab1e6-dad9-4dc0-a908-f8440619f610
title: Device-Redirecting 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4929052ed2691d6264791cac431e59faaacdb92f7f96bb610d99fdd4ded471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008446"
---
# <a name="device-redirecting-functions"></a>Device-Redirecting 函式

裝置重新導向功能會重新導向標準 MS-DOS 裝置、磁碟機號和 LPT 埠。 這可讓在系統上執行的應用程式使用裝置，並以完全透明的方式存取網路。



| 函式                                                         | 描述                                                                                                                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)                       | 將本機裝置重新導向或連接到網路資源。<br/>                                                                                                                              |
| [**NPAddConnection3**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection3)                     | 執行與 [**NPAddConnection**](/windows/desktop/api/Npapi/nf-npapi-npaddconnection)相同的動作，但讓使用者指定應擁有任何對話方塊的視窗，以及應如何建立連接。<br/> |
| [**NPCancelConnection**](/windows/desktop/api/Npapi/nf-npapi-npcancelconnection)                 | 中斷網路連接。 如果裝置已中斷連線，則會記住變更，除非連接是 deviceless 連線。<br/>                                                    |
| [**NPGetConnection**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection)                       | 傳回連接的相關資訊。<br/>                                                                                                                                                  |
| [**NPGetConnection3**](/windows/desktop/api/Npapi/nf-npapi-npgetconnection3)                     | 傳回連接的相關資訊，即使連接目前已中斷連線。<br/>                                                                                                |
| [**NPGetConnectionPerformance**](/windows/desktop/api/Npapi/nf-npapi-npgetconnectionperformance) | 傳回連接的相關效能資訊。<br/>                                                                                                                                      |
| [**NPGetUniversalName**](/windows/desktop/api/Npapi/nf-npapi-npgetuniversalname)                 | 以函式呼叫期間指定的格式，傳回遠端或區域通用名稱。<br/>                                                                                            |



 

 

 




