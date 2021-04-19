---
description: 「字碼頁」（code page）是作業系統用來將符號 (字母、數位和標點符號) 字元對應到字元數位的內部資料表。
ms.assetid: e11193a2-2c72-43a9-8d35-fa524044e306
title: 檢查安裝資料庫字碼頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ea9513ec80413e00a9f3f4c1232a06704f83e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974646"
---
# <a name="checking-the-installation-database-code-page"></a>檢查安裝資料庫字碼頁

「 *字碼頁」（code page* ）是作業系統用來將符號 (字母、數位和標點符號) 字元對應到字元數位的內部資料表。 不同的字碼頁提供不同國家或地區所使用之字元集的支援。 字碼頁以 number 參考;例如，字碼頁932代表日文字元集，而字碼頁950則代表其中一個中文字元集。 請參閱 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md) ，以取得 ASCII 字碼頁的清單。

相同的 ASCII 字碼頁1252可用於英文和法文。 因此，您不需要重設資料庫 MNP2000.msi 的字碼頁 (英文) 就能將安裝變更為法文。

如需設定字碼頁的詳細資訊，請參閱 [字碼頁處理 (Windows Installer) ](code-page-handling-windows-installer-.md)。

[繼續](importing-localized-error-and-actiontext-tables.md)

 

 



