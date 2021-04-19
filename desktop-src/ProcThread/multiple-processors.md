---
description: 具有多個處理器的電腦通常是針對兩種架構的其中一種來設計： (NUMA) 或對稱式多重處理 (SMP) 的非統一記憶體存取。
ms.assetid: 3c9186c8-a54d-4536-8237-bfff78cc7d11
title: 多個處理器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0093404a0df653a153823915f1ac72b5e41d50c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987532"
---
# <a name="multiple-processors"></a>多個處理器

具有多個處理器的電腦通常是針對兩種架構的其中一種來設計： (NUMA) 或對稱式多重處理 (SMP) 的非統一記憶體存取。

在 NUMA 電腦中，每個處理器都比其他處理器更接近某些部分的記憶體，使得記憶體的存取比其他部分更快。 在 NUMA 模型下，系統會嘗試在接近所用記憶體的處理器上排程執行緒。 如需 NUMA 的詳細資訊，請參閱 [Numa 支援](numa-support.md)。

在 SMP 電腦中，兩個或多個相同的處理器或核心會連接到單一共用的主儲存體。 在 SMP 模型下，任何執行緒都可以指派給任何處理器。 因此，在 SMP 電腦上排程執行緒，類似于在具有單處理器的電腦上排定執行緒。 不過，排程器具有處理器的集區，因此它可以排程要同時執行的執行緒。 排程仍取決於執行緒優先順序，但設定執行緒親和性和執行緒理想處理器可能會受到影響，如本主題中所述。

## <a name="thread-affinity"></a>執行緒親和性

*執行緒親和性* 會強制執行緒在特定的處理器子集上執行。 通常應該避免設定執行緒親和性，因為它可能會干擾排程器在跨處理器之間有效排程執行緒的能力。 這可能會降低平行處理所產生的效能提升。 執行緒親和性的適當使用會測試每個處理器。

系統會以位元遮罩（稱為處理器親和性遮罩）表示親和性。 親和性遮罩是系統中的處理器數目上限，並設定 bits 以識別處理器的子集。 一開始，系統會決定遮罩中的處理器子集。

您可以藉由呼叫 [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) 函式，為進程的所有線程取得目前的執行緒親和性。 您可以使用 [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) 函數，為進程的所有線程指定執行緒親和性。 若要為單一線程設定執行緒親和性，請使用 [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) 函數。 執行緒親和性必須是進程親和性的子集。

在具有64以上處理器的系統上，親和性遮罩一開始代表單一處理器群組中的處理器。 但是，執行緒親和性可以設定為不同群組中的處理器，這會改變進程的親和性遮罩。 如需詳細資訊，請參閱 [處理器群組](processor-groups.md)。

## <a name="thread-ideal-processor"></a>執行緒理想的處理器

當您指定 *執行緒理想的處理器* 時，排程器會盡可能在指定的處理器上執行執行緒。 您可以使用 [**SetThreadIdealProcessor**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessor) 函數來指定執行緒的慣用處理器。 這並不保證會選擇理想的處理器，但會對排程器提供實用的提示。 在具有64以上處理器的系統上，您可以使用 [**SetThreadIdealProcessorEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadidealprocessorex) 函式來指定特定處理器群組中的慣用處理器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[NUMA 支援](numa-support.md)
</dt> <dt>

[處理器群組](processor-groups.md)
</dt> </dl>

 

 
