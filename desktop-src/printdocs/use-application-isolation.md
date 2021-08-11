---
description: 應用程式可以在其應用程式資訊清單中宣告印表機驅動程式隔離，以隔離應用程式與印表機驅動程式，並改善應用程式的可靠性。
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: 如何：使用應用程式隔離
ms.date: 05/31/2018
ms.openlocfilehash: 818ba30e7b294c695b2f67bb9bccc485959db43818bb95aedaa67cafc26d3559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233828"
---
# <a name="how-to-use-application-isolation"></a>如何：使用應用程式隔離

應用程式可以在其應用程式資訊清單中宣告印表機驅動程式隔離，以隔離應用程式與印表機驅動程式，並改善應用程式的可靠性。 Windows 列印服務可讓印表機驅動程式在與執行列印多工緩衝處理器不同的進程中執行。 使用這項功能時，您的應用程式會在印表機驅動程式發生錯誤時，防止應用程式損毀。

印表機驅動程式隔離是在 Windows 7 和 Windows Server 2008 R2 中執行。

### <a name="prerequisites"></a>Prerequisites

-   使用 Windows 列印的 managed 程式碼或 Windows 存放區應用程式。

## <a name="instructions"></a>指示

### <a name="update-the-app-manifest"></a>更新應用程式資訊清單

啟用印表機驅動程式隔離需要您將 **printerDriverIsolation** 專案新增至應用程式的資訊清單。 方式如下：

1.  編輯應用程式資訊清單，並將值為 **true** 的 **printerDriverIsolation** 專案加入至 **應用程式** 專案的 **windowsSettings** 專案，如這個範例所示。
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  重建您的應用程式。

 

 



