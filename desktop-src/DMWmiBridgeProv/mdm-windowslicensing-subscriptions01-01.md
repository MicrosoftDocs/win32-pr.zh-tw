---
title: MDM_WindowsLicensing_Subscriptions01_01 類別
description: MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01 類別是針對訂用帳戶相關的授權管理案例而設計。
ms.assetid: dc3b7eae-89d3-4e66-a65f-f100e23ea9fd
keywords:
- MDM_WindowsLicensing_Subscriptions01_01 類別
- MDM_WindowsLicensing_Subscriptions01_01 類別，描述
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing_Subscriptions01_01
- MDM_WindowsLicensing_Subscriptions01_01.InstanceID
- MDM_WindowsLicensing_Subscriptions01_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 911c578bd0e3cbc56c61f2cf85438660e8f437b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104939"
---
# <a name="mdm_windowslicensing_subscriptions01_01-class"></a>MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** 類別是針對訂用帳戶相關的授權管理案例而設計。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing_Subscriptions01_01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
  string Name;
};
```

## <a name="members"></a>成員

**MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ WindowsLicensing \_ Subscriptions01 \_ 01** 類別具有這些屬性。

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

識別父節點的名稱。

</dd> <dt>

[名稱](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-name)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/WindowsLicensing"

</dd> <dt>

[狀態](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

