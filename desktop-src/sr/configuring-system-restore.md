---
title: 設定系統還原
description: 系統還原使用 Windows Management Instrumentation (WMI) ，以提供可編寫腳本的方式來設定及使用其功能。 它會在根預設命名空間中公開兩個類別： SystemRestore 和 SystemRestoreConfig \\ 。
ms.assetid: b510c5b7-71ec-47f9-b567-45fde8c79f57
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5627233d22025d8cead43f9fc31323ae13f85ff2ec7bde0ebfa07e171c1f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968047"
---
# <a name="configuring-system-restore"></a>設定系統還原

系統還原使用[Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) ，以提供可編寫腳本的方式來設定及使用其功能。 它會在根預設命名空間中公開兩個類別： [**SystemRestore**](systemrestore.md) 和 [**SystemRestoreConfig**](systemrestoreconfig.md) \\ 。

[**SystemRestore**](systemrestore.md)類別提供下列工作的方法：

-   停用和啟用監視
-   列出可用的還原點
-   在本機系統上起始還原
-   正在抓取上次系統還原的狀態

[**SystemRestoreConfig**](systemrestoreconfig.md)類別提供的屬性可用來控制排程的還原點建立頻率，以及每個磁片磁碟機上系統還原所耗用的磁碟空間量。

這兩個類別都可以使用標準 WMI 技術從遠端存取。 如需 WMI 的完整說明，請參閱[Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page)。

 

 