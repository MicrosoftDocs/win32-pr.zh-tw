---
description: 安裝函數可以產生對話方塊來處理常見的安裝狀況，並收集使用者的資訊。
ms.assetid: 0bff17a6-590d-4410-9ed1-0a655d94caad
title: 關於磁片提示和錯誤處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6c171d1e479d5d16198ba6d632848ff152f4ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972835"
---
# <a name="about-disk-prompting-and-error-handling"></a>關於磁片提示和錯誤處理

雖然安裝函式不提供使用者介面，但有四個設定函數會產生對話方塊來處理常見的安裝狀況，並收集使用者的資訊。 這些是： [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)、 [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora)、 [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)和 [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)。

回呼常式可以呼叫這些函式來建立對話方塊，以協助處理其他安裝程式函數（例如 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) 和 [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)）所傳送的通知。

[**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)函式會提示使用者插入卸除式媒體、指定新的來源路徑，或取消安裝。 根據呼叫函式時所指定的旗標，應用程式可以為使用者提供其他選項。 這些包括略過目前的檔案，或流覽新的來源路徑。

這三個函式（ [**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora)、 [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)和 [**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)）會建立與使用者互動的對話方塊，以收集使用者的資訊，以瞭解如何在發生錯誤時繼續進行。

[**SetupCopyError**](/windows/desktop/api/Setupapi/nf-setupapi-setupcopyerrora)函式會產生對話方塊，該對話方塊會詢問使用者如何從複製錯誤中復原。 使用者可以為複製作業指定新的來源路徑，或取消安裝。 視呼叫 **SetupCopyError** 期間指定的旗標而定，使用者也可以流覽新的來源路徑、查看錯誤詳細資料，或略過目前的檔案。

此對話方塊會詢問使用者如何處理在檔案重新命名作業期間發生的錯誤，可以藉由呼叫 [**SetupRenameError**](/windows/desktop/api/Setupapi/nf-setupapi-setuprenameerrora)來產生。 在此對話方塊中，使用者有機會重試作業、略過目前的重新命名作業或中止。

[**SetupDeleteError**](/windows/desktop/api/Setupapi/nf-setupapi-setupdeleteerrora)函式會產生一個對話方塊，該對話方塊可收集使用者希望如何處理檔案刪除作業期間發生的錯誤的輸入。 使用者可以選擇重試作業、略過目前的刪除作業或中止。

預設佇列回呼常式 [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)會使用先前所述的四個函式來產生其使用者介面的元件，以及處理錯誤並提示新的媒體。

 

 



