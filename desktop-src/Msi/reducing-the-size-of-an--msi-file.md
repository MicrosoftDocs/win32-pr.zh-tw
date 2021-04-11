---
description: Windows Installer 套件的開發人員可能會注意到，在重複編輯和儲存之後，其 .msi 檔案的結果會大於預期。
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: 減少 .msi 檔案的大小
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944155"
---
# <a name="reducing-the-size-of-an-msi-file"></a>減少 .msi 檔案的大小

Windows Installer 套件的開發人員可能會注意到，在重複編輯和儲存之後，其 .msi 檔案的結果會大於預期。 Windows Installer .msi 檔案是包含儲存和資料流程的複合檔案，而且具有與 OLE 檔檔案相同的儲存限制。 如果您編輯和儲存相同的 .msi 檔案，它會在檔案中建立浪費的儲存空間。 這只會影響 .msi 檔案的作者，對 Windows Installer 使用者沒有影響。 開發人員可能會想要移除此浪費的儲存空間，然後再寄出其最終的 .msi 檔案。

若要移除浪費的儲存空間並減少 .msi 檔案的最終大小，您可以選擇下列選項。

-   將資料庫中的所有資料表匯出為 idt 檔案，然後將它們匯入至新的資料庫。 這樣可以產生最精簡的儲存空間。
-   使用軟體公用程式壓縮 OLE 檔檔案的儲存空間。

 

 



