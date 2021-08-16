---
description: 代表已更正的電腦檢查 (CMC) 處理，以從插斷驅動程式切換至輪詢。 此類別僅適用于64位 Windows 系統。
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: MSMCAEvent_SwitchToCMCPolling 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: a8192dc83a50063b2aaabba2bf708053fadb8e094bfa1cab82b11b084f722a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640938"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a>MSMCAEvent \_ SwitchToCMCPolling 類別

**MSMCAEvent \_ SwitchToCMCPolling** 類別代表已更正的電腦檢查 (CMC) 處理，以從插斷驅動程式切換至輪詢。 在某些情況下，核心會輪詢系統抽象層 (SAL) 是否有任何 CMC 或已更正的平臺錯誤 (CPE) 發生在先前輪詢間隔內。 此類別僅適用于64位 Windows 系統。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>成員

**MSMCAEvent \_ SwitchToCMCPolling** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MSMCAEvent \_ SwitchToCMCPolling** 類別具有這些屬性。

<dl> <dt>

**使用中**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果此類別的實例為使用中，則 **為 TRUE**;否則 **為 FALSE**。

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

此類別實例的唯一識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

**MSMCAEvent \_ SwitchToCMCPolling** 類別衍生自 [**>register-wmievent**](wmievent.md)。

系統抽象層 (SAL) 是將程式碼燒錄到作業系統呼叫以執行與平臺相關的作業。 它類似于 x86 平臺上的 BIOS。 如果平臺不支援 CMC 或 CPE 輪詢的中斷，作業系統會每分鐘輪詢一次，檢查先前是否發生錯誤。 如果平臺支援中斷，且作業系統在一分鐘內收到使用者定義的 CMC 或 CPE 輪詢數量，則會停用中斷和輪詢。 如果使用者未在一分鐘內定義投票次數，系統會將預設值設定為每分鐘10個輪詢。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2003<br/>                                                         |
| 命名空間<br/>                | 根 \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSMCA 類別](msmca-classes.md)
</dt> <dt>

[**>register-wmievent**](wmievent.md)
</dt> </dl>

 

