---
title: 操作工作專案
description: IScheduledWorkItem 介面提供了用來取得和設定工作專案屬性的方法; (設定觸發程式時，必須使用 ITaskTrigger SetTrigger 方法) ，來建立、取出和刪除工作專案的觸發程式。以及執行、終止和刪除工作專案。請注意，針對特定工作專案類型的屬性，請參閱該物件類型的介面。 例如，您無法設定工作專案的優先權層級;不過，您可以使用 ITask 介面的方法來取得和設定工作的優先順序。
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- 工作排程器的工作專案，管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33680d04da9d34f54085d182ed61edda9e8b232f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682669"
---
# <a name="manipulating-work-items"></a>操作工作專案

[**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem)介面提供了用來取得和設定工作專案屬性的方法;您必須使用 [**ITaskTrigger：： SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger)方法 (設定觸發程式，才能建立、取出和刪除工作專案的觸發程式) ;以及執行、終止和刪除工作專案。

> [!Note]  
> 針對特定工作專案類型的屬性，請參閱該物件類型的介面。 例如，您無法設定工作專案的優先權層級;不過，您可以使用 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面的方法來取得和設定工作的優先順序。

 

當您修改工作專案時，您必須呼叫 [**IPersistFile：： save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) 物件將修改過的工作專案儲存至磁片。 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)介面所支援的標準 COM 介面。

| 範例                                                            | 請參閱                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| 正在抓取適用于所有工作專案類型的屬性                | [正在抓取工作專案屬性範例](retrieving-work-item-property-examples.md) |
| 設定適用于所有工作專案類型的屬性                   | [設定工作專案屬性範例](setting-work-item-property-examples.md)       |
| 執行已知的工作                                                       | [啟動工作範例](starting-a-task-example.md)                               |
| 終止正在執行的工作                                                 | [終止工作範例](terminating-a-task-example.md)                         |
| 為已知的工作建立新的觸發程式                                    | [建立新的觸發程式](creating-a-new-trigger.md)                                 |
| 為已知的工作建立事件型閒置觸發程式                      | [建立閒置觸發程式範例](creating-an-idle-trigger-example.md)             |
| 抓取與已知工作相關聯之所有觸發程式的觸發程式字串 | [正在抓取觸發字串範例](retrieving-trigger-strings-example.md)         |



 

 

 