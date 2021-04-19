---
description: 當事件傳遞給它時，以任意指令碼語言執行預先定義的腳本。
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: ActiveScriptEventConsumer 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActiveScriptEventConsumer
- ActiveScriptEventConsumer.CreatorSID
- ActiveScriptEventConsumer.KillTimeout
- ActiveScriptEventConsumer.MachineName
- ActiveScriptEventConsumer.MaximumQueueSize
- ActiveScriptEventConsumer.Name
- ActiveScriptEventConsumer.ScriptingEngine
- ActiveScriptEventConsumer.ScriptFileName
- ActiveScriptEventConsumer.ScriptText
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 11e2886fd5d0804946433e102e24617df768dcec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997892"
---
# <a name="activescripteventconsumer-class"></a>ActiveScriptEventConsumer 類別

當事件傳遞給它時， **ActiveScriptEventConsumer** 類別會以任意指令碼語言執行預先定義的腳本。 此類別是 WMI 提供的其中一個標準事件取用者。 如需詳細資訊，請參閱 [使用標準取用者監視及回應事件](monitoring-and-responding-to-events-with-standard-consumers.md)。


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



您可以在 **ScriptingStandardConsumerSetting** 的單一實例中設定 [**Timeout**](scriptingstandardconsumersetting.md)或 **MaximumScripts** 屬性的值，以設定系統上所有 **ActiveScriptEventConsumer** 實例的效能。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class ActiveScriptEventConsumer : __EventConsumer
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  uint32 KillTimeout = 0;
  string MachineName;
  uint32 MaximumQueueSize;
  string Name;
  string ScriptingEngine;
  string ScriptFileName;
  string ScriptText;
};
```

## <a name="members"></a>成員

**ActiveScriptEventConsumer** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**ActiveScriptEventConsumer** 類別具有這些屬性。

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

資料類型： **uint8** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

陣列，代表 (SID) 的安全識別碼，該識別碼可唯一識別作用中腳本事件取用者的建立者。 這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

允許腳本執行的數目（以秒為單位）。 如果 0 (零) （預設值），則腳本不會終止。

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

WMI 傳送事件的目標電腦名稱稱。 依照 Microsoft 標準取用者的慣例，腳本取用者無法從遠端執行。 協力廠商取用者也可以使用此屬性。 這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

動態指令碼事件取用者的最大佇列（以位元組為單位）。 這個屬性繼承自 [**\_ \_ EventConsumer**](--eventconsumer.md)。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](standard-qualifiers.md)
</dt> </dl>

事件取用者的唯一識別碼。 如果您重新命名取用者，結果會是兩個具有不同名稱的相同取用者。

</dd> <dt>

**ScriptFileName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

用來讀取腳本文字之檔案的名稱，目的是在 **ScriptText** 屬性中指定腳本文字的替代方案。 如果 **ScriptText** 屬性不是 **null**，則這個屬性必須是 **null** 。

> [!Note]  
> 當您指定 **ScriptFileName** 時，請務必保護您正在啟動的可執行檔。 如果可執行檔不在安全的位置，或使用強式存取控制清單來保護 (ACL) ，任何人都可以使用不同的可執行檔來取代該可執行檔。 如需 Acl 的詳細資訊，請參閱 [在 c + + 中為新物件建立安全描述項 (SD) ](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--)。

 

</dd> <dt>

**ScriptingEngine**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要使用的腳本引擎名稱，例如「VBScript」。 這個屬性不能是 **Null**。

</dd> <dt>

**ScriptText**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

腳本的文字，以腳本引擎已知的語言表示。 如果 **ScriptFileName** 屬性不是 **null**，則這個屬性必須是 **null** 。

</dd> </dl>

## <a name="remarks"></a>備註

這個類別衍生自 [**\_ \_ EventConsumer**](--eventconsumer.md)抽象類別。 它位於根訂用帳戶 \\ 命名空間中。

當「事件取用者」實例中指定腳本的文字時，腳本就可以存取腳本環境變數 **TargetEvent** 中的事件實例。

腳本會在 LocalSystem 安全性內容中執行。 做為安全性措施，只有本機系統管理員或網域系統管理員可以設定腳本取用者。 在執行時間之前不會檢查存取權限。 當取用者設定好之後，任何使用者都可以觸發引發腳本的事件。

無法載入腳本引擎或剖析和驗證腳本會視為失敗。 從腳本傳回錯誤碼，並使用超時來終止腳本，也會視為失敗。

**ScriptText** 或 **ScriptFileName** 不能是 **Null**。 如果這兩個屬性都是 **null** 或 not **null**，則會產生錯誤。

當 WMI 以服務的形式執行時，由 **ActiveScriptEventConsumer** 執行的腳本不會產生螢幕輸出。 使用 **MsgBox** 的腳本會執行，但不會在螢幕上顯示資訊。 不支援執行 WMI 服務作為可執行檔，但 WMI 允許使用 **MsgBox** 函數的腳本顯示輸出或接受使用者輸入。 [Wscript.echo](/previous-versions//at5ydy31(v=vs.85))物件提供的方法都不能使用，因為 **ActiveScriptEventConsumer** 不會使用 WINDOWS Script Host (WSH) 。

## <a name="examples"></a>範例

在 TechNet 資源庫上 [建立永久性 Wmi 事件註冊來監視](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) 檔案 PowerShell 範例使用 **ActiveScriptEventConsumer** 做為複雜字集的一部分，以設定永久的 wmi 事件註冊。

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

[標準取用者類別](standard-consumer-classes.md)
</dt> <dt>

[根據事件執行腳本](running-a-script-based-on-an-event.md)
</dt> <dt>

[隨時接收事件](receiving-events-at-all-times.md)
</dt> <dt>

[建立邏輯取用者](creating-a-logical-consumer.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md)
</dt> </dl>

 

