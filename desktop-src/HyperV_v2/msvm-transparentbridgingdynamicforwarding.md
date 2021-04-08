---
description: 將透明橋接服務連接到動態轉寄專案， (瞭解的 MAC 位址) 。
ms.assetid: CA083F15-1E75-4EB9-BE56-95742181FDAC
title: Msvm_TransparentBridgingDynamicForwarding 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TransparentBridgingDynamicForwarding
- Msvm_TransparentBridgingDynamicForwarding.Antecedent
- Msvm_TransparentBridgingDynamicForwarding.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 01b9d9c752d4781864c07ff24fca5f866a57ae54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943682"
---
# <a name="msvm_transparentbridgingdynamicforwarding-class"></a>Msvm \_ TransparentBridgingDynamicForwarding 類別

將透明橋接服務連接到動態轉寄專案， (瞭解的 MAC 位址) 。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TransparentBridgingDynamicForwarding : CIM_TransparentBridgingDynamicForwarding
{
  Msvm_TransparentBridgingService REF Antecedent;
  Msvm_DynamicForwardingEntry     REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ TransparentBridgingDynamicForwarding** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ TransparentBridgingDynamicForwarding** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ TransparentBridgingService**](msvm-transparentbridgingservice.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

代表透明橋接服務之 [**Msvm \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) 類別實例的參考。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

[**Msvm \_ DynamicForwardingEntry**](msvm-dynamicforwardingentry.md)類別實例的參考，該類別表示轉送資料庫的動態轉送專案。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ TransparentBridgingDynamicForwarding** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ TransparentBridgingDynamicForwarding**](cim-transparentbridgingdynamicforwarding.md)
</dt> <dt>

[**CIM \_ TransparentBridgingDynamicForwarding**](/previous-versions/windows/desktop/clushyperv/cim-transparentbridgingdynamicforwarding)
</dt> </dl>

 

