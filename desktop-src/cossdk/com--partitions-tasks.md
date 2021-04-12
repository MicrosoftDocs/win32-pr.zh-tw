---
description: COM + 分割工作
ms.assetid: ebcbfced-7d7a-46dc-a728-cdb920ccb874
title: COM + 分割工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055976effb5d6a93523bab9d570aec685872ab91
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187660"
---
# <a name="com-partitions-tasks"></a>COM + 分割工作

本節中的下列主題提供使用 COM + 磁碟分割的逐步指示。

**WINDOWS XP：** 無法使用建立、設定或委派 COM + 分割的能力。 全域分割區是唯一可用的 COM + 分割。

* * Windows 2000： * * COM + 分割服務無法在 Windows 2000 中使用。



| 主題                                                                                                         | 描述                                                                                    |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [建立和設定 COM + 分割](creating-and-configuring-com--partitions.md)<br/>           | 描述如何建立和設定 COM + 分割。<br/>                             |
| [管理本機磁碟分割](managing-local-partitions.md)<br/>                                         | 描述如何管理不在 Active Directory 內的 COM + 分割。<br/>       |
| [管理 Active Directory 內的磁碟分割](managing-partitions-within-active-directory.md)<br/>     | 描述如何管理 Active Directory 內指定的 COM + 分割。<br/> |
| [設定資料分割的系統管理許可權](setting-administrative-rights-for-a-partition.md)<br/> | 描述如何設定 COM + 磁碟分割的安全性許可權。<br/>                      |
| [將應用程式群組至資料分割](grouping-applications-into-partitions.md)<br/>                 | 描述如何將 COM + 應用程式設定為屬於 COM + 分割。 <br/>        |
| [收集分割區計量](collecting-partition-metrics.md)<br/>                                   | 說明如何收集 COM + 分割的相關資料。<br/>                                |
| [設定資料分割快取](configuring-the-partition-cache.md)<br/>                             | 描述如何設定 COM + 分割區快取。<br/>                                |



 

> [!Note]  
> 預設不會啟用 COM + 分割服務。 若要使用 COM + 分割服務，您必須透過 [元件服務] 系統管理工具啟用它，或將 [**LocalComputer**](localcomputer.md) 集合上的 PartitionsEnabled 屬性變更為 True。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 磁碟分割概念](com--partitions-concepts.md)
</dt> </dl>

 

 




