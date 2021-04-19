---
description: 憑證有相關聯的屬性，例如顯示名稱、描述和允許的用法，可供您查看和編輯。
ms.assetid: 23faaa03-af3e-4497-8607-4e34f8889368
title: 建立、查看及管理憑證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2136f8cd3ea3af1aab95b3c9c89ddd5787b4cefc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991816"
---
# <a name="creating-viewing-and-managing-certificates"></a>建立、查看及管理憑證

[*憑證*](../secgloss/c-gly.md) 是唯讀結構。 您可以查看憑證的內容，但無法修改。 憑證本身的資訊包括憑證的有效性日期、簽發者、主體和公開金鑰。 不過，憑證有相關聯的屬性，例如顯示名稱、描述和允許的用法，可供您查看和編輯。

本節將示範如何建立測試憑證、查看憑證，以及管理憑證和其他安全性物件。 您可以使用 MakeCert 建立的憑證和 [*軟體發行者憑證*](../secgloss/s-gly.md) (SPCs) ，完全用於測試用途。 測試 [*根憑證*](../secgloss/r-gly.md) 和測試根目錄 [*私密金鑰*](../secgloss/p-gly.md) 僅供測試之用。 獨立軟體廠商必須從 GTE、VeriSign、Inc. 或其他 [*憑證授權單位*](../secgloss/c-gly.md) 單位取得憑證 (CA) 來簽署將散發至公用的程式碼。

本節包含下列主題：

-   [使用 MakeCert](using-makecert.md)
-   [使用 Cert2spc.exe](using-cert2spc.md)
-   [使用 Certmgr.msc](using-certmgr.md)

 

 
