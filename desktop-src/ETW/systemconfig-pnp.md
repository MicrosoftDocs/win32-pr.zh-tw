---
description: 這個類別是 PnP 事件的事件型別類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 01e9a8bb-3f54-4e20-b4db-1b4bba745d4f
title: SystemConfig_PnP 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_PnP
- SystemConfig_PnP.IDLength
- SystemConfig_PnP.DescriptionLength
- SystemConfig_PnP.FriendlyNameLength
- SystemConfig_PnP.DeviceID
- SystemConfig_PnP.DeviceDescription
- SystemConfig_PnP.FriendlyName
api_type:
- NA
api_location: ''
ms.openlocfilehash: 082d9169bbd2ad30af6b2bc17600804f43ce7bbef5e52f15f7ac4c85b21f7b8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582198"
---
# <a name="systemconfig_pnp-class"></a>SystemConfig \_ PnP 類別

這個類別是 PnP 事件的事件型別類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType(22), EventTypeName("PnP")]
class SystemConfig_PnP : SystemConfig
{
  uint32 IDLength;
  uint32 DescriptionLength;
  uint32 FriendlyNameLength;
  string DeviceID;
  string DeviceDescription;
  string FriendlyName;
};
```

## <a name="members"></a>成員

**SystemConfig \_ PnP** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**SystemConfig \_ PnP** 類別具有這些屬性。

<dl> <dt>

**DescriptionLength**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (2) 
</dt> </dl>

DeviceDescription 字串的長度（以字元為單位）。

</dd> <dt>

**DeviceDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (5) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

PnP 裝置的描述。

</dd> <dt>

**DeviceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (4) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

識別 PnP 裝置。

</dd> <dt>

**FriendlyName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (6) 、StringTermination ( "NullTerminated" ) 、Format ( "w" ) 
</dt> </dl>

要在使用者介面中使用的 PnP 裝置名稱。

</dd> <dt>

**FriendlyNameLength**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (3) 
</dt> </dl>

FriendlyName 字串的長度（以字元為單位）。

</dd> <dt>

**IDLength**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： WmiDataId (1) 
</dt> </dl>

DeviceID 字串的長度（以字元為單位）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>       |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 




