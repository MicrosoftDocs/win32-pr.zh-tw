---
description: COM + 應用程式是元件服務的管理和安全性主要單位，由一組通常會執行相關功能的 COM 元件組成。
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: COM + 應用程式總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/05/2021
ms.locfileid: "106975581"
---
# <a name="com-application-overview"></a>COM + 應用程式總覽

COM + 應用程式是元件服務的管理和安全性主要單位，由一組通常會執行相關功能的 COM 元件組成。 這些元件會進一步由介面和方法所組成，如下圖所示。

![顯示方塊內介面和方法的圖表，以 COM + 應用程式內元件內部介面內的方法順序顯示。](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

您可以使用 [元件服務] 系統管理工具來建立新的 COM + 應用程式、將元件新增至應用程式，以及設定應用程式及其元件的屬性。

藉由將 COM 元件的邏輯群組建立為 COM + 應用程式，您可以利用 COM + 的下列優點：

-   COM 元件的部署範圍。
-   COM 元件的一般設定範圍，包括安全性界限和佇列。
-   元件開發人員未提供的元件屬性儲存 (例如，交易和同步處理) 。
-   元件動態連結程式庫 (Dll) 載入至進程 (DLLHost.exe 視需要) 。
-   裝載元件的受控伺服器進程。
-   建立和管理元件所使用的執行緒。
-   存取資源機的內容物件，可讓取得的資源自動與內容產生關聯。  (需有關 COM 元件和內容的詳細資訊，請參閱 [Com +](com--contexts.md)內容。 ) 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[開發 COM + 應用程式](developing-com--applications.md)
</dt> <dt>

[COM + 應用程式的元件](parts-of-a-com--application.md)
</dt> <dt>

[COM + 應用程式的類型](types-of-com--applications.md)
</dt> </dl>

 

 



