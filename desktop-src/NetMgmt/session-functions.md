---
title: " (網路管理) 的會話函數"
description: 檢查會話函式，這是網路管理功能群組。 這些功能會控制在工作站和伺服器之間建立的網路會話。
ms.assetid: ef912cd9-be5c-4202-89aa-e60f275e8938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78479391e4dc2d2aa0ced8af16a8b6cf6f3a9b05
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406121"
---
# <a name="session-functions-network-management"></a> (網路管理) 的會話函數

網路管理會話功能會控制在工作站和伺服器之間建立的網路會話。 函數需要在伺服器上啟動伺服器服務。

以下列出會話函數。



| 函式                                      | 描述                                                                                       |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)         | 刪除工作站與伺服器之間的目前連接;終止網路會話。 |
| [**NetSessionEnum**](/windows/desktop/api/lmshare/nf-lmshare-netsessionenum)       | 傳回針對伺服器建立之所有目前會話的相關資訊。                          |
| [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) | 傳回特定會話的相關資訊。                                                   |



 

*會話* 是工作站和伺服器之間的連結。 當工作站第一次建立與伺服器上共用資源的連接時，就會建立會話。 在會話結束之前，工作站和伺服器之間的所有進一步連線都是相同會話的一部分。 若要結束會話，連接的伺服器端上的應用程式會呼叫 [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) 函數。

網路管理會話函式會使用 *username* 參數來管理每個使用者的資訊。 因為每個會話可以有多個使用者，所以需要此參數才能存取會話的使用者特定資訊。

會話函數可在下列資訊層級取得：

-   [**會話 \_ 資訊 \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-session_info_0)
-   [**會話 \_ 資訊 \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-session_info_1)
-   [**會話 \_ 資訊 \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-session_info_2)
-   [**會話 \_ 資訊 \_ 10**](/windows/desktop/api/lmshare/ns-lmshare-session_info_10)
-   [**會話 \_ 資訊 \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-session_info_502)

如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理會話功能達成的相同功能。 如需詳細資訊，請參閱 [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) 和 [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)。

 

 
