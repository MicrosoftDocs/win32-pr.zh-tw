---
description: 下表顯示應用程式可用來處理插入號、理由和叢集的各種方法。
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: 使用插入號位置、對齊點和叢集之間的關聯性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973474"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a>使用插入號位置、對齊點和叢集之間的關聯性

下表顯示應用程式可用來處理插入號、理由和叢集的各種方法。



| Task                             | Uniscribe 支援                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 依字元叢集的插入號移動  | [**腳本 \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)結構之 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** 成員的 *pwLogClust* 參數<br/> [**腳本 \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)結構的 **fCharStop** 成員<br/> |
| 字元之間換行 | [**腳本 \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)結構之 [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **fClusterStart** 成員的 *pwLogClust* 參數<br/> [**腳本 \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)結構的 **fCharStop** 成員<br/> |
| 依字組移動插入號               | [**腳本 \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)結構的 **fWordStop** 成員                                                                                                                                                                                            |
| 單字之間的換行      | [**腳本 \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)結構的 **fWordStop** 成員                                                                                                                                                                                            |
| 理由                    | [**腳本 \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)結構的 **uJustification** 成員                                                                                                                                                                                       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




