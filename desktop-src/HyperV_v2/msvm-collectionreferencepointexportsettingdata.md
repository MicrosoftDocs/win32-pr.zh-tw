---
description: 將設定資料匯出為傳入 Msvm CollectionReferencePointService 類別的 ExportReferencePoint 方法 \_ 。
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Msvm_CollectionReferencePointExportSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e5b3513fd30035283a6b4dc305f2768b85cb7e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985068"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a>Msvm \_ CollectionReferencePointExportSettingData 類別

將設定資料匯出為傳入 [**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)類別的 [**ExportReferencePoint**](msvm-collectionreferencepointservice-exportreferencepoint.md)方法。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a>成員

**Msvm \_ CollectionReferencePointExportSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ CollectionReferencePointExportSettingData** 類別具有這些屬性。

<dl> <dt>

**BaseReferencePointCollection**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

[**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md)實例的路徑，代表要用於差異匯出的基底參考點集合。

</dd> <dt>

**VirtualMachinesToDisksToExport**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： **HyperVEmbeddedInstance** ( "Msvm \_ VirtualMachineToDisks" ) 
</dt> </dl>

需要匯出資料的「VirtualMachines 至 DisksToExport」對應資訊的清單。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




