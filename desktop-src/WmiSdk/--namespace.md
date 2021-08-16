---
description: 表示 WMI 命名空間。
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: __Namespace 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 4640570dd834b42652d04262b70ec84fac106d99f463ca22144e28ad388a0937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320766"
---
# <a name="__namespace-class"></a>\_\_Namespace 類別

**\_ \_ Namespace** 系統類別代表 WMI 命名空間。

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>成員

**\_ \_ Namespace** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**\_ \_ Namespace** 類別具有這些屬性。

<dl> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> <dt>

限定詞：索引 [**鍵**](standard-qualifiers.md)
</dt> </dl>

命名空間名稱。

</dd> </dl>

## <a name="remarks"></a>備註

**\_ \_ 命名空間** 類別衍生自沒有屬性的 [**\_ \_ SystemClass**](--systemclass.md)。

您可以使用 **\_ \_ 命名空間** 來識別、建立及刪除您擁有 [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)物件之目前工作命名空間內的子命名空間。 在任何工作的命名空間內建立 **\_ \_ 命名空間** 的新實例，會在工作的命名空間內建立子命名空間。 相反地，刪除 **\_ \_ 命名空間** 的實例會從工作命名空間移除子命名空間。 請注意，刪除子命名空間時，也會刪除其所有的類別和實例。

在任何工作的命名空間內列舉此類別的實例會提供可用的子命名空間。

例如，在 \\ 根命名空間內是 **\_ \_ 命名空間** 的兩個實例。 其中一個屬性設定為 "Default"，另 **一個名稱屬性** 設 **為** "Cimv2"。 這些實例分別代表 \\ 根 \\ 預設值和 \\ 根 \\ cimv2 命名空間。

## <a name="examples"></a>範例

TechNet 資源庫上的[所有 WMI 命名空間](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257)VBScript 範例都會使用遞迴呼叫來列出 \_ \_ 系統上命名空間類別的所有實例。

下列程式碼範例會取出 PowerShell 中的所有命名空間。


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



下列程式碼範例會改善先前的範例，並新增其他資訊。


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |
| 命名空間<br/>                | 所有 WMI 命名空間<br/>  |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**\_\_SystemClass**](--systemclass.md)
</dt> <dt>

[WMI 系統類別](wmi-system-classes.md)
</dt> </dl>

 

 




