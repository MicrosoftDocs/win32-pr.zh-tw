---
description: 近端分享存放區
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: 近端分享存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850579"
---
# <a name="people-near-me-stores"></a>近端分享存放區

能夠 [近端分享](about-people-near-me.md) (PNM) 的應用程式可以使用下列資料存放區：

### <a name="windows-address-book"></a>Windows 通訊錄

Windows 通訊錄會儲存連絡人及其數位憑證的相關資訊。 代表目前登入使用者的 '**Me**' 連絡人也儲存在 Windows 通訊錄中。

### <a name="certificate-store"></a>憑證存放區

憑證存放區包含 '**Me**' 連絡人的自我簽署憑證。

### <a name="application-store"></a>應用程式市集

應用程式安裝程式會在安裝過程中使用 PNM 註冊應用程式。 這些物件是在嘗試使用一般應用程式（例如電腦遊戲）連接到使用者時，可供其他使用者搜尋的物件。 針對每個應用程式，應用程式存放區包含應用程式的名稱、全域唯一識別碼 (GUID) 、應用程式範圍、描述，以及程式可執行檔的路徑。 應用程式的範圍可以設定為 [無] (未公告) 、近端分享 (在本機子網上公告) 、[連絡人] (僅針對連絡人進行公告，或在本機子網上公告的所有) 或 [連絡人] (。 應用程式存放區位於 Windows Vista 登錄中。

 

 



