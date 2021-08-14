---
title: Phone-Book 專案
description: 電話 book 專案包含建立 RAS 連線所需的資訊。 使用者或系統管理員可以使用 [撥號網路 (DUN) ] 對話方塊來建立、編輯及撥接電話簿專案。
ms.assetid: 971d7020-f9fd-42d1-97c3-79ad6eba6964
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea62595504229dd5dd920385a92214156a7d112774cb3fefbaff3f1b5edc7cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789818"
---
# <a name="phone-book-entries"></a>Phone-Book 專案

電話 book 專案包含建立 RAS 連線所需的資訊。 使用者或系統管理員可以使用 [ **撥號網路 (DUN)** ] 對話方塊來建立、編輯及撥接電話簿專案。

從 Windows NT Server 4.0 開始，系統支援 Windows 95 所述的函式，以及一些額外的功能，可供應用程式用來處理電話簿和電話簿專案。

[**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga)函式會顯示可讓使用者建立、編輯或複製電話簿專案的屬性工作表。 [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya)和 [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya)函數會呼叫 **RasEntryDlg** 函數。 您可以使用 [**RasRenameEntry**](/windows/desktop/api/Ras/nf-ras-rasrenameentrya) 函式來重新命名電話簿專案，或使用 [**RasDeleteEntry**](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya) 來刪除專案。 [**RasValidateEntryName**](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea)會判斷指定的字串是否具有要當做專案名稱使用的正確格式。

您可以使用 [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) 和 [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) 來取得和設定有關電話簿專案的其他資訊。 這些函數會使用 [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) 結構。

[**RasGetCredentials**](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa)和 [**RasSetCredentials**](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa)函式會取得並設定與指定的 RAS 電話簿專案相關聯的使用者認證。 這些函數會使用 [**RASCREDENTIALS**](/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)) 結構。

[**RasGetCountryInfo**](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa)函式會從國家/地區的 Windows 電話語音清單中，抓取國家/地區特定的撥號資訊。 **RasGetCountryInfo** 會使用 [**RASCTRYINFO**](/previous-versions/windows/desktop/legacy/aa376731(v=vs.85)) 結構。

* * Windows 95： * * 支援一組有限的函式，可處理電話簿專案。 您可以使用 [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) 和 [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) 功能來建立或編輯電話簿專案。 這些功能會顯示對話方塊，讓使用者可以在其中指定電話簿專案的相關資訊。 您可以使用 [**RasGetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa) 和 [**RasSetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa) 函式來設定或抓取電話簿專案的連接參數。 [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa)函式會捕獲 [**RASENTRYNAME**](/previous-versions/windows/desktop/legacy/aa377267(v=vs.85))結構的陣列，其中包含電話簿專案名稱。

 

 