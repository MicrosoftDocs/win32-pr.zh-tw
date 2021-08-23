---
title: 命令佇列和命令清單的設計原理
description: 啟用轉譯工作和多執行緒調整的目標，需要對 Direct3D 應用程式如何將轉譯工作提交至 GPU 的基本變更。
ms.assetid: C85C8C41-2306-4568-8FAE-F57EDA624298
keywords:
- 命令清單
- bundle
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08f996f3de54b63668d44122929feb4fdbef4380fb8b2f7bb1458f50fe274ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124216"
---
# <a name="design-philosophy-of-command-queues-and-command-lists"></a>命令佇列和命令清單的設計原理

啟用轉譯工作和多執行緒調整的目標，需要對 Direct3D 應用程式如何將轉譯工作提交至 GPU 的基本變更。 在 Direct3D 12 中，提交轉譯工作的程式與舊版不同，有三種重要的方式：

<dl> 1. 排除立即內容。 這會啟用多執行緒處理。  
2. 應用程式現在擁有轉譯呼叫如何分組為圖形處理單元， (GPU) 工作專案。 這可重複使用。  
3. 應用程式現在會明確地控制將工作提交至 GPU 的時間。 這會啟用專案1和2。  
</dl>

-   [移除立即內容](#removal-of-the-immediate-context)
-   [GPU 工作專案的群組](#grouping-of-gpu-work-items)
-   [GPU 工作提交](#gpu-work-submission)
-   [相關主題](#related-topics)

## <a name="removal-of-the-immediate-context"></a>移除立即內容

Microsoft Direct3D 11 到 Microsoft Direct3D 12 的最大變更，就是不再有與裝置相關聯的單一立即內容。 相反地，若要轉譯，應用程式會建立可在其中呼叫傳統轉譯 Api 的命令清單。 命令清單看起來類似于使用立即內容的 Direct3D 11 應用程式轉譯方法，因為它包含繪製基本專案或變更呈現狀態的呼叫。 如同立即內容，每個命令清單都不是無限制執行緒;不過，您可以同時記錄多個命令清單，以利用新式、多重核心的處理器。

命令清單通常會執行一次。 但是，如果應用程式在提交新的執行之前，確保先前的執行已完成，就可以多次執行命令清單。 如需有關命令清單同步處理的詳細資訊，請參閱 [執行和同步處理命令](executing-and-synchronizing-command-lists.md)清單。

## <a name="grouping-of-gpu-work-items"></a>GPU 工作專案的群組

除了命令清單之外，Direct3D 12 還會藉由新增第二個層級的命令清單（稱為組合），來利用目前所有硬體中的 *功能。* 為了協助區分這兩種類型，第一層命令清單可以稱為 *直接命令清單*。 套件組合的目的是要讓應用程式將少量的 API 命令群組在一起，以便於稍後從直接命令清單中重複執行。 建立配套時，驅動程式會盡可能地執行最多預先處理，以使稍後的執行更有效率。 然後，您可以從多個命令清單內執行套件組合，並在相同的命令清單中多次執行。

重複使用套件組合是使用單一 CPU 執行緒改善效率的大型驅動程式。 因為套組是預先處理的，且可以提交多次，所以在組合內可以執行哪些作業有某些限制。 如需詳細資訊，請參閱 [建立和錄製命令清單和](recording-command-lists-and-bundles.md)組合。

## <a name="gpu-work-submission"></a>GPU 工作提交

若要在 GPU 上執行工作，應用程式必須明確地將命令清單提交至與 Direct3D 裝置相關聯的命令佇列。 您可以多次提交 direct 命令清單來執行多次，但應用程式會負責確保在 GPU 上執行的直接命令清單已完成執行，然後再次提交。 套件組合沒有並行使用限制，而且可以在多個命令清單中執行多次，但無法直接將配套提交到命令佇列以供執行。

任何執行緒都可以隨時將命令清單提交至任何命令佇列，而執行時間會自動序列化命令佇列中的命令清單提交，同時保留提交順序。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 Direct3D 12 中提交工作](command-queues-and-command-lists.md)
</dt> </dl>

 

 




