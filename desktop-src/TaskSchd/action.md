---
title: Action 物件
description: 腳本物件，提供所有動作物件所繼承的通用屬性。
ms.assetid: 9d6fe5e3-1ece-47ea-a644-8cae0419324f
keywords:
- 動作物件工作排程器
- 動作物件工作排程器，說明
topic_type:
- apiref
api_name:
- Action
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4b9f41521f1af8b4601faafce9674277b172ad4cde3f364fc2ab7a84cfcc0df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739038"
---
# <a name="action-object"></a>Action 物件

腳本物件，提供所有動作物件所繼承的通用屬性。 動作物件是由 [**actioncollection 動作**](actioncollection-create.md) 建立的方法所建立。

## <a name="members"></a>成員

**Action** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**動作** 物件具有這些屬性。



| 屬性                               | 存取類型           | 描述                                           |
|:---------------------------------------|:----------------------|:------------------------------------------------------|
| [**Id**](action-id.md)<br/>     | 讀取/寫入<br/> | 取得或設定動作的識別碼。<br/> |
| [**類型**](action-type.md)<br/> | 唯讀<br/>  | 取得動作的類型。<br/>               |



 

## <a name="remarks"></a>備註

如需動作和工作如何一起運作的詳細資訊，請參閱工作 [動作](task-actions.md)。 下表包含腳本物件，代表可以執行的動作：



| API                                            | 描述                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [**ComHandlerAction**](comhandleraction.md)   | 表示引發處理常式的動作。                   |
| [**ExecAction**](execaction.md)               | 表示執行命令列操作的動作。 |
| [**EmailAction**](emailaction.md)             | 表示傳送電子郵件訊息的動作。            |
| [**ShowMessageAction**](showmessageaction.md) | 表示顯示訊息方塊的動作。               |



 

讀取或寫入 XML 時，會在工作排程器架構的 [**actions**](taskschedulerschema-actions-tasktype-element.md) 元素中指定工作的動作。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md) 、 [事件觸發程式範例 (腳本) ](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))、 [每日觸發程式範例 (腳本 ](daily-trigger-example--scripting-.md)) 、 [註冊觸發 ](registration-trigger-example--scripting-.md)程式範例 (腳本) 、 [的觸發程式 ](weekly-trigger-example--scripting-.md)範例、 [登入觸發 ](logon-trigger-example--scripting-.md)程式範例 (腳本) ，或啟動觸發程式範例 [ (腳本) ](boot-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器腳本物件](task-scheduler-objects.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





