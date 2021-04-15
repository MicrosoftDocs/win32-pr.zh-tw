---
title: MDM_AssignedAccess 類別
description: MDM \_ >assignedaccess 類別可用來將裝置設定為以 kiosk 模式執行。
ms.assetid: b9837f91-3c13-4a80-bf6d-66d8b53dfa70
keywords:
- MDM_AssignedAccess 類別
- MDM_AssignedAccess 類別，描述
topic_type:
- apiref
api_name:
- MDM_AssignedAccess
- MDM_AssignedAccess.InstanceID
- MDM_AssignedAccess.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b5f03f99183400d4e7672323072415918e8e58e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466880"
---
# <a name="mdm_assignedaccess-class"></a>MDM \_ >assignedaccess 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ >assignedaccess** 類別可用來將裝置設定為以 kiosk 模式執行。 一旦執行類別之後，與 kiosk 模式相關聯的下一個使用者登入，就會將裝置置於執行布建套件中所指定應用程式的 kiosk 模式中。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_AssignedAccess
{
  string InstanceID;
  string ParentID;
  string KioskModeApp;
  string Configuration;
};
```

## <a name="members"></a>成員

**MDM \_ >assignedaccess** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ >assignedaccess** 類別具有這些屬性。

<dl> <dt>

[Configuration](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-configuration)
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

識別父節點的名稱。 此類別的字串為 ">assignedaccess"。

</dd> <dt>

[KioskModeApp](/windows/client-management/mdm/assignedaccess-csp#assignedaccess-kioskmodeapp)
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

描述父節點的完整路徑。 此類別的字串為 "./Vendor/MSFT/"

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

