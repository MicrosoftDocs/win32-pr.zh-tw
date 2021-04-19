---
description: 使用物件共用改善效能
ms.assetid: 7a8a38d8-6549-4686-a298-f3b427b380e3
title: 使用物件共用改善效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 398b9140080d3a439293b5152b4da7251978e800
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973584"
---
# <a name="improving-performance-with-object-pooling"></a>使用物件共用改善效能

在特定情況下，物件共用可能會非常有效，並大幅提升效能。 重複使用物件以發揮最大效益的一般概念，是盡可能將最多的資源集區、從實際執行的工作中分解出來，然後在部署時將集區特性自訂為實際硬體。 也就是說，您應該依照下列步驟進行：

1.  撰寫物件，以便將針對任何用戶端所執行的昂貴初始化和資源取得納入考慮，以代表用戶端執行實際工作的先決條件。 寫入大量物件的函式，盡可能將這些資源集區化，以供物件保存，並在用戶端從集區取得物件時立即可用。
2.  系統管理員設定集區以達到可用硬體資源的最佳平衡，通常會在 exchange 中交易維護特定大小集區的記憶體，以加快用戶端存取及使用物件的速度。 在某個時間點，共用將會達到較低的報酬率，而且您可以獲得足夠的效能，同時限制特定元件可能的資源使用量。

## <a name="doing-actual-work-or-acquiring-resources"></a>執行實際工作或取得資源

如果您有一個元件，讓用戶端在執行用戶端的特定工作之前，很快就會使用部分的物件使用時間來取得資源或初始化，則撰寫您的元件以使用物件共用會是很大的好處。

您可以撰寫元件，讓在物件的函式中執行的工作，就像是所有用戶端都可以一致的耗時工作一樣-取得一或多個連線、執行腳本、從檔案或透過網路提取初始化資料等等。 這具有共用每個這類資源的效果。 您會將資源的組合和執行某些工作所需的一般狀態集中在一起。

在此情況下，當用戶端從集區取得物件時，這些資源會立即可用。 通常，它們會使用物件來執行一些小型工作單位，推送或提取資料，然後物件將呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) 或 [**IObjectCoNtext：： SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort) 並傳回。 使用像這樣的快速火災使用模式，就會產生絕佳的效能優勢。 您可以充分運用無狀態自動交易程式設計模型的簡易性，但可達成與傳統具狀態元件相同的效能。

但是，如果用戶端在每次呼叫時都使用物件一段很長的時間，共用就比較不合理。 您所獲得的速度優勢，會因為相對於初始化時間的使用時間增加而變得很低。 您會取得降低的傳回，這可能不會證明保留使用中物件集區所需的記憶體成本。

## <a name="sharing-cost-across-multiple-clients"></a>跨多個用戶端共用成本

分解初始化的變化是，您可以使用共用以統計方式分攤取得昂貴資源的成本。 如果您取得取得或初始化一次，然後重複使用物件，則會在其存留期內，于使用物件的所有用戶端之間共用該成本。 每個物件只會產生一次繁重的結構時間。

## <a name="preallocating-objects"></a>預先設定物件

如果您指定非零的最小集區大小，則會在應用程式啟動時建立並共用物件的最小數目，並準備好供任何呼叫應用程式的用戶端使用。

## <a name="governing-resource-use-with-pool-management"></a>使用集區管理管理資源使用

您可以使用最大集區大小，以精確地管理資源的使用方式。 例如，如果您已授權特定數目的資料庫連接，您可以控制隨時開啟的連接數目。

當您將用戶端使用模式、物件使用特性以及實體資源（例如記憶體和連接）納入考慮時，您可能會在進行效能調整時找到一些最佳的平衡點。 在某個時間點之後，共用物件將會產生較低的傳回。 您可以判斷所需的效能層級，並根據所需的資源進行平衡。

若要在設定物件共用時簡化效能調整，您可以監視應用程式中元件的物件統計資料。 如需詳細資訊，請參閱 [監視物件統計資料](monitoring-object-statistics.md)。

## <a name="improve-performance-of-jit-activated-components"></a>改善 JIT-Activated 元件的效能

物件共用與 [Com + 即時啟用](com--just-in-time-activation.md) 服務非常適合。 藉由共用正在 JIT 啟動的物件，您可以加快物件重新啟用的速度。 您可以透過 JIT 啟用將通道保持開啟狀態的優點，同時減輕重新開機的成本。 在此情況下，您可以使用共用來管理要配置給有作用中之物件的記憶體數量。

當 JIT 啟動的元件為交易式時，您很可能會將其共用。 物件共用已經過優化，可處理交易元件。 如需詳細資訊，請參閱共用 [交易對象](pooling-transactional-objects.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 物件的函式字串](com--object-constructor-strings.md)
</dt> <dt>

[控制物件存留期和狀態](controlling-object-lifetime-and-state.md)
</dt> <dt>

[物件共用的運作方式](how-object-pooling-works.md)
</dt> <dt>

[共用交易對象](pooling-transactional-objects.md)
</dt> <dt>

[共用物件的需求](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



