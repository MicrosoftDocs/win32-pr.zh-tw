---
description: 智慧卡介面是由一組智慧卡內可用的預先定義的服務、叫用服務所需的通訊協定，以及有關服務內容的任何假設所組成。
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: 智慧卡介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db3fb5369f36f76e8bf5909afad94959ff70541d9026762234d65ae181b0172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917767"
---
# <a name="smart-card-interfaces"></a>智慧卡介面

[*智慧卡*](../secgloss/s-gly.md)介面是由一組 *智慧卡* 內可用的預先定義的服務、叫用服務所需的通訊協定，以及有關服務內容的任何假設所組成。

就智慧卡而言，「介面」一詞類似于 COM 中使用它的方式，後者在概念上類似于 ISO 7816/5 應用程式識別碼，但具有不同的範圍。

每個智慧卡介面都是由 GUID 識別。 例如，可能定義了可提供 biorhythm 資訊給其持有者的介面。 如果指定的智慧卡支援這種服務，則可能會宣稱支援該介面 GUID。 使用介面 Guid，應用程式可能會搜尋一組特定的介面，找出支援該集合的任何卡片來完成工作。

雖然介面具有一個 GUID，但在不同的卡片上可能會有不同的執行方式。 例如，上述 biorhythm 介面可以有數個不同的實作為，但全部都是使用相同的 GUID 來參考。 不同的執行不會變更應用程式與智慧卡之間的互動;不過， [*服務提供者*](../secgloss/c-gly.md) 和智慧卡之間的互動可能會因介面的執行而有所不同。

智慧卡支援的一組介面是在智慧卡簡介中定義 (請參閱 [將智慧卡引入系統](introducing-smart-cards-to-the-system.md)) 。

 

 
