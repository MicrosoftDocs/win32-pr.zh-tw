---
title: Actioncollection 動作。內容屬性
description: 針對腳本，取得或設定工作主體的識別碼。
ms.assetid: 5d8ac31c-ce07-4801-a04e-e12e996b88c6
keywords:
- 內容屬性工作排程器
- CoNtext 屬性工作排程器，Actioncollection 動作物件
- Actioncollection 動作物件工作排程器、內容屬性
topic_type:
- apiref
api_name:
- ActionCollection.Context
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98318ba8332e4c3bb0e7fee6b702a7ed50533
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001299"
---
# <a name="actioncollectioncontext-property"></a>Actioncollection 動作。內容屬性

針對腳本，取得或設定工作主體的識別碼。

## <a name="syntax"></a>Syntax


```VB
ActionCollection.Context As String
```



## <a name="property-value"></a>屬性值

工作主體的識別碼。 在此指定的識別碼必須符合定義主體之 IPrincipal 介面的 Id 屬性中所指定的識別碼。

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
</dt> <dt>

[**Actioncollection 動作**](actioncollection.md)
</dt> </dl>

 

 





