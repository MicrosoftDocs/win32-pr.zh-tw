---
description: 網路 DDE 可用來在網路中不同電腦上執行的應用程式之間，起始和維護 DDE 交談所需的網路連線。
ms.assetid: f9eee391-2b4a-4c17-bea5-72cda5124e1c
title: 關於網路 DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412971f6bef8d2782dce38b5aef413e4d073f6b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319011"
---
# <a name="about-network-dde"></a>關於網路 DDE

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

網路 DDE 可用來在網路中不同電腦上執行的應用程式之間，起始和維護 DDE 交談所需的網路連線。 DDE *對話* 是用戶端與伺服器應用程式之間的互動。 您可以在應用程式中使用網路 DDE 搭配 DDE 和 DDE 管理程式庫 (DDEML) 。

DDE 是一種處理序間通訊形式，使用共用記憶體來交換應用程式之間的資料。 應用程式可以使用 DDE 進行一次資料傳輸，或是進行中的交換和更新資料。 如需有關 DDE 的詳細資訊，請參閱 [動態資料交換](../dataxchg/dynamic-data-exchange.md)。

DDEML 可簡化將 DDE 功能新增至應用程式的工作。 應用程式會使用 DDEML 所提供的函式來管理 DDE 交談，而不是直接傳送、張貼和處理 DDE 訊息。 如需 DDEML 的詳細資訊，請參閱 [動態資料交換管理程式庫](../dataxchg/dynamic-data-exchange-management-library.md)。

## <a name="network-dde-files"></a>網路 DDE 檔案

若要使用網路 DDE 的 API 元素，您必須在原始程式檔中包含 NDDEApi 標頭檔，並在連結行上包含 NDDEApi .lib 檔案。 您也必須確認已載入 NDDEApi.dll 的檔案。

如需詳細資訊，請參閱下列主題：

-   [網路 DDE 代理程式](network-dde-agent.md)
-   [DDE 共用](dde-shares.md)
-   [受信任的共用和安全性](trusted-shares-and-security.md)
-   [管理 DDE 共用](managing-dde-shares.md)

 

 
