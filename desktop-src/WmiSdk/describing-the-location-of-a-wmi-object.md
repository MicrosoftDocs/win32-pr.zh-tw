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
# <a name="describing-the-location-of-a-wmi-object"></a><span data-ttu-id="06aa7-103">描述 WMI 物件的位置</span><span class="sxs-lookup"><span data-stu-id="06aa7-103">Describing the Location of a WMI Object</span></span>

<span data-ttu-id="06aa7-104">在概念上類似于統一資源定位器 (URL) ，WMI 物件路徑是一個字串，可唯一識別伺服器上的命名空間、命名空間內的類別，或類別的實例。</span><span class="sxs-lookup"><span data-stu-id="06aa7-104">Conceptually similar to a Uniform Resource Locator (URL), a WMI object path is a string that uniquely identifies the namespace on a server, a class within a namespace, or instances of a class.</span></span> <span data-ttu-id="06aa7-105">物件路徑為階層式，且包含數個專案，這些專案會描述有問題之物件的位置。</span><span class="sxs-lookup"><span data-stu-id="06aa7-105">An object path is hierarchical, and contains several elements that describe the location of the object in question.</span></span> <span data-ttu-id="06aa7-106">如同檔案路徑，WMI 物件路徑可以完整描述或指定為相對路徑。</span><span class="sxs-lookup"><span data-stu-id="06aa7-106">Like file paths, WMI object paths can be described in full or specified as a relative path.</span></span>

<span data-ttu-id="06aa7-107">Wmi 物件的命名空間列在 WMI 參考頁面上。</span><span class="sxs-lookup"><span data-stu-id="06aa7-107">The namespace of a WMI object is listed on the WMI reference page.</span></span> <span data-ttu-id="06aa7-108">例如， [CIMWIN32 WMI 提供者](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) 所支援之大部分類別的位置都位於 \\ 根 \\ cimv2 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="06aa7-108">For example, the location of most of the classes supported by the [CIMWin32 WMI Providers](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) are located in the \\root\\cimv2 namespace.</span></span> <span data-ttu-id="06aa7-109">下列 PowerShell 程式碼說明在本機電腦上抓取 [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-computersystem) 系統系統的呼叫：</span><span class="sxs-lookup"><span data-stu-id="06aa7-109">The following PowerShell code describes a call to retrieve the [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) object on your local machine:</span></span>

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

<span data-ttu-id="06aa7-110">或者， [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)的特定實例可能會有 [**SWbemObject \_ 路徑**](swbemobject-path-.md)屬性中的下列路徑。</span><span class="sxs-lookup"><span data-stu-id="06aa7-110">Alternately, a specific instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) may have the following path from the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

<span data-ttu-id="06aa7-111">下列範例會顯示這個實例的相對路徑，如下所示：顯示 [**\_ SWbemObject**](swbemobject-path-.md)的呼叫所傳回之 [**SWbemObjectPath**](swbemobjectpath.md)物件的 [**Relpath**](swbemobjectpath-relpath.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="06aa7-111">The following example shows the relative path to this instance, as seen by displaying the [**Relpath**](swbemobjectpath-relpath.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the call to [**SWbemObject.Path\_**](swbemobject-path-.md).</span></span>

`Win32_LogicalDisk.DeviceID="A:"`

<span data-ttu-id="06aa7-112">請注意， **DeviceID** 是 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) 類別的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="06aa7-112">Note that **DeviceID** is the key property of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

## <a name="c"></a><span data-ttu-id="06aa7-113">C++</span><span class="sxs-lookup"><span data-stu-id="06aa7-113">C++</span></span>

<span data-ttu-id="06aa7-114">下表列出物件路徑類型，以及需要物件路徑的相關方法。</span><span class="sxs-lookup"><span data-stu-id="06aa7-114">The following table lists object path types and the associated methods that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="06aa7-115">物件路徑類型</span><span class="sxs-lookup"><span data-stu-id="06aa7-115">Object path type</span></span></th>
<th><span data-ttu-id="06aa7-116">方法</span><span class="sxs-lookup"><span data-stu-id="06aa7-116">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06aa7-117"><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></span><span class="sxs-lookup"><span data-stu-id="06aa7-117"><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></span></span></td>
<td><dl><span data-ttu-id="06aa7-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices：： OpenNamespace</strong></a></span><span class="sxs-lookup"><span data-stu-id="06aa7-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices::OpenNamespace</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06aa7-119"><a href="describing-a-class-object-path.md">類別</a></span><span class="sxs-lookup"><span data-stu-id="06aa7-119"><a href="describing-a-class-object-path.md">Class</a></span></span></td>
<td><dl><span data-ttu-id="06aa7-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices：： ExecMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="06aa7-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices::ExecMethod</strong></a></span></span><br />
<span data-ttu-id="06aa7-121">[<strong>IWbemServices：： ExecMethodAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) </span><span class="sxs-lookup"><span data-stu-id="06aa7-121">[<strong>IWbemServices::ExecMethodAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06aa7-122"><a href="describing-a-class-object-path.md">類別</a> 或 <a href="describing-an-instance-object-path.md">實例</a></span><span class="sxs-lookup"><span data-stu-id="06aa7-122"><a href="describing-a-class-object-path.md">Class</a> or <a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="06aa7-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices：： GetObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="06aa7-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices::GetObject</strong></a></span></span><br />
<span data-ttu-id="06aa7-124">[<strong>IWbemServices：： GetObjectAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) </span><span class="sxs-lookup"><span data-stu-id="06aa7-124">[<strong>IWbemServices::GetObjectAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06aa7-125"><a href="describing-an-instance-object-path.md">執行個體</a></span><span class="sxs-lookup"><span data-stu-id="06aa7-125"><a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="06aa7-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices：:D eleteInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="06aa7-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::DeleteInstance</strong></a></span></span><br />
<span data-ttu-id="06aa7-127">[<strong>IWbemServices：:D eleteinstanceasync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) </span><span class="sxs-lookup"><span data-stu-id="06aa7-127">[<strong>IWbemServices::DeleteInstanceAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a><span data-ttu-id="06aa7-128">指令碼</span><span class="sxs-lookup"><span data-stu-id="06aa7-128">Script</span></span>

<span data-ttu-id="06aa7-129">您可以透過數種方式來建立物件路徑：</span><span class="sxs-lookup"><span data-stu-id="06aa7-129">Object paths can be constructed in several ways:</span></span>

-   <span data-ttu-id="06aa7-130">取得傳回 [**SWbemObjectPath**](swbemobjectpath.md) 物件之方法的屬性。</span><span class="sxs-lookup"><span data-stu-id="06aa7-130">Retrieve the property of a method that returns an [**SWbemObjectPath**](swbemobjectpath.md) object.</span></span>
-   <span data-ttu-id="06aa7-131">取出 [**SWbemObject。 Path \_**](swbemobject-path-.md)屬性。</span><span class="sxs-lookup"><span data-stu-id="06aa7-131">Retrieve the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>
-   <span data-ttu-id="06aa7-132">建立包含物件路徑的字串變數。</span><span class="sxs-lookup"><span data-stu-id="06aa7-132">Create a string variable that contains the object path.</span></span>

<span data-ttu-id="06aa7-133">下表列出需要物件路徑的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="06aa7-133">The following table lists the scripting objects that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="06aa7-134">腳本物件</span><span class="sxs-lookup"><span data-stu-id="06aa7-134">Scripting object</span></span></th>
<th><span data-ttu-id="06aa7-135">方法</span><span class="sxs-lookup"><span data-stu-id="06aa7-135">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06aa7-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span><span class="sxs-lookup"><span data-stu-id="06aa7-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span></span></td>
<td><dl><span data-ttu-id="06aa7-137"><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a></span><span class="sxs-lookup"><span data-stu-id="06aa7-137"><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a></span></span><br />
<span data-ttu-id="06aa7-138">[<strong>AssociatorsOfAsync</strong>] (swbemservices-associatorsofasync.md) </span><span class="sxs-lookup"><span data-stu-id="06aa7-138">[<strong>AssociatorsOfAsync</strong>](swbemservices-associatorsofasync.md)</span></span><br />
<span data-ttu-id="06aa7-139">[<strong>刪除</strong>] (swbemservices-delete.md) </span><span class="sxs-lookup"><span data-stu-id="06aa7-139">[<strong>Delete</strong>](swbemservices-delete.md)</span></span><br />
<span data-ttu-id="06aa7-140">[<strong>DeleteAsync</strong>] (swbemservices-deleteasync.md) </span><span class="sxs-lookup"><span data-stu-id="06aa7-140">[<strong>DeleteAsync</strong>](swbemservices-deleteasync.md)</span></span><br />
<span data-ttu-id="06aa7-141">[<strong>ExecMethod</strong>] (swbemservices-execmethod.md) </span><span class="sxs-lookup"><span data-stu-id="06aa7-141">[<strong>ExecMethod</strong>](swbemservices-execmethod.md)</span></span><br />
<span data-ttu-id="06aa7-142">[<strong>ExecMethodAsync</strong>] (swbemservices-execmethodasync.md) </span><span class="sxs-lookup"><span data-stu-id="06aa7-142">[<strong>ExecMethodAsync</strong>](swbemservices-execmethodasync.md)</span></span><br />
<span data-ttu-id="06aa7-143">[<strong>Get</strong>] (swbemservices-get.md) </span><span class="sxs-lookup"><span data-stu-id="06aa7-143">[<strong>Get</strong>](swbemservices-get.md)</span></span><br />
<span data-ttu-id="06aa7-144">[<strong>GetAsync</strong>] (swbemservices-getasync.md) </span><span class="sxs-lookup"><span data-stu-id="06aa7-144">[<strong>GetAsync</strong>](swbemservices-getasync.md)</span></span><br />
<span data-ttu-id="06aa7-145">[<strong>ReferencesTo</strong>] (swbemservices-referencesto.md) </span><span class="sxs-lookup"><span data-stu-id="06aa7-145">[<strong>ReferencesTo</strong>](swbemservices-referencesto.md)</span></span><br />
<span data-ttu-id="06aa7-146">[<strong>ReferencesToAsync</strong>] (swbemservices-referencestoasync.md) </span><span class="sxs-lookup"><span data-stu-id="06aa7-146">[<strong>ReferencesToAsync</strong>](swbemservices-referencestoasync.md)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06aa7-147"><a href="swbemobjectset.md"><strong>Swbemobjectset 搭配使用</strong></a></span><span class="sxs-lookup"><span data-stu-id="06aa7-147"><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></span></span></td>
<td><dl><span data-ttu-id="06aa7-148"><a href="swbemobjectset-item.md"><strong>項目</strong></a></span><span class="sxs-lookup"><span data-stu-id="06aa7-148"><a href="swbemobjectset-item.md"><strong>Item</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
