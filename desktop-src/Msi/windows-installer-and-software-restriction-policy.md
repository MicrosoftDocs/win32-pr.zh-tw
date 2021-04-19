---
description: Windows Installer 已與 Microsoft Windows XP 中的軟體限制原則整合。
ms.assetid: b1e58336-8908-45ee-86f0-81b2314fa77a
title: Windows Installer 和軟體限制原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b080a1ed9a1396f4ac212e73d1fda6e2719bf40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975762"
---
# <a name="windows-installer-and-software-restriction-policy"></a>Windows Installer 和軟體限制原則

Windows Installer 已與 Microsoft Windows XP 中的軟體限制原則整合。 軟體限制原則可透過群組原則來設定。 軟體限制原則可讓系統管理員根據路徑、URL 區域、雜湊或發行者準則，限制系統管理員和非系統管理員執行檔案。 軟體限制原則有兩種層級：不受限制且不允許。 Windows Installer 只會安裝可在不受限制的層級執行的封裝。

您也必須允許修補程式或轉換在不受限制的層級上執行。 如果封裝、修補程式或轉換設定為在與不受限制的層級上執行，則 Windows Installer 會顯示錯誤訊息，並在應用程式事件記錄檔中記錄一個專案。 軟體限制原則會在應用程式第一次安裝時、套用新修補程式時，以及重新快取安裝套件時進行評估。

如果封裝、修補程式或轉換受到限制，Windows Installer 會顯示錯誤訊息，並將 [事件記錄](event-logging.md) 專案寫入應用程式事件記錄檔中。 軟體限制原則會在應用程式第一次安裝時、套用新修補程式時，以及重新快取安裝套件時進行評估。

如需軟體限制原則的詳細資訊，請參閱產品檔集並 [搜尋 TechNet 網站](https://www.microsoft.com/technet/sitemap.mspx)。

 

 



