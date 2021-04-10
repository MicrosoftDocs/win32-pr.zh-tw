---
description: 開發人員可以防止在 Windows Installer 安裝期間，將機密資訊（例如密碼）輸入記錄檔中。
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: 防止機密資訊寫入記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026628"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a>防止機密資訊寫入記錄檔

使用 Windows Installer 時，您可以防止將機密資訊（例如密碼）輸入記錄檔中，並使其成為可見的。

-   安裝程式永遠不會將 [ServiceInstall 資料表](serviceinstall-table.md) 之 Password 資料行中的資訊寫入記錄檔中。
-   您可以藉由設定[Password Control 屬性](password-control-attribute.md)，防止安裝程式將與[編輯控制項](edit-control.md)相關聯的屬性寫入記錄檔。 即使 [Debug](debug.md) 原則設定為7的值，也會隱藏與具有 Password control 屬性之編輯控制項相關聯的屬性。
-   您可以將屬性包含在 [**MsiHiddenProperties**](msihiddenproperties.md) 屬性中，以防止安裝程式將私用屬性寫入記錄檔。
    > [!Note]  
    > 此方法可讓您在記錄檔中顯示的命令列上輸入機密資訊。 當 [調試](debug.md) 程式原則設定為7的值時，安裝程式會將命令列上輸入的資訊寫入記錄檔中。 如此一來，即使屬性包含在 [**MsiHiddenProperties**](msihiddenproperties.md) 屬性中，也會顯示在命令列上輸入的屬性。

     

-   您可以藉由在 CustomAction 資料表的類型欄位中加入 HideTarget 位旗標，來防止將 [CustomAction](customaction-table.md) 資料表的目標資料行中的資訊寫入記錄檔中。 此旗標的值為 8192 (0x2000) 。 如需詳細資訊，請參閱 [自訂動作隱藏目標選項](custom-action-hidden-target-option.md)。

 

 



