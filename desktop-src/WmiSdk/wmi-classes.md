---
description: 本節提供 WMI 類別和參考頁面資訊。
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: WMI 類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa764d39c1fb048e125898a1f7e6d5cadf7f127d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977846"
---
# <a name="wmi-classes"></a><span data-ttu-id="96139-103">WMI 類別</span><span class="sxs-lookup"><span data-stu-id="96139-103">WMI Classes</span></span>

<span data-ttu-id="96139-104">本節提供 WMI 類別和參考頁面資訊。</span><span class="sxs-lookup"><span data-stu-id="96139-104">This section provides WMI class and reference page information.</span></span> <span data-ttu-id="96139-105">如需如何取出類別或實例資料的詳細資訊，請參閱 [操作類別和實例資訊](manipulating-class-and-instance-information.md)。</span><span class="sxs-lookup"><span data-stu-id="96139-105">For more information about how to retrieve class or instance data, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span> <span data-ttu-id="96139-106">下列清單列出、描述和提供特定 WMI 類別資訊的連結。</span><span class="sxs-lookup"><span data-stu-id="96139-106">The following list lists, describes, and provides links to specific WMI class information.</span></span> <span data-ttu-id="96139-107">如需使用 WMI 類別取得各種作業系統和硬體資料的詳細資訊和腳本程式碼範例，請參閱 [腳本和應用程式的 wmi](wmi-tasks-for-scripts-and-applications.md)工作。</span><span class="sxs-lookup"><span data-stu-id="96139-107">For more information and script code examples of using WMI classes to obtain a variety of operating system and hardware data, see [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span> <span data-ttu-id="96139-108">如需 c + + 的範例，請參閱 [WMI c + + 應用程式範例](wmi-c---application-examples.md)。</span><span class="sxs-lookup"><span data-stu-id="96139-108">For examples in C++, see [WMI C++ Application Examples](wmi-c---application-examples.md).</span></span> <span data-ttu-id="96139-109">[連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md) 會顯示如何取得遠端資料。</span><span class="sxs-lookup"><span data-stu-id="96139-109">[Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) shows how to obtain remote data.</span></span> <span data-ttu-id="96139-110">您也可以使用 PowerShell 來存取 WMI 物件;如需包含 PowerShell 程式碼範例的 WMI 類別清單，請參閱 [這裡](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi)。</span><span class="sxs-lookup"><span data-stu-id="96139-110">You can also use PowerShell do access WMI objects; for a list of WMI classes that include PowerShell code samples, see [here](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).</span></span>



| <span data-ttu-id="96139-111">區段</span><span class="sxs-lookup"><span data-stu-id="96139-111">Section</span></span>                                                    | <span data-ttu-id="96139-112">描述</span><span class="sxs-lookup"><span data-stu-id="96139-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96139-113">WMI 系統類別</span><span class="sxs-lookup"><span data-stu-id="96139-113">WMI System Classes</span></span>](wmi-system-classes.md)               | <span data-ttu-id="96139-114">預先定義的類別，包含在 Windows Management Instrumentation (WMI) 核心的每個命名空間中。</span><span class="sxs-lookup"><span data-stu-id="96139-114">Predefined classes that are included in every namespace in the Windows Management Instrumentation (WMI) core.</span></span> <span data-ttu-id="96139-115">您可以辨識 WMI 系統類別，因為名稱的開頭是雙底線 (\_ \_) 。</span><span class="sxs-lookup"><span data-stu-id="96139-115">You can recognize a WMI system class because the name begins with a double underscore (\_\_).</span></span> <span data-ttu-id="96139-116">這些類別提供 WMI 的許多基本功能。</span><span class="sxs-lookup"><span data-stu-id="96139-116">These classes provide much of the basic functionality for WMI.</span></span> <span data-ttu-id="96139-117">WMI 系統類別的用途與 SQL server 中的系統資料表類似。</span><span class="sxs-lookup"><span data-stu-id="96139-117">The WMI system classes are similar in purpose to the system tables in SQL server.</span></span> |
| [<span data-ttu-id="96139-118">MSFT 類別</span><span class="sxs-lookup"><span data-stu-id="96139-118">MSFT Classes</span></span>](msft-classes.md)                           | <span data-ttu-id="96139-119">其他 Microsoft 類別，提供運算元種作業系統功能的方法，例如遠端事件和原則延伸。</span><span class="sxs-lookup"><span data-stu-id="96139-119">Other Microsoft classes that offer the means to manipulate several operating system features, such as remote events and policy extensions.</span></span> <span data-ttu-id="96139-120">[Wmi 疑難排解](wmi-troubleshooting.md)類別是 MSFT 類別，可提供 WMI 作業的相關資料。</span><span class="sxs-lookup"><span data-stu-id="96139-120">The [WMI Troubleshooting](wmi-troubleshooting.md) classes are MSFT classes that provide data about WMI operations.</span></span>                                                                                               |
| [<span data-ttu-id="96139-121">CIM 類別</span><span class="sxs-lookup"><span data-stu-id="96139-121">CIM Classes</span></span>](cimclas.md)                                 | <span data-ttu-id="96139-122">[*通用訊息模型 (CIM)*](gloss-c.md) 架構類別。</span><span class="sxs-lookup"><span data-stu-id="96139-122">[*Common Information Model (CIM)*](gloss-c.md) schema classes.</span></span> <span data-ttu-id="96139-123">如果您想要撰寫自己的 WMI 類別，則可以繼承自其中一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="96139-123">If you want to write your own WMI classes then you can inherit from one or more of these classes.</span></span> <span data-ttu-id="96139-124">WMI [Win32 類別](/windows/desktop/CIMWin32Prov/win32-provider) 繼承自 CIM 類別。</span><span class="sxs-lookup"><span data-stu-id="96139-124">The WMI [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider) inherit from the CIM classes.</span></span>                                                                          |
| [<span data-ttu-id="96139-125">標準取用者類別</span><span class="sxs-lookup"><span data-stu-id="96139-125">Standard Consumer Classes</span></span>](standard-consumer-classes.md) | <span data-ttu-id="96139-126">一組 WMI 事件取用者，這些取用者會在收到任意事件時觸發動作。</span><span class="sxs-lookup"><span data-stu-id="96139-126">A set of WMI event consumers which trigger an action upon receipt of an arbitrary event.</span></span> <span data-ttu-id="96139-127">如需詳細資訊，請參閱 [監視事件](monitoring-events.md)。</span><span class="sxs-lookup"><span data-stu-id="96139-127">For more information, see [Monitoring Events](monitoring-events.md).</span></span>                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a><span data-ttu-id="96139-128">WMI 類別腳本中心程式碼範例</span><span class="sxs-lookup"><span data-stu-id="96139-128">WMI Class Scripting Center Code Examples</span></span>

<span data-ttu-id="96139-129">下列腳本中心程式碼範例會跨多個命名空間影響多個 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="96139-129">The following Scripting Center code samples affect multiple WMI classes across multiple namespaces.</span></span>



| <span data-ttu-id="96139-130">連結</span><span class="sxs-lookup"><span data-stu-id="96139-130">Link</span></span>                                                                                                                                      | <span data-ttu-id="96139-131">描述</span><span class="sxs-lookup"><span data-stu-id="96139-131">Description</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="96139-132">GUI WMI Explorer 和 WMI 方法說明產生器</span><span class="sxs-lookup"><span data-stu-id="96139-132">GUI WMI Explorer and WMI Method Help Generator</span></span>](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | <span data-ttu-id="96139-133">提供 GUI WMI Explorer 和 WMI 方法說明產生器的範例腳本。</span><span class="sxs-lookup"><span data-stu-id="96139-133">Sample script that provides a GUI WMI Explorer and WMI Method Help Generator.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="96139-134">WMI Explorer 搜尋 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="96139-134">WMI Explorer Search WMI NameSpaces</span></span>](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | <span data-ttu-id="96139-135">可讓使用者在指定的電腦上搜尋所有可用命名空間中的類別。</span><span class="sxs-lookup"><span data-stu-id="96139-135">Allows users to search for classes in all of the available namespaces on the specified computers.</span></span> <span data-ttu-id="96139-136">此範例是 GUI WMI Explorer 範例的命令列新版，可視為 Get-WmiObject 清單的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="96139-136">This sample is the command-line verison of the GUI WMI Explorer sample, and may be considered an extension of Get-WmiObject -List.</span></span> |
| [<span data-ttu-id="96139-137">Arposh Windows 系統管理工具</span><span class="sxs-lookup"><span data-stu-id="96139-137">Arposh Windows System Administration tool</span></span>](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | <span data-ttu-id="96139-138">AWSA 是由系統管理員所建立。</span><span class="sxs-lookup"><span data-stu-id="96139-138">AWSA was built with the System Administrator in mind.</span></span> <span data-ttu-id="96139-139">針對 Windows 問題進行疑難排解需要大量的工具和知識。</span><span class="sxs-lookup"><span data-stu-id="96139-139">Troubleshooting Windows issues requires a vast array of tools and knowledge.</span></span> <span data-ttu-id="96139-140">AWSA 會將這些工具結合在一個中央位置，並新增額外的功能。</span><span class="sxs-lookup"><span data-stu-id="96139-140">AWSA brings those tools together in one central location and adds additional functionality.</span></span>       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a><span data-ttu-id="96139-141">WMI 類別和屬性的命名慣例</span><span class="sxs-lookup"><span data-stu-id="96139-141">Naming Conventions for WMI Classes and Properties</span></span>

<span data-ttu-id="96139-142">屬性名稱必須符合分散式管理工作推動力 (DTMF) 所定義的受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="96139-142">Property names must conform to the Managed Object Format (MOF) syntax defined by the Distributed Management Task Force (DTMF).</span></span> <span data-ttu-id="96139-143">初始識別碼字元必須是來自字母 a 到 z，而底線字元 (\_) 。</span><span class="sxs-lookup"><span data-stu-id="96139-143">The initial identifier characters must be from the letters a through z and the underscore character (\_).</span></span> <span data-ttu-id="96139-144">所有其他字元都必須來自字母 a 到 z、底線字元和數位0到9。</span><span class="sxs-lookup"><span data-stu-id="96139-144">All additional characters must be from the letters a through z, the underscore character, and the numerals 0 through 9.</span></span> <span data-ttu-id="96139-145">如需詳細資訊，請參閱 [CIM 規格2.2 版](https://www.dmtf.org/standards/cim)的 Unicode 使用方式一節。</span><span class="sxs-lookup"><span data-stu-id="96139-145">For more information, see the Unicode Usage section of the [CIM Specification Version 2.2](https://www.dmtf.org/standards/cim).</span></span>

<span data-ttu-id="96139-146">SQL 保留字不應該用在類別和屬性名稱中。</span><span class="sxs-lookup"><span data-stu-id="96139-146">SQL reserve words should not be used in class and property names.</span></span> <span data-ttu-id="96139-147">如需 SQL 保留字和詳細資訊的完整清單，請參閱 [CIM 規格2.2 版](https://www.dmtf.org/standards/cim)的指導方針一節。</span><span class="sxs-lookup"><span data-stu-id="96139-147">For a complete list of the SQL reserve words and for more information, see the Guidelines section of the [CIM Specification Version 2.2](https://www.dmtf.org/standards/cim).</span></span>

## <a name="document-conventions-for-a-wmi-class-reference-page"></a><span data-ttu-id="96139-148">WMI 類別參考頁面的檔慣例</span><span class="sxs-lookup"><span data-stu-id="96139-148">Document Conventions for a WMI Class Reference Page</span></span>

<span data-ttu-id="96139-149">本節將識別及描述 WMI 類別參考頁面的檔慣例。</span><span class="sxs-lookup"><span data-stu-id="96139-149">This section identifies and describes the document conventions for a WMI class reference page.</span></span>

<span data-ttu-id="96139-150">一般參考頁面包含語法區塊、方法資料表和屬性清單。</span><span class="sxs-lookup"><span data-stu-id="96139-150">A typical reference page contains a syntax block, methods table, and a properties list.</span></span>

-   <span data-ttu-id="96139-151">語法區塊</span><span class="sxs-lookup"><span data-stu-id="96139-151">Syntax block</span></span>

    <span data-ttu-id="96139-152">MOF 程式碼的簡化版本，包含類別名稱、父類別 (（如果有任何) ）和類別屬性（以字母順序表示）與資料類型。</span><span class="sxs-lookup"><span data-stu-id="96139-152">A simplified version of MOF code that includes the class name, parent class (if any), and class properties, in alphabetical order, with data types.</span></span>

-   <span data-ttu-id="96139-153">方法資料表</span><span class="sxs-lookup"><span data-stu-id="96139-153">Methods table</span></span>

    <span data-ttu-id="96139-154">如果類別具有方法，則方法會列在緊接在語法區塊後面的資料表中。</span><span class="sxs-lookup"><span data-stu-id="96139-154">If a class has methods, the methods are listed in the table immediately following the syntax block.</span></span> <span data-ttu-id="96139-155">每個已執行的方法都會連結到參考頁面。</span><span class="sxs-lookup"><span data-stu-id="96139-155">Each implemented method is linked to a reference page.</span></span>

-   <span data-ttu-id="96139-156">屬性清單</span><span class="sxs-lookup"><span data-stu-id="96139-156">Properties list</span></span>

    <span data-ttu-id="96139-157">每個類別屬性都會以資料類型、存取類型 (唯讀或讀取/寫入) 、限定詞，以及屬性的描述來列出。</span><span class="sxs-lookup"><span data-stu-id="96139-157">Each class property is listed with a data type, access type (read-only or read/write), qualifiers, and a description of the property.</span></span>

## <a name="syntax-block"></a><span data-ttu-id="96139-158">語法區塊</span><span class="sxs-lookup"><span data-stu-id="96139-158">Syntax block</span></span>

``` syntax
class Win32_xyz : CIM_xyz 
{
  uint16 abc  ;
  string def  ;
};
```

## <a name="methods-table"></a><span data-ttu-id="96139-159">方法資料表</span><span class="sxs-lookup"><span data-stu-id="96139-159">Methods table</span></span>



| <span data-ttu-id="96139-160">Win32 \_ xyz 方法</span><span class="sxs-lookup"><span data-stu-id="96139-160">Win32\_xyz methods</span></span> | <span data-ttu-id="96139-161">Description</span><span class="sxs-lookup"><span data-stu-id="96139-161">Description</span></span>                                |
|--------------------|--------------------------------------------|
| <span data-ttu-id="96139-162">*SomeMethod*</span><span class="sxs-lookup"><span data-stu-id="96139-162">*SomeMethod*</span></span>       | <span data-ttu-id="96139-163">方法用途的簡短描述。</span><span class="sxs-lookup"><span data-stu-id="96139-163">Brief description of what the method does.</span></span> |



 

## <a name="properties-list"></a><span data-ttu-id="96139-164">屬性清單</span><span class="sxs-lookup"><span data-stu-id="96139-164">Properties list</span></span>

<dl> <dt>

<span data-ttu-id="96139-165"><span id="abc"></span><span id="ABC"></span>Abc</span><span class="sxs-lookup"><span data-stu-id="96139-165"><span id="abc"></span><span id="ABC"></span>abc</span></span>
</dt> <dd>

<span data-ttu-id="96139-166">資料類型： **uint16**</span><span class="sxs-lookup"><span data-stu-id="96139-166">Data type: **uint16**</span></span>

<span data-ttu-id="96139-167">存取類型：顯示您是否擁有這個屬性的讀取/寫入或唯讀存取權。</span><span class="sxs-lookup"><span data-stu-id="96139-167">Access type: Shows whether you have read/write or read-only access to this property.</span></span>

<span data-ttu-id="96139-168">限定詞：如果存在，則會顯示內容的限定詞。</span><span class="sxs-lookup"><span data-stu-id="96139-168">Qualifiers: If present, shows the qualifiers for the property.</span></span> <span data-ttu-id="96139-169">例如， **Key**、 **Override**。</span><span class="sxs-lookup"><span data-stu-id="96139-169">For example, **Key**, **Override**.</span></span>

<span data-ttu-id="96139-170">描述屬性，並提供屬性的繼承資訊。</span><span class="sxs-lookup"><span data-stu-id="96139-170">Describes the property and provides inheritance information for the property.</span></span> <span data-ttu-id="96139-171">例如，這個屬性繼承自 \**CIM \_* xyz \* \* \*。</span><span class="sxs-lookup"><span data-stu-id="96139-171">For example, this property is inherited from \**CIM\_* xyz\*\*\*.</span></span> <span data-ttu-id="96139-172">如果 Microsoft 提供該類別的執行，則會有父類別的連結。</span><span class="sxs-lookup"><span data-stu-id="96139-172">There is a link to the parent class if Microsoft provides an implementation of that class.</span></span> <span data-ttu-id="96139-173">但是，無法使用 CIM 類別。</span><span class="sxs-lookup"><span data-stu-id="96139-173">However, the CIM classes are not available.</span></span>

</dd> <dt>

<span data-ttu-id="96139-174"><span id="def"></span><span id="DEF"></span>Def</span><span class="sxs-lookup"><span data-stu-id="96139-174"><span id="def"></span><span id="DEF"></span>def</span></span>
</dt> <dd>

<span data-ttu-id="96139-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="96139-175">Data type: **string**</span></span>

<span data-ttu-id="96139-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="96139-176">Access type: Read-only</span></span>

<span data-ttu-id="96139-177">屬性的描述。</span><span class="sxs-lookup"><span data-stu-id="96139-177">Description of the property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96139-178">備註</span><span class="sxs-lookup"><span data-stu-id="96139-178">Remarks</span></span>

<span data-ttu-id="96139-179">提供類別的詳細資訊（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="96139-179">Gives more information about the class, if applicable.</span></span> <span data-ttu-id="96139-180">也提供衍生資訊（如果適用）。</span><span class="sxs-lookup"><span data-stu-id="96139-180">Also provides derivation information, if applicable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96139-181">相關主題</span><span class="sxs-lookup"><span data-stu-id="96139-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96139-182">WMI 參考</span><span class="sxs-lookup"><span data-stu-id="96139-182">WMI Reference</span></span>](wmi-reference.md)
</dt> </dl>

 

 
