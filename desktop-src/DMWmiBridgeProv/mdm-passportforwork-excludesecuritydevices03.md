---
title: MDM_PassportForWork_ExcludeSecurityDevices03 類別
description: MDM \_ PassportForWork \_ ExcludeSecurityDevices03 類別會定義可以與商務用 Windows Hello 搭配使用的可信賴平臺模組。
ms.assetid: ca8fba3a-736b-4bd3-ac93-e0d44d54798d
keywords:
- MDM_PassportForWork_ExcludeSecurityDevices03 類別
- MDM_PassportForWork_ExcludeSecurityDevices03 類別，描述
topic_type:
- apiref
api_name:
- MDM_PassportForWork_ExcludeSecurityDevices03
- MDM_PassportForWork_ExcludeSecurityDevices03.InstanceID
- MDM_PassportForWork_ExcludeSecurityDevices03.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5957e42d8df1a6c41ad8c27067119503f9a40034d6133081bc9460afc5c72f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119391368"
---
# <a name="mdm_passportforwork_excludesecuritydevices03-class"></a>MDM \_ PassportForWork \_ ExcludeSecurityDevices03 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

MDM \_ PassportForWork \_ ExcludeSecurityDevices03 類別會定義可以與商務用 Windows Hello 搭配使用的可信賴平臺模組。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_PassportForWork_ExcludeSecurityDevices03
{
  string  InstanceID;
  string  ParentID;
  boolean TPM12;
};
```

## <a name="members"></a>成員

**MDM \_ PassportForWork \_ ExcludeSecurityDevices03** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ PassportForWork \_ ExcludeSecurityDevices03** 類別具有這些屬性。

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

根節點。

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

描述父節點的完整路徑。 如需詳細資訊，請參閱 [PASSPORTFORWORK CSP](/windows/client-management/mdm/passportforwork-csp)。

</dd> <dt>

[TPM12](/windows/client-management/mdm/passportforwork-csp)
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

