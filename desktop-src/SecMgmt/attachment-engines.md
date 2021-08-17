---
description: 附件引擎是處理服務特定設定和分析要求的 DLL。
ms.assetid: bbca486a-9eec-4510-b5fd-435972182a69
title: 附件引擎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62e09996bfb58e0447ec8e25bb627af6a4c93751a86f9f73f3499cf7f8b0fdb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895051"
---
# <a name="attachment-engines"></a>附件引擎

附件引擎是處理服務特定設定和分析要求的 DLL。

使用者使用附件嵌入式管理單元擴充功能，進行服務專屬的設定和分析要求。 然後，此要求會透過「安全性設定」嵌入式管理單元傳遞至一般安全性設定引擎，然後將服務特定的處理傳遞至適當的附件引擎。 附件引擎接著會連接到服務並變更其設定。 換句話說，附件引擎會提供支援附件嵌入式管理單元擴充功能的後端處理。

附件引擎必須執行下列三個功能：

-   [**SceSvcAttachmentAnalyze**](scesvcattachmentanalyze.md)，它會計算服務設定和儲存在安全性資料庫中設定之間的差異。 這些差異會寫入安全性資料庫。
-   [**SceSvcAttachmentConfig**](scesvcattachmentconfig.md)，會設定嵌入式管理單元使用者介面中指定的服務。
-   [**SceSvcAttachmentUpdate**](scesvcattachmentupdate.md)，它會更新安全性資料庫中服務的基本設定和設定分析。

為了簡化上述函式的執行，安全性設定工具集會提供支援函式和結構，讓您的應用程式可用來查詢及設定安全性資料庫中的資訊。 如需詳細資訊，請參閱附加函式 [回呼函數](management-functions.md)。

當您建立附件引擎 DLL 時，您必須先安裝它，然後再向安全性設定引擎註冊。 若要註冊 DLL，您可以將特定的金鑰新增至登錄。 當安全性設定引擎啟動時，它會檢查登錄並載入所有已註冊的附件引擎 Dll。 然後，它會將服務特定的設定和分析要求傳遞至適當的附件引擎。 標準設定和分析要求（非服務特定的要求）是由安全性設定引擎處理。

 

 



