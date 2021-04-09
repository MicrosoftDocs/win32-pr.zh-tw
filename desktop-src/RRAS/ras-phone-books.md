---
title: RAS 電話書籍
description: 電話簿提供一種標準方式來收集和指定遠端存取連線管理員建立遠端連線所需的資訊。
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- 電話書籍，RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021547"
---
# <a name="ras-phone-books"></a>RAS 電話書籍

電話簿提供一種標準方式來收集和指定遠端存取連線管理員建立遠端連線所需的資訊。 電話簿將專案名稱與電話號碼、COM 埠和數據機設定等資訊相關聯。 每個電話簿專案都包含建立 RAS 連線所需的資訊。

電話簿儲存在電話簿檔案中，也就是包含專案名稱和相關資訊的文字檔。 RAS 會建立名為 RASPHONE 的電話簿檔案。.PBK. 使用者可以使用 [主要 **撥號網路 (DUN)** ] 對話方塊來建立個人的電話簿檔案。 RAS API 目前不提供建立電話簿檔案的支援。 某些 RAS 函式（例如 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式）有指定電話簿檔案的參數。 如果呼叫者未指定電話簿檔案，則該函式會使用預設的電話簿檔案，也就是使用者在 [**撥號網路 (DUN)** ] 對話方塊的 [**使用者喜好** 設定] 屬性工作表中選取的檔案。

Windows NT 4.0 提供的 [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) 和 [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) 函式會顯示內建的 RAS 使用者介面，讓使用者可以使用電話簿和電話簿專案。

**Windows 95：** 撥號網路會將電話簿專案儲存在登錄中，而不是在電話簿檔案中。 Windows 95 不支援顯示內建 RAS 對話方塊的個人電話簿檔案或功能。

 

 




