---
description: CIM \_ MonitorResolution 類別代表水準和垂直解析度之間的關聯性，以及桌面監視器的重新整理頻率和掃描模式。 影片控制器物件中指定了值。
ms.assetid: 064620dd-2d92-42d0-9167-35867830a077
ms.tgt_platform: multiple
title: CIM_MonitorResolution 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MonitorResolution
- CIM_MonitorResolution.Caption
- CIM_MonitorResolution.Description
- CIM_MonitorResolution.SettingID
- CIM_MonitorResolution.HorizontalResolution
- CIM_MonitorResolution.MaxRefreshRate
- CIM_MonitorResolution.MinRefreshRate
- CIM_MonitorResolution.RefreshRate
- CIM_MonitorResolution.ScanMode
- CIM_MonitorResolution.VerticalResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aa1fd025c87b3b497e400351aed91af71bf4958f3ee8748bf5d23255540dc6cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506711"
---
# <a name="cim_monitorresolution-class"></a>CIM \_ MonitorResolution 類別

**CIM \_ MonitorResolution** 類別代表水準和垂直解析度之間的關聯性，以及桌面監視器的重新整理頻率和掃描模式。 影片控制器物件中指定了值。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{1008CCEC-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class CIM_MonitorResolution : CIM_Setting
{
  string Caption;
  string Description;
  string SettingID;
  uint32 HorizontalResolution;
  uint32 MaxRefreshRate;
  uint32 MinRefreshRate;
  uint32 RefreshRate;
  uint16 ScanMode;
  uint32 VerticalResolution;
};
```

## <a name="members"></a>成員

**CIM \_ MonitorResolution** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ MonitorResolution** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) 
</dt> </dl>

目前物件的簡短文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

目前物件的文字描述。

這個屬性繼承自 [**CIM \_ 設定**](cim-setting.md)。

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentHorizontalResolution**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.2 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 圖元 ") 
</dt> </dl>

監視器的水準解析度（以圖元為單位）。

</dd> <dt>

**MaxRefreshRate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**MaxRefreshRate**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.7 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") 
</dt> </dl>

監視器的最大重新整理速率（以赫茲為單位），可在指定的解析度支援速率範圍時使用。

</dd> <dt>

**MinRefreshRate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**MinRefreshRate**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.6 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") 
</dt> </dl>

監視器的最小重新整理速率（以赫茲為單位），可在指定的解析度支援速率範圍時使用。

</dd> <dt>

**RefreshRate**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentRefreshRate**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.4 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 赫茲 ") 
</dt> </dl>

監視的重新整理頻率（以赫茲為單位）。 如果支援的速率範圍，請使用 **MinRefreshRate** 和 **MaxRefreshRate** 屬性，並將此屬性設定為0。

</dd> <dt>

**ScanMode**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentScanMode**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.5 ") 
</dt> </dl>

監視器使用的掃描模式。

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**其他** (1) 


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (2) 


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**不支援** (3) 


</dt> <dd></dd> <dt>

<span id="Non-Interlaced_Operation"></span><span id="non-interlaced_operation"></span><span id="NON-INTERLACED_OPERATION"></span>

 (4) **的非交錯操作**


</dt> <dd></dd> <dt>

<span id="Interlaced_Operation"></span><span id="interlaced_operation"></span><span id="INTERLACED_OPERATION"></span>

**交錯操作** (5) 


</dt> <dd></dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "SettingID" ) ， [**Key**](/windows/desktop/WmiSdk/key-qualifier)， [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256) 
</dt> </dl>

作為目前實例之索引鍵的一部分。

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ VideoController**](cim-videocontroller.md).**CurrentVerticalResolution**") ， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" MIF。DMTF \| 監視器解析度 \| 002.3 ") ， [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) (" 圖元 ") 
</dt> </dl>

監視器的垂直解析度（以圖元為單位）。

</dd> </dl>

## <a name="remarks"></a>備註

WMI 不會執行這個類別。

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

[**CIM \_ 設定**](cim-setting.md)
</dt> </dl>

 

