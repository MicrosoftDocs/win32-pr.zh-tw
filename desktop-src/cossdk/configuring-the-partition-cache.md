---
description: COM + 分割功能包含分割區快取。 此快取會儲存使用者對分割區對應，並設計為避免重複 Active Directory 存取。
ms.assetid: 8c3a269d-1933-4df6-aefb-f1f5587f1f42
title: 設定資料分割快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1389cc2685861e06d1b5c86baf2ad7b5fa9bd038
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973182"
---
# <a name="configuring-the-partition-cache"></a>設定資料分割快取

COM + 分割功能包含分割區快取。 此快取會儲存使用者對分割區對應，並設計為避免重複 Active Directory 存取。

## <a name="changing-cache-size"></a>變更快取大小

分割區快取是由三個數據表所組成，其大小可加以修改以增強效能。 這些資料表包含快取中的 SID 專案數目、快取中的 OU 專案數目，以及快取中的分割區專案數目。

若要變更這些資料表大小，系統管理員可以修改登錄機碼的值。 登錄機碼和其值如下：

**HKLM \\ SOFTWARE \\ Microsoft \\ COM3 \\ PartitionCache**



| 金鑰值                         | Description                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NumSidEntries**<br/>       | 包含快取 \_ (預設值 = 512) 中 SID 專案數目的 REG DWORD 值。 此值應該設定為大於電腦將在快取失效時間範圍內服務的唯一識別數目的值。<br/>                                                                                                                                                  |
| **NumNameEntries**<br/>      | 包含快取 \_ (預設值 = 64) 中 OU 名稱專案數目的 REG DWORD 值。 此值應該設定為大於電腦將在快取失效時間範圍內服務的唯一 OU 名稱數目的值。<br/>                                                                                                                                                 |
| **NumPartitionEntries**<br/> | 包含快取 \_ (預設值 = 1024) 中分割區專案數目的 REG DWORD 值。<br/> 在 [快取失效時間] 視窗中，DWORD 值應該設定為大於機器所要服務之唯一分割區數目的數位。 這是因為元件的內容可以包含不在該電腦上之分割區的分割區識別碼。 <br/> |
| **EntryExpiration**<br/>     | 包含 \_ 滴答計數的 REG DWORD 值 (每個刻度 = ~ 7 分鐘) 直到快取專案變成無效為止 (預設值 = 4 (~ 28 分鐘) ) 。<br/>                                                                                                                                                                                                                                                          |



 

## <a name="flushing-the-cache"></a>清除快取

由於 COM + 會快取使用者的預設資料分割，因此您可能會想要在 Active Directory 中變更使用者的預設資料分割之後，呼叫這個方法。 系統管理員可以藉由呼叫 [**FlushPartitionCache**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog2-flushpartitioncache) 方法，以程式設計方式來完成這項作業。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[收集分割區計量](collecting-partition-metrics.md)
</dt> <dt>

[將應用程式群組至資料分割](grouping-applications-into-partitions.md)
</dt> <dt>

[管理本機磁碟分割](managing-local-partitions.md)
</dt> <dt>

[管理 Active Directory 內的磁碟分割](managing-partitions-within-active-directory.md)
</dt> <dt>

[設定資料分割的系統管理許可權](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




