---
description: 工作組模式中的安全性限制
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: 工作組模式中的安全性限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af613b8de16b99090bcdb02bde0015d01312df3d642c895d61ef59ff80873eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546272"
---
# <a name="security-limitations-in-workgroup-mode"></a>工作組模式中的安全性限制

[訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85))工作組設定不允許 com + 佇列元件服務支援應用程式安全性。 如果您已安裝含有工作組設定的訊息佇列，您必須在 [COM + 應用程式內容] 對話方塊的 [**佇列**] 索引標籤上，使用 [元件 **服務] 系統** 管理工具選取 [不要 **驗證訊息**]，以停用此設定中所存取之每個佇列應用程式的 [安全性](specifying-the-authentication-protocol.md)。 這應該只在信任的網路上完成，而且必須在用戶端和伺服器上執行（如果已匯出應用程式的話）。

 

 



