---
description: 使用對等圖形或對等群組基礎結構時，資訊 (記錄對等發行至圖形或群組的) 會儲存為每個對等電腦上的資料庫。
ms.assetid: 1412b2eb-c97d-4415-998c-5f21eaadcc66
title: 資料庫匯入和匯出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48fc09259c06e6ebaf537d26c7288d0ad09c501
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944284"
---
# <a name="database-import-and-export"></a>資料庫匯入和匯出

使用對等圖形或對等群組基礎結構時，資訊 (記錄對等發行至圖形或群組的) 會儲存為每個對等電腦上的資料庫。 若要將應用程式從一部電腦遷移至另一部電腦，您可以從一部電腦匯出對等圖形或對等群組資料庫，然後將它匯入至另一部電腦。

下列清單會識別有關使用資料庫的重要資訊：

-   您只能匯入具有相同圖表和對等識別碼的資料庫。
-   如果已呼叫 [**PeerGraphListen**](/windows/desktop/api/P2P/nf-p2p-peergraphlisten)、 [**PeerGroupConnect**](/windows/desktop/api/P2P/nf-p2p-peergroupconnect)或 [**PeerGraphConnect**](/windows/desktop/api/P2P/nf-p2p-peergraphconnect) ，您就無法呼叫匯入和匯出函數。

**對等圖形基礎結構** 會使用下列呼叫來匯入和匯出記錄資料庫：

-   [**PeerGraphExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphexportdatabase)
-   [**PeerGraphImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergraphimportdatabase)

**對等群組基礎結構** 會使用下列呼叫來匯入和匯出記錄資料庫：

-   [**PeerGroupExportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupexportdatabase)
-   [**PeerGroupImportDatabase**](/windows/desktop/api/P2P/nf-p2p-peergroupimportdatabase)

 

 



