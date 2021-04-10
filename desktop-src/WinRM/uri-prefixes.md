---
title: URI 首碼
description: 資源 URI 前置詞會根據描述資源的 XML 架構而有所不同。
ms.assetid: 47c32da6-98c9-4f66-82ac-647976127cb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e73de4d6d1762e87aa05e72b6cb6b3fbb228b80d
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "103842860"
---
# <a name="uri-prefixes"></a><span data-ttu-id="1bdb2-103">URI 首碼</span><span class="sxs-lookup"><span data-stu-id="1bdb2-103">URI prefixes</span></span>

<span data-ttu-id="1bdb2-104">[*資源 URI*](windows-remote-management-glossary.md)前置詞會根據描述資源的 XML 架構而有所不同。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-104">The [*resource URI*](windows-remote-management-glossary.md) prefix is different depending on which XML schema describes the resource.</span></span>

## <a name="prefixes"></a><span data-ttu-id="1bdb2-105">首碼</span><span class="sxs-lookup"><span data-stu-id="1bdb2-105">Prefixes</span></span>

<span data-ttu-id="1bdb2-106">如果您存取 cim [*2.1 類別*](windows-remote-management-glossary.md) ，例如 [**cim \_ 資料檔案**](/windows/desktop/CIMWin32Prov/cim-datafile)，URI 的前置詞會與 cim 2.9 類別的前置詞不同，例如 **cim \_ AdminDomain**。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-106">If you access a [*CIM*](windows-remote-management-glossary.md) 2.1 class, such as [**CIM\_DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile), the prefix of the URI differs from the prefix for a CIM 2.9 class, such as **CIM\_AdminDomain**.</span></span> <span data-ttu-id="1bdb2-107">CIM 2.1 類別記載于 Windows Management Instrumentation (WMI) 的 [Cim 類別](/windows/desktop/WmiSdk/cimclas) 一節中。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-107">CIM 2.1 classes are documented in the [CIM Classes](/windows/desktop/WmiSdk/cimclas) section of Windows Management Instrumentation (WMI).</span></span>

<span data-ttu-id="1bdb2-108">大部分的 [wmi 類別](/windows/desktop/WmiSdk/wmi-classes) 都是在 **根 \\ cimv2** wmi 命名空間中。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-108">Most [WMI classes](/windows/desktop/WmiSdk/wmi-classes) are in the **root\\cimv2** WMI namespace.</span></span> <span data-ttu-id="1bdb2-109">適用于 Microsoft 智慧型平臺管理介面 ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) 提供者的類別位於 **根 \\ 硬體** 中。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-109">Classes for the Microsoft Intelligent Platform Management Interface ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) provider are in **root\\hardware**.</span></span>

<span data-ttu-id="1bdb2-110">下列清單包含這些架構的資源 URI 首碼：</span><span class="sxs-lookup"><span data-stu-id="1bdb2-110">The following list contains the resource URI prefixes for these schemas:</span></span>

-   <span data-ttu-id="1bdb2-111">**根 \\ cimv2** 命名空間中的 WMI 或 CIM 2.1 類別</span><span class="sxs-lookup"><span data-stu-id="1bdb2-111">WMI or CIM 2.1 classes in the **root\\cimv2** namespace</span></span>

    <span data-ttu-id="1bdb2-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span><span class="sxs-lookup"><span data-stu-id="1bdb2-112">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"</span></span>

-   <span data-ttu-id="1bdb2-113">CIM 2.9 類別或 IPMI 類別</span><span class="sxs-lookup"><span data-stu-id="1bdb2-113">CIM 2.9 classes or IPMI classes</span></span>

    <span data-ttu-id="1bdb2-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span><span class="sxs-lookup"><span data-stu-id="1bdb2-114">"https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"</span></span>

-   <span data-ttu-id="1bdb2-115">存取 IPMI 提供者類別的替代方式</span><span class="sxs-lookup"><span data-stu-id="1bdb2-115">Alternate way to access IPMI provider classes</span></span>

    <span data-ttu-id="1bdb2-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span><span class="sxs-lookup"><span data-stu-id="1bdb2-116">"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"</span></span>

<span data-ttu-id="1bdb2-117">如需詳細資訊，請參閱 [資源 uri](resource-uris.md) 和 [UrlPrefix 字串](/windows/desktop/Http/urlprefix-strings)。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-117">For more information, see [Resource URIs](resource-uris.md) and [UrlPrefix Strings](/windows/desktop/Http/urlprefix-strings).</span></span> <span data-ttu-id="1bdb2-118">如需有關為 WMI 類別或方法產生 URI 的詳細資訊，請參閱 [Windows 遠端管理和 wmi](windows-remote-management-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-118">For more information about generating a URI for a WMI class or method, see [Windows Remote Management and WMI](windows-remote-management-and-wmi.md).</span></span>

## <a name="prefix-aliases"></a><span data-ttu-id="1bdb2-119">前置詞別名</span><span class="sxs-lookup"><span data-stu-id="1bdb2-119">Prefix Aliases</span></span>

<span data-ttu-id="1bdb2-120">前置別名是代表長資源 URI 前置詞的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-120">A prefix alias is a shortcut that represents the long resource URI prefix.</span></span> <span data-ttu-id="1bdb2-121">您也可以在 **Winrm** 命令列中使用別名。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-121">You can also use aliases in the **Winrm** command-line.</span></span> <span data-ttu-id="1bdb2-122">若要查看可用的別名清單，請輸入 **Winrm help 別名**。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-122">To view a list of available aliases, type **Winrm help aliases**.</span></span>

<span data-ttu-id="1bdb2-123">請注意，在指定資源 URI 時，無法在端點參考 (EPR) 內使用別名。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-123">Be aware that an alias cannot be used inside an endpoint reference (EPR) when specifying a resource URI.</span></span> <span data-ttu-id="1bdb2-124">Windows 遠端管理在內嵌于 XML 時無法展開別名。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-124">Windows Remote Management is unable to expand the alias when it is embedded in XML.</span></span>

<span data-ttu-id="1bdb2-125">在下列程式碼範例中，會在 EPR 中使用 winrm 別名，而不是完整的資源 URI，也就是 `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` 。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-125">In the following code example, the winrm alias is used in an EPR instead of the complete resource URI, which is `http://schemas.microsoft.com/wbem/wsman/1/config/Listener`.</span></span> <span data-ttu-id="1bdb2-126">在此情況下，WinRM 會傳回錯誤，指出服務無法處理要求。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-126">In this case, WinRM returns an error that indicates the service cannot process the request.</span></span>


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



<span data-ttu-id="1bdb2-127">以下列出它們所取代的已定義別名和資源 Uri。</span><span class="sxs-lookup"><span data-stu-id="1bdb2-127">The following lists defined aliases and resource URIs for which they substitute.</span></span>

<dl> <dt>

<span data-ttu-id="1bdb2-128"><span id="wmi"></span><span id="WMI"></span>Wmi</span><span class="sxs-lookup"><span data-stu-id="1bdb2-128"><span id="wmi"></span><span id="WMI"></span>wmi</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span data-ttu-id="1bdb2-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span><span class="sxs-lookup"><span data-stu-id="1bdb2-129"><span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span data-ttu-id="1bdb2-130"><span id="cimv2"></span><span id="CIMV2"></span>cimv2</span><span class="sxs-lookup"><span data-stu-id="1bdb2-130"><span id="cimv2"></span><span id="CIMV2"></span>cimv2</span></span>
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span data-ttu-id="1bdb2-131"><span id="winrm"></span><span id="WINRM"></span>winrm</span><span class="sxs-lookup"><span data-stu-id="1bdb2-131"><span id="winrm"></span><span id="WINRM"></span>winrm</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="1bdb2-132"><span id="wsman"></span><span id="WSMAN"></span>wsman</span><span class="sxs-lookup"><span data-stu-id="1bdb2-132"><span id="wsman"></span><span id="WSMAN"></span>wsman</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span data-ttu-id="1bdb2-133"><span id="shell"></span><span id="SHELL"></span>殼</span><span class="sxs-lookup"><span data-stu-id="1bdb2-133"><span id="shell"></span><span id="SHELL"></span>shell</span></span>
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="1bdb2-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="1bdb2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bdb2-135">關於 Windows 遠端管理</span><span class="sxs-lookup"><span data-stu-id="1bdb2-135">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="1bdb2-136">Windows 遠端管理和 WMI</span><span class="sxs-lookup"><span data-stu-id="1bdb2-136">Windows Remote Management and WMI</span></span>](windows-remote-management-and-wmi.md)
</dt> <dt>

[<span data-ttu-id="1bdb2-137">資源 URI</span><span class="sxs-lookup"><span data-stu-id="1bdb2-137">Resource URIs</span></span>](resource-uris.md)
</dt> </dl>
