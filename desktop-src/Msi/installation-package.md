---
description: 安裝套件包含安裝或卸載應用程式或產品，以及執行安裝程式使用者介面時，Windows Installer 所需的所有資訊。
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: 安裝套件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61daf878a7933353382a52acd9a7172e87b97b14cdf41a047279360342ca768b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633818"
---
# <a name="installation-package"></a>安裝套件

安裝套件包含安裝或卸載應用程式或產品，以及執行安裝程式使用者介面時，Windows Installer 所需的所有資訊。 每個安裝套件都包含一個 .msi 檔案，其中包含安裝資料庫、摘要資訊資料流程，以及安裝的各種元件的資料流程。 .msi 檔案也可以包含一或多個轉換、內部來源檔案，以及安裝所需的外部原始程式檔或封包檔。

應用程式開發人員必須撰寫安裝以使用安裝程式。 因為安裝程式會根據 [元件和功能](components-and-features.md)的概念來組織安裝，並且將安裝的所有相關資訊儲存在關係資料庫中，所以撰寫安裝套件的程式會廣泛地牽涉到下列步驟：

-   識別要呈現給使用者的功能。
-   將應用程式組織為元件。
-   填入安裝資料庫中的資訊。
-   驗證安裝套件。

下一節將討論安裝程式元件和功能。 如需詳細資訊，請參閱 [元件和功能](components-and-features.md)。 從使用者的觀點來看，應用程式的功能通常會決定功能的選擇。

建議開發人員使用標準程式來選擇元件。 如需詳細資訊，請參閱將 [應用程式組織成元件](organizing-applications-into-components.md)。

封裝作者可以使用協力廠商套件建立工具或資料表編輯器和 Windows Installer SDK 來填入安裝資料庫。 所有安裝套件都必須經過驗證，才能進行內部一致性。 如需詳細資訊，請參閱 [封裝驗證](package-validation.md)。

 

 



