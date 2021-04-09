---
title: 工作排程器1.0 的觸發程式結構
description: 工作排程器1.0 會使用數個結構來定義觸發程式的準則。
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a03f28f85782d87ee3349582929babe6f907e8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021580"
---
# <a name="trigger-structures-for-task-scheduler-10"></a>工作排程器1.0 的觸發程式結構

工作排程器1.0 會使用數個結構來定義觸發程式的準則。

> [!Note]  
> 如需工作排程器2.0 觸發程式的詳細資訊，請參閱 [觸發程式介面](trigger-interfaces.md)。

 

## <a name="task-scheduler-10-structures"></a>工作排程器1.0 結構

下圖顯示工作 [**\_ 觸發**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) 程式結構。 它有三個必要的成員 (在建立新的觸發程式時必須設定的 **wBeginYear**、 **wBeginMonth** 和 **wBeginDay**) 。  (跳到此結構的參考頁面，請按一下圖例中的結構名稱。 ) 

![工作觸發程式結構](images/tsktri1.png)

請注意， **TriggerType** 成員使用工作 [**觸發程式 \_ \_ 類型**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) 列舉，而 **類型** 成員使用工作觸發程式聯 **\_ \_ 集** 結構。 工作 **\_ 觸發程式 \_ 類型** 列舉是用來指定觸發程式的類型 (事件和以時間為基礎的觸發程式類型) 。 [**觸發程式 \_ 類型聯 \_ 集**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union)結構是用來合併 [**每日**](/windows/desktop/api/Mstask/ns-mstask-daily)、[**每週**](/windows/desktop/api/Mstask/ns-mstask-weekly)、 [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (日的月份) ，以及 [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (星期幾) 結構，用來指定何時會引發以時間為基礎的觸發程式。

如果 **TriggerType** 指定以時間為基礎的觸發程式或以事件為基礎的觸發程式，則會忽略 **類型** 成員。 只有當 **TriggerType** 成員指定每日、每週、每月或每週的時間型觸發程式時，才會使用 [**觸發型別聯 \_ \_ 集**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union)結構。

此外， **類型** 成員的設定會指出要使用的 [**觸發程式類型聯 \_ \_ 集**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) 結構的成員。 下圖顯示工作 [**\_ 觸發程式 \_ 類型**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) 列舉值與 **觸發程式 \_ 類型 \_ 結構** 結構的成員之間的關聯性。  (跳至這些結構的參考頁面，請按一下圖例中的結構名稱。 ) 

![工作觸發程式類型列舉值與觸發程式類型結構結構成員之間的關聯性](images/tsktri3.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作觸發程式](task-triggers.md)
</dt> <dt>

[觸發程式類型](trigger-types.md)
</dt> <dt>

[觸發程式介面](trigger-interfaces.md)
</dt> </dl>

 

 




