---
title: 虛擬目錄清理
description: BITS 會擴充 IIS 虛擬目錄以支援上傳。
ms.assetid: 8214904e-8a95-4c4b-a1c5-91e84031587f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83fb689bb3c797a311ec7c2ef8134eb51ffd6f1a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933407"
---
# <a name="virtual-directory-cleanup"></a>虛擬目錄清理

BITS 會擴充 IIS 虛擬目錄以支援上傳。 每個虛擬目錄都有會話超時屬性 (IIS [BITSSessionTimeout](bits-iis-extension-properties.md) 元檔案屬性) ，指定 BITS 用戶端必須在上傳檔案中進行的時間長度。 如果在該期間內未進行任何進度 (在進行) 的進度時，會重設計時器，BITS 會關閉會話。 預設會話超時時間為14天。

BITS 會針對您所建立和啟用的每個虛擬目錄，將工作專案新增至 [工作排程器](/windows/desktop/TaskSchd/task-scheduler-start-page) 。 工作專案會刪除與已關閉會話相關聯的資源。 依預設，會每隔12小時執行一次清除。 如果兩個虛擬目錄指向相同的實體目錄，由其中一個目錄所起始的清除程式會刪除與實體目錄中所有已關閉會話相關聯的資源。

使用 [BITS 延伸] 索引標籤或 [工作排程器](/windows/desktop/TaskSchd/task-scheduler-start-page) 介面，視需要變更應用程式的清除排程。 您也可以呼叫 [**IBITSExtensionSetup：： GetCleanupTask**](/windows/desktop/api/Bitscfg/nf-bitscfg-ibitsextensionsetup-getcleanuptask) 方法，以取得與虛擬目錄相關聯之清除工作的介面指標。

> [!Note]  
> 如果在啟用虛擬目錄之後停用工作排程器，虛擬目錄清除程式將無法運作。

 

 

 