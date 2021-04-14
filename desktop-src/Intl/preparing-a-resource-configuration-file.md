---
description: 準備資源設定檔
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: 準備資源設定檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112809"
---
# <a name="preparing-a-resource-configuration-file"></a><span data-ttu-id="ef8a6-103">準備資源設定檔</span><span class="sxs-lookup"><span data-stu-id="ef8a6-103">Preparing a Resource Configuration File</span></span>

<span data-ttu-id="ef8a6-104">[資源公用程式](resource-utilities.md)中所述的 MUIRCT 和 RC 編譯器公用程式都會提供命令列選項，可讓您指定基礎語言資源的資源設定檔。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-104">Both the MUIRCT and the RC Compiler utilities described in [Resource Utilities](resource-utilities.md) provide a command line option that allows you to specify a resource configuration file for the base language resources.</span></span> <span data-ttu-id="ef8a6-105">使用這個公開、人類可讀取的 XML 檔案，可讓您更充分掌控資源的分割，而不是使用公用程式的一般命令列參數來取得。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-105">Use of this public, human-readable XML file allows more control over the splitting of resources than can be obtained using the regular command line switches of the utilities.</span></span> <span data-ttu-id="ef8a6-106">但是，即使您未提供資源設定檔做為輸入，但 LN 和特定語言的資源檔將包含資源設定資料。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-106">However, even if you do not provide a resource configuration file as an input, the LN and language-specific resource files will contain resource configuration data.</span></span>

<span data-ttu-id="ef8a6-107">Win32 應用程式的所有資源設定檔都會以相同的方式開始和結束：</span><span class="sxs-lookup"><span data-stu-id="ef8a6-107">All resource configuration files for Win32 applications begin and end identically:</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



<span data-ttu-id="ef8a6-108">本主題著重于在 Windows Vista 和更新版本上建立非受控碼時，適用于 XML 架構的各個層面。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-108">This topic focuses on the aspects of the XML schema that are useful in building unmanaged code on Windows Vista and later.</span></span> <span data-ttu-id="ef8a6-109">尤其是，它只關心 win32Resources 元素的行為。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-109">In particular, it is only concerned with the behavior of the win32Resources element.</span></span>

## <a name="win32resources-element"></a><span data-ttu-id="ef8a6-110">win32Resources 元素</span><span class="sxs-lookup"><span data-stu-id="ef8a6-110">win32Resources Element</span></span>

<span data-ttu-id="ef8a6-111">Win32Resources 元素具有下表所述的屬性。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-111">The win32Resources element has the attributes described in the following table.</span></span>



| <span data-ttu-id="ef8a6-112">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="ef8a6-112">Attribute name</span></span>           | <span data-ttu-id="ef8a6-113">強制性</span><span class="sxs-lookup"><span data-stu-id="ef8a6-113">Mandatory</span></span> | <span data-ttu-id="ef8a6-114">Description</span><span class="sxs-lookup"><span data-stu-id="ef8a6-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8a6-115">fileType</span><span class="sxs-lookup"><span data-stu-id="ef8a6-115">fileType</span></span>                 | <span data-ttu-id="ef8a6-116">No</span><span class="sxs-lookup"><span data-stu-id="ef8a6-116">No</span></span>        | <span data-ttu-id="ef8a6-117">檔案類型。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-117">Type of file.</span></span> <span data-ttu-id="ef8a6-118">應一律為 "Application"。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-118">Should always be "Application".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="ef8a6-119">總和檢查碼</span><span class="sxs-lookup"><span data-stu-id="ef8a6-119">checksum</span></span>                 | <span data-ttu-id="ef8a6-120">No</span><span class="sxs-lookup"><span data-stu-id="ef8a6-120">No</span></span>        | <span data-ttu-id="ef8a6-121">要出現在 LN 檔案的資源設定資料和特定語言資源檔的總和檢查碼值。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-121">Checksum value to appear in the resource configuration data of the LN file and language-specific resource files.</span></span> <span data-ttu-id="ef8a6-122">例如，這個屬性可讓您從單一語言專屬的資源檔中複製總和檢查碼，方法是使用英文 (美國) 的慣例，並將總和檢查碼放在不同的語言特定資源檔中。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-122">For example, this attribute allows you to copy the checksum from a single language-specific resource file, by convention the one for English (United States), and place the checksum in a different language-specific resource file.</span></span> <span data-ttu-id="ef8a6-123">總和檢查碼可指定為不超過32個字元的十六進位數位字串。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-123">The checksum can be specified as a hexadecimal number string that is no longer than 32 characters.</span></span> <span data-ttu-id="ef8a6-124">數值必須 containable 在128位的數位中。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-124">The numerical value must be containable in a 128-bit number.</span></span> |
| <span data-ttu-id="ef8a6-125">語言</span><span class="sxs-lookup"><span data-stu-id="ef8a6-125">language</span></span>                 | <span data-ttu-id="ef8a6-126">No</span><span class="sxs-lookup"><span data-stu-id="ef8a6-126">No</span></span>        | <span data-ttu-id="ef8a6-127">使用符合 RFC 4646 的名稱格式指定的語言 (Windows Vista 和更新版本的) ，例如 en-us （ (英文）) 。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-127">Language specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="ef8a6-128">ultimateFallbackLanguage</span><span class="sxs-lookup"><span data-stu-id="ef8a6-128">ultimateFallbackLanguage</span></span> | <span data-ttu-id="ef8a6-129">No</span><span class="sxs-lookup"><span data-stu-id="ef8a6-129">No</span></span>        | <span data-ttu-id="ef8a6-130">要插入 LN 檔案之資源設定資料中的語言，代表要在搜尋對應語言專屬資源檔時使用的最終回溯語言。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-130">Language to insert into the resource configuration data for the LN file, representing the ultimate fallback language to use in a search for a corresponding language-specific resource file.</span></span> <span data-ttu-id="ef8a6-131">如果資源載入器無法從執行緒慣用 UI 語言載入要求的資源檔，它會使用最終的回溯語言做為最後一次嘗試。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-131">If the resource loader fails to load a requested resource file from the thread preferred UI languages, it uses an ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="ef8a6-132">語言的指定方式是使用與 RFC 4646 相容的名稱格式 (Windows Vista 和更新版本) ，例如 en-us （ (英文）) 。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-132">The language is specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>       |
| <span data-ttu-id="ef8a6-133">ultimateFallbackLocation</span><span class="sxs-lookup"><span data-stu-id="ef8a6-133">ultimateFallbackLocation</span></span> | <span data-ttu-id="ef8a6-134">No</span><span class="sxs-lookup"><span data-stu-id="ef8a6-134">No</span></span>        | <span data-ttu-id="ef8a6-135">Fallback 位置。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-135">Fallback location.</span></span> <span data-ttu-id="ef8a6-136">如果最終的回復資源編譯成 LN 檔，請指定「內部」。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-136">Specify "internal" if ultimate fallback resources are compiled into the LN file.</span></span> <span data-ttu-id="ef8a6-137">如果 LN 檔案要參考特定語言的資源檔，以取得其最終的回溯資源，請指定 "external" (預設) 。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-137">Specify "external" (default) if the LN file is to reference a language-specific resource file for its ultimate fallback resources.</span></span>                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="ef8a6-138">在資源設定檔中，win32Resources 元素具有下表所述的子項目。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-138">In the resource configuration file, the win32Resources element has the sub-elements described in the next table.</span></span>



| <span data-ttu-id="ef8a6-139">元素名稱</span><span class="sxs-lookup"><span data-stu-id="ef8a6-139">Element Name</span></span>       | <span data-ttu-id="ef8a6-140">Description</span><span class="sxs-lookup"><span data-stu-id="ef8a6-140">Description</span></span>                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8a6-141">localizedResources</span><span class="sxs-lookup"><span data-stu-id="ef8a6-141">localizedResources</span></span> | <span data-ttu-id="ef8a6-142">封裝資源類型和個別資源（包含在特定語言的資源檔中）相關資訊的資源。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-142">Resources that encapsulate information about the resource types and individual resources contained in a language-specific resource file.</span></span> |
| <span data-ttu-id="ef8a6-143">neutralResources</span><span class="sxs-lookup"><span data-stu-id="ef8a6-143">neutralResources</span></span>   | <span data-ttu-id="ef8a6-144">封裝包含在 LN 檔案中之資源類型相關資訊的資源。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-144">Resources that encapsulate information about the resource types contained in an LN file.</span></span>                                                 |



 

## <a name="localizedresources-element"></a><span data-ttu-id="ef8a6-145">localizedResources 元素</span><span class="sxs-lookup"><span data-stu-id="ef8a6-145">localizedResources Element</span></span>

<span data-ttu-id="ef8a6-146">當地語系化的資源元素。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-146">Localized resources element.</span></span> <span data-ttu-id="ef8a6-147">根據預設，這個元素沒有任何屬性，而且只有一個子項目類型。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-147">By default, this element has no attributes and only one type of sub-element.</span></span> <span data-ttu-id="ef8a6-148">它只是 resourceType 元素的容器。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-148">It is just a container for resourceType elements.</span></span>



| <span data-ttu-id="ef8a6-149">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="ef8a6-149">Attribute Name</span></span> | <span data-ttu-id="ef8a6-150">描述</span><span class="sxs-lookup"><span data-stu-id="ef8a6-150">Description</span></span>                                                                    |
|----------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="ef8a6-151">resourceType</span><span class="sxs-lookup"><span data-stu-id="ef8a6-151">resourceType</span></span>   | <span data-ttu-id="ef8a6-152">特定語言的資源檔中包含的個別資源類型。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-152">Type of an individual resource contained in a language-specific resource file.</span></span> |



 

## <a name="neutralresources-element"></a><span data-ttu-id="ef8a6-153">neutralResources 元素</span><span class="sxs-lookup"><span data-stu-id="ef8a6-153">neutralResources Element</span></span>

<span data-ttu-id="ef8a6-154">中立的資源元素。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-154">Neutral resources element.</span></span> <span data-ttu-id="ef8a6-155">此元素只是 resourceType 元素的容器。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-155">This element is just a container for resourceType elements.</span></span>



| <span data-ttu-id="ef8a6-156">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="ef8a6-156">Attribute Name</span></span> | <span data-ttu-id="ef8a6-157">描述</span><span class="sxs-lookup"><span data-stu-id="ef8a6-157">Description</span></span>                                        |
|----------------|----------------------------------------------------|
| <span data-ttu-id="ef8a6-158">resourceType</span><span class="sxs-lookup"><span data-stu-id="ef8a6-158">resourceType</span></span>   | <span data-ttu-id="ef8a6-159">包含在 LN 檔中的單一資源類型。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-159">Type of a single resource contained in an LN file.</span></span> |



 

## <a name="resourcetype-element"></a><span data-ttu-id="ef8a6-160">resourceType 元素</span><span class="sxs-lookup"><span data-stu-id="ef8a6-160">resourceType Element</span></span>

<span data-ttu-id="ef8a6-161">ResourceType 元素會封裝單一資源類型或個別資源的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-161">The resourceType element encapsulates information about a single resource type or individual resource.</span></span> <span data-ttu-id="ef8a6-162">它具有下列屬性。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-162">It has the attributes listed below.</span></span>

> [!Caution]  
> <span data-ttu-id="ef8a6-163">某些資源設定瑕疵僅由 RC 編譯器或 MUIRCT 捕捉，視輸入資源檔或二進位檔內容而定。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-163">Some resource configuration defects are caught only by RC Compiler or MUIRCT, depending on the input resource file or binary file content.</span></span> <span data-ttu-id="ef8a6-164">資源設定檔中不存在於輸入檔中的 resourceType 錯誤不會被攔截，而導致非預期的行為。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-164">The resourceType errors in the resource configuration file that do not exist in the input file are not caught, resulting in unexpected behavior.</span></span> <span data-ttu-id="ef8a6-165">使用者可以使用有缺陷的資源設定檔，而且在導入使用資源設定檔的損毀部分的二進位檔之前，並不知道，這會從目前的二進位檔建立中斷的外觀。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-165">Users can be using a defective resource configuration file and do not know until they introduce binaries that use the broken parts of the resource configuration file, which creates the appearance that the breaks are from the current binaries.</span></span>

 



| <span data-ttu-id="ef8a6-166">屬性名稱</span><span class="sxs-lookup"><span data-stu-id="ef8a6-166">Attribute name</span></span> | <span data-ttu-id="ef8a6-167">強制性</span><span class="sxs-lookup"><span data-stu-id="ef8a6-167">Mandatory</span></span> | <span data-ttu-id="ef8a6-168">Description</span><span class="sxs-lookup"><span data-stu-id="ef8a6-168">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef8a6-169">typeNameId</span><span class="sxs-lookup"><span data-stu-id="ef8a6-169">typeNameId</span></span>     | <span data-ttu-id="ef8a6-170">Yes</span><span class="sxs-lookup"><span data-stu-id="ef8a6-170">Yes</span></span>       | <span data-ttu-id="ef8a6-171">資源的類型名稱或識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-171">Type name or identifier for the resource.</span></span> <span data-ttu-id="ef8a6-172">指定字串名稱或數位。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-172">Specify a string name or a number.</span></span> <span data-ttu-id="ef8a6-173">如果使用數位，請在字串前面加上 " \# "，表示它代表一個數位。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-173">If using a number, prepend the string with a "\#" to indicate that it represents a number.</span></span> <span data-ttu-id="ef8a6-174">每個 resourceType 元素都只能有一個 *typeNameId* 屬性。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-174">Each resourceType element must have only one *typeNameId* attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ef8a6-175">itemName</span><span class="sxs-lookup"><span data-stu-id="ef8a6-175">itemName</span></span>       | <span data-ttu-id="ef8a6-176">No</span><span class="sxs-lookup"><span data-stu-id="ef8a6-176">No</span></span>        | <span data-ttu-id="ef8a6-177">資源的專案名稱字串，要放在特定語言的資源檔中。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-177">Item name string for the resource, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="ef8a6-178">您可以指定多個名稱，並以空格分隔，例如 "HTML MOFDATA"。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-178">You can specify multiple names, separated by white spaces, for example, "HTML MOFDATA".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="ef8a6-179">itemId</span><span class="sxs-lookup"><span data-stu-id="ef8a6-179">itemId</span></span>         | <span data-ttu-id="ef8a6-180">No</span><span class="sxs-lookup"><span data-stu-id="ef8a6-180">No</span></span>        | <span data-ttu-id="ef8a6-181">個別資源專案的識別碼，要放在特定語言的資源檔中。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-181">Identifier of individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="ef8a6-182">您可以將此專案指定為範圍 (例如 "1-12" ) 或個別識別碼以空白字元分隔 (例如 "1 3 4" ) 。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-182">The item can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="ef8a6-183">Stringid 指定</span><span class="sxs-lookup"><span data-stu-id="ef8a6-183">stringId</span></span>       | <span data-ttu-id="ef8a6-184">No</span><span class="sxs-lookup"><span data-stu-id="ef8a6-184">No</span></span>        | <span data-ttu-id="ef8a6-185">個別資源專案的字串識別碼，要放在特定語言的資源檔中。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-185">String identifier for individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="ef8a6-186">字串可以指定為範圍 (例如 "1-12" ) 或個別識別碼以空白字元分隔 (例如 "1 3 4" ) 。這個屬性可讓您指定可當地語系化和 nonlocalizable 的字串資料表專案。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-186">The string can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").This attribute allows the specification of both localizable and nonlocalizable string table entries.</span></span> <span data-ttu-id="ef8a6-187">它必須與 "6" 的 *typeNameId* 值搭配使用，以表示字串資料表專案的資源類型。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-187">It must be used in conjunction with the *typeNameId* value of "6", denoting a string table entry resource type.</span></span><br/> <span data-ttu-id="ef8a6-188">字串會儲存在字串資料表中的16區塊內。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-188">Strings are stored in blocks of 16 in a string table.</span></span> <span data-ttu-id="ef8a6-189">例如，字串0到15會儲存在單一資源專案區塊中，而且可以在資源設定檔中作為 *itemId* 1 或 *stringid 指定* "0-15" 來參考。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-189">For example, strings 0 to 15 are stored in a single resource item block and can be referenced in the resource configuration file as *itemId* 1, or as *stringId* "0-15".</span></span> <span data-ttu-id="ef8a6-190">例如，如果有五個可當地語系化的字串和三個 nonlocalizable 字串，您應該針對可當地語系化的字串指派字串識別碼0-4，並為 nonlocalizable 字串指派字串識別碼16-18。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-190">For example, if there are five localizable strings and three nonlocalizable strings, you should assign string identifiers 0-4 for the localizable strings, and string identifiers 16-18 for the nonlocalizable strings.</span></span> <span data-ttu-id="ef8a6-191">如果您未以這種方式組織字串，則會將受影響的字串區塊放在 LN 檔和特定語言的資源檔中。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-191">If you do not organize strings this way, the affected blocks of strings are placed in both the LN file and the language-specific resource file.</span></span><br/> |



 

<span data-ttu-id="ef8a6-192">如果您在 localizedResource 元素下指定特定資源類型的專案類型、 *itemId* 和/或 *stringid 指定* 屬性，則只有指定之資源 *類型的這些* 指定專案或字串會放置在特定語言的資源檔中。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-192">If you specify the *itemName*, *itemId*, and/or *stringId* attributes for a particular resource type under the localizedResource element, only these specified items or strings for the designated resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="ef8a6-193">如果指定 resourceType 元素時未指定任何明確的專案名稱、專案識別碼或字串識別碼，則會將指定之資源類型的所有專案都放在特定語言的資源檔中。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-193">If a resourceType element is specified without any explicit item name, item identifier, or string identifier, all items of the specified resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="ef8a6-194">未列在任何 localizedResource 專案中的專案或類型都會放置在 LN 檔案中。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-194">Items or types not listed in any localizedResource element are placed in the LN file.</span></span>

<span data-ttu-id="ef8a6-195">以下是標準資源類型和其數值識別碼：</span><span class="sxs-lookup"><span data-stu-id="ef8a6-195">The following are the standard resource types and their numeric identifiers:</span></span>

-   <span data-ttu-id="ef8a6-196">資料指標 (1) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-196">CURSOR(1)</span></span>
-   <span data-ttu-id="ef8a6-197">點陣圖 (2) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-197">BITMAP(2)</span></span>
-   <span data-ttu-id="ef8a6-198">圖示 (3) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-198">ICON(3)</span></span>
-   <span data-ttu-id="ef8a6-199">功能表 (4) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-199">MENU(4)</span></span>
-   <span data-ttu-id="ef8a6-200">對話方塊 (5) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-200">DIALOG(5)</span></span>
-   <span data-ttu-id="ef8a6-201">字串 (6) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-201">STRING(6)</span></span>
-   <span data-ttu-id="ef8a6-202">FONTDIR (7) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-202">FONTDIR(7)</span></span>
-   <span data-ttu-id="ef8a6-203">字型 (8) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-203">FONT(8)</span></span>
-   <span data-ttu-id="ef8a6-204">加速器 (9) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-204">ACCELERATORS(9)</span></span>
-   <span data-ttu-id="ef8a6-205">RCDATA (10) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-205">RCDATA(10)</span></span>
-   <span data-ttu-id="ef8a6-206">MESSAGETABLE (11) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-206">MESSAGETABLE(11)</span></span>
-   <span data-ttu-id="ef8a6-207">群組資料 \_ 指標 (12) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-207">GROUP\_CURSOR(12)</span></span>
-   <span data-ttu-id="ef8a6-208">群組 \_ 圖示 (14) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-208">GROUP\_ICON(14)</span></span>
-   <span data-ttu-id="ef8a6-209">版本 (16) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-209">VERSION(16)</span></span>
-   <span data-ttu-id="ef8a6-210">HTML (23) </span><span class="sxs-lookup"><span data-stu-id="ef8a6-210">HTML(23)</span></span>

## <a name="example"></a><span data-ttu-id="ef8a6-211">範例</span><span class="sxs-lookup"><span data-stu-id="ef8a6-211">Example</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>
  <resources>
    <win32Resources fileType="Application">
      <neutralResources>
        <resourceType
           typeNameId="#16"
        />
      </neutralResources>
      <localizedResources> 
         <resourceType
                typeNameId="#2"
                itemId="5 6 7 8 9 10 11 12"
                itemName="HTML PRI"
         />
         <resourceType
                typeNameId="#4"
         />
         <resourceType
                typeNameId="#5"
         />
         <resourceType
                typeNameId="#6"
         />
         <resourceType
                typeNameId="#9"
         />
         <resourceType
                typeNameId="#11"
         />
         <resourceType
                typeNameId="#16"
         />
         <resourceType
                typeNameId="HTML"
         />
         <resourceType
                typeNameId="#23"
         />
         <resourceType
                typeNameId="#240"
         />
         <resourceType
                typeNameId="#1024"
         />
         <resourceType
                typeNameId="MY_TYPE"
         />
      </localizedResources> 
    </win32Resources>
  </resources>
</localization>
```



## <a name="remarks"></a><span data-ttu-id="ef8a6-212">備註</span><span class="sxs-lookup"><span data-stu-id="ef8a6-212">Remarks</span></span>

<span data-ttu-id="ef8a6-213">如果您在 neutralResources 元素中包含任何圖示 (3) 、對話方塊 (5) 、字串 (6) 或版本 (16) 資源類型，則必須在 localizedResources 元素中複製該專案。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-213">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element.</span></span> <span data-ttu-id="ef8a6-214">您可以看到上述範例中所示的範例，其中資源類型16出現在 [中性] 和 [當地語系化的資源] 區段中。</span><span class="sxs-lookup"><span data-stu-id="ef8a6-214">You can see this illustrated in the example above, where resource type 16 appears in both neutral and localized resources sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef8a6-215">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef8a6-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef8a6-216">準備資源</span><span class="sxs-lookup"><span data-stu-id="ef8a6-216">Preparing Resources</span></span>](preparing-resources.md)
</dt> </dl>

 

 




