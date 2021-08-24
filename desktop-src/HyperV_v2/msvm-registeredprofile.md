---
description: 描述一組具有必要屬性和方法的類別，這些類別具有必要的屬性和方法，需要用來管理真實世界的實體，或以互通的方式支援使用案例。
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Msvm_RegisteredProfile 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0773ad1b7c992211e8bc578ac2cf2bea7706313918581ef2da9df8e2887b536d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535768"
---
# <a name="msvm_registeredprofile-class"></a>Msvm \_ RegisteredProfile 類別

描述一組具有必要屬性和方法的類別，這些類別具有必要的屬性和方法，需要用來管理真實世界的實體，或以互通的方式支援使用案例。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a>成員

**Msvm \_ RegisteredProfile** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ RegisteredProfile** 類別具有這些屬性。

<dl> <dt>

**AdvertiseTypeDescriptions**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

提供與 **AdvertiseType** 屬性相關之其他資訊的字串陣列。 當 **AdvertiseType** 是 1 (其他) 時，必須提供描述。 這個陣列中的專案會對應至 **AdvertiseTypes** 陣列中的相同索引。 這個屬性繼承自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。

</dd> <dt>

**AdvertiseTypes**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定設定檔資訊的公告。 WBEM 基礎結構的廣告服務會使用它，透過哪些機制來判斷應公告的內容。 屬性是陣列，因此可以使用數種機制來公告設定檔。 如果此屬性為 **Null**，這就相當於指定值 2 (不會) 公告。 這個屬性繼承自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**未公告** (2) 
</dt> <dt>

<span id="SLP_"></span><span id="slp_"></span>**SLP** (3 ) 
</dt> </dl>

</dd> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的簡短描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

對物件的描述。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的顯示名稱。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**、覆 **寫**
</dt> </dl>

可唯一識別這個類別之實例的字串。 這個屬性繼承自 [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)。

</dd> <dt>

**OtherRegisteredOrganization**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 256 ) 
</dt> </dl>

當 **RegisteredOrganization** 包含 1 (其他) 時，提供組織描述的字串。 這個屬性繼承自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。

</dd> <dt>

**RegisteredName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： **MaxLen** ( 256 ) 
</dt> </dl>

這個已註冊設定檔的名稱。 由於相同 **RegisteredName** 可以有多個版本， **RegisteredName**、 **RegisteredOrganization** 和 **RegisteredVersion** 的組合必須在組織範圍內唯一識別已註冊的設定檔。 這個屬性繼承自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。

</dd> <dt>

**RegisteredOrganization**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

定義此設定檔的組織。 這個屬性繼承自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 
</dt> <dt>

<span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2) 
</dt> <dt>

<span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3) 
</dt> <dt>

<span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**服務創新的聯盟** (4) 
</dt> <dt>

<span id="FAST"></span><span id="fast"></span>**FAST** (5) 
</dt> <dt>

<span id="GGF"></span><span id="ggf"></span>**GGF** (6) 
</dt> <dt>

<span id="INTAP"></span><span id="intap"></span>**INTAP** (7) 
</dt> <dt>

<span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8) 
</dt> <dt>

<span id="NAC"></span><span id="nac"></span>**NAC** (9) 
</dt> <dt>

<span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**10 名西北部能源效率聯盟** (10) 
</dt> <dt>

<span id="SNIA"></span><span id="snia"></span>**SNIA** (11) 
</dt> <dt>

<span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**TM 論壇** (12) 
</dt> <dt>

<span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**開啟的群組** (13) 
</dt> <dt>

<span id="ANSI"></span><span id="ansi"></span>**ANSI** (14) 
</dt> <dt>

<span id="IEEE"></span><span id="ieee"></span>**IEEE** (15) 
</dt> <dt>

<span id="IETF"></span><span id="ietf"></span>**IETF** (16) 
</dt> <dt>

<span id="INCITS"></span><span id="incits"></span>**INCITS** (17) 
</dt> <dt>

<span id="ISO"></span><span id="iso"></span>**ISO** (18) 
</dt> <dt>

<span id="W3C"></span><span id="w3c"></span>**W3C** (19) 
</dt> <dt>

<span id="__20___________OGF"></span><span id="__20___________ogf"></span>**20 OGF** (20) 
</dt> <dt>

<span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**綠色方格** (21) 
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF 保留** ( .。。 )
</dt> </dl>

</dd> <dt>

**RegisteredVersion**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此設定檔的版本。 字串的格式必須為： "*M*。*N*。*U*"Where：

-   *M* 是以數值形式 (的主要版本，) 描述設定檔的建立或上次修改。
-   *N* 是以數值形式 (的次要版本，) 描述設定檔的建立或上次修改。
-   *U* 是以數值形式 (的更新，) 描述設定檔的建立或上次修改。

這個屬性繼承自 [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ interop<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

