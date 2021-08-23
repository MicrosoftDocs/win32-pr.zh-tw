---
description: 在還原作業之後，服務可能需要先停止再重新開機。
ms.assetid: 111d1281-ad83-49bc-868c-1106a0e25a2a
title: 停止服務以供要求者還原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa8051fc20c5ba1bd930da8c7da5c40829c07772572c2b1fb795250d34b8c92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511618"
---
# <a name="stopping-services-for-restore-by-requesters"></a>停止服務以供要求者還原

在還原作業之後，服務可能需要先停止再重新開機。

一般而言，處理 [*PreRestore*](vssgloss-p.md) 事件 (時，寫入器會將服務停止並啟動以支援還原，而 [**CVssWriter：： OnPreRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onprerestore)) 和 [*PostRestore*](vssgloss-p.md) 事件 (與 [**CVssWriter：： OnPostRestore**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-onpostrestore)) 。

不過，在某些情況下，要求者必須明確地停止執行中的服務。 寫入器會藉由將 \_ \_ \_ vss RESTOREMETHOD 列舉列舉的 vss RME 停止還原 \_ 啟動或 vss \_ RME \_ 還原 \_ \_ 開始值設定為 [**\_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) [**IVssCreateWriterMetadata：： SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) 方法呼叫的 restore method 引數，並指定要停止的服務名稱，來指出是否為這種情況。

當使用 [**IVssExamineWriterMetadata：： GetRestoreMethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod) 方法時，要求者會取得還原方法的相關資訊，以及使用寫入器中繼資料時要停止的服務名稱。

寫入器指定要停止的服務名稱時，請務必使用該服務的正確公開已知名稱。 不明確或不正確的名稱可能會導致要求者停止錯誤的服務，或無法判斷要停止的服務。

完成還原作業之後，要求者必須重新開機服務。

您必須謹慎設計和執行支援要求者必須停止並重新啟動的寫入器。 具體而言，這類寫入器實際上不應該是服務的一部分，也就是，寫入器本身應該不需要停止，然後在還原作業期間重新開機。

在重新開機時，其進程已停止的寫入器會有不同的寫入器實例。 寫入器的新實例將不會收到適用于寫入器原始實例的 VSS 事件。 具體而言，如果在處理 PreRestore 事件之後停止寫入器實例的進程，新的實例將不會收到 PostRestore 事件。 此外，VSS 將會產生錯誤，指出在還原作業中遺失參與的寫入器，而 [**>ivssbackupcomponents：:P ostrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-postrestore) 可能會傳回失敗。

 

 



