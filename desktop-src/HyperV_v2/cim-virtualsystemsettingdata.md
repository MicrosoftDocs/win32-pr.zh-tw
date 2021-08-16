---
description: 描述虛擬系統透過一組虛擬化特定屬性的虛擬層面。 CIM \_ VirtualSystemSettingData 也可作為虛擬系統組態的最上層類別。
ms.assetid: 501e659d-f190-41f9-aafa-447048a60e7c
title: CIM_VirtualSystemSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingData
- CIM_VirtualSystemSettingData.VirtualSystemIdentifier
- CIM_VirtualSystemSettingData.VirtualSystemType
- CIM_VirtualSystemSettingData.Notes
- CIM_VirtualSystemSettingData.CreationTime
- CIM_VirtualSystemSettingData.ConfigurationID
- CIM_VirtualSystemSettingData.ConfigurationDataRoot
- CIM_VirtualSystemSettingData.ConfigurationFile
- CIM_VirtualSystemSettingData.SnapshotDataRoot
- CIM_VirtualSystemSettingData.SuspendDataRoot
- CIM_VirtualSystemSettingData.SwapFileDataRoot
- CIM_VirtualSystemSettingData.LogDataRoot
- CIM_VirtualSystemSettingData.AutomaticStartupAction
- CIM_VirtualSystemSettingData.AutomaticStartupActionDelay
- CIM_VirtualSystemSettingData.AutomaticStartupActionSequenceNumber
- CIM_VirtualSystemSettingData.AutomaticShutdownAction
- CIM_VirtualSystemSettingData.AutomaticRecoveryAction
- CIM_VirtualSystemSettingData.RecoveryFile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1caed7797343eac9babd320af42fd6c9aaaffeff054211cc55bda0d437582d57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068488"
---
# <a name="cim_virtualsystemsettingdata-class"></a>CIM \_ VirtualSystemSettingData 類別

描述虛擬系統透過一組虛擬化特定屬性的虛擬層面。 **CIM \_VirtualSystemSettingData** 也可作為虛擬系統組態的最上層類別。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.25.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingData : CIM_SettingData
{
  string   VirtualSystemIdentifier;
  string   VirtualSystemType;
  string   Notes[];
  datetime CreationTime;
  string   ConfigurationID;
  string   ConfigurationDataRoot;
  string   ConfigurationFile;
  string   SnapshotDataRoot;
  string   SuspendDataRoot;
  string   SwapFileDataRoot;
  string   LogDataRoot;
  uint16   AutomaticStartupAction;
  datetime AutomaticStartupActionDelay;
  uint16   AutomaticStartupActionSequenceNumber;
  uint16   AutomaticShutdownAction;
  uint16   AutomaticRecoveryAction;
  string   RecoveryFile;
};
```

## <a name="members"></a>成員

**CIM \_ VirtualSystemSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ VirtualSystemSettingData** 類別具有這些屬性。

<dl> <dt>

**AutomaticRecoveryAction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當虛擬系統執行的軟體失敗時，對虛擬系統採取的動作。 這個屬性所解決的失敗只包含主機平臺可偵測的失敗，例如無法中斷的等候狀態條件。

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**無** (2) 


</dt> <dd></dd> <dt>

<span id="Restart"></span><span id="restart"></span><span id="RESTART"></span>

 (3) **重新開機**


</dt> <dd></dd> <dt>

<span id="Revert_to_snapshot"></span><span id="revert_to_snapshot"></span><span id="REVERT_TO_SNAPSHOT"></span>

**還原為 snapshot** (4) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticShutdownAction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當主機關閉時，要對虛擬系統採取的動作。

<dt>

<span id="Turn_Off"></span><span id="turn_off"></span><span id="TURN_OFF"></span>

**關閉** (2) 


</dt> <dd></dd> <dt>

<span id="Save_state"></span><span id="save_state"></span><span id="SAVE_STATE"></span>

**儲存狀態** (3) 


</dt> <dd></dd> <dt>

<span id="Shutdown"></span><span id="shutdown"></span><span id="SHUTDOWN"></span>

**關機** (4) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupAction**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

當主機啟動時，要在虛擬系統上採取的動作。

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**無** (2) 


</dt> <dd></dd> <dt>

<span id="Restart_if_previously_active"></span><span id="restart_if_previously_active"></span><span id="RESTART_IF_PREVIOUSLY_ACTIVE"></span>

**如果先前** 作用中的 (3) 重新開機


</dt> <dd></dd> <dt>

<span id="Always_startup"></span><span id="always_startup"></span><span id="ALWAYS_STARTUP"></span>

**一律啟動** (4) 


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**AutomaticStartupActionDelay**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

啟動動作的延遲。 這個值是 **datetime** 資料類型的間隔變異。

</dd> <dt>

**AutomaticStartupActionSequenceNumber**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

啟動主機系統時，虛擬系統啟用的序號。 較低的數位表示先前的啟用。 如果有一或多個設定顯示相同的值，則序列會相依。 值為 "0" 表示序列與實值相依。

</dd> <dt>

**ConfigurationDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬系統組態相關資訊之目錄的檔案路徑。 這個屬性的格式是以 RFC 2079 為基礎的 URI。

</dd> <dt>

**ConfigurationFile**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬系統組態相關資訊之檔案的相對路徑。 相對路徑會附加至 **ConfigurationDataRoot** 屬性的值。 這個屬性的格式是以 RFC 2079 為基礎的 URI。

</dd> <dt>

**ConfigurationID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬系統組態的唯一識別碼。

> [!Note]  
> **ConfigurationID** 與 **InstanceID** 不同，它是由實作為虛擬系統或虛擬系統組態的實作為指派。 **ConfigurationID** 不是索引鍵，而且一個以上的實例可能會發生相同的值。

 

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

建立虛擬系統組態的日期和時間。

</dd> <dt>

**LogDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬系統記錄檔資訊之目錄的相對檔案路徑。 相對路徑會附加至 **ConfigurationDataRoot** 屬性的值。 這個屬性的格式是以 RFC 2079 為基礎的 URI。

</dd> <dt>

**注意事項**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

陣列，其中包含與虛擬系統相關的使用者提供的附注。

</dd> <dt>

**RecoveryFile**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬系統復原相關資訊之檔案的路徑。 這個屬性的格式是以 RFC 2079 為基礎的 URI。

</dd> <dt>

**SnapshotDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬系統快照相關資訊之目錄的相對路徑。 相對路徑會附加至 **ConfigurationDataRoot** 屬性的值。 這個屬性的格式是以 RFC 2079 為基礎的 URI。

</dd> <dt>

**SuspendDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬系統暫停相關資訊之目錄的相對路徑。 相對路徑會附加至 **ConfigurationDataRoot** 屬性的值。 這個屬性的格式是以 RFC 2079 為基礎的 URI。

</dd> <dt>

**SwapFileDataRoot**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

儲存虛擬系統之交換檔的目錄相對檔案路徑。 相對路徑會附加至 **ConfigurationDataRoot** 屬性的值。 這個屬性的格式是以 RFC 2079 為基礎的 URI。

</dd> <dt>

**VirtualSystemIdentifier**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬化平臺內系統的唯一名稱。 **VirtualSystemIdentifier** 不是指派給虛擬系統內執行之作業系統實例的主機名稱，而是指派給其任何網路埠的 IP 位址或 MAC 位址。

**VirtualSystemIdentifier** 可能包含執行特定的規則，例如簡單模式或在設定 **VirtualSystemIdentifier** 時可由執行所解讀的正則運算式。

</dd> <dt>

**VirtualSystemType**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬系統的類型。

> [!Note]  
> 如果虛擬系統類型不明，此值必須設為 "DMTF： unknown"。

 

這個屬性會使用下列增強型巴克斯格斯格式來格式化 (ABNF) 格式：

vs-type = dmtf-值/其他-組織-值/舊版-值;dmtf-value = "DMTF：" 定義-org "：" org-vs type;其他-org-value = 定義-org "：" org-vs type;

上述 ABNF 格式的值為：

-   *dmtf-值*   ：由 dmtf 定義的屬性值，定義于這個屬性的描述中。
-   *其他-組織-值*   是由 DMTF 以外的商務實體所定義的屬性值，不會在這個屬性的描述中定義。
-   *舊版-值*   是由 DMTF 以外的商務實體所定義的屬性值，而且不會定義在這個屬性的描述中。 允許這些值，但建議在一段時間後淘汰。
-   *定義-org*   ：定義虛擬系統類型之商務實體的識別碼。 它應該包含受著作權、商標或商務實體所擁有的唯一名稱。 它不應該是 "DMTF"，且不能包含冒號。
-   *組織-vs-*   在定義商務實體內輸入虛擬系統類型的識別碼。 它在定義-組織內應該是唯一的。組織型別可以使用 CIM 字串允許的任何字元，但下列除外： U0000-U001F (Unicode C0 控制項) 、U0020 (空間) 、U007F (Unicode C0 控制項) 或 U0080-U009F (Unicode C1 控制項) 。
-   如果需要將值結構組成區段，則應該以單一冒號分隔區段。
-   這個屬性的值應該處理案例區分大小寫。 它們的目的是要以程式設計的方式處理，而不是顯示名稱，而且應該簡短。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




