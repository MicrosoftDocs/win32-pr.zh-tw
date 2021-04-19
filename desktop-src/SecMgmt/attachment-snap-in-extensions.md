---
description: 附件嵌入式管理單元延伸模組是顯示服務特定使用者介面之附件的元件。
ms.assetid: 1cafa02f-f240-476c-8ce2-ba088afaf889
title: 附件嵌入式管理單元擴充功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55267edcd30f32ad371a4aa276587b4eca06c57
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106997321"
---
# <a name="attachment-snap-in-extensions"></a>附件嵌入式管理單元擴充功能

附件嵌入式管理單元延伸模組是顯示服務特定使用者介面之附件的元件。 此嵌入式管理單元的擴充功能是由安全性設定嵌入式管理單元所主控。附件延伸模組與其嵌入式管理單元主機之間的通訊，是由 [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) 檔中所述的標準 MMC 機制所處理。

除了嵌入式管理單元延伸模組必須支援的介面才能成為 MMC 嵌入式管理單元擴充功能之外，附件嵌入式管理單元延伸模組也必須支援 COM 介面 [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)。 這個介面會執行方法，指出是否有應儲存至安全性資料庫的服務特定資料，如果是，則會取出並儲存這項新資料。 [安全性設定] 嵌入式管理單元會定期呼叫此介面的方法，以便更新安全性資料庫。

[安全性設定] 嵌入式管理單元會執行介面 [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)，以提供從安全性資料庫取出服務特定資料的方法。 附件嵌入式管理單元擴充功能可以呼叫這個介面的方法，從安全性資料庫中取出資料。

下圖說明此架構。

![附件嵌入式管理單元擴充功能](images/model2.png)

當您建立附件嵌入式管理單元延伸模組時，您必須加以安裝，並使用 [安全性設定] 嵌入式管理單元來註冊它。若要這麼做，請將機碼新增到登錄中，如 [註冊附件嵌入式管理單元擴充功能](registering-an-attachment-snap-in-extension.md)中所述。 當安全性設定嵌入式管理單元開始時，它會檢查登錄並載入任何已註冊的嵌入式管理單元擴充功能。 延伸模組會在 [安全性設定] 嵌入式管理單元中，顯示為每個服務的 [安全性] 區域下的節點。

> [!Note]
> 附件嵌入式管理單元延伸模組只能擴充服務節點。 [服務] 節點是 MMC 嵌入式管理單元，其中包含的工具可用來管理系統上安裝的服務。 附件嵌入式管理單元延伸模組會將本身宣告為特定服務節點類型的次級，然後針對該服務節點類型的每個出現專案，MMC 主控台會自動新增相關的嵌入式管理單元擴充功能。
> 
> 每個附件嵌入式管理單元延伸模組都擁有一個 [領域] 窗格節點，以及 MMC 中的 [相關結果] 窗格。

 

 

 
