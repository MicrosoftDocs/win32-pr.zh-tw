---
description: 附件嵌入式管理單元擴充功能提供一個介面，讓使用者可用來變更服務特定的設定。
ms.assetid: 6f2dc372-dee4-4793-b943-395c0587ed5e
title: 建立附件嵌入式管理單元擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1a4cd4ccecf7fba6e33062fd2bb4df810316f2d66d42165ca207d855a14f961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894828"
---
# <a name="creating-an-attachment-snap-in-extension"></a>建立附件嵌入式管理單元擴充功能

附件嵌入式管理單元擴充功能提供一個介面，讓使用者可用來變更服務特定的設定。 附件嵌入式管理單元延伸模組必須符合 MMC 需求，才能成為有效的嵌入式管理單元延伸模組。 如需這些需求的詳細資訊，請參閱 [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) 檔。

除了 MMC 所需的介面之外，附件嵌入式管理單元擴充功能還必須執行 COM 介面 [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)。 [安全性設定] 嵌入式管理單元會呼叫此介面的方法，以判斷設定資料是否已變更，如果有的話，則會更新安全性資料庫。 在 [安全性設定] 嵌入式管理單元抓取該資料之前，[附件] 嵌入式管理單元必須儲存任何設定變更。

附件嵌入式管理單元延伸模組必須提供下列功能：

-   [顯示設定和分析資訊](displaying-configuration-and-analysis-information.md)
-   [修改消費者介面中的設定資訊](modifying-configuration-information-in-the-user-interface.md)
-   [修改安全性資料庫中的設定資訊](modifying-configuration-information-in-the-database.md)

為了協助您的嵌入式管理單元擴充功能執行這些工作，安全性設定嵌入式管理單元會執行 COM 介面 [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)，以提供您的嵌入式管理單元擴充功能可呼叫的方法，以初始化本身並從安全性資料庫查詢資訊。

建立附件嵌入式管理單元擴充功能之後，您必須使用 [ [註冊附件嵌入式管理](registering-an-attachment-snap-in-extension.md)單元] 延伸模組中所述的 [安全性設定] 嵌入式管理單元來註冊它。

 

 
