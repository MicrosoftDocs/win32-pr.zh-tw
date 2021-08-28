---
description: 復原是指應用程式從遺失重要元件，或已被不相容版本取代的情況下，能夠正常復原的能力。
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: 復原
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73565a129c25b19e0fb362e5363626f1acfee0387b2d4e4826f79222e7425b96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810778"
---
# <a name="resiliency"></a>復原

復原是指應用程式從遺失重要元件，或已被不相容版本取代的情況下，能夠正常復原的能力。 藉由撰寫安裝套件並使用[安裝程式功能](installer-functions.md)，開發人員可以使用 Windows Installer 來產生可從這類情況復原的復原應用程式。

-   使用安裝程式的來源清單來提高依賴網路資源的應用程式的復原能力。 如需詳細資訊，請參閱 [來源復原](source-resiliency.md)。
-   使用安裝程式的 API 來檢查是否已安裝重要功能、元件、檔案或檔案版本。
-   使用安裝程式的 API，在執行時間檢查元件的路徑。 這可減少應用程式對靜態檔案路徑的相依性，這通常會在電腦之間有所不同。
-   您可以使用安裝程式來重新安裝損毀的快捷方式、登錄專案和其他元件，而不需要重新執行安裝程式。
-   藉由讓安裝程式的復原功能保持啟用，來提高產品安裝的復原能力。 如需詳細資訊，請參閱 [復原安裝](rollback-installation.md)。

 

 



