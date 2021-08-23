---
description: USB 裝置的管理特性。
ms.assetid: c0589346-7683-49c6-bd34-5ee38d71d00e
title: 'CIM_USBDevice 類別 (Hyper-v 管理) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBDevice
- CIM_USBDevice.USBVersion
- CIM_USBDevice.ClassCode
- CIM_USBDevice.SubclassCode
- CIM_USBDevice.ProtocolCode
- CIM_USBDevice.USBVersionInBCD
- CIM_USBDevice.MaxPacketSize
- CIM_USBDevice.VendorID
- CIM_USBDevice.ProductID
- CIM_USBDevice.DeviceReleaseNumber
- CIM_USBDevice.Manufacturer
- CIM_USBDevice.Product
- CIM_USBDevice.SerialNumber
- CIM_USBDevice.NumberOfConfigs
- CIM_USBDevice.CurrentConfigValue
- CIM_USBDevice.CurrentAlternateSettings
- CIM_USBDevice.CommandTimeout
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3766d6c2fdc46b36350e9259e0e988f3a276cee6376d02de349abbe83bf8031b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119427728"
---
# <a name="cim_usbdevice-class-hyper-v-management"></a>CIM_USBDevice 類別 (Hyper-v 管理) 

USB 裝置的管理特性。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Device::USB")]
class CIM_USBDevice : CIM_LogicalDevice
{
  uint16   USBVersion;
  uint8    ClassCode;
  uint8    SubclassCode;
  uint8    ProtocolCode;
  uint16   USBVersionInBCD;
  uint8    MaxPacketSize;
  uint16   VendorID;
  uint16   ProductID;
  uint16   DeviceReleaseNumber;
  string   Manufacturer;
  string   Product;
  string   SerialNumber;
  uint8    NumberOfConfigs;
  uint8    CurrentConfigValue;
  uint8    CurrentAlternateSettings[];
  datetime CommandTimeout;
};
```

## <a name="members"></a>成員

**CIM \_ USBDevice** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**CIM \_ USBDevice** 類別具有這些方法。



| 方法                                               | 描述                                   |
|:-----------------------------------------------------|:----------------------------------------------|
| [**GetDescriptor**](cim-usbdevice-getdescriptor.md) | 抓取 USB 裝置描述項。<br/> |



 

### <a name="properties"></a>屬性

**CIM \_ USBDevice** 類別具有這些屬性。

<dl> <dt>

**ClassCode**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bDeviceClass」 ) 
</dt> </dl>

USB 類別程式碼。

</dd> <dt>

**CommandTimeout**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

可由支援 USB 重新導向的管理應用程式設定的逾時間隔。 當重新導向服務將 USB 裝置命令重新導向至遠端裝置，而且遠端裝置未在逾時間隔之前回應時，重新導向服務將會模擬 media 退出事件。 此外，服務可能會重新嘗試命令，或嘗試重新建立與遠端裝置的連線。

</dd> <dt>

**CurrentAlternateSettings**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ USBDevice**.**CurrentConfigValue**") 
</dt> </dl>

陣列，其中包含裝置目前設定中每個介面的替代設定。

</dd> <dt>

**CurrentConfigValue**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ USBDevice**.**CurrentAlternateSettings**") 
</dt> </dl>

目前為裝置選取的設定。 如果此值為零，則不會設定裝置。

</dd> <dt>

**DeviceReleaseNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bcdDevice」 ) 
</dt> </dl>

BCD 格式的裝置版本號碼。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| iManufacturer」 ) 
</dt> </dl>

裝置的製造商字串。

</dd> <dt>

**MaxPacketSize**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bMaxPacketSize」 ) 
</dt> </dl>

USB 零端點的封包大小上限。

</dd> <dt>

**NumberOfConfigs**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bNumConfigurations」 ) 
</dt> </dl>

為裝置定義的裝置設定數目。

</dd> <dt>

**產品**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| iProduct」 ) 
</dt> </dl>

裝置的產品字串。

</dd> <dt>

**ProductID**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| idProduct」 ) 
</dt> </dl>

依製造商指派給裝置的產品識別碼。

</dd> <dt>

**ProtocolCode**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bDeviceProtocol」 ) 
</dt> </dl>

USB 通訊協定代碼。

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| iSerialNumber」 ) 
</dt> </dl>

裝置的序號。

</dd> <dt>

**SubclassCode**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bDeviceSubClass」 ) 
</dt> </dl>

USB 子類別程式碼。

</dd> <dt>

**USBVersion**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

USB 裝置支援的最新 USB 版本。 屬性會以二進位編碼的 decimal (BCD) ，其中包含第二和第3位數之間的小數點。 例如，0x201 的值表示支援2.01 版。

</dd> <dt>

**USBVersionInBCD**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| bcdUSB」 ) 
</dt> </dl>

裝置符合的 USB 規格編號。 此屬性的格式為 BCD 格式。

</dd> <dt>

**VendorID**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「通用序列匯流排規格。 USB-如果 \| 標準裝置描述項 \| idVendor」 ) 
</dt> </dl>

依 USB.org 指派給裝置的廠商識別碼。

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

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

