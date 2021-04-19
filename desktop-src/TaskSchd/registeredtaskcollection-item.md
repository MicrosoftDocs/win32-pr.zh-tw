---
title: RegisteredTaskCollection 專案屬性
description: 針對腳本，從集合取得指定的已註冊工作。
ms.assetid: 8b396478-4cd9-426c-afe8-29539ff0b859
keywords:
- Item 屬性工作排程器
- 專案屬性工作排程器，RegisteredTaskCollection 物件
- RegisteredTaskCollection 物件工作排程器，Item 屬性
topic_type:
- apiref
api_name:
- RegisteredTaskCollection.Item
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ec79eb526b85b88afc0e5747a80b45f07b99a9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969145"
---
# <a name="registeredtaskcollectionitem-property"></a>RegisteredTaskCollection 專案屬性

針對腳本，從集合取得指定的已註冊工作。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```VB
RegisteredTaskCollection.Item( _
  ByVal Index _
) As RegisteredTask
```



## <a name="property-value"></a>屬性值

[**RegisteredTask**](registeredtask.md)物件，其中包含已註冊的工作。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





