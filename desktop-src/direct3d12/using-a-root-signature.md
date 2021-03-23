---
title: 使用根簽章
description: 根簽章是描述項資料表的任意排列集合的定義， (包括其配置) 、根常數和根描述項。
ms.assetid: 0131CDE4-02DB-440A-92B8-B0933C6414B0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3babe26dc06d4f85ce3d6fb771e18c78b54a3701
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104797"
---
# <a name="using-a-root-signature"></a>使用根簽章

根簽章是描述項資料表的任意排列集合的定義， (包括其配置) 、根常數和根描述項。 每個專案都有最大限制的成本，因此應用程式可以在根簽章將包含的每個專案類型的數目之間，權衡平衡。

-   [命令清單語義](#command-list-semantic)
-   [組合語義](#bundle-semantics)
-   [相關主題](#related-topics)

根簽章是可由 API 手動規格建立的物件。 PSO 中的所有著色器都必須與 PSO 所指定的根配置相容，否則個別的著色器必須包含彼此相符的內嵌根配置;否則，PSO 建立將會失敗。 根簽章的一個屬性，就是在撰寫時，著色器不需要知道它，雖然根簽章也可以直接在著色器中撰寫（如有需要）。 現有的著色器資產不需要任何變更，即可與根簽章相容。 引進著色器模型5.1，以提供一些額外的彈性 (從著色器) 內動態編制描述項的索引，並可依需要從現有的著色器資產開始逐漸採用。

## <a name="command-list-semantic"></a>命令清單語義

在命令清單的開頭，未定義根簽章。 圖形著色器的計算著色器會有不同的根簽章，每個都是在命令清單上個別指派。 命令清單或套件組合上設定的根簽章，也必須符合 Draw/分派目前設定的 PSO;否則，行為會是未定義的。 繪製/分派之前的暫時性根簽章不相符，例如在切換到相容的根簽章之前，先設定不相容的 PSO，然後再切換到相容的根簽章 (，只要這些都是由稱為「繪製/分派」) 。 設定 PSO 並不會變更根簽章。 應用程式必須呼叫專用的 API 來設定根簽章。

在命令清單上設定根簽章之後，配置會定義應用程式預期要提供的一組系結，以及哪些 Pso 可 (用於使用相同配置) 進行下一個繪製/分派呼叫的編譯。 例如，應用程式可能會定義根簽章，以提供下列專案。 每個專案都稱為「位置」。

-   \[0 \] CBV 描述項內嵌 (根描述元) 
-   \[1 \] 包含 2 SRVs、1 CBVs 和 1 UAV 的描述中繼資料表
-   \[2 \] 包含1個取樣器的描述項資料表
-   \[3 \] 根常數的4x32 位集合
-   \[4 \] 包含未指定 SRVs 數目的描述中繼資料表

在此情況下，在能夠發出繪製/分派之前，應用程式應該將適當的系結設定為每個位置 \[ 0 \] 和4，應用程式是以其目前的根簽章來定義。 例如，在位置 \[ 1 \] ，必須系結描述中繼資料表，這是描述項堆積中的連續區域，其中包含 (或將在執行時包含) 2 SRVs、1 CBVs 和 1 UAV。 同樣地，描述項資料表必須設定在插槽 \[ 2 \] 和 \[ 4 \] 。

應用程式一次可以變更根簽章系結的一部分， (其餘部分會維持不變) 。 例如，如果只需要在繪圖之間變更的唯一一件事是位置2的其中一個常數，則必須重新系結 \[ \] 應用程式。 如先前所述，驅動程式/硬體會在自動修改時的所有根簽章系結狀態。 如果命令清單上的根簽章已變更，則所有先前的根簽章系結都會變成過時，而且必須先設定所有新的預期系結，才能進行繪製/分派;否則，行為會是未定義的。 如果根簽章重複設定為目前設定的相同，則現有的根簽章系結不會變成過時。

## <a name="bundle-semantics"></a>組合語義

組合會將命令清單的根簽章系結 (系結至上述) 的命令清單範例中的不同位置。 如果套件組合需要變更部分繼承的根簽章系結，則必須先將根簽章設定為與呼叫命令清單相同， (繼承的系結不會變成過時) 。 如果套件組合將根簽章設定為與呼叫的命令清單不同，則其效果與變更上述命令清單上的根簽章相同：所有先前的根簽章系結都已過時，而且必須在繪製/分派之前設定新的預期系結;否則，行為會是未定義的。 如果組合不需要變更任何根簽章系結，就不需要設定根簽章。

下列程式碼顯示組合中的範例呼叫流程。

``` syntax
// Command List
...
pCmdList->SetGraphicsRootSignature(pRootSig); // new parameter space
MyEngine_SetTextures(); // bundle inherits descriptor table setting
MyEngine_SetAnimationFactor(fTime); // bundle inherits root constant
pCmdList->ExecuteBundle(...);
...
// Bundle
pBundle->SetGraphicsRootSignature(pRootSig); // same as caller, in order to inherits bindings
pBundle->SetPipelineState(pPS); 
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,0,drawIDOffset);
pBundle->Draw(...); // using inherited textures / animation factor
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,1,drawIDOffset);
pBundle->Draw(...);
...
```

當套件組合完成執行時，套件組合的任何根配置變更和/或系結變更都將會被繼承回呼叫的命令清單。

如需有關繼承的詳細資訊，請參閱在 [Direct3D 12 中管理圖形管線狀態](managing-graphics-pipeline-state-in-direct3d-12.md)的「**圖形管線狀態繼承**」一節。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[根簽章](root-signatures.md)
</dt> </dl>

 

 




