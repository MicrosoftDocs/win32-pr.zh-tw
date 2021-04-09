---
description: 收集分割區計量
ms.assetid: 2dc35011-24fa-49df-9cf8-96db2de39efa
title: 收集分割區計量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6467dfb9c891e7ae57505c8ec3815bfa99e49d8a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110409"
---
# <a name="collecting-partition-metrics"></a>收集分割區計量

在某些情況下，組織可能會想要針對監視、容量規劃和資源計量的用途，收集 COM + 應用程式使用的相關資訊。

例如，應用程式服務提供者 (ASP) 可能會想要對客戶收取其資源使用量的費用。 若要這樣做，COM + 可讓您根據每個資料分割收集事件和計量資訊。

針對特定資料分割收集這項資訊的方式，就是針對每個 COM + 檢測介面，指定標準事件結構內的資料分割識別碼成員。 事件結構是 COM + 檢測介面的第一個值。 如需詳細資訊，請參閱 [Com + 檢測介面](com--instrumentation-interfaces.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定資料分割快取](configuring-the-partition-cache.md)
</dt> <dt>

[將應用程式群組至資料分割](grouping-applications-into-partitions.md)
</dt> <dt>

[管理本機磁碟分割](managing-local-partitions.md)
</dt> <dt>

[管理 Active Directory 內的磁碟分割](managing-partitions-within-active-directory.md)
</dt> <dt>

[設定資料分割的系統管理許可權](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



