---
description: 安裝程式函數可以用來執行特定動作或動作順序。
ms.assetid: ceb4f70b-1179-416a-9030-3d87341cb956
title: 執行動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ab566b90ec43a33f3e70b994b01446700e353b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981154"
---
# <a name="running-actions"></a>執行動作

安裝程式函數可以用來執行特定動作或動作順序。 這些動作可以是 [標準](standard-actions.md) 或 [自訂](custom-actions.md) 動作。 下列程式說明如何執行動作：

**執行動作順序**

1.  藉由呼叫 [**MsiSequence**](/windows/desktop/api/Msiquery/nf-msiquery-msisequencea) 函數來執行資料表中定義的動作序列。

    如果查詢的條件運算式評估為 TRUE，則安裝程式會查詢指定的資料表，並執行每個動作。

2.  藉由呼叫 [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) 函數來檢查條件運算式。
3.  藉由呼叫 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) 函數來執行動作。 動作可以是標準動作、自訂動作或使用者介面對話方塊。
4.  如果在執行此動作期間發生錯誤，請呼叫 [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) 函數。 安裝程式將會處理錯誤。

 

 



