---
title: 連線管理員
description: 如果客戶想要使用遠端存取服務 API 開發自訂的撥號，可能會想要調查 Microsoft 連線管理員和連線管理員系統管理組件。
ms.assetid: c3227aea-ba36-44f6-b69d-2c6aa4be360e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7959482542630b6dc90149971df08f7944f83fc
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104023106"
---
# <a name="connection-manager"></a>連線管理員

如果客戶想要使用遠端存取服務 API 開發自訂的撥號，可能會想要調查 Microsoft 連線管理員和連線管理員系統管理組件。 連線管理員是 Microsoft 的受控遠端存取用戶端。 它可讓系統管理員建立遠端存取設定套件，以散發給系統管理員的遠端使用者。 如需有關連線管理員和連線管理員系統管理組件的詳細資訊，請參閱 Microsoft Windows 2000 Server 和更新版本作業系統的線上說明。

您可以在完整的平臺軟體發展工具組 (SDK) 中找到範例連線管理員自訂動作的原始程式碼。 您可以從 [Microsoft 網站](https://msdn.microsoft.com/windowsserver/bb980924.aspx)下載 Platform SDK。 安裝之後，範例程式碼的路徑為% Install Path% \\ MICROSOFT SDK \\ sample \\ netds \\ Ras \\ ConnectionManager，其中% INSTALL path% 指定 Platform SDK 的基底安裝目錄 (例如 C： \\ Program Files) 。

自訂動作可讓遠端存取用戶端在連線程式的不同點上採取特定動作。 範例中示範的自訂動作會根據連接的伺服器位址，自動調整連線的 proxy 伺服器設定。 客戶可以使用此範例作為開始建立自己自訂動作的起點。

 

 




