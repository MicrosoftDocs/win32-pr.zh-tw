---
description: Windows安裝程式與 Microsoft Windows XP 中的軟體限制原則整合。
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows安裝程式和軟體限制原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e96d1c422b38fd82110cac34953f24be39909eeb64fa2236d3a993925a55c6e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786558"
---
# <a name="windows-installer-and-software-restriction-policy"></a>Windows安裝程式和軟體限制原則

Windows安裝程式與 Microsoft Windows XP 中的軟體限制原則整合。 軟體限制原則可透過群組原則來設定。 軟體限制原則可讓系統管理員根據路徑、URL 區域、雜湊或發行者準則，限制系統管理員和非系統管理員執行檔案。 軟體限制原則有兩種層級：不受限制且不允許。 Windows Installer 只會安裝可在不受限制的層級執行的封裝。

您也必須允許修補程式或轉換在不受限制的層級上執行。 如果封裝、修補程式或轉換設定為在與不受限制的層級上執行，則 Windows Installer 會顯示錯誤訊息，並在應用程式事件記錄檔中記錄一個專案。 軟體限制原則會在應用程式第一次安裝時、套用新修補程式時，以及重新快取安裝套件時進行評估。

如果封裝、修補程式或轉換受到限制，Windows Installer 會顯示錯誤訊息，並將[事件記錄](event-logging.md)專案寫入應用程式事件記錄檔中。 軟體限制原則會在應用程式第一次安裝時、套用新修補程式時，以及重新快取安裝套件時進行評估。

如需軟體限制原則的詳細資訊，請參閱產品檔集並 [搜尋 TechNet 網站](https://www.microsoft.com/technet/sitemap.mspx)。

 

 



