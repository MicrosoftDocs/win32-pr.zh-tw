---
description: 如果網路 dde 代理程式偵測到區域網路 DDE 活動，則會啟動網路 dde。
ms.assetid: bc1e6a06-be07-4ae8-94da-9603a885b3a5
title: 網路 DDE 代理程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a6259b512782102936f54f65646454509c6b37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001658"
---
# <a name="network-dde-agent"></a>網路 DDE 代理程式

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

如果網路 dde 代理程式偵測到區域網路 DDE 活動，則會啟動網路 dde。 它不會偵測到嘗試連接的遠端用戶端。 因此，在任何用戶端可以成功連接之前，必須先在伺服器電腦上啟動網路 DDE。 請注意，網路 DDE 預設並不會啟動。 若要啟動網路 DDE，請執行 NETDDE.EXE。 這個檔案位於您的 Windows 目錄中。

網路 DDE 代理程式也會啟動網路 DDE 所需的應用程式。 在網路 DDE 啟動之後，DDE 交談是透過與其中一個網路 DDE 應用程式相關聯的網路 DDE 視窗來控制。 此應用程式會作為 proxy。 它會與所有本機和遠端 DDE 應用程式進行通訊。

 

 



