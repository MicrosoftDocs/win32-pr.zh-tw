---
description: 除了透過 Active Directory 消費者和電腦系統管理工具來管理 Active Directory 分割區之外，您還可以透過在 Active Directory 系統介面 (ADSI) 中使用一組 COM + 物件，以程式設計方式管理 COM + 分割。
ms.assetid: 915b4643-cbda-433a-a383-65a6b0fd0874
title: 管理 Active Directory 內的磁碟分割
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6635e49b7d2833a1e6e177c25f9f2fb05ff0dff4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510705"
---
# <a name="managing-partitions-within-active-directory"></a>管理 Active Directory 內的磁碟分割

除了透過 Active Directory 消費者和電腦系統管理工具來管理 Active Directory 分割區之外，您還可以透過在 Active Directory 系統介面 (ADSI) 中使用一組 COM + 物件，以程式設計方式管理 COM + 分割。

無論您選擇用來管理 COM + 分割的管理技術為何，系統管理員都必須遵循一般的步驟順序：

1.  在您的網域 Active Directory 內建立新的 COM + 分割。
2.  在 Active Directory 中建立 COM + 分割集，並將它們對應到新建立的 COM + 分割。
3.  使用適當的 COM + 物件，在本機電腦上設定 Active Directory 的資料分割。 當您在本機電腦上設定 Active Directory 分割區時，會自動在該分割區資料夾中建立 **Com + 應用程式** 資料夾。
4.  將您的 COM + 應用程式安裝在適當的 COM + 分割中。

您可以使用一組稱為 ADSI 的 Active Directory 介面，以程式設計的方式完成上述所有步驟。 可用來管理 ADSI 中可用之分割區的物件如下所示：

-   DS \_ USERPARTITIONSETLINK \_ 名稱
-   DS \_ PARTITIONLINK \_ 名稱
-   DS \_ OBJECTID \_ 名稱
-   DS \_ DEFAULTPARTITIONLINK \_ 名稱
-   DS \_ USERLINK \_ 名稱
-   DS \_ PARTITIONSET \_ 名稱
-   DS \_ 磁碟分割 \_ 名稱

如需使用 Active Directory 消費者和電腦和元件服務系統管理工具來建立和管理 COM + 分割的相關資訊，請參閱每個工具中的可用線上說明。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[收集分割區計量](collecting-partition-metrics.md)
</dt> <dt>

[設定資料分割快取](configuring-the-partition-cache.md)
</dt> <dt>

[將應用程式群組至資料分割](grouping-applications-into-partitions.md)
</dt> <dt>

[管理本機磁碟分割](managing-local-partitions.md)
</dt> <dt>

[設定資料分割的系統管理許可權](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 



