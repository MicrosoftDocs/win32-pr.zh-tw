---
title: RegisteredTaskCollection 物件
description: 腳本物件，其中包含所有已註冊的工作。
ms.assetid: 0bd2010d-af25-4316-8829-62e4ec4761e2
keywords:
- RegisteredTaskCollection 物件工作排程器
- RegisteredTaskCollection 物件工作排程器，說明
topic_type:
- apiref
api_name:
- RegisteredTaskCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c11c299bc8817cc1627c40b3c465cd182e0f4c67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024773"
---
# <a name="registeredtaskcollection-object"></a>RegisteredTaskCollection 物件

腳本物件，其中包含所有已註冊的工作。

## <a name="members"></a>成員

**RegisteredTaskCollection** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**RegisteredTaskCollection** 物件具有這些屬性。



| 屬性                                                   | 存取類型          | Description                                                        |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------|
| [**計數**](registeredtaskcollection-count.md)<br/> | 唯讀<br/> | 取得集合中已註冊工作的數目。<br/>  |
| [**項目**](registeredtaskcollection-item.md)<br/>   | 唯讀<br/> | 從集合中取得指定的已註冊工作。<br/> |



 

## <a name="examples"></a>範例

如需此腳本物件的詳細資訊和程式碼範例，請參閱 [顯示工作名稱和狀態 (腳本) ](displaying-task-names-and-state--scripting-.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TaskFolder.GetTasks**](taskfolder-gettasks.md)
</dt> </dl>

 

 





