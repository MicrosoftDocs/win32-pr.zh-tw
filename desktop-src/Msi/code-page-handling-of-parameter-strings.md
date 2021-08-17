---
description: 您可以使用資料庫資料表編輯器（例如 Windows Installer SDK 提供的 Orca）或從應用程式呼叫資料庫函式，將當地語系化資訊新增至安裝資料庫。
ms.assetid: cc1eb336-5dec-40cc-8aa5-564cd167855d
title: 參數字串的字碼頁處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37555b905c60cb8f4727ccb723435d28b24d41d3aca1fc7026e34b799e25414a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328336"
---
# <a name="code-page-handling-of-parameter-strings"></a>參數字串的字碼頁處理

您可以使用資料庫資料表編輯器（例如 Windows Installer SDK 提供的 Orca）或從應用程式呼叫[資料庫](database-functions.md)函式，將當地語系化資訊新增至安裝資料庫。 請小心只傳遞使用正在當地語系化的資料庫字碼頁的字串參數。 如果字串參數包含的字元無法由資料庫的字碼頁表示，則在呼叫 [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta)時，安裝程式會傳回錯誤。 如需數值字碼頁的清單，請參閱 [當地語系化錯誤和 ActionText 資料表](localizing-the-error-and-actiontext-tables.md)。

如需詳細資訊，請參閱 [判斷安裝資料庫的字碼頁](determining-an-installation-database-s-code-page.md)。

## <a name="adding-localization-information-to-a-database"></a>將當地語系化資訊新增至資料庫

當您將當地語系化資訊加入至資料庫時，作業系統必須支援資料庫的字碼頁。 它不一定要是系統目前的字碼頁。 [**IsValidCodePage**](/windows/desktop/api/winnls/nf-winnls-isvalidcodepage) 必須針對資料庫字碼頁傳回 **TRUE** 。 由於系統會將 ANSI 字串轉換為 Unicode，因此如果目前使用者字碼頁與資料庫字碼頁不同，就會發生錯誤。

呼叫 ANSI 版本的 Windows Installer API 會使用目前的系統字碼頁，將當地語系化的字串轉換成 Unicode。 認可資料庫時，會使用資料庫的字碼頁，將 Unicode 字串轉換為 ANSI。 如果目前的系統字碼頁與當地語系化字串的字碼頁不同，則結果可能會遺失資料和不正確的字串轉換。

下列程式說明如何儲存當地語系化資料。

**若要儲存當地語系化資料**

1.  將資料庫的字碼頁設定為當地語系化字串的字碼頁。
2.  使用 [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) 函式將 ANSI 字串轉換為 Unicode，並指定當地語系化資料的字碼頁。
3.  使用 unicode 字串來新增當地語系化資料，以呼叫 Windows Installer API 的 unicode 版本。
4.  使用 [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit)認可資料庫的當地語系化變更。

您也可以匯入和匯出 ASCII 文字保存檔案，以將當地語系化資訊新增至安裝資料庫。 如需詳細資訊，請參閱匯 [入和匯出資料表的字碼頁處理](code-page-handling-of-imported-and-exported-tables.md)。

 

 
