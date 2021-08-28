---
title: 撰寫回溯相容的用戶端和伺服器
description: 理論上，RPC 的版本控制配置有助於防止修改的伺服器和用戶端之間的 miscommunication，以及其部署的對應專案。
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- 遠端程序呼叫 RPC、最佳作法、回溯相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a55cc3731e75893fa1ab1390769131c3d1ad7263c15b08daebd9049f49f87c0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010336"
---
# <a name="writing-backward-compatible-clients-and-servers"></a>撰寫回溯相容的用戶端和伺服器

理論上，RPC 的版本控制配置有助於防止修改的伺服器和用戶端之間的 miscommunication，以及其部署的對應專案。 不過在實務上，開發人員經常必須在不修改版本的情況下，對現有介面進行變更，因為先前的用戶端和伺服器必須能夠與新的用戶端和伺服器通訊。 這是比 COM 更大的標準 RPC 問題;查詢是在 COM 中搜尋支援介面的自然方式，但在 RPC 例外狀況處理中，必須用於對等的涵蓋範圍。

本節將討論解決這些情況的最佳 RPC 程式設計作法。 本節分為下列主題：

-   [RPC 和 COM 的版本控制理論](the-versioning-theory-for-rpc-and-com.md)
-   [以回溯相容的方式變更介面](changing-interfaces-in-a-backward-compatible-manner.md)
-   [不相容變更的範例](examples-of-incompatible-changes.md)

 

 




