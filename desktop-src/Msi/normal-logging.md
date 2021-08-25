---
description: 安裝程式會在自己的錯誤記錄檔中記錄錯誤和事件。
ms.assetid: 244e9afa-2052-469e-aa57-424e03ce5673
title: 一般記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd1abeb4f110603bcc596cb7981ea65c7d9820d8054adc7533c4f85de2d8bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828538"
---
# <a name="normal-logging"></a>一般記錄

安裝程式會在自己的錯誤記錄檔中記錄錯誤和事件。 安裝程式所執行的記錄類型是由記錄模式的設定所決定。 記錄已啟用，而且可以使用下列方法來設定模式：

-   您可以使用 [命令列選項](command-line-options.md)的/l 選項，來指定從命令列啟動之安裝的記錄模式。 如果未使用/L 命令列選項指定記錄模式，則會使用預設的記錄模式。
-   您可以使用 [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) 函數或 [**EnableLog**](installer-enablelog.md) 方法，以程式設計方式指定安裝程式的記錄模式。 如果未使用 **MsiEnableLog** 函數或 **EnableLog** 方法來指定記錄模式，則會使用預設的記錄模式。
-   您可以藉由在封裝的 [屬性工作表](property-table.md)中設定 [**MsiLogging**](msilogging.md)屬性，來指定特定安裝封裝的預設記錄模式。 從 Windows Installer 4.0 開始，可以使用此屬性。
-   如果 [屬性工作表](property-table.md)中有 [**MsiLogging**](msilogging.md)屬性，則可以使用 [資料庫轉換](database-transforms.md)來變更值，藉以修改封裝的預設記錄模式。 使用 (.msp 檔的 [Patch 封裝](patch-packages.md) ，無法變更預設的記錄模式。 ) 
-   如果未設定 [**MsiLogging**](msilogging.md) 屬性，則可以使用 [記錄](logging.md) 原則來指定電腦上所有使用者的預設記錄模式。
-   如果已設定 [**MsiLogging**](msilogging.md) 屬性，則可以藉由設定 [DisableLoggingFromPackage](disableloggingfrompackage.md) 原則和 [記錄](logging.md) 原則來指定電腦上所有使用者的預設記錄模式。
-   如果/L 選項、 [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)、 [**EnableLog**](installer-enablelog.md)、 [**MsiLogging**](msilogging.md) 屬性或 [記錄](logging.md) 原則未指定記錄模式，則封裝的預設記錄模式會與將 **MsiLogging** 屬性設定為 ' iwearmo ' 時所取得的模式相同。

 

 



