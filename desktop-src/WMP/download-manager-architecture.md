---
title: 下載管理員架構
description: 下載管理員架構
ms.assetid: cbd46bf2-613f-40ae-8506-2f3c5eb84ada
keywords:
- Windows Media Player 線上商店，下載管理員
- 線上商店、下載管理員
- 輸入2個線上商店、下載管理員
- Windows Media Player，下載管理員
- Windows Media Player 下載管理員
- 下載管理員
- 下載管理員的架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0567c32430e0cc15ea589bed43e2e81ffb3a08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671907"
---
# <a name="download-manager-architecture"></a>下載管理員架構

Windows Media Player 下載管理員使用 COM 技術。 這項功能是以一組程式設計介面來進行。您可以使用 Microsoft JScript 或 c + + 撰寫使用這些介面的程式設計程式碼。

指令碼語言會使用物件的概念來分割程式設計功能。 **DownloadManager** 物件模型會使用數個物件，將方法和屬性分割為邏輯組織，以將語義相關函數群組在一起。 下列各節包含下載管理員物件的相關資訊。



| 區段                                                                     | 描述                                                                                              |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [關於 DownloadManager 物件](#about-the-downloadmanager-object)       | **DownloadManager** 物件代表 Windows Media Player 下載管理員的根物件。 |
| [關於 DownloadCollection 物件](#about-the-downloadcollection-object) | **DownloadCollection** 物件代表下載專案的集合。                             |
| [關於 DownloadItem 物件](#about-the-downloaditem-object)             | **DownloadItem** 物件代表個別的下載要求。                                   |



 

## <a name="about-the-downloadmanager-object"></a>關於 DownloadManager 物件

**DownloadManager** 是 Windows Media Player 下載管理員的根物件。 所有其他物件都可透過此物件存取。 若要取得 **DownloadManager** 物件的存取權，請使用下列 JScript 語法：


```C++
var DownloadManager = external.DownloadManager;
```



這會建立 **DownloadManager** 物件的實例，然後用它來取出子物件。 例如，下列語法會從下載集合中取出識別碼為253675的第一個專案：


```C++
var firstItem = DownloadManager.getDownloadCollection(253675).item(0);
```



## <a name="about-the-downloadcollection-object"></a>關於 DownloadCollection 物件

**DownloadCollection** 物件代表要下載的檔案集合。 您可以使用此物件來判斷集合中有多少下載、從集合中移除專案、取出特定的下載專案，以及開始新的下載。 開始新的下載會自動將下載新增至集合。

## <a name="about-the-downloaditem-object"></a>關於 DownloadItem 物件

**DownloadItem** 物件代表個別下載。 下載專案一律會存在作為下載集合的一部分。 您可以使用此物件來取出下載專案的相關資訊，以及暫停、繼續或取消下載進行中的工作。

當您取消下載時，下載專案就會保留在其下載集合中。 在此情況下， **downloadCollection**。**downloadState** 會捕獲值4，表示已取消。

您可以使用 **downloadItem**。通知使用者已傳送多少檔案，或仍有多少時間可供下載的 **進度** 。 您可以使用這個值來估計剩餘的時間。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**下載管理員**](download-manager.md)
</dt> </dl>

 

 




