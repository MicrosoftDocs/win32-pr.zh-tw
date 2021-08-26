---
title: RPC 模型
description: C 和 c + + 程式設計語言 (RPC) 的遠端程序呼叫，其設計目的是為了協助滿足開發人員在下一代軟體上 Windows 作業系統時的需求。
ms.assetid: ebab41a5-e841-4e0f-8acd-d0aab94f01c1
keywords:
- 遠端程序呼叫 RPC （說明） RPC 模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4c21a9fbbff24f4aafe9bad67186b65f4e3411b507d07953e29f806c6ff73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019708"
---
# <a name="the-rpc-model"></a>RPC 模型

C 和 c + + 程式設計語言 (RPC) 的遠端程序呼叫，其設計目的是為了協助滿足開發人員在下一代軟體上 Windows 作業系統時的需求。

RPC 是一種功能強大、穩固、有效率且安全的處理序間通訊 (IPC) 機制，可讓您在不同的進程中進行資料交換和叫用功能。 不同的進程可以位於相同電腦、區域網路或網際網路上。 本節說明 RPC 程式設計模型，以及可使用 RPC 來執行之分散式系統的模型。

RPC 完全支援64位 Windows。 有三種類型的進程：原生32位程式、原生64位處理常式，以及在64位系統上以32位程式模擬器執行的32位處理常式 (通常稱為 WOW64 進程) 。 如需 WOW64 的詳細資訊，請參閱執行 [32 位應用程式](/windows/desktop/WinProg64/running-32-bit-applications)。 使用 RPC，開發人員可以在不同類型的進程之間透明地通訊;RPC 會自動管理幕後的進程差異。

RPC 最初開發為憑證 RPC 的延伸模組。 除了部分的 advanced 功能之外，RPC 也可與其他廠商的憑證 RPC 實現互通。

本節也提供 RPC 元件及其操作的總覽。 下列主題將提供此資訊：

-   [程式設計模型](the-programming-model.md)
-   [分散式系統的模型](the-model-for-distributed-systems.md)
-   [RPC 的運作方式](how-rpc-works.md)
-   [Microsoft RPC 元件](microsoft-rpc-components.md)

 

 