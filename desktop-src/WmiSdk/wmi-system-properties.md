---
description: WindowsManagement Instrumentation (WMI) 會定義一組與類別的所有類別和實例相關聯的系統屬性。
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: WMI 系統屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3471665e2e818037bb831c8d8ab39bbe0d56e01912afb1a3399b4055d3670a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120658"
---
# <a name="wmi-system-properties"></a>WMI 系統屬性

WindowsManagement Instrumentation (WMI) 會定義一組與類別的所有類別和實例相關聯的系統屬性。 和系統類別一樣，系統屬性名稱會以雙底線開頭，與應用程式或提供者所建立的屬性區別，其不能以單一或雙底線開頭。 識別系統屬性的另一種方式是使用 [**IWbemClassObject：： Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) 方法。

系統屬性可以隨時使用，但值可能是 **Null**。 **Null** 表示屬性不會套用至特定物件。 不過，所有類別或實例的所有時間都可能無法使用系統屬性。

## <a name="system-properties"></a>系統屬性

下列清單說明 WMI 系統屬性。 提供的範例取自 [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) 類別的系統屬性，其描述于本主題的底部。

<dl> <dt>

<span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_類**
</dt> <dd>

資料類型： **CIM \_ 字串**

存取類型：實例的唯讀;類別的讀取/寫入

類別的名稱。

範例： Win32 \_ OptionalFeature

</dd> <dt>

<span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_推導**
</dt> <dd>

資料類型： **CIM \_ 字串** 陣列

存取類型：實例和類別的唯讀

目前類別或實例的類別階層。 第一個元素是直屬父類別，下一個是其父系，依此類推。最後一個元素是基類。

範例： {CIM \_ LogicalElement，cim \_ ManagedSystemElement}

</dd> <dt>

<span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_代**
</dt> <dd>

資料類型： **CIM \_ 字串**

存取類型：唯讀

衍生類別或實例的最上層類別名稱。 當此類別或實例為最上層類別時， **\_ \_ 時代** 和 **\_ \_ 類別** 的值相同。

範例： CIM \_ ManagedSystemElement

</dd> <dt>

<span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_屬**
</dt> <dd>

資料類型： **CIM \_ SINT32**

存取類型：唯讀

用來區別類別和實例的值。 此值為類別 (1) 的 **wbem \_ 拼出動植物 \_ 類別** ，以及適用于實例和事件的 **wbem \_ 拼出動植物 \_ 實例** (2) 。

範例：2

</dd> <dt>

<span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_命名 空間**](--namespace.md)
</dt> <dd>

資料類型： **CIM \_ 字串**

存取類型：唯讀

類別或實例的 [*命名空間*](gloss-n.md) 名稱。

範例：根 \\ cimv2

</dd> <dt>

<span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_路徑**
</dt> <dd>

資料類型： **CIM \_ 字串**

存取類型：唯讀

類別或實例的完整路徑，包括伺服器和命名空間。

範例： \\ \\ MyServer \\ 根 \\ cimv2： Win32 \_ OptionalFeature。 Name = "TelnetClient"

</dd> <dt>

<span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_屬性 \_ 計數**
</dt> <dd>

資料類型： **CIM \_ SINT32**

存取類型：唯讀

為類別或實例定義的非系統屬性數目。

範例: 6

</dd> <dt>

<span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**
</dt> <dd>

資料類型： **CIM \_ 字串**

存取類型：唯讀

類別或實例的相對路徑。

範例： Win32 \_ OptionalFeature. Name = "TelnetClient"

</dd> <dt>

<span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_伺服器**
</dt> <dd>

資料類型： **CIM \_ 字串**

存取類型：唯讀

提供類別或實例的伺服器名稱。

範例： MyServer

</dd> <dt>

<span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_超級**
</dt> <dd>

資料類型： **CIM \_ 字串**

存取類型：唯讀

類別或實例的直屬父類別名稱。

範例： CIM \_ LogicalElement

</dd> </dl>

下列 PowerShell 程式碼會抓取 [**Win32 \_ OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) 類別的屬性，其中包括系統屬性。


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



上述程式碼範例會傳回下列內容：


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
