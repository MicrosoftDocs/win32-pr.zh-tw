---
title: RAS 通用對話方塊
description: Windows 提供一組功能，可顯示系統所提供的 RAS 對話方塊。
ms.assetid: 8231511a-7339-4fbb-8a39-f643ac575856
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3032da8b0647b48941d85fc4f085ddb8ced0125f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093192"
---
# <a name="ras-common-dialog-boxes"></a>RAS 通用對話方塊

Windows 提供一組功能，可顯示系統所提供的 RAS 對話方塊。 這些功能可讓應用程式輕鬆地顯示熟悉的使用者介面，讓使用者可以執行 RAS 工作。 例如，使用者可以建立和監視連接，或使用電話簿專案。 Windows 95 目前不支援這些功能。

[**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga)函式會顯示主要 **撥號網路 (DUN)** ] 對話方塊。 在此對話方塊中，使用者可以撥打、編輯或刪除選取的電話簿專案、建立新的電話簿專案，或指定使用者喜好設定。 **RasPhonebookDlg** 函數會使用 [**RASPBDLG**](/previous-versions/windows/desktop/legacy/aa377607(v=vs.85))結構來指定其他輸入和輸出參數。 例如，您可以設定結構的成員，以控制對話方塊在螢幕上的位置。 您可以使用 **RASPBDLG** 結構來指定 [**RasPBDlgFunc**](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca) 回呼函式，此函式會在對話方塊開啟時接收使用者活動的通知。 例如，當使用者撥打電話、編輯、建立或刪除電話簿專案時，RAS 會呼叫您的 **RasPBDlgFunc** 函式。

您可以使用 [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) 函式來啟動 RAS 連接作業，而不顯示主要 **撥號網路 (DUN)** 對話方塊。 使用 **RasDialDlg**，您可以指定要撥打的電話號碼或電話簿專案。 函數會顯示對話方塊的資料流程，指出連接作業的狀態。 **RasDialDlg** 函式會使用 [**RasDialDlg**](/previous-versions/windows/desktop/legacy/aa377023(v=vs.85))結構來指定其他輸入和輸出參數，例如對話方塊的位置以及要呼叫的電話通訊錄子索引。

若要顯示 **撥號網路 (DUN)** 屬性工作表，請呼叫 [**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85)) 函數。 此對話方塊可讓使用者監視現有連接的狀態。 **RasMonitorDlg** 函式會使用 [**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377591(v=vs.85))結構來指定其他輸入和輸出參數，例如對話方塊的位置以及要顯示在頂端的屬性工作表頁面。

您可以呼叫 [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) 函式，以顯示用來建立、編輯或複製電話簿專案的屬性工作表。 **RasEntryDlg** 函式會使用 [**RasEntryDlg**](/previous-versions/windows/desktop/legacy/aa377260(v=vs.85))結構來指定其他輸入和輸出參數，例如對話方塊的位置和電話簿操作的類型。

 

 