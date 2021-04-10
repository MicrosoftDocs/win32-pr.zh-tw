---
title: 列舉工作
description: 工作排程器1.0 提供列舉物件來列舉 [排定的工作] 資料夾中的工作。
ms.assetid: ccd140a1-06f6-4e6b-afa6-f7ac9b9ff904
keywords:
- 列舉工作工作排程器
- 列舉工作工作排程器，說明
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dda98cf40bc1ea360d20bcf13084faa692aa22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021743"
---
# <a name="enumerating-tasks"></a>列舉工作

工作排程器1.0 提供列舉物件來列舉 [排定的工作] [*資料夾*](s.md)中的工作。

> [!Note]  
> 若為 Windows Server 2003、Windows XP 或 Windows 2000 電腦，可在 Windows Vista 電腦上建立、監視或控制工作，則必須在 Windows Vista 電腦上完成某些作業。 如需詳細資訊，請參閱[工作](tasks.md)。

 

## <a name="using-the-enumeration-object"></a>使用列舉物件

這個物件的 [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) 介面會提供方法來列舉資料夾中的工作、將列舉順序重設為清單的開頭、略過工作，以及建立目前列舉物件的複本以供稍後使用。

如需列舉 [排定的工作] 資料夾中之工作的詳細資訊，請參閱 [**IEnumWorkItems：： Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next)。

如需將列舉值重設為清單開頭的詳細資訊，請參閱 [**IEnumWorkItems：： Reset**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-reset)。

如需略過工作的詳細資訊，請參閱 [**IEnumWorkItems：： Skip**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-skip)。

如需建立目前列舉物件複本的詳細資訊，請參閱 [**IEnumWorkItems：： Clone**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-clone)。

如需列舉 [排定的工作] 資料夾中之工作的範例，請參閱 [列舉工作範例](enumerating-tasks-example.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**概念**
</dt> <dt>

[工作排程器1.0 工作資訊](task-scheduler-1-0-task-informatation.md)
</dt> </dl>

 

 




