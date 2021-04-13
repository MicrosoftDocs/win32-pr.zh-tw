---
title: 引數 (execType) 元素
description: 指定與命令列操作相關聯的引數。
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Arguments 元素工作排程器
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff35465fbad1de82d096b583499ea6cdafe93ca7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508852"
---
# <a name="arguments-exectype-element"></a>引數 (execType) 元素

指定與命令列操作相關聯的引數。

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

**引數** 元素是由 [**execType**](taskschedulerschema-exectype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                      | 衍生自                                                 | Description                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | 指定執行命令列操作的動作。<br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IExecAction 的引數屬性**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)。

如需腳本開發，請參閱 [**ExecAction。**](execaction-arguments.md)

## <a name="examples"></a>範例

如需使用可執行動作之工作的 XML 完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





