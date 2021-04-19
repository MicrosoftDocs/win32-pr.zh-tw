---
description: 代表磁帶機的功能和管理。
ms.assetid: 8140fd9a-8a12-43b4-bc61-ec143e5d754c
title: 'CIM_TapeDrive 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TapeDrive
- CIM_TapeDrive.EOTWarningZoneSize
- CIM_TapeDrive.MaxPartitionCount
- CIM_TapeDrive.Padding
- CIM_TapeDrive.MaxRewindTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b92360388b71abcb0b67d30fddea9b4f5ed7920f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981524"
---
# <a name="cim_tapedrive-class-hyper-v-management"></a>CIM_TapeDrive 類別 (Hyper-v 管理) 

代表磁帶機的功能和管理。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.6.0"), UMLPackagePath("CIM::Device::StorageDevices")]
class CIM_TapeDrive : CIM_MediaAccessDevice
{
  uint32 EOTWarningZoneSize;
  uint32 MaxPartitionCount;
  uint32 Padding;
  uint64 MaxRewindTime;
};
```

## <a name="members"></a>成員

**CIM \_ disable-tapedrive** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ disable-tapedrive** 類別具有這些屬性。

<dl> <dt>

**EOTWarningZoneSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) 
</dt> </dl>

指定為「磁帶結尾」之區域的大小（以位元組為單位）。 此區域中的存取會產生「磁帶結束」警告。

</dd> <dt>

**MaxPartitionCount**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

磁帶機的最大分割區計數。

</dd> <dt>

**MaxRewindTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "毫秒" ) ， **PUnit** ( "第 \* 10 ^-3" ) 
</dt> </dl>

以毫秒為單位的時間，從磁帶上的最遠距離點移到一開始。

</dd> <dt>

**填補**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Bytes" ) ， **PUnit** ( "byte" ) 
</dt> </dl>

在磁帶媒體上的區塊之間插入的位元組數目。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)
</dt> </dl>

 

