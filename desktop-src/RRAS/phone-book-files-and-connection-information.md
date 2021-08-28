---
title: Phone-Book 檔案和連接資訊
description: RasDial 呼叫必須指定遠端存取連線管理員建立連接所需的資訊。
ms.assetid: bc3885a4-3c1e-47bc-b622-072b33ac3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77a4bc7831673fb51a4c48177692674d6d2560ccec327dd3260dacb49e8ecfa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029118"
---
# <a name="phone-book-files-and-connection-information"></a>Phone-Book 檔案和連接資訊

[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)呼叫必須指定遠端存取連線管理員建立連接所需的資訊。 一般而言， **RasDial** 呼叫會藉由指定電話簿專案來提供連接資訊。 電話簿專案中的連接資訊包括電話號碼、bps 費率、 [使用者驗證資訊](user-authentication-information.md)，以及 [其他連線資訊](other-connection-information.md)。

RAS 用戶端會使用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式的參數來指定電話簿檔案，以及該檔案中的專案。 *LpszPhonebookPath* 參數可以指定電話簿檔案的名稱，也可以是 **Null** ，表示應使用預設的電話簿檔案。 *LpRasDialParams* 參數會指向 [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85))結構，以指定要使用的電話簿專案名稱。

若要顯示使用者可以從中選取連線的電話簿專案清單，RAS 用戶端可以呼叫 [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) 函式來列舉電話簿檔案中的專案。

若要在不使用電話簿專案的情況下建立連接， [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)呼叫可以為 [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85))結構的 **szEntryName** 成員指定空字串。 **RASDIALPARAMS. szPhoneNumber** 成員必須包含要呼叫的數位。 在此情況下，遠端存取連線管理員會使用第一個可用的數據機埠，以及所有其他設定的預設值。

 

 