---
title: TaskSettings. NetworkSettings 屬性
description: 針對腳本，取得或設定包含網路設定檔識別碼和名稱的網路設定物件。
ms.assetid: 3d368f6c-4534-4e71-8fbd-84361730a3e2
keywords:
- NetworkSettings 屬性工作排程器
- NetworkSettings 屬性工作排程器，TaskSettings 物件
- TaskSettings 物件工作排程器、NetworkSettings 屬性
topic_type:
- apiref
api_name:
- TaskSettings.NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 730701c71a69f05b73524d6f9d1d8ad3d89b5e93620664be33a80c5c41af1479
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059653"
---
# <a name="tasksettingsnetworksettings-property"></a>TaskSettings. NetworkSettings 屬性

針對腳本，取得或設定包含網路設定檔識別碼和名稱的網路設定物件。 如果 [**TaskSettings**](tasksettings.md)的 [**RunOnlyIfNetworkAvailable**](tasksettings-runonlyifnetworkavailable.md)屬性為 **True** ，而且 **NetworkSettings** 屬性中指定了網路 propfile，則只有在指定的網路設定檔可用時，才會執行此工作。

## <a name="syntax"></a>Syntax


```VB
TaskSettings.NetworkSettings As NetworkSettings
```



## <a name="property-value"></a>屬性值

[**NetworkSettings**](networksettings.md)物件，其中包含網路設定檔識別碼和名稱。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TaskSettings**](tasksettings.md)
</dt> <dt>

[**NetworkSettings**](networksettings.md)
</dt> </dl>

 

 





