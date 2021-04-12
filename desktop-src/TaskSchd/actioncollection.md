---
title: Actioncollection 動作物件
description: 包含工作所執行之動作的腳本物件。
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- 動作工作排程器，集合物件
- Actioncollection 動作物件工作排程器
- Actioncollection 動作物件工作排程器，說明
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dee7182cc79684dec1fd052f7ad67409ba513f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509448"
---
# <a name="actioncollection-object"></a>Actioncollection 動作物件

包含工作所執行之動作的腳本物件。

## <a name="members"></a>成員

**Actioncollection 動作** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Actioncollection 動作** 物件有這些方法。



| 方法                                    | 描述                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [**清楚**](actioncollection-clear.md)   | 清除集合中的所有動作。<br/>      |
| [**建立**](actioncollection-create.md) | 建立新的動作，並將其加入至集合。<br/> |
| [**移除**](actioncollection-remove.md) | 從集合中移除指定的動作。<br/>  |



 

### <a name="properties"></a>屬性

**Actioncollection 動作** 物件具有這些屬性。



| 屬性                                               | 存取類型           | Description                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Context**](actioncollection-context.md)<br/> | 讀取/寫入<br/> | 取得或設定工作主體的識別碼。<br/> |
| [**計數**](actioncollection-count.md)<br/>     | 唯讀<br/>  | 取得集合中的動作數目。<br/>              |
| [**項目**](actioncollection-item.md)<br/>       | 唯讀<br/>  | 從集合中取得指定的動作。<br/>               |
| [**XmlText**](actioncollection-xmltext.md)<br/> | 讀取/寫入<br/> | 取得或設定集合的 XML 格式版本。<br/>   |



 

## <a name="remarks"></a>備註

讀取或寫入 XML 時，會在工作排程器架構的 [**actions**](taskschedulerschema-actions-tasktype-element.md) 元素中指定工作的動作。

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和範例程式碼，請參閱 [時間觸發程式範例 (腳本) ](time-trigger-example--scripting-.md)、 [事件觸發程式範例 (腳本) ](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting))、 [每日觸發程式範例 (腳本 ](daily-trigger-example--scripting-.md)) 、 [註冊觸發 ](registration-trigger-example--scripting-.md)程式範例 (腳本) 、 [的觸發程式 ](weekly-trigger-example--scripting-.md)範例、 [登入觸發 ](logon-trigger-example--scripting-.md)程式範例 (腳本) ，或啟動觸發程式範例 [ (腳本) ](boot-trigger-example--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





