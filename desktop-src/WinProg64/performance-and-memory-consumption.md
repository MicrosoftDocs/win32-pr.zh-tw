---
title: WOW64 下的效能和記憶體耗用量
description: WOW64 下的效能和記憶體耗用量取決於下列因素。
ms.assetid: 77759840-7b1a-4956-a038-d6374b6ec354
keywords:
- WOW64 64 位 Windows 程式設計下的效能
- WOW64 64 位 Windows 程式設計下的記憶體耗用量
- WOW64 64 位 Windows 程式設計，效能
- WOW64 64 位 Windows 程式設計，記憶體耗用量
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8928e7d50c8396aa2b5b34081af3e4ee2719e044
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382581"
---
# <a name="performance-and-memory-consumption-under-wow64"></a>WOW64 下的效能和記憶體耗用量

WOW64 下的效能和記憶體耗用量取決於下列因素：

-   處理器硬體。 指令模擬會在晶片上執行。 在 x64 處理器上，x86 指令是由處理器以原生方式執行。 因此，在 x64 上的 WOW64 下執行速度類似于32位 Windows 下的速度。 在 Intel Itanium 處理器和任何 ARM64 處理器上，模擬有更多的軟體，因此效能也會受到影響。
-   API Thunk 的額外負荷。 相較于 NT 核心的系統呼叫，此額外負荷很小。 NT 核心函式的設計不常被呼叫。
-   虛擬記憶體大小。 在 Intel Itanium 處理器上，如果相同32位應用程式的兩個或多個實例同時執行，WOW64 會增加大量負荷。 這是因為 Intel Itanium 上的原生 8 KB 頁面，它會使 x86 架構上原生 4 KB 頁面的模擬變得更複雜 (更多頁面標記為可寫入;所有可寫入的頁面都是進程) 的私用。 這可能會對特定處理器上的終端機服務的擴充性造成負面影響。 這不是 x64 處理器的情況。
-   工作集。 WOW64 會增加應用程式的工作集大小。

WOW64 可讓32位應用程式利用64位核心。 因此，32位應用程式可以使用較大量的核心控制碼和視窗控制碼。 不過，32位應用程式可能無法在 WOW64 上建立多個執行緒，因為它們可以在 x86 系統上以原生方式執行，因為 WOW64 會配置額外的64位堆疊， (通常會為每個執行緒 512 KB) 。 此外，某些位址空間會保留給 WOW64 本身，以及它所使用的資料結構。 保留的數量取決於處理器;優於 x64 或 ARM64 處理器上的 Intel Itanium 有更多保留。

如果應用程式在映射標頭中設定了 [**圖像 \_ 檔案 \_ 大型 \_ 位址 \_ 感知**](/windows/desktop/api/dbghelp/ns-dbghelp-loaded_image) 旗標，則每個32位應用程式會在 WOW64 環境中收到 4 GB 的虛擬位址空間。 如果未設定 **圖像 \_ 檔案 \_ 大型 \_ 位址 \_ 感知** 旗標，每個32位應用程式會在 WOW64 環境中收到 2 GB 的虛擬位址空間。

 

 