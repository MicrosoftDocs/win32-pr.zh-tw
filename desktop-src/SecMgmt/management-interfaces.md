---
description: 列出附件引擎提供的介面。
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: 安全性管理介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979309"
---
# <a name="security-management-interfaces"></a>安全性管理介面

本章節包含下列介面群組的參考頁面：

-   [附件引擎介面](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a>附件引擎介面



| 介面                                                            | 描述                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | 從 [安全性設定] 嵌入式管理單元抓取指定安全性服務的設定和分析資料。[安全性設定] 嵌入式管理單元會公開這個介面，也就是會呼叫以查詢設定或分析資訊的附件嵌入式管理單元延伸模組。                                                 |
| [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | 從附件嵌入式管理單元抓取修改過的設定或分析資訊。 [安全性設定] 嵌入式管理單元會呼叫這個介面，以從附件嵌入式管理單元擴充功能抓取任何修改過的資訊。 然後，[安全性設定] 嵌入式管理單元會將此資料適當地儲存在安全性資料庫中。 |



 

如需嵌入式管理單元擴充功能必須執行之 COM 介面的詳細資訊，請參閱 [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) 檔。

 

 
