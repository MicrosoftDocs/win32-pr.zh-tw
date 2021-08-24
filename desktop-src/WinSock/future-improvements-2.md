---
description: 範例 Winsock 應用程式程式碼的未來改進。
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: 未來的改進
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384d5a4f4ee9a4d6cb4a0f258d63262930dc5a6636be8d0e7f709b0e4f04e152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132361"
---
# <a name="future-improvements"></a>未來的改進

您可以對這個應用程式進行幾項改進，例如：

-   應用程式可能會建立單一的持續性連接。 必須新增適當的錯誤處理。 這會降低與連線啟動和卸載相關的額外負荷。
-   您可以將伺服器上的回復碼優化以合併回復，減少從伺服器傳送的封包數目。
-   您可以對通訊協定進行改善。 例如，「更新位元遮罩」可用來表示要更新的資料格，以及只有傳送的資料格。
-   您可以使用不同的執行緒來重迭更新，如此一來，當 **ComputeNext** 函式正在執行時，就不會讓網路處於閒置狀態。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[改善應用程式緩慢](improving-a-slow-application-2.md)
</dt> <dt>

[基準版本：執行效能不佳的應用程式](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[修訂1：清除明顯的](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[修訂2：重新設計較少的連接](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[修訂3：壓縮的區區塊轉送](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



