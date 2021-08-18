---
description: 提供 VHD 設定檔案中快照集的相關資訊。
ms.assetid: 922bf0b8-523d-488e-9a41-1a27594e2e44
title: Msvm_VHDSnapshotInformation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VHDSnapshotInformation
- Msvm_VHDSnapshotInformation.FilePath
- Msvm_VHDSnapshotInformation.SnapshotId
- Msvm_VHDSnapshotInformation.SnapshotPath
- Msvm_VHDSnapshotInformation.ParentPathsList
- Msvm_VHDSnapshotInformation.CreationTime
- Msvm_VHDSnapshotInformation.ResilientChangeTrackingId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c256ee2d3fb277fc98fa440403cf385377d7f64160267ff39a2d905c59f9d3ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068448"
---
# <a name="msvm_vhdsnapshotinformation-class"></a>Msvm \_ VHDSnapshotInformation 類別

提供 VHD 設定檔案中快照集的相關資訊

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class Msvm_VHDSnapshotInformation
{
  string   FilePath;
  string   SnapshotId;
  string   SnapshotPath;
  string   ParentPathsList[];
  DATETIME CreationTime;
  string   ResilientChangeTrackingId;
};
```

## <a name="members"></a>成員

**Msvm \_ VHDSnapshotInformation** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VHDSnapshotInformation** 類別具有這些屬性。

<dl> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立此快照集的日期和時間。

</dd> <dt>

**FilePath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

VHD 設定檔案的路徑。

</dd> <dt>

**ParentPathsList**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

檔案路徑的清單，代表這個快照相依的所有檔案。 除非特別要求，否則此欄位將是空的。 第一個專案是檔案的直屬父系，最後一個專案是根目錄。

</dd> <dt>

**ResilientChangeTrackingId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與此快照集相關聯的復原變更追蹤識別碼（如果有的話）。

</dd> <dt>

**SnapshotId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

可在 VHD 設定檔案中唯一識別此快照集的 GUID。

</dd> <dt>

**SnapshotPath**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此快照所表示之檔案的路徑。 如果沒有與此快照集相關聯的檔案，此欄位可能是空的。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




