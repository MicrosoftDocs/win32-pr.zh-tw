---
description: 當您想要顯示 COM + 元件的各種效能計量時，COM + 檢測服務可讓您建立自己的 COM + 事件管理和記錄程式。
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: COM + 檢測概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d86b5dbb7bb3f6db14d82220d88c58dbc0a8255
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972962"
---
# <a name="com-instrumentation-concepts"></a>COM + 檢測概念

當您想要顯示 COM + 元件的各種效能計量時，COM + 檢測服務可讓您建立自己的 COM + 事件管理和記錄程式。 您也可以使用 COM + 檢測來設定使用者定義的事件，以及在升級要接收 MTS 事件的 MTS 套件時，將 COM + 事件轉換成 Visual Studio Analyzer (VSA) 格式。

> [!Note]  
> 從 Windows Server 2003 版，只有系統管理員對系統事件的追蹤記錄具有讀取存取許可權。

 

藉由訂閱系統事件發行者所發佈的事件，用戶端可以執行 [Com + 檢測介面](com--instrumentation-interfaces.md) ，以接收各種 com + 效能度量的通知，例如特定 com + 物件、com + 應用程式和 com + 服務的相關資訊。 系統會使用 [Com + 事件服務](com--events.md)將計量發佈至用戶端，這是鬆散結合的事件 (LCE) 系統，將不同發行者的事件資訊儲存在 com + 目錄的事件存放區中。

> [!Note]  
> COM + 檢測不保證事件的傳遞。

 

每個度量都有一個指出計量產生時間的時間戳記，而不是其分派或接收時間。 用戶端可以將時間戳記相互關聯，並找出執行 COM + 應用程式的成本、在 COM + 應用程式內部執行的交易成本，或 COM + 應用程式內方法呼叫的成本。

您也可以使用 COM + 檢測服務來篩選您想要查看的特定效能度量資訊。 例如，當您訂閱 COM + 檢測介面或方法時，您可以在 [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) 結構中指定訂用帳戶的屬性，例如應用程式識別碼 (**guidApp** 成員) 或 (**DWPID** 成員) 的處理序識別碼。

當您指定應用程式識別碼時，您只會收到來自指定應用程式的計量。 當指定進程識別碼時，您會從指定的伺服器應用程式和該進程載入的程式庫應用程式接收度量。 使用者可以同時指定應用程式識別碼和處理常式識別碼，但應用程式識別碼必須是在進程中執行的伺服器應用程式的識別碼，並具有指定的處理序識別碼。 如果未指定，則使用者會接收來自所有伺服器和程式庫應用程式的計量。

COM + 檢測計量提供足夠的資訊，讓監視應用程式將它們與作業系統計量相互關聯，以進行效能分析、容量規劃，以及進行模型化和預測。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 檢測介面](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



