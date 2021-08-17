---
description: CIM \_ 底座類別代表包含其他元素的實體元素，並提供可定義的功能，例如桌面、處理節點、UPS、磁片或磁帶存放裝置，或這些專案的組合。
ms.assetid: 4c55dbff-bc4a-4cc9-8f34-29636defaa56
ms.tgt_platform: multiple
title: CIM_Chassis 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis
- CIM_Chassis.Caption
- CIM_Chassis.Description
- CIM_Chassis.InstallDate
- CIM_Chassis.Name
- CIM_Chassis.Status
- CIM_Chassis.CreationClassName
- CIM_Chassis.Manufacturer
- CIM_Chassis.Model
- CIM_Chassis.OtherIdentifyingInfo
- CIM_Chassis.PartNumber
- CIM_Chassis.PoweredOn
- CIM_Chassis.SerialNumber
- CIM_Chassis.SKU
- CIM_Chassis.Tag
- CIM_Chassis.Version
- CIM_Chassis.Depth
- CIM_Chassis.Height
- CIM_Chassis.HotSwappable
- CIM_Chassis.Removable
- CIM_Chassis.Replaceable
- CIM_Chassis.Weight
- CIM_Chassis.Width
- CIM_Chassis.AudibleAlarm
- CIM_Chassis.BreachDescription
- CIM_Chassis.CableManagementStrategy
- CIM_Chassis.LockPresent
- CIM_Chassis.SecurityBreach
- CIM_Chassis.ServiceDescriptions
- CIM_Chassis.ServicePhilosophy
- CIM_Chassis.VisibleAlarm
- CIM_Chassis.ChassisTypes
- CIM_Chassis.CurrentRequiredOrProduced
- CIM_Chassis.HeatGeneration
- CIM_Chassis.NumberOfPowerCords
- CIM_Chassis.TypeDescriptions
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 271f01587dc67c14464cfdb06de321d853b8b9a606a99cb1aca8fdcb0ff2ca17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835033"
---
# <a name="cim_chassis-class"></a>CIM \_ 底座類別

**CIM \_ 底座** 類別代表包含其他元素的實體元素，並提供可定義的功能，例如桌面、處理節點、UPS、磁片或磁帶存放裝置，或這些專案的組合。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[abstract, UUID("{FAF76B72-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Chassis : CIM_PhysicalFrame
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   Manufacturer;
  string   Model;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   SerialNumber;
  string   SKU;
  string   Tag;
  string   Version;
  real32   Depth;
  real32   Height;
  boolean  HotSwappable;
  boolean  Removable;
  boolean  Replaceable;
  real32   Weight;
  real32   Width;
  boolean  AudibleAlarm;
  string   BreachDescription;
  string   CableManagementStrategy;
  boolean  LockPresent;
  uint16   SecurityBreach;
  string   ServiceDescriptions[];
  uint16   ServicePhilosophy[];
  boolean  VisibleAlarm;
  uint16   ChassisTypes[];
  sint16   CurrentRequiredOrProduced;
  uint16   HeatGeneration;
  uint16   NumberOfPowerCords;
  string   TypeDescriptions[];
};
```

## <a name="members"></a>成員

**CIM \_ 底座** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**CIM \_ 底座** 類別有這些方法。



| 方法                                                           | 描述                                                                                                                                      |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IsCompatible**](iscompatible-method-in-class-cim-chassis.md) | 確認參考的實體元素是否可包含或插入實體封裝中。 不是由 WMI 所執行。<br/> |



 

### <a name="properties"></a>屬性

**CIM \_ 底座** 類別具有這些屬性。

<dl> <dt>

**AudibleAlarm**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則框架具有可聽見的警示。

這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。

</dd> <dt>

**BreachDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ PhysicalFrame**](cim-physicalframe.md).**SecurityBreach**") 
</dt> </dl>

提供詳細資訊的自由格式字串，如果 **SecurityBreach** 屬性指出發生缺口或某些其他安全性相關事件，則會提供更多資訊。

這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。

</dd> <dt>

**CableManagementStrategy**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

自由格式的字串，其中包含有關如何連接及配套框架的各種纜線的相關資訊。 使用許多網路、儲存體相關和電源線，纜線管理可能是複雜且富有挑戰性的工作。 此字串屬性包含的資訊可協助框架的元件和服務。

這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) 
</dt> </dl>

物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**ChassisTypes**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) ， [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) (」 MIF。DMTF \| 實體容器 Global Table \| 002.1 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ 底座**。**TypeDescriptions**") 
</dt> </dl>

列舉的整數值陣列，指出底座的類型。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd>

其他。

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (2) 


</dt> <dd>

未知。

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**桌面** (3) 


</dt> <dd>

桌上型電腦。

</dd> <dt>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>

<span id="Low_Profile_Desktop"></span><span id="low_profile_desktop"></span><span id="LOW_PROFILE_DESKTOP"></span>**低設定檔桌面** (4) 


</dt> <dd>

低設定檔桌面。

</dd> <dt>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>

<span id="Pizza_Box"></span><span id="pizza_box"></span><span id="PIZZA_BOX"></span>**比薩 Box** (5) 


</dt> <dd>

比薩方塊。

</dd> <dt>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>

<span id="Mini_Tower"></span><span id="mini_tower"></span><span id="MINI_TOWER"></span>**迷你塔式** (6) 


</dt> <dd>

迷你塔式。

</dd> <dt>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>

<span id="Tower"></span><span id="tower"></span><span id="TOWER"></span>**塔** (7) 


</dt> <dd>

[立式]：

</dd> <dt>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>

<span id="Portable"></span><span id="portable"></span><span id="PORTABLE"></span>**便攜** (8) 


</dt> <dd>

可擕式。

</dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**膝上型電腦** (9) 


</dt> <dd>

[膝上型電腦]：

</dd> <dt>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>

<span id="Notebook"></span><span id="notebook"></span><span id="NOTEBOOK"></span>**筆記本** (10) 


</dt> <dd>

筆記本。

</dd> <dt>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>

<span id="Hand_Held"></span><span id="hand_held"></span><span id="HAND_HELD"></span>**保留** (11) 


</dt> <dd>

掌上型。

</dd> <dt>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>

<span id="Docking_Station"></span><span id="docking_station"></span><span id="DOCKING_STATION"></span>**銜接站** (12) 


</dt> <dd>

銜接站。

</dd> <dt>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>

<span id="All_in_One"></span><span id="all_in_one"></span><span id="ALL_IN_ONE"></span>**全都在一個** (13) 


</dt> <dd>

全部-一。

</dd> <dt>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>

<span id="Sub_Notebook"></span><span id="sub_notebook"></span><span id="SUB_NOTEBOOK"></span>**子筆記本** (14) 


</dt> <dd>

Subnotebook.

</dd> <dt>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>

<span id="Space-Saving"></span><span id="space-saving"></span><span id="SPACE-SAVING"></span>**節省空間** (15) 


</dt> <dd>

節省空間。

</dd> <dt>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span>

<span id="Lunch_Box"></span><span id="lunch_box"></span><span id="LUNCH_BOX"></span> (16) **午餐箱**


</dt> <dd>

飯盒。

</dd> <dt>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>

<span id="Main_System_Chassis"></span><span id="main_system_chassis"></span><span id="MAIN_SYSTEM_CHASSIS"></span>**主要系統底座** (17) 


</dt> <dd>

主要系統底座。

</dd> <dt>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>

<span id="Expansion_Chassis"></span><span id="expansion_chassis"></span><span id="EXPANSION_CHASSIS"></span>**擴充底座** (18) 


</dt> <dd>

擴充底座。

</dd> <dt>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>

<span id="SubChassis"></span><span id="subchassis"></span><span id="SUBCHASSIS"></span>**SubChassis** (19) 


</dt> <dd>

Subchassis.

</dd> <dt>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>

<span id="Bus_Expansion_Chassis"></span><span id="bus_expansion_chassis"></span><span id="BUS_EXPANSION_CHASSIS"></span>**匯流排擴充底座** (20) 


</dt> <dd>

匯流排-擴充底座。

</dd> <dt>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>

<span id="Peripheral_Chassis"></span><span id="peripheral_chassis"></span><span id="PERIPHERAL_CHASSIS"></span>**週邊底座** (21) 


</dt> <dd>

週邊底座。

</dd> <dt>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>

<span id="Storage_Chassis"></span><span id="storage_chassis"></span><span id="STORAGE_CHASSIS"></span>**儲存體底座** (22) 


</dt> <dd>

儲存體主機殼。

</dd> <dt>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>

<span id="Rack_Mount_Chassis"></span><span id="rack_mount_chassis"></span><span id="RACK_MOUNT_CHASSIS"></span>**機架掛接底座** (23) 


</dt> <dd>

機架掛接底座。

</dd> <dt>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>

<span id="Sealed-Case_PC"></span><span id="sealed-case_pc"></span><span id="SEALED-CASE_PC"></span>**Sealed-CASE PC** (24) 


</dt> <dd>

密封的案例電腦。

</dd> </dl>

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

建立實例時所使用之類別或子類別的名稱。 搭配類別的其他索引鍵屬性使用時，此屬性可讓類別和其子類別的所有實例都能唯一識別。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**CurrentRequiredOrProduced**
</dt> <dd> <dl> <dt>

資料類型： **sint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "安培 at 120 伏特" ) 
</dt> </dl>

目前，底座的120伏要求。 如果電源是由底座提供 (就像在 UPS) 的情況下，此屬性可能會指出產生的 amperage 為負數。

</dd> <dt>

**深度**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) 
</dt> </dl>

實體套件的深度（以英寸為單位）。

這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) 
</dt> </dl>

物件的文字描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**HeatGeneration**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每小時 BTU」 ) 
</dt> </dl>

底座在 Btu/小時內產生的熱度數量。

</dd> <dt>

**高度**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) 
</dt> </dl>

實體封裝的高度（以英寸為單位）。

這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則可以熱交換套件。 如果專案可由實體不同的 (取代，但在包含套件開啟時) 一個，則實體封裝可以熱交換。 例如，風扇元件可能會設計為熱交換。 所有可以熱交換的元件都是可卸載和取代的。

這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") 
</dt> </dl>

指出物件的安裝時間。 缺少值並不表示物件未安裝。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**LockPresent**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則會使用鎖定來保護框架。

這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

負責產生實體元素的組織名稱。 如需詳細資訊，請參閱 [**CIM \_ 產品**](cim-product.md)的 **廠商** 屬性。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**型號**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

實體元素一般已知的名稱。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) 
</dt> </dl>

已知物件的標籤。 子類別化時，可以將這個屬性覆寫為索引鍵屬性。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**NumberOfPowerCords**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

必須連接到底座才能操作所有元件的電源線數目。

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

除了資產標記資訊以外的其他資料，可用來識別實體元素。 其中一個範例是與專案相關聯的橫條程式碼資料，也有一個資產標記。 請注意，如果只有條碼資料可用，而且是唯一的，而且可以當做專案索引鍵使用，則這個屬性會是 null，而條碼資料會當做 **標記** 屬性中的類別索引鍵使用。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**PartNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

負責產生或製造實體元素的組織所指派的元件編號。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**PoweredOn**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則表示實體元素已開啟電源。 否則，它目前為關閉狀態。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**移動**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則會將封裝設計成在通常找到它的實體容器中取出，而不會因而影響整體封裝的功能。 即使電源必須關閉才能執行移除，套件仍會被視為可移動。 如果電源可以開啟且封裝已移除，則該元素會卸載，而且可以熱交換。 例如，「可升級處理器」晶片是卸載式的。

這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。

</dd> <dt>

**更換**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則可以使用實體不同的元素來取代專案。 例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。 在此情況下，即表示處理器被視為可更換。 所有卸載式元件本身都可取代。

這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。

</dd> <dt>

**SecurityBreach**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 實體容器 Global Table \| 002.12 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ PhysicalFrame**](cim-physicalframe.md)。**BreachDescription**") 
</dt> </dl>

指出是否嘗試執行框架的實體缺口，但不成功或嘗試成功。

這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="No_Breach"></span><span id="no_breach"></span><span id="NO_BREACH"></span>

**無缺口** (3) 


</dt> <dd></dd> <dt>

<span id="Breach_Attempted"></span><span id="breach_attempted"></span><span id="BREACH_ATTEMPTED"></span>

 (4) **嘗試缺口**


</dt> <dd></dd> <dt>

<span id="Breach_Successful"></span><span id="breach_successful"></span><span id="BREACH_SUCCESSFUL"></span>

**缺口成功** (5) 


</dt> <dd></dd> </dl>

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

製造商配置的數位，用來識別實體元素。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**ServiceDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ PhysicalFrame**](cim-physicalframe.md)。**ServicePhilosophy**") 
</dt> </dl>

提供 **ServicePhilosophy** 陣列中專案詳細說明的自由格式字串。

> [!Note]  
> 這個陣列的每個專案都與 **ServicePhilosophy** 陣列中位於相同索引的專案有關。

 

這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。

</dd> <dt>

**ServicePhilosophy**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ PhysicalFrame**](cim-physicalframe.md)。**ServiceDescriptions**") 
</dt> </dl>

指出框架是否從頂端、前端、背面或側邊提供服務;以及是否有滑動的紙匣或卸載式邊，以及是否有可移動的框架 (例如，有滾筒) 。

這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Service_From_Top"></span><span id="service_from_top"></span><span id="SERVICE_FROM_TOP"></span>

**從 Top** (2) 的服務


</dt> <dd></dd> <dt>

<span id="Service_From_Front"></span><span id="service_from_front"></span><span id="SERVICE_FROM_FRONT"></span>

前 (3) **的服務**


</dt> <dd></dd> <dt>

<span id="Service_From_Back"></span><span id="service_from_back"></span><span id="SERVICE_FROM_BACK"></span>

**從背面** (4) 的服務


</dt> <dd></dd> <dt>

<span id="Service_From_Side"></span><span id="service_from_side"></span><span id="SERVICE_FROM_SIDE"></span>

**服務從側** (5) 


</dt> <dd></dd> <dt>

<span id="Sliding_Trays"></span><span id="sliding_trays"></span><span id="SLIDING_TRAYS"></span>

**滑動紙** 匣 (6) 


</dt> <dd></dd> <dt>

<span id="Removable_Sides"></span><span id="removable_sides"></span><span id="REMOVABLE_SIDES"></span>

**可移動側** (7) 


</dt> <dd></dd> <dt>

<span id="Moveable"></span><span id="moveable"></span><span id="MOVEABLE"></span>

**可移動** (8) 


</dt> <dd></dd> </dl>

</dd> <dt>

**SKU**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

此實體元素的庫存單位號碼。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) 
</dt> </dl>

表示物件目前狀態的字串。 您可以定義操作和非運作狀態。 操作狀態可以包含「確定」、「降級」和「Pred 失敗」。 「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。

非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。 「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

包括下列值：

<dt>

<span id="OK"></span><span id="ok"></span>

**確定** ( [確定] ) 


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**錯誤** ( 「錯誤」 ) 


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**降級** ( 「降級」 ) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 ( 「未知」 ) 


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred 失敗** ( 「Pred 失敗」 ) 


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**開始** ( 「開始」 ) 


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**停止** ( 「正在停止」 ) 


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**服務** ( 「服務」 ) 


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**壓力** ( 「壓力」 ) 


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ( "NonRecover" ) 


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**沒有連絡人** ( 「沒有連絡人」 ) 


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**遺失的 comm** ( 「遺失的通訊」 ) 


</dt> <dd></dd> </dl>

</dd> <dt>

**Tag**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

可唯一識別實體元素，並作為專案的索引鍵。 這個屬性可包含資產標記或序號資料等資訊。 在物件階層中， [**CIM \_ PhysicalElement**](cim-physicalelement.md) 的金鑰會放在物件階層中很高的位置，以獨立識別硬體或實體，而不論 (中的實體位置或) 的封包、介面卡等等。 例如，可進行熱交換的可移動元件可以從其包含 (範圍) 套件，並暫時未使用。 物件仍會持續存在，甚至可以插入至不同的範圍容器。 實體元素的索引鍵是任一字元串，此字串不會與位置或位置導向階層分開定義。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**TypeDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Indexed" ) ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "**CIM \_ 底座**.**ChassisTypes**") 
</dt> </dl>

提供 **ChassisTypes** 陣列專案相關資訊之自由格式字串的陣列。

> [!Note]  
> 每個陣列專案都與 **ChassisTypes** 屬性中的專案相關，該專案位於相同的索引處。

 

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

指出實體元素的版本。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**VisibleAlarm**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，表示設備包含可見的警示。

這個屬性繼承自 [**CIM \_ PhysicalFrame**](cim-physicalframe.md)。

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「磅」 ) 
</dt> </dl>

實體封裝的加權（以磅為單位）。

這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。

</dd> <dt>

**寬度**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "英寸" ) 
</dt> </dl>

實體套件的寬度（以英寸為單位）。

這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ 底座** 類別衍生自 [**cim \_ PhysicalFrame**](cim-physicalframe.md)。

WMI 不會執行這個類別。 如需衍生自 **CIM \_ 底座** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ PhysicalFrame**](cim-physicalframe.md)
</dt> </dl>

 

