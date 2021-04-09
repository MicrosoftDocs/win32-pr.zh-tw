---
description: 通訊/datamodem/撥出
ms.assetid: b1cc19d2-4a9f-4d3f-a868-d5928654ad75
title: 通訊/datamodem/撥出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 553e998acdfe77509d62050b825dae6ea88d3b3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944731"
---
# <a name="commdatamodemdialout"></a>通訊/datamodem/撥出

**通訊/datamodem/撥** 出裝置類別包含僅用於撥出電話的 datamodem 裝置。 此類別會取代 Windows 2000 和更新版本作業系統上的 [**comm/datamodem**](comm-datamodem.md) 類別。

在 Windows 2000 之前，Unimodem TSP 只支援 [**comm/datamodem**](comm-datamodem.md) 裝置類別。 當應用程式撥出來電時發生非預期的行為。當應用程式撥出來電時，可能會變更由服務等候來電的設定。 使用 Windows 2000 和更新版本作業系統的應用程式應在對 [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)或 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)的呼叫中，指定 [**通訊/datamodem/撥**](comm-datamodem-dialin.md)入或 **comm/datamodem/撥** 出。 這可讓 Unimodem 維持與撥出設定無關的撥入設定。

當 Unimodem 在 Windows 2000 和更新版本上使用 **comm/datamodem/撥** 出時，其他 tsp 也可以在任何平臺上使用。 必須在所有平臺上執行的應用程式應該先在需要裝置類別的 API 呼叫中使用 **通訊/datamodem/撥** 出，而且如果 Api 傳回 **LINEERR \_ INVALCALLSTATE**，則只使用 [**通訊/datamodem**](comm-datamodem.md) 。

Unimodem 服務提供者會將 [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)和 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig)呼叫中的 [**comm/datamodem**](comm-datamodem.md)裝置類別轉譯為 [**comm/datamodem/撥**](comm-datamodem-dialin.md)入或 **comm/datamodem/撥** 出，如下所示：

-   Windows 2000 和更新版本：
    -   如果在呼叫 [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)的 *lpszDeviceClass* 參數中指定了 **Null** ，則會假設有 [**通訊/datamodem/撥**](comm-datamodem-dialin.md)入。 如果在 **lineConfigDialog** 的呼叫中指定了 [**comm/datamodem**](comm-datamodem.md)或 [**tapi/line**](tapi-line.md) ，則 Unimodem 會將其轉譯為 **comm/datamodem/撥** 出。
    -   在對 [**lineSetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linesetdevconfig) 或 [**lineGetDevConfig**](/windows/desktop/api/Tapi/nf-tapi-linegetdevconfig)的呼叫中，會將 [**comm/datamodem**](comm-datamodem.md) 處理為 **comm/datamodem/撥** 出。 **Null** 表示不正確裝置類別。
-   Windows 2000 之前：
    -   如果在 [**lineConfigDialog**](/windows/desktop/api/Tapi/nf-tapi-lineconfigdialog)中指定了 **Null** 或 [**tapi/行**](tapi-line.md)，則會假設是 [**comm/datamodem**](comm-datamodem.md)。

**Comm/datamodem/撥** 出類別會使用 [**comm/datamodem**](comm-datamodem.md)裝置類別中所述的結構和設定。

 

 



