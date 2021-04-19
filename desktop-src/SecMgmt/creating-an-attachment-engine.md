---
description: 附件引擎是處理服務特定設定和分析要求的 DLL。 換句話說，它會處理標準安全性設定工具集無法處理的處理。
ms.assetid: c04779f4-f1e9-40b0-9f00-0176afb1b839
title: 建立附件引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96b16e768956e61fe76406777da2bce9affbfa2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984995"
---
# <a name="creating-an-attachment-engine"></a>建立附件引擎

附件引擎是處理服務特定設定和分析要求的 DLL。 換句話說，它會處理標準安全性設定工具集無法處理的處理。

若要建立附件引擎，您必須執行下列三個功能：

-   [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)，它會計算服務設定和儲存在安全性資料庫中設定之間的差異。 這些差異會寫入安全性資料庫。 如需詳細資訊，請參閱 [執行 SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md)。
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)，會設定嵌入式管理單元使用者介面中指定的服務。 如需詳細資訊，請參閱 [執行 SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)。
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)，它會更新安全性資料庫中服務的基本設定和設定分析。 如需詳細資訊，請參閱 [執行 SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)。

安全性設定工具集會實行一組支援函式，讓您的應用程式可以呼叫這些函式，以查詢及設定安全性資料庫中的資訊。 如需詳細資訊，請參閱附加函式 [回呼函數](management-functions.md)。

建立附件引擎 DLL 之後，您必須使用「安全性設定」工具組來註冊它。 [註冊附件引擎](registering-an-attachment-engine.md)時，會說明此程式。

除了建立附件引擎之外，您還必須建立附件嵌入式管理單元延伸模組。 嵌入式管理單元擴充功能可提供使用者介面給服務特定的工作。 當使用者使用嵌入式管理單元擴充功能指定新的設定時，會將要求傳遞至適當的附件引擎。 然後，引擎會連線到服務並變更其設定。 如果您未執行嵌入式管理單元延伸模組，使用者將無法變更服務設定或分析。 如需有關如何建立附件嵌入式管理單元延伸模組的詳細資訊，請參閱 [建立附件嵌入式管理單元延伸](creating-an-attachment-snap-in-extension.md)。

 

 



