---
title: 重複工作
description: 工作排程器可以在引發觸發程式之後，任意次數執行一次工作。
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- 重複模式工作排程器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7039b57bdc6cc7f53125e74b8a6fda7d017106cd44c66d2535f7fdf27505a960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759351"
---
# <a name="repeating-a-task"></a>重複工作

工作排程器可以在引發觸發程式之後，任意次數執行一次工作。 若要這樣做，此觸發程式會定義重複模式，告知工作排程器它應該繼續重複工作的時間，以及每個工作重複之間的時間間隔。

## <a name="repetition-pattern"></a>重複模式

下圖顯示持續時間為60分鐘的重複模式，以及25分鐘的間隔。 請注意，在此情況下，工作排程器會在觸發程式引發時執行工作，它會在25分鐘之後再次執行工作，然後根據 IRepetitionPattern () [**RepetitionPattern**](repetitionpattern-stopatdurationend.md)的 [**StopAtDurationEnd 屬性**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend)設定，在50分鐘後再執行一次此工作。 如果 [ **StopAtDurationEnd** ] 屬性設定為 [True]，工作排程器在60分鐘後仍在執行時，停止工作的最後一個實例。 如果 **StopAtDurationEnd** 屬性設定為 False，就會執行工作的最後一個實例，而不管持續時間。

![觸發重複模式](images/repetition-pattern.png)

如果您註冊的工作包含重複間隔等於1分鐘的觸發程式，且重複持續時間等於四分鐘，則工作會啟動五次。 您可以使用下列模式來定義五次重複：

1.  工作會在第一分鐘的開頭開始。
2.  下一項工作會在第一分鐘結束時啟動。
3.  下一項工作會在第二分鐘結束時啟動。
4.  下一項工作會從第三分鐘的結尾開始。
5.  下一項工作會在第四分鐘結束時啟動。

**Windows Server 2003、Windows XP 和 Windows 2000：** 如果您註冊的工作包含重複間隔等於1分鐘的觸發程式，且重複持續時間等於四分鐘，則工作會啟動四次。

## <a name="objects-interfaces-and-xml-elements"></a>物件、介面和 XML 元素

針對開發腳本，會使用 [**RepetitionPattern**](repetitionpattern.md) 物件來定義重複模式。

針對 c + + 開發，重複模式是由 [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) 介面所定義。

讀取或寫入工作的 XML 時，重複的模式是在 [**重複**](taskschedulerschema-repetition-triggerbasetype-element.md) 專案中指定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作觸發程式](task-triggers.md)
</dt> </dl>

 

 




