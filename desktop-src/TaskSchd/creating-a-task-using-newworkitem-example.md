---
title: 使用 NewWorkItem 範例建立工作
description: 建立工作時，您將會使用兩個工作排程器介面 ITaskScheduler 和 ITask。
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- 工作排程器建立工作專案
- 工作專案工作排程器，建立工作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315820"
---
# <a name="creating-a-task-using-newworkitem-example"></a>使用 NewWorkItem 範例建立工作

建立工作時，您將使用兩個工作排程器介面： [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) 和 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)。 您必須為工作提供唯一的名稱、工作物件的類別識別碼，以及 **ITask** 的介面識別碼。 本主題後面的程式碼範例會顯示類別識別碼和介面識別碼。

> [!Note]  
> 您也可以藉由呼叫 [**ITaskScheduler：： azuretasks**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem)來建立工作。 當您採用此路由時，您必須負責建立 **(的工作物件實例** ，以支援 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面) 然後使用您提供的名稱來新增工作。

 

> [!Note]  
> 依預設，只有 Administrators、Backup Operators 或 Server Operators 群組的成員可以在 Windows Server 2003 上建立工作。 Administrators 群組的成員可以變更 Windows 工作資料夾的安全描述項， \\ 讓其他人可以建立工作。

 

您為工作提供的名稱在 [排程工作] 資料夾中必須是唯一的。 如果已經存在具有相同名稱的工作， [**ITaskScheduler：： NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) 會傳回錯誤 \_ 檔案 \_ 。 如果您收到此傳回值，您應該指定不同的名稱，然後再次嘗試建立工作。

下列程式描述如何建立新的工作專案工作。

**若要建立新的工作專案工作**

1.  呼叫 [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) 以初始化 COM 程式庫和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得工作排程器物件。  (此範例假設工作排程器服務正在執行。 ) 
2.  呼叫 [**ITaskScheduler：： NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) 來建立新的工作。  (這個方法會傳回 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) 介面的指標。 ) 
3.  藉由呼叫 [**IPersistFile：： save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save)，將新的工作儲存至磁片。 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)介面 (是 **ITask** 介面所支援的標準 COM 介面。 ) 
4.  呼叫 **ITask：： release** 以釋放所有資源。  (請注意，[**版本**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)是 [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)所繼承的 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)方法 ) 



| 如需的程式碼範例  | 請參閱                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| 建立單一工作 | [C/c + + 程式碼範例：使用 NewWorkItem 建立工作](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作排程器1.0 範例](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 