---
title: MDM_RemoteFind 類別
description: MDM \_ RemoteFind 類別會捕獲特定裝置的位置資訊。
ms.assetid: 8dfbe951-b4ca-4709-bec9-0821571f9b0e
keywords:
- MDM_RemoteFind 類別
- MDM_RemoteFind 類別，描述
topic_type:
- apiref
api_name:
- MDM_RemoteFind
- MDM_RemoteFind.InstanceID
- MDM_RemoteFind.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8930d80ede9daad5c721cd3b226c85e3d9918a19
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685551"
---
# <a name="mdm_remotefind-class"></a>MDM \_ RemoteFind 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ RemoteFind** 類別會捕獲特定裝置的位置資訊。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind
{
  string InstanceID;
  string ParentID;
  sint32 DesiredAccuracy;
  sint32 MaximumAge;
  sint32 Timeout;
};
```

## <a name="members"></a>成員

**MDM \_ RemoteFind** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**MDM \_ RemoteFind** 類別具有這些屬性。

<dl> <dt>

[DesiredAccuracy](/windows/client-management/mdm/remotefind-csp#desiredaccuracy)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
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

識別父節點的名稱。 此類別的字串為 "RemoteFind"。

</dd> <dt>

[MaximumAge](/windows/client-management/mdm/remotefind-csp#maximumage)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
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

</dd> <dt>

[逾時](/windows/client-management/mdm/remotefind-csp#timeout)
</dt> <dd> <dl> <dt>

資料類型： **sint32**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                     |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                       |
| 命名空間<br/>                | 根 \\ CIMv2 \\ MDM \\ DMMap<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

