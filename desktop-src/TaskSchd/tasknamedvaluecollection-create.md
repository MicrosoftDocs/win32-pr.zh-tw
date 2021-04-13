---
title: TaskNamedValueCollection. Create 方法
description: 針對腳本，會在集合中建立名稱/值組。
ms.assetid: f64e0548-fad3-4682-b50b-ff8ec685af36
keywords:
- 建立方法工作排程器
- 建立方法工作排程器，TaskNamedValueCollection 物件
- TaskNamedValueCollection 物件工作排程器，建立方法
topic_type:
- apiref
api_name:
- TaskNamedValueCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3926142b25cbb2d65efaa45d6b767ce2e56ba86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466425"
---
# <a name="tasknamedvaluecollectioncreate-method"></a>TaskNamedValueCollection. Create 方法

針對腳本，會在集合中建立名稱/值組。

## <a name="syntax"></a>語法


```VB
TaskNamedValueCollection.Create( _
  ByVal name, _
  ByVal value, _
  ByRef pair _
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*名稱* \[在\]
</dt> <dd>

與名稱/值配對中的值相關聯的名稱。

</dd> <dt>

*值* \[在\]
</dt> <dd>

與名稱/值配對中的名稱相關聯的值。

</dd> <dt>

*配對* \[擴展\]
</dt> <dd>

在集合中建立的名稱/值組。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





