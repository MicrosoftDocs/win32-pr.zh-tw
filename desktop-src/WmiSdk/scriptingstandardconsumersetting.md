---
description: Singleton ScriptingStandardConsumerSetting 類別提供 ActiveScriptEventConsumer 標準取用者類別的所有實例通用的註冊資料。
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: ScriptingStandardConsumerSetting 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 43eae14eea445f546f731605c94b38e770b08691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192073"
---
# <a name="scriptingstandardconsumersetting-class"></a>ScriptingStandardConsumerSetting 類別

Singleton **ScriptingStandardConsumerSetting** 類別提供 [**ActiveScriptEventConsumer**](activescripteventconsumer.md) 標準取用者類別的所有實例通用的註冊資料。 **ActiveScriptEventConsumer** 實例會使用 **MaximumScripts** 和 **Timeout** 屬性。 如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a>成員

**ScriptingStandardConsumerSetting** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ScriptingStandardConsumerSetting** 類別具有這些屬性。

<dl> <dt>

**標題**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](standard-qualifiers.md) (64) 
</dt> </dl>

物件的簡短描述（一行字串）。 包含字串 **ScriptingStandardConsumerSetting** ，因為這是單一類別。

</dd> <dt>

**說明**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

物件的文字描述。

</dd> <dt>

**MaximumScripts**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

取用者啟動新實例之前所執行的腳本數目上限。 若要清除腳本的記憶體流失，請定期關閉取用者。 預設值為 300。

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MaxLen**](standard-qualifiers.md) (256) 
</dt> </dl>

設定物件的識別碼。

</dd> <dt>

**逾時**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞： [**單位**](standard-qualifiers.md) ( "分鐘" ) 
</dt> </dl>

取用者啟動新實例之前的最大分鐘數。 如果 0 (零) ， **MaximumScripts** 屬性會控制取用者存留期。 **Timeout** 的有效範圍是0到71000，預設值是 0 (零) 。

</dd> </dl>

## <a name="remarks"></a>備註

**ScriptingStandardConsumerSetting** 類別的單一實例位於根 \\ cimv2 命名空間中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                               |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                         |
| 命名空間<br/>                | 根 \\ 訂用帳戶<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Scrcons mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scrcons.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 設定**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[標準取用者類別](standard-consumer-classes.md)
</dt> <dt>

[根據事件執行腳本](running-a-script-based-on-an-event.md)
</dt> <dt>

[建立邏輯取用者](creating-a-logical-consumer.md)
</dt> <dt>

[隨時接收事件](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

