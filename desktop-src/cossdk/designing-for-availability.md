---
description: 可用性是指應用程式容忍伺服器資源失敗的能力。
ms.assetid: 5d9a8216-a568-4443-b94f-1b2f2827a4be
title: 可用性設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222583c9f53a1ccc88f2a4f984f445de02a2c976
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510548"
---
# <a name="designing-for-availability"></a>可用性設計

可用性是指應用程式容忍伺服器資源失敗的能力。 這表示用戶端會繼續透過失敗提供服務，而且在理想情況下，用戶端的失敗是透明的。 顯然，失敗可能來自硬體或軟體來源，因此您必須針對這兩種情況進行開發。

可用性可能會受到下列因素影響：

-   應用程式模型。 為了達到最高可用性，請確定使用 [Com + 交易](com--transactions.md) 服務來進行重要的應用程式邏輯。 此外，使用補償機制可有效確保資源在失敗之後仍處於狀況良好的狀態。
-   用戶端模型。 將「失敗時重試」邏輯整合至用戶端應用程式，並在資源或服務無法使用時，盡力在應用程式中進行正常的效能降低。 瞭解用戶端從應用程式所預期的內容，並建立可在發生失敗時提供替代方案的設計。
-   資料/狀態可用性。 若要一致地存取持續性資料，請使用 Windows 叢集來提供容錯移轉支援。
-   服務可用性。 您可以使用網路負載平衡，以平衡伺服器叢集內的連入 IP 要求。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設計部署](designing-for-deployment.md)
</dt> <dt>

[擴充性設計](designing-for-scalability.md)
</dt> <dt>

[安全性設計](designing-for-security.md)
</dt> </dl>

 

 



