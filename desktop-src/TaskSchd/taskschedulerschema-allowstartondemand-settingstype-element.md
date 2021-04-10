---
title: AllowStartOnDemand (settingsType) 元素
description: 指定可使用 [執行] 命令或內容功能表來啟動工作。
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- AllowStartOnDemand 元素工作排程器
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934073"
---
# <a name="allowstartondemand-settingstype-element"></a>AllowStartOnDemand (settingsType) 元素

指定可使用 [執行] 命令或內容功能表來啟動工作。

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

**AllowStartOnDemand** 元素是由 [**settingsType**](taskschedulerschema-settingstype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                           | 衍生自                                                         | Description                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**設定**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | 包含工作排程器用來執行工作的設定。<br/> |



## <a name="remarks"></a>備註

當此專案設定為 True 時，可以在任何觸發程式啟動工作時，獨立啟動工作。

針對 c + + 開發，請參閱 [**ITaskSettings 的 AllowDemandStart 屬性**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart)。

如需腳本開發，請參閱 [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md)。

## <a name="examples"></a>範例

如需允許要求開始之工作的 XML 完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





