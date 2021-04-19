---
description: Win32 \_ VideoSettings 關聯 WMI 類別會將可以套用的影片控制器和影片設定產生關聯。
ms.assetid: 0cc42352-0a89-434d-a8b6-230c677de49c
ms.tgt_platform: multiple
title: Win32_VideoSettings 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_VideoSettings
- Win32_VideoSettings.Setting
- Win32_VideoSettings.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 38e949b6b6501dc51b39448d72e6bf61f37fbecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970713"
---
# <a name="win32_videosettings-class"></a>Win32 \_ VideoSettings 類別

**Win32 \_ VideoSettings** 關聯 [WMI 類別](../wmisdk/retrieving-a-class.md)會將可以套用的影片控制器和影片設定產生關聯。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{1008CCEE-7BFF-11D2-AAD2-006008C78BC7}"), AMENDMENT]
class Win32_VideoSettings : CIM_VideoSetting
{
  CIM_VideoControllerResolution REF Setting;
  Win32_VideoController         REF Element;
};
```

## <a name="members"></a>成員

**Win32 \_ VideoSettings** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Win32 \_ VideoSettings** 類別具有這些屬性。

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

資料類型： **Win32 \_ VideoController**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Key**](../wmisdk/key-qualifier.md)、 [**Override**](../wmisdk/standard-qualifiers.md) ( "Element" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "WMI \| Win32 \_ VideoController" ) 
</dt> </dl>

[**Win32 \_ VideoController**](win32-videocontroller.md) ，其中包含可用於影片設定的影片控制器屬性。

</dd> <dt>

**設定**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ VideoControllerResolution**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](../wmisdk/key-qualifier.md)、覆 [**寫**](../wmisdk/standard-qualifiers.md) ( "設定" ) 、 [**MappingStrings**](../wmisdk/standard-qualifiers.md) ( "cim \| CIM \_ VideoControllerResolution" ) 
</dt> </dl>

[**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) ，包含可套用至視訊控制器的設定。

</dd> </dl>

## <a name="remarks"></a>備註

**Win32 \_ VideoSettings** 類別衍生自 [**CIM \_ VideoSetting**](cim-videosetting.md)。

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

[**CIM \_ VideoSetting**](cim-videosetting.md)
</dt> <dt>

[電腦系統硬體類別](computer-system-hardware-classes.md)
</dt> </dl>

 

 
