---
description: 若要安裝檔案、字型或登錄機碼，使其不會在卸載產品時移除，則必須將包含檔案、字型或登錄機碼的整個元件設為永久。
ms.assetid: 99db6485-2e85-47c3-a449-ef85b7efc865
title: 安裝永久元件、檔案、字型、登錄機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd9a6e77f2e6bb2d8d7a6f48d80f6855906e4d93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027542"
---
# <a name="installing-permanent-components-files-fonts-registry-keys"></a>安裝永久元件、檔案、字型、登錄機碼

若要安裝檔案、字型或登錄機碼，使其不會在卸載產品時移除，則必須將包含檔案、字型或登錄機碼的整個元件設為永久。 若要將元件設為永久，請在 [元件資料表](component-table.md)的 [屬性] 資料行中設定 **msidbComponentAttributesPermanent** 。

請注意，在移除機碼下的最後一個值或子機碼之後，安裝程式會移除登錄機碼。 若要防止在卸載時移除空白的登錄機碼，請在您需要保留的機碼下寫入虛設值，然後在登錄 [資料表](registry-table.md)的 [名稱] 資料行中輸入 +。

 

 



