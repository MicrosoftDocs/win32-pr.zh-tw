---
description: Windows Installer 會使用 Microsoft .NET Framework 將 common language runtime 元件安裝到全域組件快取中。
ms.assetid: 21d535d5-f05b-411a-8719-2662e6046fbd
title: 將元件安裝到全域組件快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719be313ad74374950092936bbd6124da779a0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191741"
---
# <a name="installation-of-assemblies-to-the-global-assembly-cache"></a>將元件安裝到全域組件快取

Windows Installer 會使用 Microsoft .NET Framework 將 common language runtime 元件安裝到全域組件快取中。 將元件安裝到全域組件快取時，安裝程式在安裝一般 Windows Installer 元件時，無法使用它所使用的相同目錄結構和檔案版本規則。 標準 Windows Installer 元件可能會依不同的產品安裝到多個目錄位置。 元件只能存在於組件快取中。 每個元件都會從元件快取中新增和移除，以做為不可分割的整體;因此，一律會同時安裝或移除組成元件的所有檔案。

標準 Windows Installer 元件和 common language runtime 元件的磁片成本，會以不同的方式計算。 一般 Windows Installer 元件的總磁片成本包括本地成本、來源成本和移除成本。 如需詳細資訊，請參閱檔案 [成本](file-costing.md)。 這個方法不能用來產生 common language runtime 元件的成本，因為這些元件可能會有 Windows Installer 以外的用戶端。 Common language runtime 元件的成本必須透過查詢 Microsoft .NET Framework common language runtime 來決定。

Windows Installer 會使用兩步驟的交易式程式來安裝包含 common language runtime 元件的產品。 這會啟用元件安裝和移除的復原。 如需詳細資訊，請參閱 [全域組件快取中的元件回復](rollback-of-assemblies-in-the-global-assembly-cache.md)。

請注意，安裝在每個使用者 [安裝內容](installation-context.md) 中之全域組件快取的元件，不受 Windows 檔案保護的保護。 在每部電腦安裝內容中，安裝安裝到全域組件快取的元件會受到 [Windows 資源保護](../wfp/windows-resource-protection-portal.md)的保護。

 

 
