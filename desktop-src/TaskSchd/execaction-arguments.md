---
title: ExecAction. Arguments 屬性
description: 針對腳本，取得或設定與命令列操作相關聯的引數。
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Arguments 屬性工作排程器
- Arguments 屬性工作排程器，ExecAction 物件
- ExecAction 物件工作排程器、Arguments 屬性
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899e4ceaaf3a0d04dc678592add18184401d54569fea71f0570a0acbf2a33027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011488"
---
# <a name="execactionarguments-property"></a>ExecAction. Arguments 屬性

針對腳本，取得或設定與命令列操作相關聯的引數。

## <a name="syntax"></a>Syntax


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a>屬性值

命令列操作所需的引數。

## <a name="remarks"></a>備註

讀取或寫入 XML 時，命令列作業引數是在工作排程器架構的 [**引數**](taskschedulerschema-arguments-exectype-element.md) 元素中指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





