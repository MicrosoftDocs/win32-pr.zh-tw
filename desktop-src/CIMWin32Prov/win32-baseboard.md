---
description: 代表基礎板，也稱為主機板或系統面板。
ms.assetid: 04ac7522-8b99-4ffc-9f7d-d1225f55a862
ms.tgt_platform: multiple
title: Win32_BaseBoard 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseBoard
- Win32_BaseBoard.IsCompatible
- Win32_BaseBoard.Caption
- Win32_BaseBoard.ConfigOptions
- Win32_BaseBoard.CreationClassName
- Win32_BaseBoard.Depth
- Win32_BaseBoard.Description
- Win32_BaseBoard.Height
- Win32_BaseBoard.HostingBoard
- Win32_BaseBoard.HotSwappable
- Win32_BaseBoard.InstallDate
- Win32_BaseBoard.Manufacturer
- Win32_BaseBoard.Model
- Win32_BaseBoard.Name
- Win32_BaseBoard.OtherIdentifyingInfo
- Win32_BaseBoard.PartNumber
- Win32_BaseBoard.PoweredOn
- Win32_BaseBoard.Product
- Win32_BaseBoard.Removable
- Win32_BaseBoard.Replaceable
- Win32_BaseBoard.RequirementsDescription
- Win32_BaseBoard.RequiresDaughterBoard
- Win32_BaseBoard.SerialNumber
- Win32_BaseBoard.SKU
- Win32_BaseBoard.SlotLayout
- Win32_BaseBoard.SpecialRequirements
- Win32_BaseBoard.Status
- Win32_BaseBoard.Tag
- Win32_BaseBoard.Version
- Win32_BaseBoard.Weight
- Win32_BaseBoard.Width
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c4287076a550e25bf74a160b191c777c25d9ab3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026004"
---
# <a name="win32_baseboard-class"></a>Win32 基礎板 \_ 類別

**\_ Win32** 基礎板 [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表一種基礎板，也稱為主機板或系統面板。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B95-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_BaseBoard : CIM_Card
{
  string   Caption;
  string   ConfigOptions[];
  string   CreationClassName;
  real32   Depth;
  string   Description;
  real32   Height;
  boolean  HostingBoard;
  boolean  HotSwappable;
  datetime InstallDate;
  string   Manufacturer;
  string   Model;
  string   Name;
  string   OtherIdentifyingInfo;
  string   PartNumber;
  boolean  PoweredOn;
  string   Product;
  boolean  Removable;
  boolean  Replaceable;
  string   RequirementsDescription;
  boolean  RequiresDaughterBoard;
  string   SerialNumber;
  string   SKU;
  string   SlotLayout;
  boolean  SpecialRequirements;
  string   Status;
  string   Tag;
  string   Version;
  real32   Weight;
  real32   Width;
};
```

## <a name="members"></a>成員

**Win32 基礎 \_** 板類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Win32 基礎 \_** 板類別具有這些方法。



| 方法           | 描述                 |
|:-----------------|:----------------------------|
| **IsCompatible** | 未實作。<br/> |



 

### <a name="properties"></a>屬性

**Win32 基礎 \_** 板類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) 
</dt> </dl>

物件的簡短描述（單行字串）。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**ConfigOptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 12 \| Configuration Options Strings" ) 
</dt> </dl>

代表位於基礎板上的跳線和交換器設定的陣列。

範例： ".JP2：1-2 快取大小為256K，2-3 快取大小為512K，SW1-1：關閉以停用面板影片"

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**CIM \_ 金鑰**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

第一個具象類別的名稱，這個類別會出現在建立實例時所用的繼承鏈中。 當搭配類別的其他索引鍵屬性使用時，屬性允許唯一識別此類別的所有實例和其子類別。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

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

物件的描述。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

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

**HostingBoard**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則表示卡片是主機板或底座中的基礎板。

這個屬性繼承自 [**CIM \_ 卡**](cim-card.md)。

</dd> <dt>

**HotSwappable**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則可以熱交換套件。 如果您可以將專案取代為實體不同但對等的元素，而包含的套件已套用電源（也就是開啟時），則實體封裝可以熱交換。 例如，使用 SCA 連接器插入的磁片磁碟機套件會卸載，而且可以熱交換。 所有可以熱交換的封裝，本質上都是卸載且可取代的。

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

物件的安裝日期和時間。 這個屬性不需要值來表示已安裝物件。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**製造商**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

負責產生實體元素的組織名稱。

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

已知實體元素的名稱。

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

已知物件的標籤。 子類別化時，可以將屬性覆寫為索引鍵屬性。

這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。

</dd> <dt>

**OtherIdentifyingInfo**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

會捕捉資產標籤資訊以外的其他資料，可用來識別實體元素。 其中一個範例是與也有資產標記的專案相關聯的條碼資料。 請注意，如果只有條碼資料可供使用，而且是唯一的或可作為專案索引鍵，則屬性值會是 **Null** ，而條碼資料會在標記屬性中當做類別機碼使用。

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

若 **為 TRUE**，則表示實體元素已開啟電源。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**產品**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SMBIOS \| Type 2 \| Product" ) 
</dt> </dl>

製造商所定義的基礎板零件編號。

</dd> <dt>

**移動**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則會卸載套件。 如果實體封裝的設計目的是要將它放入和移出實體容器（通常是在不因而影響整體封裝的函式的情況下找到），則會卸載。 如果電源必須關閉才能執行移除，則套件仍可以卸載。 如果電源可以開啟且封裝已移除，則該元素會卸載，而且可以熱交換。 例如，膝上型電腦中的額外電池會卸載，也就是使用 SCA 連接器插入的磁片磁碟機套件。 不過，後者也可以熱交換。 膝上型電腦的顯示器不是可移動的，也不是 nonredundant 電源供應器。 移除這些元件會影響整體封裝的功能，或由於封裝的緊密整合而無法進行。

這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。

</dd> <dt>

**更換**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則可替換套件。 如果可以更換 (FRU 或升級) 具有實體不同的元素，則可以更換實體套件。 例如，某些電腦系統可讓主要處理器晶片升級為較高的頻率分級之一。 在此情況下，即表示處理器被視為可更換。 另一個範例是掛接在滑動滑軌上的電源供應器套件。 所有卸載式套件本質上都是可取代的。

這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalpackage.md)。

</dd> <dt>

**RequirementsDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 卡**](cim-card.md)」。**SpecialRequirements**") 
</dt> </dl>

描述此卡片與其他卡片實際獨特之方式的自由格式字串。 當對應的布林值屬性 **SpecialRequirements** 設為 **TRUE** 時，屬性才有意義。

這個屬性繼承自 [**CIM \_ 卡**](cim-card.md)。

</dd> <dt>

**RequiresDaughterBoard**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

若 **為 TRUE**，則至少需要一個 daughterboard 或輔助卡才能正常運作。

這個屬性繼承自 [**CIM \_ 卡**](cim-card.md)。

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

**SKU**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

實體元素的庫存單位號碼。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**SlotLayout**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述位置位置、一般使用方式、限制、個別位置間距或卡片上任何其他相關資訊的自由格式字串。

這個屬性繼承自 [**CIM \_ 卡**](cim-card.md)。

</dd> <dt>

**SpecialRequirements**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「[**CIM \_ 卡**](cim-card.md)」。**RequirementsDescription**") 
</dt> </dl>

若 **為 TRUE**，則這張卡片與相同類型的其他卡片實際上是唯一的，因此需要特殊的位置。 例如，雙卡片需要兩個插槽。 另一個範例是，特定卡片可用於與其他卡片相同的一般功能，但需要特殊插槽 (例如，額外的長) ，而其他卡片則可以放置在任何可用的位置。 如果設定為 **TRUE**，則對應的屬性 **RequirementsDescription** 應該指定卡片唯一性或用途的本質。

這個屬性繼承自 [**CIM \_ 卡**](cim-card.md)。

</dd> <dt>

**狀態**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) 
</dt> </dl>

物件的目前狀態。 您可以定義各種操作和 nonoperational 狀態。 作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。 Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。 後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。 並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。

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

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 、覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Tag" ) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "WMI" ) 
</dt> </dl>

系統基礎板的唯一識別碼。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

範例：「基本板」

</dd> <dt>

**版本**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

實體元素的版本。

這個屬性繼承自 [**CIM \_ PhysicalElement**](cim-physicalelement.md)。

</dd> <dt>

**Weight**
</dt> <dd> <dl> <dt>

資料類型： **real32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「磅」 ) 
</dt> </dl>

實體套件的加權（以磅為單位）。

這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalelement.md)。

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

這個屬性繼承自 [**CIM \_ PhysicalPackage**](cim-physicalelement.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 基礎 \_** 板類別衍生自 cim [**\_ 卡**](cim-card.md)，這是從 [**cim \_ PhysicalPackage**](cim-physicalelement.md)衍生的。

## <a name="examples"></a>範例

[列出電腦](https://Gallery.TechNet.Microsoft.Com/932346d8-4a23-4dac-bdbd-01fc14d526f8)基礎板屬性 Perl 範例會傳回電腦基礎板的相關資訊。

[列出電腦](https://Gallery.TechNet.Microsoft.Com/359772a2-c70e-45e9-bdad-f79efe2420a9)基礎板屬性 PowerShell 範例會傳回電腦基礎板的相關資訊。

下列 VBScript 範例也會傳回電腦基礎板的相關資訊。


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colItems = objWMIService.ExecQuery("Select * from Win32_BaseBoard") 
 
For Each objItem in colItems 
    For Each strOption in objItem.ConfigOptions 
        Wscript.Echo "Configuration Option: " & strOption 
    Next 
    Wscript.Echo "Depth: " & objItem.Depth 
    Wscript.Echo "Description: " & objItem.Description 
    Wscript.Echo "Height: " & objItem.Height 
    Wscript.Echo "Hosting Board: " & objItem.HostingBoard 
    Wscript.Echo "Hot Swappable: " & objItem.HotSwappable 
    Wscript.Echo "Manufacturer: " & objItem.Manufacturer 
    Wscript.Echo "Model: " & objItem.Model 
    Wscript.Echo "Name: " & objItem.Name 
    Wscript.Echo "Other Identifying Information: " & _ 
        objItem.OtherIdentifyingInfo 
    Wscript.Echo "Part Number: " & objItem.PartNumber 
    Wscript.Echo "Powered-On: " & objItem.PoweredOn 
    Wscript.Echo "Product: " & objItem.Product 
    Wscript.Echo "Removable: " & objItem.Removable 
    Wscript.Echo "Replaceable: " & objItem.Replaceable 
    Wscript.Echo "Requirements Description: " & objItem.RequirementsDescription 
    Wscript.Echo "Requires Daughterboard: " & objItem.RequiresDaughterBoard 
    Wscript.Echo "Serial Number: " & objItem.SerialNumber 
    Wscript.Echo "SKU: " & objItem.SKU 
    Wscript.Echo "Slot Layout: " & objItem.SlotLayout 
    Wscript.Echo "Special Requirements: " & objItem.SpecialRequirements 
    Wscript.Echo "Tag: " & objItem.Tag 
    Wscript.Echo "Version: " & objItem.Version 
    Wscript.Echo "Weight: " & objItem.Weight 
    Wscript.Echo "Width: " & objItem.Width 
Next 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 卡片**](cim-card.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

