---
title: Exec (actionGroup) 元素
description: 指定執行命令列操作的動作。
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Exec 元素工作排程器
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106975603"
---
# <a name="exec-actiongroup-element"></a>Exec (actionGroup) 元素

指定執行命令列操作的動作。

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

**Exec** 元素是由 [**actionGroup**](taskschedulerschema-actiongroup-group.md)所定義。

## <a name="parent-element"></a>父元素



| 元素                                                         | 衍生自                                                       | Description                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**行動**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | 包含工作所執行的動作。<br/> |



## <a name="child-elements"></a>子元素



| 元素                                                                           | 類型       | Description                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [**引數**](taskschedulerschema-arguments-exectype-element.md)               | **string** | 指定與命令列操作相關聯的引數。<br/>                               |
| [**命令**](taskschedulerschema-command-exectype-element.md)                   | **string** | 指定要執行的可執行檔或檔。<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | 字串     | 指定可執行檔或可執行檔所使用的檔案所在的目錄。<br/> |



## <a name="attributes"></a>屬性



| 名稱 | 類型       | 描述                                                    |
|------|------------|----------------------------------------------------------------|
| id   | **string** | 工作所執行之動作的識別碼。<br/> |



## <a name="remarks"></a>備註

上方所列的子專案是由 [**execType**](taskschedulerschema-exectype-complextype.md) 複雜型別定義。

針對腳本開發，執行動作是由 [**ExecAction**](execaction.md) 物件定義。

針對 c + + 開發，執行動作是由 [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) 介面所定義。

如果在 [**命令**](taskschedulerschema-command-exectype-element.md)、 [**引數**](taskschedulerschema-arguments-exectype-element.md)或 [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) 元素中使用環境變數，則會快取環境變數的值，並在啟動工作引擎)  (Taskeng.exe 時使用。 工作引擎啟動後所發生的環境變數變更將不會由工作引擎使用。

## <a name="examples"></a>範例

如需使用事件觸發程式之工作的完整 XML 範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器架構元素](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





