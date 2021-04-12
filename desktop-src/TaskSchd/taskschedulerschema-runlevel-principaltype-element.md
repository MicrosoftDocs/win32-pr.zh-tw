---
title: RunLevel (runLevelType) 元素
description: 包含指定執行工作之安全性內容層級的值。
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- RunLevel 元素工作排程器
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317499"
---
# <a name="runlevel-runleveltype-element"></a>RunLevel (runLevelType) 元素

包含指定執行工作之安全性內容層級的值。 您可以指定使用最低許可權或更高的許可權來執行工作。 值為0會指定以最低許可權來執行工作，而值為1則指定以較高的許可權執行工作。

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

**RunLevel** 元素是由 [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) simple 型別定義。

## <a name="parent-element"></a>父元素



| 元素                                                                                  | 衍生自                                                           | Description                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Principal (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | 指定主體的安全性認證。 這些認證會定義工作執行所在的安全性內容。 <br/> |



## <a name="remarks"></a>備註

針對 c + + 開發，請參閱 [**IPrincipal 的 RunLevel 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel)。

如需腳本開發，請參閱 [**Principal. RunLevel**](principal-runlevel.md)。

如果工作是使用內 **建 \\ 系統管理員** 帳戶或 [LocalSystem](/windows/desktop/Services/localsystem-account) 或 [LocalService](/windows/desktop/Services/localservice-account) 帳戶來註冊的，則會忽略 [**RunLevel**](principal-runlevel.md) 屬性。 如果已關閉 [使用者帳戶控制](/windows/desktop/SecAuthZ/user-account-control) (UAC) ，也會忽略屬性值。

如果工作是使用工作安全性內容的 **Administrators** 群組來註冊的，則您也必須將 [**RunLevel**](principal-runlevel.md) 屬性設定為 "HighestAvailable"，才能執行工作。 如需詳細資訊，請參閱工作 [的安全性](security-contexts-for-running-tasks.md)內容。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



 

