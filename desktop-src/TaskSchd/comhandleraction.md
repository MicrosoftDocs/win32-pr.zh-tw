---
title: ComHandlerAction 物件
description: 代表引發處理常式之動作的腳本物件。
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- COM 處理常式動作工作排程器，物件
- ComHandlerAction 物件工作排程器
- ComHandlerAction 物件工作排程器，說明
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd803d67d292df22e651e4393880038835c862e0e81dde19e0d0a7e15fccd32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659678"
---
# <a name="comhandleraction-object"></a>ComHandlerAction 物件

代表引發處理常式之動作的腳本物件。

## <a name="members"></a>成員

**ComHandlerAction** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ComHandlerAction** 物件具有這些屬性。



| 屬性                                               | 存取類型           | 描述                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**ClassId**](comhandleraction-classid.md)<br/> | 讀取/寫入<br/> | 取得或設定處理常式類別的識別碼。<br/>                                              |
| [**資料**](comhandleraction-data.md)<br/>       | 讀取/寫入<br/> | 取得或設定與處理常式相關聯的其他資料。<br/>                              |
| [**Id**](action-id.md)<br/>                     | 讀取/寫入<br/> | 繼承自 [**動作**](action.md) 物件。 取得或設定動作的識別碼。<br/> |
| [**類型**](action-type.md)<br/>                 | 唯讀<br/>  | 繼承自 [**動作**](action.md) 物件。 取得動作的類型。<br/>               |



 

## <a name="remarks"></a>備註

COM 處理常式必須針對工作排程器執行 [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) 介面，以啟動和停止處理常式。 接著，COM 處理常式會使用 [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) 物件的方法，將狀態傳達給工作排程器。

讀取或寫入 XML 時，會在工作排程器架構的 [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) 元素中指定 COM 處理常式動作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[工作排程器物件](task-scheduler-objects.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





