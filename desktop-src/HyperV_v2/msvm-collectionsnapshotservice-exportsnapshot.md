---
description: 將虛擬電腦系統的快照集集合匯出到檔案。 快照集集合、其相關聯的設定設定，以及其相關聯的資源設定將會保留在產生的檔案中。
ms.assetid: 61fbc81c-c3e8-4058-b11a-4ed69481207c
title: Msvm_CollectionSnapshotService 類別的 ExportSnapshot 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ExportSnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ec61899e92da562250bf392077468adef14a35eda72d89d28ad9b3ddc3da2f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426838"
---
# <a name="exportsnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Msvm CollectionSnapshotService 類別的 ExportSnapshot 方法 \_

將虛擬電腦系統的快照集集合匯出到檔案。 快照集集合、其相關聯的設定設定，以及其相關聯的資源設定將會保留在產生的檔案中。

## <a name="syntax"></a>語法


```mof
uint32 ExportSnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [in]  string              ExportDirectory,
  [in]  string              ExportSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SnapshotCollection* \[在\]
</dt> <dd>

[**CIM \_ 集合**](cim-collection.md)的參考，代表要匯出的快照集集合。

</dd> <dt>

*ExportDirectory* \[在\]
</dt> <dd>

要匯出虛擬系統集合之目錄的完整路徑。 如果 *ExportSettingData* 參數中的 **CreateVmExportSubdirectory** 屬性設定為 **True** ，則可以重複使用此目錄來匯出多個虛擬系統集合，這個方法會將每個虛擬系統集合定義放在此路徑底下的個別子目錄中。

</dd> <dt>

*ExportSettingData* \[在\]
</dt> <dd>

[**Msvm \_ CollectionSnapshotExportSettingData**](msvm-collectionsnapshotexportsettingdata.md)的實例，表示匯出作業的設定。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果以非同步方式執行作業，則會傳回選擇性的參考。 如果有，則會使用 [**CIM \_ ConcreteJob**](cim-concretejob.md) 實例的傳回參考來監視進度，並取得方法的結果。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法是以同步方式執行，它會在成功時傳回0。 如果這個方法是以非同步方式執行，它會傳回4096，而作業輸出參數可以用來追蹤非同步作業的進度。 任何其他傳回值表示錯誤。

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

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




