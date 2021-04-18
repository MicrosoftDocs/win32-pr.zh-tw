---
title: WorkingDirectory (execType) 元素
description: 指定可執行檔或可執行檔所使用的檔案所在的目錄。
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- WorkingDirectory 元素工作排程器
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965532"
---
# <a name="workingdirectory-exectype-element"></a>WorkingDirectory (execType) 元素

指定可執行檔或可執行檔所使用的檔案所在的目錄。

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

**WorkingDirectory** 元素是由 [**execType**](taskschedulerschema-exectype-complextype.md)複雜型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                      | 衍生自                                                 | Description                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | 指定執行命令列操作的動作。<br/> |



## <a name="remarks"></a>備註

針對腳本開發，工作目錄是由 [**ExecAction. WorkingDirectory**](execaction-workingdirectory.md) 屬性所指定。

針對 c + + 開發，工作目錄是由 [**IExecAction：： WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) 屬性所指定。

## <a name="examples"></a>範例

下列 XML 會定義執行動作。


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





