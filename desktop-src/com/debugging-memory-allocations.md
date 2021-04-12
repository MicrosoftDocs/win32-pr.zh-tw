---
title: 調試記憶體配置
description: 調試記憶體配置
ms.assetid: 522adb1f-0e3e-4dfb-8836-f539a79a3d9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beb6a7dbe313cfe571fa6b4d244df35407fa331e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316525"
---
# <a name="debugging-memory-allocations"></a>調試記憶體配置

COM 提供 [**IMallocSpy**](/windows/desktop/api/ObjIdl/nn-objidl-imallocspy) 介面讓開發人員用來偵測其記憶體配置。 針對 [**IMalloc**](/windows/win32/api/objidlbase/nn-objidlbase-imalloc)中的每個方法， **IMallocSpy** 中有兩種方法： "pre" 方法和 "post" 方法。 當開發人員在執行並將它發佈至系統之後，系統就會在對應的 **IMalloc** 方法之前呼叫 **IMallocSpy** 的 "pre" 方法，有效地允許偵錯工具代碼在配置作業上「spy」，並呼叫「post」方法來釋放 spy。

例如，當 COM 偵測到下一個呼叫呼叫 [**IMalloc：：**](/windows/desktop/api/ObjIdl/nf-objidl-imalloc-alloc)配置時，它會呼叫 [**IMallocSpy：:P realloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-prealloc)，在配置執行期間執行開發人員想 **要的任何** 偵錯工具， **然後在配置呼叫傳回** 時，呼叫 [**IMallocSpy：:P ostalloc**](/windows/desktop/api/ObjIdl/nf-objidl-imallocspy-postalloc) 來釋放 spy 並將控制項傳回給程式碼。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管理記憶體配置](managing-memory-allocation.md)
</dt> </dl>

 

 