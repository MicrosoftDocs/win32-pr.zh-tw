---
title: 使用 SIS 的優點
description: 使用 SIS 和 SIS 備份架構的優點如下所示。
ms.assetid: c72a14a1-92ae-4875-ae73-e277ed2b0c0d
keywords:
- 單一實例存放區 (SIS) 備份，優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cc27eeefe8aa9a61566ea0a1d1e8fd1eca6c718c594ebf232572f16c44e3f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118173962"
---
# <a name="advantages-of-using-sis"></a>使用 SIS 的優點

使用 SIS 和 SIS 備份架構的優點如下：

-   Sis 架構會自動維護 SIS 連結和支援檔案之間的連線，因為您的備份應用程式會呼叫 SIS 備份 API 函數。
-   SIS 重新分析點的內容對您的備份和還原應用程式而言是不透明的，以確保升級至 SIS 內部不需要變更 SIS API 或您的備份與還原呼叫 SIS API 函式的應用程式。 您只需要使用名為 Sisbkup.dll 的新版本 SIS DLL 重新編譯應用程式。
-   由於 SIS 是實作為檔案系統篩選器驅動程式，因此它會持續追蹤 SIS 連結與支援檔案之間的連線。 當備份和還原檔案時，SIS 備份可確保備份和還原每個備份檔案的實例，無論指向它的 SIS 連結數目為何。

 

 




