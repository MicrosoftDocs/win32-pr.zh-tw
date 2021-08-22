---
description: 已設定之屬性的邏輯值為 True。
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: 在條件陳述式中使用屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5dcee5c2d657b8014ac98c0d4d1ce5b56f0f3614a597cd63611ae965e30720
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499208"
---
# <a name="using-properties-in-conditional-statements"></a>在條件陳述式中使用屬性

已設定之屬性的邏輯值為 True。 若要判斷是否已設定屬性，但未實際取得其值，請測試邏輯運算式 "MyProperty" 或 "Not MyProperty"。 當設定屬性 MyProperty 時，前者會評估為 True，後者則會評估為 False。

一或多個屬性可以與運算子結合，以形成條件陳述式中所使用的邏輯運算式。 如需有關可在條件陳述式中使用之運算子的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。

您可以在 [條件資料表](condition-table.md) 的 [條件] 資料行中輸入使用屬性的條件陳述式，以修改 [功能資料表](feature-table.md)中任何專案的選取狀態。

具有一或多個屬性的條件陳述式，通常用於資料庫資料表的 [條件] 資料行中。

下表各有條件運算式的資料行：

-   [條件資料表](condition-table.md)
-   [ControlEvent 資料表](controlevent-table.md)
-   [LaunchCondition 資料表](launchcondition-table.md)
-   [InstallUISequence 資料表](installuisequence-table.md)
-   [InstallExecuteSequence 資料表](installexecutesequence-table.md)
-   [ControlCondition 資料表](controlcondition-table.md)
-   [AdminExecuteSequence 資料表](adminexecutesequence-table.md)
-   [AdvtExecuteSequence 資料表](advtexecutesequence-table.md)
-   [AdminUISequence 資料表](adminuisequence-table.md)

請注意，六個動作順序資料表有條件的欄位。 如果此欄位中的條件運算式評估為 False，則安裝程式會略過該動作。

如果您在 UI 序列中，藉由在其中一個使用者介面順序資料表中撰寫自訂動作來設定 [私用屬性](private-properties.md) ，該屬性就不會在執行順序中設定。 若要在執行順序中設定屬性，您也必須在執行順序資料表中放置自訂動作。 或者，您可以將屬性設為 [公用屬性](public-properties.md) ，並將它包含在 [**SecureCustomProperties**](securecustomproperties.md) 屬性中。

如需詳細資訊，請參閱 [使用順序資料表](using-a-sequence-table.md) 或 [使用屬性](using-properties.md)。

 

 



