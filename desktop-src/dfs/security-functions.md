---
title: 安全性函數
description: 網路管理安全性功能會取得並設定以 DFS 網域為基礎和獨立根目錄的安全描述項。
ms.assetid: 90860842-0f4d-49ad-b835-50305328a050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31611aa650bb55ecdc29af468e0ef784b670555b247d536d27b397de356f4ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677798"
---
# <a name="security-functions"></a>安全性函數

網路管理安全性功能會取得並設定以 DFS 網域為基礎和獨立根目錄的安全描述項。

DFS 安全性功能如下所示。

| 函式                                                               | 描述                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**NetDfsGetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetsecurity)                         | 取得指定之 DFS 根目錄之根物件的安全描述項。                                       |
| [**NetDfsSetSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetsecurity)                         | 尋找指定之 DFS 根目錄的根物件，並在其上設定提供的安全描述項。                  |
| [**NetDfsGetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity) | 取得指定之 DFS 獨立根目錄之容器物件的安全描述項。                      |
| [**NetDfsSetStdContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetstdcontainersecurity) | 尋找指定之 DFS 獨立根目錄的容器物件，並在其上設定提供的安全描述項。 |
| [**NetDfsGetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfsgetftcontainersecurity)   | 取得指定之 DFS 網域根目錄之容器物件的安全描述項。                           |
| [**NetDfsSetFtContainerSecurity**](/windows/desktop/api/lmdfs/nf-lmdfs-netdfssetftcontainersecurity)   | 尋找指定之 DFS 網域根目錄的容器物件，並在其上設定提供的安全描述項。      |
