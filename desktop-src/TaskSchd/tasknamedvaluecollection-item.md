---
title: TaskNamedValueCollection 專案屬性
description: 針對腳本，從集合取得指定的名稱/值組。
ms.assetid: 89c87b22-e459-435d-8c15-69907e9b1329
keywords:
- Item 屬性工作排程器
- 專案屬性工作排程器，TaskNamedValueCollection 物件
- TaskNamedValueCollection 物件工作排程器，Item 屬性
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55dd6479486bb481f31e7aaf2b920ef591d1fa1019d432b22568fa7d7f56bf9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991468"
---
# <a name="tasknamedvaluecollectionitem-property"></a>TaskNamedValueCollection 專案屬性

針對腳本，從集合取得指定的名稱/值組。

## <a name="syntax"></a>Syntax


```VB
TaskNamedValueCollection.Item( _
  ByVal index, _
  ByRef pair _
) As long
```



## <a name="property-value"></a>屬性值

代表所要求之配對的 [**TaskNamedValuePair**](tasknamedvaluepair.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





