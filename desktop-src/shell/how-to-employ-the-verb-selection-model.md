---
description: 您必須為動詞設定登錄值，以處理使用者可以從專案中選取單一專案、多個專案或選取專案的情況。 針對此動詞支援的三種情況，動詞都需要個別的登錄值。
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: 如何使用動詞選取模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973160"
---
# <a name="how-to-employ-the-verb-selection-model"></a>如何使用動詞選取模型

您必須為動詞設定登錄值，以處理使用者可以從專案中選取單一專案、多個專案或選取專案的情況。 針對此動詞支援的三種情況，動詞都需要個別的登錄值。

## <a name="instructions"></a>指示


指定所有動詞的 MultiSelectModel 值。 如果未指定 MultiSelectModel 值，則會從您選擇的動詞執行類型推斷。 針對以 COM 為基礎的方法 (例如 DropTarget 和 ExecuteCommand) **播放** 程式，並假設為其他方法 **檔** 。

動詞選取模型的可能值如下：

1.  針對僅支援單一選取專案的動詞指定 **single** 。
2.  針對支援任意數量專案的動詞指定 **播放** 程式。
3.  針對每個專案建立最上層視窗的動詞命令指定 **檔** 。 這麼做會限制啟用的專案數目，如果使用者開啟太多視窗，則有助於避免系統資源不足。

## <a name="remarks"></a>備註

當選取的專案數目不符合動詞選取模型，或大於下表所述的預設限制時，就無法顯示該動詞。



| 動詞執行的類型 | 文件 | 播放器    |
|-----------------------------|----------|-----------|
| 舊版                      | 15個專案 | 100專案 |
| COM                         | 15個專案 | 沒有限制  |



 

以下是使用 MultiSelectModel 值的範例登錄專案。

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



