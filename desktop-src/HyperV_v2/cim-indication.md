---
description: '\_對於架構物件中的變更、架構物件資料、提供者和檢測所偵測到的事件，CIM 表示是所有相關通知的抽象基類。 CIM 指示的子類別 \_ 代表特定類型的通知。'
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: CIM_Indication 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Indication
- CIM_Indication.IndicationIdentifier
- CIM_Indication.CorrelatedIndications
- CIM_Indication.IndicationTime
- CIM_Indication.PerceivedSeverity
- CIM_Indication.OtherSeverity
- CIM_Indication.IndicationFilterName
- CIM_Indication.SequenceContext
- CIM_Indication.SequenceNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 46b8d50f2e90d9a51c8ffa0b93de9ac16c889340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982386"
---
# <a name="cim_indication-class"></a>CIM \_ 指示類別

**CIM \_** 針對架構物件中的變更、架構物件資料、提供者和檢測所偵測到的事件，其指示是所有通知的抽象基類。 **CIM \_ 指示** 的子類別代表特定類型的通知。

## <a name="syntax"></a>語法

``` syntax
[Indication, Version("2.24.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_Indication : __ExtrinsicEvent
{
  string   IndicationIdentifier;
  string   CorrelatedIndications[];
  datetime IndicationTime;
  uint16   PerceivedSeverity;
  string   OtherSeverity;
  string   IndicationFilterName;
  string   SequenceContext;
  sint64   SequenceNumber;
};
```

## <a name="members"></a>成員

**CIM \_ 指示** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ 指示** 類別具有這些屬性。

<dl> <dt>

**CorrelatedIndications**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。相互關聯的通知 ") ， [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ 表示**。**IndicationIdentifier**") 
</dt> </dl>

陣列，其中包含與這個相關之通知的 **IndicationIdentifier** 值。

</dd> <dt>

**IndicationFilterName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "CIM \_ IndicationFilter.Name" ) 
</dt> </dl>

處理指示之指示篩選準則的識別碼。 傳送服務會設定這個屬性。 這個屬性會與 **CIM \_ IndicationFilter** 物件的 **Name** 屬性相互關聯。 **IndicationFilterName** 的值應使用下列格式：

-   *<OrgID>*:*<LocalID>*
-   *<OrgID>* 必須包含擁有該物件之商務實體所擁有的受著作權、商標或唯一名稱。
-   *<OrgID>* 不得包含冒號 (： ) 
-   *<LocalID>* 擁有物件之商務實體所選擇的唯一識別碼。

</dd> <dt>

**IndicationIdentifier**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。通知識別碼 ") 
</dt> </dl>

指示的識別碼。 這個屬性可用來作為 **CorrelatedIndications** 屬性陣列中的索引鍵值。 因此， **IndicationIdentifier** 應該是這個類別實例命名空間內的唯一值。

若要確保 **IndicationIdentifier** 是唯一的，應該使用下列格式：

-   *<OrgID>*:*<LocalID>*
-   *<OrgID>* 必須包含擁有該物件之商務實體所擁有的受著作權、商標或唯一名稱。
-   *<OrgID>* 不得包含冒號 (： ) 
-   *<LocalID>* 擁有物件之商務實體所選擇的唯一識別碼。
-   針對 DMTF 定義的實例， *<OrgID>* 應該設為 "CIM"。

</dd> <dt>

**IndicationTime**
</dt> <dd> <dl> <dt>

資料類型： **datetime**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指示的建立時間和日期。 如果建立指示的實體無法判斷這項資訊，則屬性可以設定為 **Null** 。

> [!Note]  
> **IndicationTime** 值對於快速連續產生的指示而言可能相同。

 

</dd> <dt>

**OtherSeverity**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( "[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**") 
</dt> </dl>

當 **PerceivedSeverity** 設為 "1" (其他) 時，來自通知者觀點的指示嚴重性。

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "建議。 ITU \| X733。察覺嚴重性」 ) 
</dt> </dl>

來自通知者觀點的指示嚴重性。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**未知** 的 (0) 


</dt> <dd>

已知的指示嚴重性不明或不定。

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**其他** (1) 


</dt> <dd>

表示可以在 **OtherSeverity** 屬性中找到嚴重性的值。

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**資訊** (2) 


</dt> <dd>

提供資訊性回應時應使用資訊。

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**降級/警告** (3) 


</dt> <dd>

如果適合讓使用者決定是否需要採取動作，則應該使用。

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**次要** (4) 


</dt> <dd>

需要採取動作，但這次的情況並不嚴重。

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**主要** (5) 


</dt> <dd>

現在需要採取動作。

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (6) 


</dt> <dd>

現在需要採取動作，而範圍很廣泛 (可能會導致重要資源的即將中斷) 。

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**嚴重/** 無法恢復 (7) 


</dt> <dd>

發生錯誤，但太晚採取補救動作。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** ( .。。) 


</dt> <dd></dd> </dl>

</dd> <dt>

**SequenceCoNtext**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 指示**」。**SequenceNumber**") 
</dt> </dl>

指示之序列識別碼的序列內容。 如果服務不支援指示的序列識別碼，這個屬性應該設為 **Null**。 如果重新傳遞指示，這個屬性會維持不變。

> [!Note]  
> 當服務嘗試 redeliver 指示、重新排列未按順序抵達的指示，以及偵測遺失的指示時，指示的序列識別碼可讓接聽程式識別重複的指示。

 

若要確保 **SequenceCoNtext** 是唯一的，應該使用下列格式：

-   *指示-服務-名稱* \#*cim-服務-開始-識別碼* \#接聽 *程式-目的地建立時間*
-   *指示-服務-名稱* 是可傳遞指示之 **CIM \_ IndicationService** 實例的 **名稱** 屬性值。
-   *cim-服務-開始-* 識別碼是唯一識別服務啟動作業的識別碼。 例如，這可能是開始時間的時間戳記，或每次啟動或重新開機服務時增加的計數器。
-   接聽 *程式-目的地建立時間* 是 **CIM \_ ListenerDestination** 實例建立時間的時間戳記，代表接聽程式目的地。 nSince 此格式只是建議，CIM 用戶端應將值視為順序內容的不透明識別碼，且不應依賴此格式。

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

資料類型： **sint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「**CIM \_ 指示**」。**SequenceCoNtext**") 
</dt> </dl>

指示之序列識別碼的序號。

> [!Note]  
> 當服務嘗試 redeliver 指示、重新排列未按順序抵達的指示，以及偵測遺失的指示時，指示的序列識別碼可讓接聽程式識別重複的指示。

 

序號具有下列特性：

-   每當 **SequenceCoNtext** 值變更時，序號就會重設為 "0"。
-   每當接聽程式目的地收到新的指示時，序號就會增加為 "1"。
-   當超過值範圍時，序號會換行為 "0"。
-   如果重新傳遞指示， **SequenceNumber** 會維持不變。

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

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

