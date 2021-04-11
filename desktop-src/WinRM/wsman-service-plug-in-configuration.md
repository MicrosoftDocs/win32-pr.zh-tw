---
title: WinRM 服務外掛程式設定
description: Windows 遠端管理 (WinRM) 外掛程式必須在 WinRM 類別目錄中註冊，才能讓基礎結構動態地判斷可用的外掛程式集合，以及它們所支援的資源 Uri。
ms.assetid: d71cd244-3f10-40e3-a756-36cdf41b9cad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60bf618d71e55c6afd28de918198725895088559
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104316735"
---
# <a name="winrm-service-plug-in-configuration"></a><span data-ttu-id="e6276-103">WinRM 服務外掛程式設定</span><span class="sxs-lookup"><span data-stu-id="e6276-103">WinRM Service Plug-in Configuration</span></span>

<span data-ttu-id="e6276-104">Windows 遠端管理 (WinRM) 外掛程式必須在 WinRM 類別目錄中註冊，才能讓基礎結構動態地判斷可用的外掛程式集合，以及它們所支援的 [*資源 uri*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="e6276-104">A Windows Remote Management (WinRM) plug-in must be registered in the WinRM catalog to enable the infrastructure to dynamically determine the set of available plug-ins and the [*resource URIs*](windows-remote-management-glossary.md) that they support.</span></span> <span data-ttu-id="e6276-105">WinRM 外掛程式的所有 [*資源 uri*](windows-remote-management-glossary.md) 都應符合 RFC 3986 () 中所定義的格式 [https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt) 。</span><span class="sxs-lookup"><span data-stu-id="e6276-105">All [*resource URIs*](windows-remote-management-glossary.md) for WinRM plug-ins should conform to the format that is defined in RFC 3986 ([https://www.ietf.org/rfc/rfc3986.txt](https://www.ietf.org/rfc/rfc3986.txt)).</span></span> <span data-ttu-id="e6276-106">設定是透過主要 WinRM 服務完成。</span><span class="sxs-lookup"><span data-stu-id="e6276-106">Configuration is done through the main WinRM service.</span></span>

<span data-ttu-id="e6276-107">下列命令會向 WinRM 服務註冊外掛程式設定：</span><span class="sxs-lookup"><span data-stu-id="e6276-107">The following command registers a plug-in configuration with the WinRM service:</span></span>

```console
winrm create http://schemas.microsoft.com/wbem/wsman/1/config/plugin?name=MyPlugIn -file:myplugin.xml
```

> [!NOTE]
> <span data-ttu-id="e6276-108">WinRM 服務需要重新開機才能公開新註冊的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e6276-108">The WinRM service needs to be restarted to expose the newly registered plug-ins.</span></span>

<span data-ttu-id="e6276-109">外掛程式設定是以 XML 指定的。</span><span class="sxs-lookup"><span data-stu-id="e6276-109">Plug-in configuration is specified in XML.</span></span> <span data-ttu-id="e6276-110">以下是一個範例。</span><span class="sxs-lookup"><span data-stu-id="e6276-110">The following is an example.</span></span>

```XML
<PlugInConfiguration xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
                     Name="MyPlugIn"
                     Filename="%systemroot%\system32\myplugin.dll" 
                     SDKVersion="1"
                     XmlRenderingType="text"
                     Architecture="64"
                     Enabled="true">

 <InitializationParameters>
  <Param Name="myParam1" Value="myValue1"/>
  <Param Name="myParam2" Value="myValue2"/>
 </InitializationParameters>

 <Resources>
  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri1" SupportsOptions="true" ExactMatch="false">
   <Capability Type="Get" SupportsFragment="true"/>
   <Capability Type="Put" SupportsFragment="true"/>
   <Capability Type="Create"/>
   <Capability Type="Delete"/>
   <Capability Type="Invoke"/>
   <Capability Type="Enumerate" SupportsFiltering="true"/>
  </Resource>

  <Resource ResourceUri="https://schemas.MyCompany.com/MyUri2" SupportsOptions="false" ExactMatch="true">
   <Security Uri="https://schemas.MyCompany.com/MyUri2" Sddl="O:NSG:BAD:P(A;;GA;;;BA)"/>
   <Security Uri="https://schemas.MyCompany.com/MyUri2/MoreSpecific" Sddl="O:NSG:BAD:P(A;;GR;;;BA)" ExactMatch="true"/>
   <Capability Type="Shell"/>
  </Resource>
 </Resources>
</PlugInConfiguration>
```



<span data-ttu-id="e6276-111">下列清單會更詳細地描述 XML 元素，後面接著指定為 XSD 的設定架構。</span><span class="sxs-lookup"><span data-stu-id="e6276-111">The following list describes the XML elements in more detail and is followed by the configuration schema specified as an XSD.</span></span>

<dl> <dt>

<span data-ttu-id="e6276-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration** /**OperationsConfiguration**</span><span class="sxs-lookup"><span data-stu-id="e6276-112"><span id="PlugInConfiguration_OperationsConfiguration"></span><span id="pluginconfiguration_operationsconfiguration"></span><span id="PLUGINCONFIGURATION_OPERATIONSCONFIGURATION"></span>**PlugInConfiguration**/**OperationsConfiguration**</span></span>
</dt> <dd>

<span data-ttu-id="e6276-113">指定作業外掛程式的檔案名。</span><span class="sxs-lookup"><span data-stu-id="e6276-113">Specifies the file name of the operations plug-in.</span></span> <span data-ttu-id="e6276-114">當要求進入時，會在使用者的內容中展開任何放置於此專案中的環境變數。</span><span class="sxs-lookup"><span data-stu-id="e6276-114">Any environment variables that are put in this entry will be expanded in the users' context when a request comes in.</span></span> <span data-ttu-id="e6276-115">每個使用者可能會有相同環境變數的不同版本，因此每個使用者最後可能會有不同的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e6276-115">Each user could have a different version of the same environment variable, so each user could end up with a different plug-in.</span></span> <span data-ttu-id="e6276-116">這個專案不能空白，且必須指向有效的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e6276-116">This entry cannot be blank and must point to a valid plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration** /**名稱**</span><span class="sxs-lookup"><span data-stu-id="e6276-117"><span id="PlugInConfiguration_Name"></span><span id="pluginconfiguration_name"></span><span id="PLUGINCONFIGURATION_NAME"></span>**PlugInConfiguration**/**Name**</span></span>
</dt> <dd>

<span data-ttu-id="e6276-118">指定要用於外掛程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="e6276-118">Specifies the display name to use for the plug-in.</span></span> <span data-ttu-id="e6276-119">如果從外掛程式傳回錯誤，則會將此名稱放入傳回給用戶端應用程式的錯誤 XML。</span><span class="sxs-lookup"><span data-stu-id="e6276-119">If an error is returned from the plug-in, this name will be put into the error XML that is returned to the client application.</span></span> <span data-ttu-id="e6276-120">名稱不是地區設定特定名稱。</span><span class="sxs-lookup"><span data-stu-id="e6276-120">The name is not locale specific.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration** /**架構**</span><span class="sxs-lookup"><span data-stu-id="e6276-121"><span id="PlugInConfiguration_Architecture"></span><span id="pluginconfiguration_architecture"></span><span id="PLUGINCONFIGURATION_ARCHITECTURE"></span>**PlugInConfiguration**/**Architecture**</span></span>
</dt> <dd>

<span data-ttu-id="e6276-122">指定作業外掛程式是否為32位或64位。</span><span class="sxs-lookup"><span data-stu-id="e6276-122">Specifies whether the operations plug-in is 32-bit or 64-bit.</span></span> <span data-ttu-id="e6276-123">如果未指定這個元素，則在 x86 系統上的值會預設為 "32"，在64位系統上則會預設為 "64"。</span><span class="sxs-lookup"><span data-stu-id="e6276-123">If this element is not specified, the value will default to "32" on x86 systems and to "64" on 64-bit systems.</span></span> <span data-ttu-id="e6276-124">若是 x86 系統，唯一有效的值是 "32"。</span><span class="sxs-lookup"><span data-stu-id="e6276-124">For x86 systems, the only valid value is "32".</span></span> <span data-ttu-id="e6276-125">如果在64位系統上的值是 "32"，則在輸入 **檔案名** 資訊時必須將 wow64 重新導向列入考慮。</span><span class="sxs-lookup"><span data-stu-id="e6276-125">If the value is "32" on an 64-bit system, wow64 redirection needs to be taken into account when entering the **Filename** information.</span></span> <span data-ttu-id="e6276-126">基礎檔案系統會使用 wow64 重新導向，將 system32 轉譯為 syswow64。</span><span class="sxs-lookup"><span data-stu-id="e6276-126">The underlying file system will use wow64 redirection to translate system32 to syswow64.</span></span> <span data-ttu-id="e6276-127">例如，如果 **Filename** 是 "% windir% \\ system32 \\myplugin.dll" 且 **架構** 為 "32"，則實際的外掛程式檔案位於 "% windir% \\ syswow64 \\myplugin.dll"。</span><span class="sxs-lookup"><span data-stu-id="e6276-127">For example, if **Filename** is "%windir%\\system32\\myplugin.dll" and **Architecture** is "32", the actual plug-in file is located at "%windir%\\syswow64\\myplugin.dll".</span></span>

</dd> <dt>

<span data-ttu-id="e6276-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration** /**XmlRenderingType**</span><span class="sxs-lookup"><span data-stu-id="e6276-128"><span id="PlugInConfiguration_XmlRenderingType"></span><span id="pluginconfiguration_xmlrenderingtype"></span><span id="PLUGINCONFIGURATION_XMLRENDERINGTYPE"></span>**PlugInConfiguration**/**XmlRenderingType**</span></span>
</dt> <dd>

<span data-ttu-id="e6276-129">設定 XML 透過 [**WSMAN \_ 資料**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) 物件傳遞至外掛程式的格式。</span><span class="sxs-lookup"><span data-stu-id="e6276-129">Configures the format in which XML is passed to plug-ins through the [**WSMAN\_DATA**](/windows/desktop/api/Wsman/ns-wsman-wsman_data) object.</span></span> <span data-ttu-id="e6276-130">目前有下列類型可供使用：</span><span class="sxs-lookup"><span data-stu-id="e6276-130">The following types are available:</span></span>

<dl> <dt>

<span data-ttu-id="e6276-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>文本</span><span class="sxs-lookup"><span data-stu-id="e6276-131"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="e6276-132">傳入的 XML 資料會包含在 WSMAN \_ 資料 \_ 類型 \_ 文字結構中，這表示 xml 為 **PCWSTR** 記憶體緩衝區。</span><span class="sxs-lookup"><span data-stu-id="e6276-132">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_TEXT structure, which represents the XML as a **PCWSTR** memory buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader</span><span class="sxs-lookup"><span data-stu-id="e6276-133"><span id="XMLReader"></span><span id="xmlreader"></span><span id="XMLREADER"></span>XMLReader</span></span>
</dt> <dd>

<span data-ttu-id="e6276-134">傳入的 XML 資料會包含在 WSMAN \_ 資料 \_ 類型 \_ WS \_ XML \_ 讀取器結構中，它會將 XML 表示為 **XmlReader** 物件，該物件是定義于 WebServices .h 標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="e6276-134">Incoming XML data is contained in a WSMAN\_DATA\_TYPE\_WS\_XML\_READER structure, which represents the XML as an **XmlReader** object, which is defined in the WebServices.h header file.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e6276-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration** /**InitializationXml**</span><span class="sxs-lookup"><span data-stu-id="e6276-135"><span id="PlugInConfiguration_InitializationXml"></span><span id="pluginconfiguration_initializationxml"></span><span id="PLUGINCONFIGURATION_INITIALIZATIONXML"></span>**PlugInConfiguration**/**InitializationXml**</span></span>
</dt> <dd>

<span data-ttu-id="e6276-136">這個節點是選擇性的，可讓外掛程式設定將傳遞給 [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)方法的額外 XML。</span><span class="sxs-lookup"><span data-stu-id="e6276-136">This node is optional and allows a plug-in to configure extra XML that will be passed in to the [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)method.</span></span> <span data-ttu-id="e6276-137">大部分的外掛程式都不需要這項額外的資訊，但如果外掛程式需要在需要不同執行時間語義的多個案例下使用，則此 XML 將會賦予外掛程式彈性來執行這項作業。</span><span class="sxs-lookup"><span data-stu-id="e6276-137">Most plug-ins will not need this extra information, but if a plug-in needs to be used under more than one scenario that requires different run-time semantics, this XML will give the plug-in the flexibility to do this.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration** /**資源**</span><span class="sxs-lookup"><span data-stu-id="e6276-138"><span id="PlugInConfiguration_Resources"></span><span id="pluginconfiguration_resources"></span><span id="PLUGINCONFIGURATION_RESOURCES"></span>**PlugInConfiguration**/**Resources**</span></span>
</dt> <dd>

<span data-ttu-id="e6276-139">指定此外掛程式支援的 [*資源 uri*](windows-remote-management-glossary.md)清單。</span><span class="sxs-lookup"><span data-stu-id="e6276-139">Specifies a list of [*resource URIs*](windows-remote-management-glossary.md)that this plug-in supports.</span></span> <span data-ttu-id="e6276-140">至少必須指定一個 **ResourceUri** 專案;否則，XML 將會遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="e6276-140">At least one **ResourceUri** entry must be specified; otherwise, the XML will be rejected.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration** /**資源** /**資源**</span><span class="sxs-lookup"><span data-stu-id="e6276-141"><span id="PlugInConfiguration_Resources_Resource"></span><span id="pluginconfiguration_resources_resource"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE"></span>**PlugInConfiguration**/**Resources**/**Resource**</span></span>
</dt> <dd>

<span data-ttu-id="e6276-142">代表單一 [*資源 URI*](windows-remote-management-glossary.md)設定。</span><span class="sxs-lookup"><span data-stu-id="e6276-142">Represents a single [*resource URI*](windows-remote-management-glossary.md)configuration.</span></span>

> [!Note]  
> <span data-ttu-id="e6276-143">**SupportsOptions** 屬性可以設定為 false。</span><span class="sxs-lookup"><span data-stu-id="e6276-143">The **SupportsOptions** attribute can be set to false.</span></span> <span data-ttu-id="e6276-144">如果 **SupportsOptions** 設定為 false，則列舉資源時，不會列出此屬性。</span><span class="sxs-lookup"><span data-stu-id="e6276-144">If **SupportsOptions** is set to false, this attribute is not listed when the resource is enumerated.</span></span>

 

</dd> <dt>

<span data-ttu-id="e6276-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration** /**資源** /**資源** /**ResourceUri**</span><span class="sxs-lookup"><span data-stu-id="e6276-145"><span id="PlugInConfiguration_Resources_Resource_ResourceUri"></span><span id="pluginconfiguration_resources_resource_resourceuri"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_RESOURCEURI"></span>**PlugInConfiguration**/**Resources**/**Resource**/**ResourceUri**</span></span>
</dt> <dd>

<span data-ttu-id="e6276-146">以 full 或 **ExactMatch** 屬性為基礎的部分相符字串，指定單一 [*資源 URI*](windows-remote-management-glossary.md) 。</span><span class="sxs-lookup"><span data-stu-id="e6276-146">Specifies a single [*resource URI*](windows-remote-management-glossary.md) either in full or as a partial match string based on the **ExactMatch** attribute.</span></span> <span data-ttu-id="e6276-147">如果 **ExactMatch** 不存在，則會預設為 **False**，這表示 WinRM SOAP 處理器會對 *資源 URI* 的開頭進行部分相符，如果有相符的值，請將它傳遞給外掛程式。</span><span class="sxs-lookup"><span data-stu-id="e6276-147">If **ExactMatch** is not present, it defaults to **False**, which means the WinRM SOAP processor will do a partial match to the start of the *resource URI* and, if there is a match, pass it to the plug-in.</span></span> <span data-ttu-id="e6276-148">如果允許此 *資源 URI* 傳入任何選項，則可以指定 **SupportsOptions** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e6276-148">The **SupportsOptions** attribute can be specified if this *resource URI* is allowed to have any options passed in.</span></span> <span data-ttu-id="e6276-149">根據預設，不支援任何選項，如果用戶端要求中有任何選項，則會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="e6276-149">By default, no options are supported, and if any are present in the client request, an error will be returned.</span></span> <span data-ttu-id="e6276-150">如果外掛程式支援選項，則如果有外掛程式無法理解當 **mustUnderstand** 旗標設為 **True** 的選項時，外掛程式就會傳回正確的錯誤，這是很重要的。</span><span class="sxs-lookup"><span data-stu-id="e6276-150">If options are supported by the plug-in, it is important that the plug-in returns the correct error if an option is present that the plug-in does not understand when the **mustUnderstand** flag is set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration** /**資源** /**資源** /**功能**</span><span class="sxs-lookup"><span data-stu-id="e6276-151"><span id="PlugInConfiguration_Resources_Resource_Capability"></span><span id="pluginconfiguration_resources_resource_capability"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_CAPABILITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Capability**</span></span>
</dt> <dd>

<span data-ttu-id="e6276-152">指定可在此 [*資源 URI*](windows-remote-management-glossary.md)上使用的功能。</span><span class="sxs-lookup"><span data-stu-id="e6276-152">Specifies a capability that is available on this [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="e6276-153">它支援的每一種作業類型都會有一個專案。</span><span class="sxs-lookup"><span data-stu-id="e6276-153">There will be one entry for each type of operation that it supports.</span></span> <span data-ttu-id="e6276-154">可用選項如下：</span><span class="sxs-lookup"><span data-stu-id="e6276-154">The following options are available:</span></span>

<dl> <dt>

<span data-ttu-id="e6276-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>獲取</span><span class="sxs-lookup"><span data-stu-id="e6276-155"><span id="Get"></span><span id="get"></span><span id="GET"></span>Get</span></span>
</dt> <dd>

<span data-ttu-id="e6276-156">[*資源 URI*](windows-remote-management-glossary.md)支援 Get 作業。</span><span class="sxs-lookup"><span data-stu-id="e6276-156">Get operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="e6276-157">如果 get 作業支援這個概念，就會使用 **SupportFragment** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e6276-157">The **SupportFragment** attribute is used if the get operation supports the concept.</span></span> <span data-ttu-id="e6276-158">**SupportFiltering** 屬性無效，應設定為 false。</span><span class="sxs-lookup"><span data-stu-id="e6276-158">The **SupportFiltering** attribute is not valid and should be set to false.</span></span> <span data-ttu-id="e6276-159">如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="e6276-159">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>把</span><span class="sxs-lookup"><span data-stu-id="e6276-160"><span id="Put"></span><span id="put"></span><span id="PUT"></span>Put</span></span>
</dt> <dd>

<span data-ttu-id="e6276-161">[*資源 URI*](windows-remote-management-glossary.md)支援 Put 作業。</span><span class="sxs-lookup"><span data-stu-id="e6276-161">Put operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="e6276-162">如果 put 作業支援這個概念，就會使用 **SupportFragment** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e6276-162">The **SupportFragment** attribute is used if the put operation supports the concept.</span></span> <span data-ttu-id="e6276-163">**SupportFiltering** 屬性無效，應設定為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e6276-163">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="e6276-164">如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="e6276-164">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>創建</span><span class="sxs-lookup"><span data-stu-id="e6276-165"><span id="Create"></span><span id="create"></span><span id="CREATE"></span>Create</span></span>
</dt> <dd>

<span data-ttu-id="e6276-166">[*資源 URI*](windows-remote-management-glossary.md)支援建立作業。</span><span class="sxs-lookup"><span data-stu-id="e6276-166">Create operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="e6276-167">如果建立作業支援這個概念，就會使用 **SupportFragment** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e6276-167">The **SupportFragment** attribute is used if the create operation supports the concept.</span></span> <span data-ttu-id="e6276-168">**SupportFiltering** 屬性無效，應設定為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e6276-168">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="e6276-169">如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="e6276-169">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>刪除</span><span class="sxs-lookup"><span data-stu-id="e6276-170"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>Delete</span></span>
</dt> <dd>

<span data-ttu-id="e6276-171">[*資源 URI*](windows-remote-management-glossary.md)支援刪除作業。</span><span class="sxs-lookup"><span data-stu-id="e6276-171">Delete operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="e6276-172">如果刪除作業支援這個概念，就會使用 **SupportFragment** 屬性。</span><span class="sxs-lookup"><span data-stu-id="e6276-172">The **SupportFragment** attribute is used if the delete operation supports the concept.</span></span> <span data-ttu-id="e6276-173">**SupportFiltering** 屬性無效，應設定為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e6276-173">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="e6276-174">如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="e6276-174">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>調用</span><span class="sxs-lookup"><span data-stu-id="e6276-175"><span id="Invoke"></span><span id="invoke"></span><span id="INVOKE"></span>Invoke</span></span>
</dt> <dd>

<span data-ttu-id="e6276-176">[*資源 URI*](windows-remote-management-glossary.md)支援 Invoke 作業。</span><span class="sxs-lookup"><span data-stu-id="e6276-176">Invoke operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="e6276-177">Invoke 作業不支援 **SupportFragment** 屬性，應設定為 false。</span><span class="sxs-lookup"><span data-stu-id="e6276-177">The **SupportFragment** attribute is not supported for invoke operations and should be set to false.</span></span> <span data-ttu-id="e6276-178">**SupportFiltering** 屬性無效，應設定為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e6276-178">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="e6276-179">如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="e6276-179">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>枚舉</span><span class="sxs-lookup"><span data-stu-id="e6276-180"><span id="Enumerate"></span><span id="enumerate"></span><span id="ENUMERATE"></span>Enumerate</span></span>
</dt> <dd>

<span data-ttu-id="e6276-181">[*資源 URI*](windows-remote-management-glossary.md)支援列舉作業。</span><span class="sxs-lookup"><span data-stu-id="e6276-181">Enumerate operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="e6276-182">列舉作業不支援 **SupportFragment** 屬性，應設定為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e6276-182">The **SupportFragment** attribute is not supported for enumerate operations and should be set to **False**.</span></span> <span data-ttu-id="e6276-183">**SupportFiltering** 屬性是有效的，而且如果外掛程式支援篩選，則應該將此屬性設定為 **True**。</span><span class="sxs-lookup"><span data-stu-id="e6276-183">The **SupportFiltering** attribute is valid, and if the plug-in supports filtering this attribute should be set to **True**.</span></span> <span data-ttu-id="e6276-184">如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="e6276-184">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>訂閱</span><span class="sxs-lookup"><span data-stu-id="e6276-185"><span id="Subscribe"></span><span id="subscribe"></span><span id="SUBSCRIBE"></span>Subscribe</span></span>
</dt> <dd>

<span data-ttu-id="e6276-186">[*資源 URI*](windows-remote-management-glossary.md)支援訂閱作業。</span><span class="sxs-lookup"><span data-stu-id="e6276-186">Subscribe operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="e6276-187">訂閱作業不支援 **SupportFragment** 屬性，應設定為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e6276-187">The **SupportFragment** attribute is not supported for subscribe operations and should be set to **False**.</span></span> <span data-ttu-id="e6276-188">**SupportFiltering** 屬性無效，應設定為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e6276-188">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="e6276-189">如果也支援 shell 作業，則這項功能對 *資源 URI* 而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="e6276-189">This capability is not valid for a *resource URI* if shell operations are also supported.</span></span>

</dd> <dt>

<span data-ttu-id="e6276-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>殼</span><span class="sxs-lookup"><span data-stu-id="e6276-190"><span id="Shell"></span><span id="shell"></span><span id="SHELL"></span>Shell</span></span>
</dt> <dd>

<span data-ttu-id="e6276-191">[*資源 URI*](windows-remote-management-glossary.md)支援 Shell 作業。</span><span class="sxs-lookup"><span data-stu-id="e6276-191">Shell operations are supported on the [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="e6276-192">Shell 作業不支援 **SupportFragment** 屬性，應設定為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e6276-192">The **SupportFragment** attribute is not supported for shell operations and should be set to **False**.</span></span> <span data-ttu-id="e6276-193">**SupportFiltering** 屬性無效，應設定為 **False**。</span><span class="sxs-lookup"><span data-stu-id="e6276-193">The **SupportFiltering** attribute is not valid and should be set to **False**.</span></span> <span data-ttu-id="e6276-194">如果也支援任何其他作業功能，這項功能對 *資源 URI* 而言是不正確。</span><span class="sxs-lookup"><span data-stu-id="e6276-194">This capability is not valid for a *resource URI* if any other operation capability is also supported.</span></span> <span data-ttu-id="e6276-195">如果 shell 作業功能設定為 *資源 URI*，則 get、put、create、delete、invoke 和列舉作業會在 WinRm 服務內部處理，以管理 shell。</span><span class="sxs-lookup"><span data-stu-id="e6276-195">If a shell operation capability is configured for a *resource URI*, then get, put, create, delete, invoke, and enumerate operations are processed internally within the WinRm service to manage shells.</span></span> <span data-ttu-id="e6276-196">因此，外掛程式無法處理作業本身。</span><span class="sxs-lookup"><span data-stu-id="e6276-196">As a result, the plug-in cannot deal with the operations itself.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="e6276-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration** /**資源** /**資源** /**安全性**</span><span class="sxs-lookup"><span data-stu-id="e6276-197"><span id="PlugInConfiguration_Resources_Resource_Security"></span><span id="pluginconfiguration_resources_resource_security"></span><span id="PLUGINCONFIGURATION_RESOURCES_RESOURCE_SECURITY"></span>**PlugInConfiguration**/**Resources**/**Resource**/**Security**</span></span>
</dt> <dd>

<span data-ttu-id="e6276-198">這個元素會透過 **Sddl** 屬性定義安全描述項 (，) 應該套用此屬性，以透過 **URI** 屬性) 來判斷特定 [*資源 URI*](windows-remote-management-glossary.md) (的存取權。</span><span class="sxs-lookup"><span data-stu-id="e6276-198">This element defines the security descriptor (via the **Sddl** attribute) that should be applied to determine access to a particular [*resource URI*](windows-remote-management-glossary.md) (via the **Uri** attribute).</span></span> <span data-ttu-id="e6276-199">如果 **ExactMatch** 不存在，**安全性** 元素就會預設為 **False**，這表示 **Sddl** 會套用至共用 **Uri** 做為前置詞的所有 *資源 uri* 。</span><span class="sxs-lookup"><span data-stu-id="e6276-199">If **ExactMatch** is not present, the **Security** element defaults to **False**, which means that the **Sddl** applies to all *resource URIs* that share **Uri** as a prefix.</span></span> <span data-ttu-id="e6276-200">如果 **ExactMatch** 設定為 true，則 **Sddl** 只適用于指定的確切 **Uri** 。</span><span class="sxs-lookup"><span data-stu-id="e6276-200">If **ExactMatch** is set to true, the **Sddl** applies only to the exact **Uri** specified.</span></span> <span data-ttu-id="e6276-201">如果有多個可套用至特定 *資源 uri* 的 **安全性** 專案，則會使用最長的前置詞比對來判斷適當的 **Sddl**。</span><span class="sxs-lookup"><span data-stu-id="e6276-201">If there are multiple **Security** entries that could apply to a particular *resource URIs*, the longest-prefix match is used to determine the appropriate **Sddl**.</span></span> <span data-ttu-id="e6276-202">由於有最長的前置詞相符專案，因此，如果有完全相符的 **Uri** 專案存在，一律會將其選擇為適當的安全性元素。</span><span class="sxs-lookup"><span data-stu-id="e6276-202">As a result of the longest-prefix match, if an exact-match **Uri** entry exists, it will always be chosen as the appropriate Security element.</span></span>

</dd> </dl>

<span data-ttu-id="e6276-203">以下是指定為 XSD 的外掛程式設定架構。</span><span class="sxs-lookup"><span data-stu-id="e6276-203">The following is the plug-in configuration schema specified as an XSD.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8"?>
<xs:schema attributeFormDefault="unqualified" 
           elementFormDefault="qualified" 
           targetNamespace="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns="http://schemas.microsoft.com/wbem/wsman/1/config/PluginConfiguration" 
           xmlns:xs="https://www.w3.org/2001/XMLSchema">
 <xs:element name="PlugInConfiguration">
  <xs:complexType>
   <xs:sequence>
    <xs:element name="InitializationParameters" minOccurs="0" maxOccurs="1">
     <xs:complexType>
      <xs:sequence>
       <xs:element name="Param">
        <xs:complexType>
         <xs:sequence></xs:sequence>
         <xs:attribute name="Name" type="xs:string"/>
         <xs:attribute name="Value" type="xs:string"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
    <xs:element name="Resources">
     <xs:complexType>
      <xs:sequence>
       <xs:element minOccurs="1" maxOccurs="unbounded" name="Resource">
        <xs:complexType>
         <xs:sequence>
          <xs:element name="Capability" minOccurs="1" maxOccurs="unbounded">
           <xs:complexType>
            <xs:simpleContent>
             <xs:extension base="ResourceCapabilityType">
              <xs:attribute name="SupportsFragment" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="SupportsFiltering" type="xs:boolean" use="optional" default="false"/>
              <xs:attribute name="Type" type="ResourceCapabilityType"/>
             </xs:extension>
            </xs:simpleContent>
           </xs:complexType>
          </xs:element>
          <xs:element name="Security" minOccurs="0" maxOccurs="unbounded">
           <xs:complexType>
            <xs:sequence></xs:sequence>
            <xs:attribute name="Uri" type="xs:string"/>
            <xs:attribute name="Sddl" type="xs:string"/>
            <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
           </xs:complexType>
          </xs:element>
         </xs:sequence>
         <xs:attribute name="ResourceUri" type="xs:string"/>
         <xs:attribute name="ExactMatch" type="xs:boolean" use="optional" default="false"/>
         <xs:attribute name="SupportOptions" type="xs:boolean" use="optional" default="false"/>
        </xs:complexType>
       </xs:element>
      </xs:sequence>
     </xs:complexType>
    </xs:element>
   </xs:sequence>
   <xs:attribute name="Filename" type="xs:token"/>
   <xs:attribute name="SDKVersion" type="xs:unsignedInt"/>
   <xs:attribute name="Name" type="xs:string"/>
   <xs:attribute name="XmlRenderingType" type="XmlRenderingTypeType" use="optional" default="text"/>
   <!--Architecture will default to 32 on x86 systems; 64 on 64-bit systems.-->
   <xs:attribute name="Architecture" type="ArchitectureType" use="optional" default="32"/>
  </xs:complexType>
 </xs:element>
 <xs:simpleType name="ResourceCapabilityType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="Get"/>
   <xs:enumeration value="Put"/>
   <xs:enumeration value="Create"/>
   <xs:enumeration value="Delete"/>
   <xs:enumeration value="Invoke"/>
   <xs:enumeration value="Enumerate"/>
   <xs:enumeration value="Subscribe"/>
   <xs:enumeration value="Shell"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="XmlRenderingTypeType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="text"/>
   <xs:enumeration value="XmlReader"/>
  </xs:restriction>
 </xs:simpleType>
 <xs:simpleType name="ArchitectureType">
  <xs:restriction base="xs:token">
   <xs:enumeration value="32"/>
   <xs:enumeration value="64"/>
  </xs:restriction>
 </xs:simpleType>
</xs:schema>
```

 

 




