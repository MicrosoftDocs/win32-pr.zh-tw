---
description: 定義提供者和它所提供的計數器。
ms.assetid: 85299b01-5679-40f8-8aec-5c2ff8d7cfc8
title: 提供者複雜類型
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6eec52139710d0ffafe06f22504a735e59312818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849280"
---
# <a name="provider-complex-type"></a><span data-ttu-id="b3d79-103">提供者複雜類型</span><span class="sxs-lookup"><span data-stu-id="b3d79-103">provider Complex Type</span></span>

<span data-ttu-id="b3d79-104">定義提供者和它所提供的計數器。</span><span class="sxs-lookup"><span data-stu-id="b3d79-104">Defines a provider and the counters that it provides.</span></span>

``` syntax
<xs:complexType name="provider">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="counterSet"
            type="man:counterSet"
        >
            <xs:key name="uniqueCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@id"
                 />
            </xs:key>
            <xs:unique name="uniqueCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:unique>
            <xs:keyref name="existBaseID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@baseID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfTimeID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfTimeID"
                 />
            </xs:keyref>
            <xs:keyref name="existPerfFreqID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@perfFreqID"
                 />
            </xs:keyref>
            <xs:keyref name="existMultiCounterID">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@multiCounterID"
                 />
            </xs:keyref>
            <xs:key name="uniqueStructNames">
                <xs:selector
                    xpath="./man:structs/man:struct"
                 />
                <xs:field
                    xpath="@name"
                 />
            </xs:key>
            <xs:keyref name="existCounterName">
                <xs:selector
                    xpath="./man:counter"
                 />
                <xs:field
                    xpath="@struct"
                 />
            </xs:keyref>
        </xs:element>
    </xs:choice>
    <xs:attribute name="symbol"
        type="man:CSymbolType"
        use="optional"
     />
    <xs:attribute name="callback"
        use="optional"
        default="default"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="custom"
                 />
                <xs:enumeration
                    value="default"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerGuid"
        type="man:GUIDType"
        use="required"
     />
    <xs:attribute name="applicationIdentity"
        type="xs:string"
        use="required"
     />
    <xs:attribute name="providerType"
        use="optional"
        default="userMode"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="userMode"
                 />
                <xs:enumeration
                    value="kernelMode"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="providerName"
        type="xs:string"
        use="optional"
        default="Counters"
     />
    <xs:attribute name="resourceBase"
        type="man:UInt32Type"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b3d79-105">子元素</span><span class="sxs-lookup"><span data-stu-id="b3d79-105">Child elements</span></span>



| <span data-ttu-id="b3d79-106">元素</span><span class="sxs-lookup"><span data-stu-id="b3d79-106">Element</span></span>        | <span data-ttu-id="b3d79-107">類型</span><span class="sxs-lookup"><span data-stu-id="b3d79-107">Type</span></span>                                                                   | <span data-ttu-id="b3d79-108">Description</span><span class="sxs-lookup"><span data-stu-id="b3d79-108">Description</span></span>                                                                                 |
|----------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3d79-109">**counterSet**</span><span class="sxs-lookup"><span data-stu-id="b3d79-109">**counterSet**</span></span> | [<span data-ttu-id="b3d79-110">**男人： counterSet**</span><span class="sxs-lookup"><span data-stu-id="b3d79-110">**man:counterSet**</span></span>](performance-counters-counterset-complex-type.md) | <span data-ttu-id="b3d79-111">識別包含一或多個邏輯相關計數器的計數器集合。</span><span class="sxs-lookup"><span data-stu-id="b3d79-111">Identifies the counter set that contains one or more logically related counters.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="b3d79-112">屬性</span><span class="sxs-lookup"><span data-stu-id="b3d79-112">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3d79-113">名稱</span><span class="sxs-lookup"><span data-stu-id="b3d79-113">Name</span></span></th>
<th><span data-ttu-id="b3d79-114">類型</span><span class="sxs-lookup"><span data-stu-id="b3d79-114">Type</span></span></th>
<th><span data-ttu-id="b3d79-115">Description</span><span class="sxs-lookup"><span data-stu-id="b3d79-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3d79-116">applicationIdentity</span><span class="sxs-lookup"><span data-stu-id="b3d79-116">applicationIdentity</span></span></td>
<td><span data-ttu-id="b3d79-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="b3d79-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="b3d79-118">包含當地語系化資源字串（.exe 或 .dll 檔案）的二進位檔案名稱 (不包含二進位) 的路徑。</span><span class="sxs-lookup"><span data-stu-id="b3d79-118">The name of the binary file that contains the localized resource strings, either an .exe or .dll file (do not include the path to the binary).</span></span><br/> <span data-ttu-id="b3d79-119">Lodctr.exe 公用程式會使用選擇性 [<em>path</em>] 參數的路徑來搜尋二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="b3d79-119">The Lodctr.exe utility uses the path from the optional [<em>path</em>] parameter to search for the binary file.</span></span> <span data-ttu-id="b3d79-120">例如， <strong>lodctr</strong> [<strong>/m：</strong><em>manifest</em> [<em>path</em>]]。</span><span class="sxs-lookup"><span data-stu-id="b3d79-120">For example, <strong>lodctr</strong> [<strong>/m:</strong><em>manifest</em> [<em>path</em>]].</span></span> <span data-ttu-id="b3d79-121">如果您未包含 [<em>path</em>] 參數，Lodctr.exe 會搜尋包含資訊清單的資料夾。</span><span class="sxs-lookup"><span data-stu-id="b3d79-121">If you do not include the [<em>path</em>] parameter, Lodctr.exe searches the folder that contains the manifest.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3d79-122">回撥</span><span class="sxs-lookup"><span data-stu-id="b3d79-122">callback</span></span></td>

<td><span data-ttu-id="b3d79-123">這個屬性指出當取用者執行某些動作時，您想要收到通知。</span><span class="sxs-lookup"><span data-stu-id="b3d79-123">This attribute indicates that you want to receive notification when a consumer performs certain actions.</span></span> <br/> <span data-ttu-id="b3d79-124">如果您包含這個屬性，CTRPP 工具會使用替代的 <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> 函式簽章，您可以使用此簽章來傳遞函式的名稱，以執行 <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> 回呼函式。</span><span class="sxs-lookup"><span data-stu-id="b3d79-124">If you include this attribute, the CTRPP tool uses the alternate <a href="counterinitialize.md"><strong>CounterInitialize</strong></a> function signature, which you use to pass in the name of your function that implements the <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span><br/> <span data-ttu-id="b3d79-125">除了指定此屬性之外，您還可以使用 <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> 引數。</span><span class="sxs-lookup"><span data-stu-id="b3d79-125">As an alternative to specifying this attribute, you can use the <strong>-NotificationCallback</strong><a href="ctrpp.md">CTRPP</a> argument.</span></span><br/> <span data-ttu-id="b3d79-126"><strong>Windows Vista：</strong> 這個屬性唯一有效的值為 &quot; custom &quot; 。</span><span class="sxs-lookup"><span data-stu-id="b3d79-126"><strong>Windows Vista:</strong> The only valid value for this attribute is &quot;custom&quot;.</span></span> <span data-ttu-id="b3d79-127"><a href="ctrpp.md">CTRPP</a>公用程式會產生<a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a>回呼函數的範本。</span><span class="sxs-lookup"><span data-stu-id="b3d79-127">The <a href="ctrpp.md">CTRPP</a> utility generates the template for a <a href="/windows/desktop/api/Perflib/nc-perflib-perflibrequest"><strong>ControlCallback</strong></a> callback function.</span></span> <span data-ttu-id="b3d79-128">範本會包含在 CTRPP 產生的 .c 檔案中。</span><span class="sxs-lookup"><span data-stu-id="b3d79-128">The template is included in the .c file that CTRPP generated.</span></span> <br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3d79-129">providerGuid</span><span class="sxs-lookup"><span data-stu-id="b3d79-129">providerGuid</span></span></td>
<td><span data-ttu-id="b3d79-130"><a href="performance-counters-guidtype-simple-type.md"><strong>男人： GUIDType</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3d79-130"><a href="performance-counters-guidtype-simple-type.md"><strong>man:GUIDType</strong></a></span></span></td>
<td><span data-ttu-id="b3d79-131">可在資訊清單中唯一識別提供者的字串 GUID。</span><span class="sxs-lookup"><span data-stu-id="b3d79-131">String GUID that uniquely identifies the provider in the manifest.</span></span> <span data-ttu-id="b3d79-132">GUID 在資訊清單中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="b3d79-132">The GUID must be unique within the manifest.</span></span><br/> <span data-ttu-id="b3d79-133">只有 (當您支援) 的並存安裝時，您才需要提供新的 GUID。</span><span class="sxs-lookup"><span data-stu-id="b3d79-133">You need to provide a new GUID only when the version of the application changes (if you support side-by-side installations).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3d79-134">providerName</span><span class="sxs-lookup"><span data-stu-id="b3d79-134">providerName</span></span></td>
<td><span data-ttu-id="b3d79-135"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="b3d79-135"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="b3d79-136">用來建立 WMI Win32_PerfRawData 類別名稱的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3d79-136">The name that is used to create the WMI Win32_PerfRawData class name.</span></span> <span data-ttu-id="b3d79-137">如果您未指定名稱，則 &quot; &quot; 會使用計數器作為類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3d79-137">If you do not specify a name, &quot;Counters&quot; is used as the name of the class.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3d79-138">providerType</span><span class="sxs-lookup"><span data-stu-id="b3d79-138">providerType</span></span></td>

<td><span data-ttu-id="b3d79-139">識別提供者是否為使用者模式提供者、核心模式提供者或驅動程式提供者。</span><span class="sxs-lookup"><span data-stu-id="b3d79-139">Identifies whether the provider is a user-mode provider, kernel-mode provider, or driver provider.</span></span> <span data-ttu-id="b3d79-140">可能的值如下。</span><span class="sxs-lookup"><span data-stu-id="b3d79-140">Possible values are as follows.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3d79-141">詞彙</span><span class="sxs-lookup"><span data-stu-id="b3d79-141">Term</span></span></th>
<th><span data-ttu-id="b3d79-142">描述</span><span class="sxs-lookup"><span data-stu-id="b3d79-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3d79-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode</span><span class="sxs-lookup"><span data-stu-id="b3d79-143"><span id="userMode"></span><span id="usermode"></span><span id="USERMODE"></span>userMode</span></span><br/></td>
<td><span data-ttu-id="b3d79-144">為使用者模式元件指定此模式，例如應用程式、DLL 或使用者模式驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b3d79-144">Specify this mode for a user-mode component such as an application, a DLL, or a user-mode driver.</span></span> <span data-ttu-id="b3d79-145">使用者模式元件的一般擴充功能為 .exe 或 .dll。</span><span class="sxs-lookup"><span data-stu-id="b3d79-145">The typical extensions for user-mode components are .exe or .dll.</span></span> <span data-ttu-id="b3d79-146">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="b3d79-146">This is the default.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3d79-147"><span id="kernel"></span><span id="KERNEL"></span>內核</span><span class="sxs-lookup"><span data-stu-id="b3d79-147"><span id="kernel"></span><span id="KERNEL"></span>kernel</span></span><br/></td>
<td><span data-ttu-id="b3d79-148">為核心模式元件指定此模式，例如 WDM 或 WDF 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="b3d79-148">Specify this mode for a kernel-mode component such as a WDM or WDF driver.</span></span> <span data-ttu-id="b3d79-149">核心模式元件的一般延伸模組是 sys。</span><span class="sxs-lookup"><span data-stu-id="b3d79-149">The typical extension for kernel-mode components is .sys.</span></span><br/> <span data-ttu-id="b3d79-150"><strong>Windows Vista 和 Windows Server 2008：</strong> 在 Windows 7 和 Windows Server 2008 R2 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="b3d79-150"><strong>Windows Vista and Windows Server 2008:</strong> This value is not supported until Windows 7 and Windows Server 2008 R2.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3d79-151">resourceBase</span><span class="sxs-lookup"><span data-stu-id="b3d79-151">resourceBase</span></span></td>
<td><span data-ttu-id="b3d79-152"><a href="performance-counters-uint32type-simple-type.md"><strong>男人： UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3d79-152"><a href="performance-counters-uint32type-simple-type.md"><strong>man:UInt32Type</strong></a></span></span></td>
<td><p><span data-ttu-id="b3d79-153">定義 <a href="ctrpp.md">CTRPP</a> 用來產生資源識別碼的起始資源索引值。</span><span class="sxs-lookup"><span data-stu-id="b3d79-153">Defines the starting resource index value that <a href="ctrpp.md">CTRPP</a> uses to generate the resource identifiers.</span></span></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3d79-154">符號</span><span class="sxs-lookup"><span data-stu-id="b3d79-154">symbol</span></span></td>
<td><span data-ttu-id="b3d79-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>男人： CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="b3d79-155"><a href="performance-counters-csymboltype-simple-type.md"><strong>man:CSymbolType</strong></a></span></span></td>
<td><p><span data-ttu-id="b3d79-156">識別提供者的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="b3d79-156">A symbolic name that identifies the provider.</span></span> <span data-ttu-id="b3d79-157"><a href="ctrpp.md">CTRPP</a>工具會建立控制碼變數，您可以在呼叫需要提供 (者控制碼的函式時使用，例如<a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>) 。</span><span class="sxs-lookup"><span data-stu-id="b3d79-157">The <a href="ctrpp.md">CTRPP</a> tool creates a HANDLE variable that you can use when calling functions that require a handle to the provider (for example, <a href="/windows/desktop/api/Perflib/nf-perflib-perfsetulongcountervalue"><strong>PerfSetULongCounterValue</strong></a>).</span></span> <span data-ttu-id="b3d79-158">符號名稱是變數的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3d79-158">The symbolic name is the name of the variable.</span></span></p>
<p><span data-ttu-id="b3d79-159">如果您在呼叫<a href="ctrpp.md">CTRPP</a>時包含<strong>-prefix</strong>引數，則前置詞字串會加入符號名稱的開頭。</span><span class="sxs-lookup"><span data-stu-id="b3d79-159">If you include the <strong>-prefix</strong> argument when calling <a href="ctrpp.md">CTRPP</a>, the prefix string is added to the beginning of the symbolic name.</span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="b3d79-160">規格需求</span><span class="sxs-lookup"><span data-stu-id="b3d79-160">Requirements</span></span>



| <span data-ttu-id="b3d79-161">需求</span><span class="sxs-lookup"><span data-stu-id="b3d79-161">Requirement</span></span> | <span data-ttu-id="b3d79-162">值</span><span class="sxs-lookup"><span data-stu-id="b3d79-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b3d79-163">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b3d79-163">Minimum supported client</span></span><br/> | <span data-ttu-id="b3d79-164">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3d79-164">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b3d79-165">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b3d79-165">Minimum supported server</span></span><br/> | <span data-ttu-id="b3d79-166">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b3d79-166">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




