---
description: Msvm_WiFiDeviceSAPImplementation 類別-服務存取點 (SAP) 與其執行方式之間的關聯。
ms.assetid: d1d99299-f2d9-4025-a48d-cf8180f2f7af
title: Msvm_WiFiDeviceSAPImplementation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiDeviceSAPImplementation
- Msvm_WiFiDeviceSAPImplementation.Antecedent
- Msvm_WiFiDeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 99826ce3a37e19867cef1a6ddf276f5136b21a3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109246"
---
# <a name="msvm_wifidevicesapimplementation-class"></a>Msvm \_ WiFiDeviceSAPImplementation 類別

服務存取點之間的關聯 (SAP) 與其如何實行。 此關聯的基數為多對多。 SAP 可由一個以上的邏輯裝置提供，並結合運作。 任何裝置都可以提供一個以上的 SAP。 當有許多邏輯裝置與單一 SAP 相關聯時，會假設這些專案會一起運作以提供存取點。 如果有不同的 SAP 執行，則每個執行都會導致 SAP 物件的個別具現化。 這些個別的具現化會與唯一的實作為關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiDeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  Msvm_WiFiPort     REF Antecedent;
  Msvm_WiFiEndpoint REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ WiFiDeviceSAPImplementation** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ WiFiDeviceSAPImplementation** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ WiFiPort**](msvm-wifiport.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

代表邏輯裝置之 [**Msvm \_ WiFiPort**](msvm-wifiport.md) 類別的實例。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ WiFiEndpoint**](msvm-wifiendpoint.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

[**Msvm \_ WiFiEndpoint**](msvm-wifiendpoint.md)類別的實例，代表使用邏輯裝置所執行的服務存取點。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

