---
description: TAPI 伺服器 (TAPISRV) 是使用者電腦上電話語音資料的中央存放庫。
ms.assetid: 794d230c-abe8-429d-bbf5-91ba364b16ab
title: TAPI 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a6886a5d8e56519f10fc370ed15adc3b1af7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850796"
---
# <a name="tapi-server"></a>TAPI 伺服器

TAPI 伺服器 (TAPISRV) 是使用者電腦上電話語音資料的中央存放庫。 此服務處理常式會追蹤本機和遠端電話語音資源、註冊用來處理輔助電話語音要求的應用程式，以及擱置中的非同步函式，也會啟用與電話語音服務提供者一致的介面， (Tsp) 。 如需詳細資訊以及說明 TAPI 伺服器與其他元件的關係以及其角色總覽的圖表，請參閱 [Microsoft 電話語音程式設計模型](microsoft-telephony-programming-model.md)。

針對在 Windows Server 2003 作業系統、Windows XP 及 Windows 2000 上執行的電腦，TAPISRV 會在 Svchost.exe 的內容中執行。 針對在 Windows NT 上執行的電腦，它會以個別的服務程式執行。 當應用程式將 TAPI DLL 載入其進程空間並執行初始化操作時，DLL 會建立與 TAPI 伺服器的 RPC 連結。 TAPI 伺服器會將電話服務提供者 (Tsp) 載入其進程空間中。 無論有多少應用程式存取指定提供者的裝置，都只會有一個指定之 TSP 的實例存在。

 

 



