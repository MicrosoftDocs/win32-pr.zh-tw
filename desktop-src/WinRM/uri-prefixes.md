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
# <a name="uri-prefixes"></a>URI 首碼

[*資源 URI*](windows-remote-management-glossary.md)前置詞會根據描述資源的 XML 架構而有所不同。

## <a name="prefixes"></a>首碼

如果您存取 cim [*2.1 類別*](windows-remote-management-glossary.md) ，例如 [**cim \_ 資料檔案**](/windows/desktop/CIMWin32Prov/cim-datafile)，URI 的前置詞會與 cim 2.9 類別的前置詞不同，例如 **cim \_ AdminDomain**。 CIM 2.1 類別記載于 Windows Management Instrumentation (WMI) 的 [Cim 類別](/windows/desktop/WmiSdk/cimclas) 一節中。

大部分的 [wmi 類別](/windows/desktop/WmiSdk/wmi-classes) 都是在 **根 \\ cimv2** wmi 命名空間中。 適用于 Microsoft 智慧型平臺管理介面 ([IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)) 提供者的類別位於 **根 \\ 硬體** 中。

下列清單包含這些架構的資源 URI 首碼：

-   **根 \\ cimv2** 命名空間中的 WMI 或 CIM 2.1 類別

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/"

-   CIM 2.9 類別或 IPMI 類別

    "https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2"

-   存取 IPMI 提供者類別的替代方式

    "http://schemas.microsoft.com/wbem/wsman/1/wmi/root/hardware/"

如需詳細資訊，請參閱 [資源 uri](resource-uris.md) 和 [UrlPrefix 字串](/windows/desktop/Http/urlprefix-strings)。 如需有關為 WMI 類別或方法產生 URI 的詳細資訊，請參閱 [Windows 遠端管理和 wmi](windows-remote-management-and-wmi.md)。

## <a name="prefix-aliases"></a>前置詞別名

前置別名是代表長資源 URI 前置詞的快捷方式。 您也可以在 **Winrm** 命令列中使用別名。 若要查看可用的別名清單，請輸入 **Winrm help 別名**。

請注意，在指定資源 URI 時，無法在端點參考 (EPR) 內使用別名。 Windows 遠端管理在內嵌于 XML 時無法展開別名。

在下列程式碼範例中，會在 EPR 中使用 winrm 別名，而不是完整的資源 URI，也就是 `http://schemas.microsoft.com/wbem/wsman/1/config/Listener` 。 在此情況下，WinRM 會傳回錯誤，指出服務無法處理要求。


```XML
ResourceUri = "</wxf:ResourceCreated>.....
<w:ResourceURI>winrm/config/listener</w:ResourceURI>...
</w:SelectorSet></a:ReferenceParameters></wxf:ResourceCreated>"

Set ResourceLocator = WSManObj.CreateResourceLocator(resourceUri)
ResponseStr = Session.Get(ResourceLocator, 0)
```



以下列出它們所取代的已定義別名和資源 Uri。

<dl> <dt>

<span id="wmi"></span><span id="WMI"></span>Wmi
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi`

</dd> <dt>

<span id="wmicimv2"></span><span id="WMICIMV2"></span>wmicimv2
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2`

</dd> <dt>

<span id="cimv2"></span><span id="CIMV2"></span>cimv2
</dt> <dd>

`https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2`

</dd> <dt>

<span id="winrm"></span><span id="WINRM"></span>winrm
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="wsman"></span><span id="WSMAN"></span>wsman
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1`

</dd> <dt>

<span id="shell"></span><span id="SHELL"></span>殼
</dt> <dd>

`http://schemas.microsoft.com/wbem/wsman/1/windows/shell`

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md)
</dt> <dt>

[資源 URI](resource-uris.md)
</dt> </dl>
