---
description: 在概念上類似于統一資源定位器 (URL) ，WMI 物件路徑是一個字串，可唯一識別伺服器上的命名空間、命名空間內的類別，或類別的實例。
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: 描述 WMI 物件的位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969310"
---
# <a name="describing-the-location-of-a-wmi-object"></a>描述 WMI 物件的位置

在概念上類似于統一資源定位器 (URL) ，WMI 物件路徑是一個字串，可唯一識別伺服器上的命名空間、命名空間內的類別，或類別的實例。 物件路徑為階層式，且包含數個專案，這些專案會描述有問題之物件的位置。 如同檔案路徑，WMI 物件路徑可以完整描述或指定為相對路徑。

Wmi 物件的命名空間列在 WMI 參考頁面上。 例如， [CIMWIN32 WMI 提供者](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) 所支援之大部分類別的位置都位於 \\ 根 \\ cimv2 命名空間中。 下列 PowerShell 程式碼說明在本機電腦上抓取 [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-computersystem) 系統系統的呼叫：

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

或者， [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的特定實例可能會有 [**SWbemObject \_ 路徑**](swbemobject-path-.md)屬性中的下列路徑。

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

下列範例會顯示這個實例的相對路徑，如下所示：顯示 [**\_ SWbemObject**](swbemobject-path-.md)的呼叫所傳回之 [**SWbemObjectPath**](swbemobjectpath.md)物件的 [**Relpath**](swbemobjectpath-relpath.md)屬性。

`Win32_LogicalDisk.DeviceID="A:"`

請注意， **DeviceID** 是 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的索引鍵屬性。

## <a name="c"></a>C++

下表列出物件路徑類型，以及需要物件路徑的相關方法。



<table>
<thead>
<tr class="header">
<th>物件路徑類型</th>
<th>方法</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices：： OpenNamespace</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-a-class-object-path.md">類別</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices：： ExecMethod</strong></a><br />
[<strong>IWbemServices：： ExecMethodAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) <br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="describing-a-class-object-path.md">類別</a> 或 <a href="describing-an-instance-object-path.md">實例</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices：： GetObject</strong></a><br />
[<strong>IWbemServices：： GetObjectAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) <br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-an-instance-object-path.md">執行個體</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices：:D eleteInstance</strong></a><br />
[<strong>IWbemServices：:D eleteinstanceasync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) <br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a>指令碼

您可以透過數種方式來建立物件路徑：

-   取得傳回 [**SWbemObjectPath**](swbemobjectpath.md) 物件之方法的屬性。
-   取出 [**SWbemObject。 Path \_**](swbemobject-path-.md)屬性。
-   建立包含物件路徑的字串變數。

下表列出需要物件路徑的腳本物件。



<table>
<thead>
<tr class="header">
<th>腳本物件</th>
<th>方法</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="swbemservices.md"><strong>SWbemServices</strong></a></td>
<td><dl><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a><br />
[<strong>AssociatorsOfAsync</strong>] (swbemservices-associatorsofasync.md) <br />
[<strong>刪除</strong>] (swbemservices-delete.md) <br />
[<strong>DeleteAsync</strong>] (swbemservices-deleteasync.md) <br />
[<strong>ExecMethod</strong>] (swbemservices-execmethod.md) <br />
[<strong>ExecMethodAsync</strong>] (swbemservices-execmethodasync.md) <br />
[<strong>Get</strong>] (swbemservices-get.md) <br />
[<strong>GetAsync</strong>] (swbemservices-getasync.md) <br />
[<strong>ReferencesTo</strong>] (swbemservices-referencesto.md) <br />
[<strong>ReferencesToAsync</strong>] (swbemservices-referencestoasync.md) <br />
</dl></td>
</tr>
<tr class="even">
<td><a href="swbemobjectset.md"><strong>Swbemobjectset 搭配使用</strong></a></td>
<td><dl><a href="swbemobjectset-item.md"><strong>項目</strong></a><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
