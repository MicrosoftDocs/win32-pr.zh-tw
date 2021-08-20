---
description: 用來建立、摧毀和匯出虛擬系統快照集集合的服務。
ms.assetid: 55a6c7b4-5352-4766-b5b7-6699b1f40b78
title: Msvm_CollectionSnapshotService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d9b4a0f68979d1fbe37477b3d7d65d33a6e8c55794743d0f475ec9b017c5a257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117994755"
---
# <a name="msvm_collectionsnapshotservice-class"></a>Msvm \_ CollectionSnapshotService 類別

用來建立、摧毀和匯出虛擬系統快照集集合的服務。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotService : CIM_Service
{
};
```

## <a name="members"></a>成員

**Msvm \_ CollectionSnapshotService** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**Msvm \_ CollectionSnapshotService** 類別具有這些方法。



| 方法                                                                                    | 描述                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplySnapshot**](msvm-collectionsnapshotservice-applysnapshot.md)                     | 將快照集集合套用至虛擬電腦系統的集合。<br/>                                                                                                                                        |
| [**ConvertToReferencePoint**](msvm-collectionsnapshotservice-converttoreferencepoint.md) | 將現有的集合快照集轉換為參考點集合。 快照集集合被刪除為副作用。 只有修復快照集可以轉換成參考點。<br/>                      |
| [**>icloudblob.createsnapshot**](msvm-collectionsnapshotservice-createsnapshot.md)                   | 建立虛擬系統集合的快照集。<br/>                                                                                                                                                                 |
| [**DestroySnapshot**](msvm-collectionsnapshotservice-destroysnapshot.md)                 | 終結虛擬系統集合的現有快照集。 這個方法可能會損毀其他相依于受影響快照集的快照集。<br/>                                                   |
| [**ExportSnapshot**](msvm-collectionsnapshotservice-exportsnapshot.md)                   | 將虛擬電腦系統的快照集集合匯出到檔案。 快照集集合、其相關聯的設定設定，以及其相關聯的資源設定將會保留在產生的檔案中。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 服務**](cim-service.md)
</dt> </dl>

 

 




