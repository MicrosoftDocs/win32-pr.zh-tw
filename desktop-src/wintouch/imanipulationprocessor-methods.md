---
title: '方法 (IInertiaProcessor) '
description: 本節包含 IInertiaProcessor 介面的方法。
ms.assetid: e4acfcac-06c1-42a5-9722-4534a4492ab8
keywords:
- Windows Touch，IInertiaProcessor 介面
- Windows Touch，介面方法
- 慣性、IInertiaProcessor 介面
- IInertiaProcessor 介面，方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662bb9aaa51400c4fd302f56bfec7c845ce57645
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106967514"
---
# <a name="methods-iinertiaprocessor"></a>方法 (IInertiaProcessor) 

本節包含 [**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor) 介面的方法。



| 方法                                                 | 描述                                                                                                                                                                                                                |
|--------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**重設**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-reset)               | 使用初始時間戳記初始化處理器，並重新啟動慣性。                                                                                                                                                    |
| [**處理序**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)           | 針對目前的刻度執行計算，並根據外推是否已完成來引發 **差異** 或 **已完成** 的事件。 如果在上一個刻度完成推斷，則方法為無作業。 |
| [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime)   | 針對指定的刻度執行計算，並根據外推是否已完成來引發 **Delta** 或 **Completed** 事件。                                                                        |
| [**完成**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-complete)         | 完成目前的操作，並停止慣性處理器上的慣性。                                                                                                                                              |
| [**CompleteTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-completetime) | 在指定的刻度完成目前的操作、停止慣性處理器上的慣性，並引發 System.windows.uielement.manipulationcompleted> 事件。                                                                                   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IInertiaProcessor**](/windows/desktop/api/manipulations/nn-manipulations-iinertiaprocessor)
</dt> </dl>

 

 




