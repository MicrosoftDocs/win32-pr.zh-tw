---
title: 系統感應器集區
description: 可共用的生物識別單位集合，可讓您存取 Windows 驗證服務。 此集區是由 Winlogon、UAC 和任何其他用戶端所使用，這些用戶端會將 SID 與特定生物特徵辨識範本產生關聯。
ms.assetid: 308306a9-e12c-4ff6-92c3-a36667a5e548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ae9487b91b57b2e9568817c92e44b4b7197f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965587"
---
# <a name="system-sensor-pool"></a>系統感應器集區

系統感應器集區是可共用的生物特徵辨識單位集合，可提供 Windows 驗證服務的存取權。 此集區是由 Winlogon、UAC 和任何其他用戶端所使用，這些用戶端會將 SID 與特定生物特徵辨識範本產生關聯。 系統集區中的生物識別單位：

-   可以由多個用戶端應用程式共用。
-   將完成生物特徵辨識作業所產生的事件通知傳送給具有目前視窗焦點的應用程式。
-   使用帳戶 Sid 來代表範本身分識別。 所有與單一使用者帳戶相關聯的範本都會以指派給該帳戶的 SID 標記。
-   取決於 Windows 生物特徵辨識服務所提供的可信任範本儲存體。

您可以在系統集區中包含生物識別單位（如果可能的話）：

-   設定為在基本模式下運作，只做為生物特徵辨識捕獲裝置。
-   設定為以 advanced 模式操作，但沒有上架的範本儲存體。 也就是說，它必須使用 Microsoft 提供的儲存體介面卡和範本存放區。
-   設定為以 advanced 模式運作、包含上架範本儲存體，而且可以產生必要的雜湊。

當新的感應器裝置插入電源時，Windows 生物特徵辨識服務會為其建立生物特徵辨識單位，並嘗試設定該單位以供系統感應器集區使用。 如果設定失敗，則會將生物特徵辨識單位放在未指派的感應器集區中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[私人感應器集區](private-sensor-pool.md)
</dt> <dt>

[感應器集區](sensor-pools.md)
</dt> <dt>

[系統集區行為](system-pool-behavior.md)
</dt> </dl>

 

 




