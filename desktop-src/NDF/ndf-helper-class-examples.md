---
title: NDF Helper 類別延伸模組範例
description: 這些範例只適用于開發人員認為需要擴充宣告為可延伸的 Microsoft NDF Helper 類別的功能時。
ms.assetid: 048e42f5-66d8-41c6-9e97-8da68c9ad151
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3ecf34bb8e90aad8c28f582860d44e81706e77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670915"
---
# <a name="ndf-helper-class-extension-examples"></a><span data-ttu-id="c1252-103">NDF Helper 類別延伸模組範例</span><span class="sxs-lookup"><span data-stu-id="c1252-103">NDF Helper Class Extension Examples</span></span>

<span data-ttu-id="c1252-104">這些範例只適用于開發人員認為需要擴充宣告為可延伸的 Microsoft NDF Helper 類別的功能時。</span><span class="sxs-lookup"><span data-stu-id="c1252-104">These examples apply only when developers believe it is necessary to extend the functionality of a Microsoft NDF Helper Class that is declared to be extensible.</span></span> <span data-ttu-id="c1252-105">這通常不是必要的，但在某些情況下，唯一的診斷機會因為元件的特定硬體或軟體需求而出現本身。</span><span class="sxs-lookup"><span data-stu-id="c1252-105">This is generally not necessary, but in some cases, unique diagnostic opportunities present themselves because of the specific hardware or software requirements of the component.</span></span>

<span data-ttu-id="c1252-106">接下來的兩個範例都是相關的，而且應該先瞭解第一個範例，再分析第二個範例。</span><span class="sxs-lookup"><span data-stu-id="c1252-106">The two examples that follow are related and the first should be understood before analyzing the second.</span></span> <span data-ttu-id="c1252-107">第一個使用名為 SimpleHelperFileClass 的類別，提供 NDF 協助程式 [類別延伸](ndf-helper-class-example.md) 的執行。</span><span class="sxs-lookup"><span data-stu-id="c1252-107">The first provides an implementation of an [NDF Helper Class Extension](ndf-helper-class-example.md) using a class called SimpleHelperFileClass.</span></span>

<span data-ttu-id="c1252-108">第二種是具有交付功能的 NDF 協助程式 [類別延伸](ndf-helper-class-example-with-handoff.md)，提供的延伸模組範例不會執行特定的診斷工作，而只會在第一個範例中產生 SimpleHelperFileClass 的低健康情況假設。</span><span class="sxs-lookup"><span data-stu-id="c1252-108">The second, [NDF Helper Class Extension with Handoff](ndf-helper-class-example-with-handoff.md), provides an example of an extension that does not perform specific diagnostic tasks but only generates a low health hypothesis for the SimpleHelperFileClass in the first example.</span></span>

 

 




