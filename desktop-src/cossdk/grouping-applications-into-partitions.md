---
description: 將應用程式群組至資料分割
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: 將應用程式群組至資料分割
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973594"
---
# <a name="grouping-applications-into-partitions"></a>將應用程式群組至資料分割

當您決定如何將應用程式群組至資料分割時，系統管理員必須留意特定的規則和限制，包括下列各項：

-   您可以將應用程式安裝到一或多個磁碟分割。
-   應用程式中只能存在一個指定元件的實例。

## <a name="public-and-private-components"></a>公用和私用元件

決定如何分組 COM + 應用程式時，會有其他限制。 這些限制與應用程式內的公用或私用元件相關。 應用程式元件通常可以是公用或私用。 不過，將應用程式群組成分割區時，系統管理員應留意公用和私用元件的一些限制。 下表列出這些限制。



| 如果應用程式為：              | 然後，磁碟分割中的元件可以是：                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| 伺服器應用程式<br/>    | 公用和私用。<br/>                                                                                           |
| 程式庫應用程式<br/>   | 僅限 Public。 否則，呼叫端應用程式可能會有相同的元件，而這會造成混淆。<br/> |
| 在全域資料分割中<br/> | 僅限 Public。 這可確保回溯相容性。<br/>                                                             |



 

## <a name="application-ids"></a>應用程式識別碼

每個安裝在電腦上的 COM + 應用程式都有唯一的應用程式識別碼。 不過，應用程式名稱只需要在單一磁碟分割中，而不是整部電腦上的唯一名稱。

下表顯示當應用程式匯入分割區或從分割區匯出時，應用程式識別碼會發生什麼事。



| 如果應用程式為：                                              | 然後是應用程式識別碼：                    |
|--------------------------------------------------------------------|---------------------------------------------|
| 匯入至全域分割區<br/>                        | 保持不變<br/>                 |
| 匯入至全域資料分割以外的磁碟分割<br/> | 已變更<br/>                       |
| 已匯出<br/>                                                | 包含在匯出的檔案中<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[收集分割區計量](collecting-partition-metrics.md)
</dt> <dt>

[設定資料分割快取](configuring-the-partition-cache.md)
</dt> <dt>

[管理本機磁碟分割](managing-local-partitions.md)
</dt> <dt>

[管理 Active Directory 內的磁碟分割](managing-partitions-within-active-directory.md)
</dt> <dt>

[設定資料分割的系統管理許可權](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




