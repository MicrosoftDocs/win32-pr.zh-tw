---
description: 當選取的資料夾從某個目錄變更為控制項中的另一個目錄時，DirectoryList 控制項就會發佈 IgnoreChange ControlEvent。 此事件應該撰寫于 EventMapping 資料表中。
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000273"
---
# <a name="ignorechange-controlevent"></a>IgnoreChange ControlEvent

當選取的資料夾從某個目錄變更為控制項中的另一個目錄時， [DirectoryList 控制項](directorylist-control.md) 就會發佈 IgnoreChange ControlEvent。 此事件應該撰寫于 [EventMapping 資料表](eventmapping-table.md)中。

此 ControlEvent 要求使用者介面必須在 [*完整的 UI*](f-gly.md) 層級上執行。 此事件將無法用於 [*縮減 ui*](r-gly.md) 或 [*基本 ui*](b-gly.md)。 如需詳細資訊，請參閱 [消費者介面層級](user-interface-levels.md)。

## <a name="published-by"></a>發佈者

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>引數

這個 ControlEvent 不會使用引數。

## <a name="action-on-subscribers"></a>訂閱者的動作

此 ControlEvent 不會在訂閱者上執行動作。

## <a name="typical-use"></a>一般用法

[DirectoryCombo 控制項](directorycombo-control.md)通常會採用 IgnoreChange ControlEvent。

 

 



