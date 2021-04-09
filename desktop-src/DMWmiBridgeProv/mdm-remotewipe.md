---
title: MDM_RemoteWipe 類別
description: MDM \_ RemoteWipe 類別允許遠端抹除裝置。
ms.assetid: 8c7c8705-8694-4ce3-ba21-ca610fe1f547
keywords:
- MDM_RemoteWipe 類別
- MDM_RemoteWipe 類別，描述
topic_type:
- apiref
api_name:
- MDM_RemoteWipe
- MDM_RemoteWipe.InstanceID
- MDM_RemoteWipe.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ece626fca573e34cf938105f5e59b61e0585fd3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024629"
---
# <a name="mdm_remotewipe-class"></a>MDM \_ RemoteWipe 類別

\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。 Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]

**MDM \_ RemoteWipe** 類別允許遠端抹除裝置。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_RemoteWipe
{
  string InstanceID;
  string ParentID;
};
```

## <a name="members"></a>成員

**MDM \_ RemoteWipe** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MDM \_ RemoteWipe** 類別具有這些方法。



| 方法                                              | 描述                                              |
|:----------------------------------------------------|:---------------------------------------------------------|
| [**doWipeMethod**](mdm-remotewipe-dowipemethod.md) | 觸發裝置以啟動遠端清除。<br/> |



 

### <a name="properties"></a>屬性

**MDM \_ RemoteWipe** 類別具有這些屬性。

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 [**鍵**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

識別父節點的名稱。 此類別的字串為 "RemoteWipe"。

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

## <a name="example"></a>範例

下列範例示範如何使用 RemoteWipe 並叫用 doWipeMethod。

> [!Note]  
> 這個範例必須在本機系統使用者下執行。 若要這樣做，請從 <https://technet.microsoft.com/sysinternals/bb897553.aspx> `psexec.exe -i -s cmd.exe` 已提升許可權的系統管理命令提示字元中下載 psexec 工具，然後執行。

 

``` syntax
$namespaceName = "root\cimv2\mdm\dmmap"
$className = "MDM_RemoteWipe"
$methodName = "doWipeMethod"

$session = New-CimSession

$params = New-Object Microsoft.Management.Infrastructure.CimMethodParametersCollection
$param = [Microsoft.Management.Infrastructure.CimMethodParameter]::Create("param", "", "String", "In")
$params.Add($param)

try
{
    $instance = Get-CimInstance -Namespace $namespaceName -ClassName $className -Filter "ParentID='./Vendor/MSFT' and InstanceID='RemoteWipe'"
    $session.InvokeMethod($namespaceName, $instance, $methodName, $params)
}
catch [Exception]
{
    write-host $_ | out-string
}
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                      |
| 命名空間<br/>                | 根 \\ CIMv2 \\ MDM \\ DMMap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 PowerShell 指令碼搭配 WMI 橋接器提供者](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

