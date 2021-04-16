---
title: 資源 URI
description: 資源 URI 是管理作業的相異類型識別碼，或管理服務用來執行 WS-Management 通訊協定的值。
ms.assetid: 478a6e5d-0675-462e-b2fd-fd2b5379e298
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 665c73caf5cf636ab7f0a0162f488ff073917984
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104507931"
---
# <a name="resource-uris"></a>資源 URI

[*資源 URI*](windows-remote-management-glossary.md)是管理作業的相異類型識別碼，或管理服務用來執行 WS-Management 通訊協定的值。 管理值可能是電腦內的溫度。 管理作業的範例是啟動已停止的服務或設定磁片區使用者配額。

## <a name="resource-uri-format"></a>資源 URI 格式

URI 是由前置詞和資源路徑所組成，如下列範例所示：

"http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32\_LogicalDisk"

此架構規格指出 URI 是以正式 WS-Management 通訊協定的第1版為基礎，而且資源是 WMI 儲存機制的「根 cimv2」命名空間中的 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) \\ 。 URI 首碼包含架構規格，例如 "schemas.microsoft.com/wbem/wsman/1/wmi" 和特定類型的資源，例如 **Win32 \_ LogicalDisk**。 如需識別 WMI 類別之特定實例的詳細資訊，請參閱 [Windows 遠端管理和 wmi](windows-remote-management-and-wmi.md)。

如需詳細資訊，請參閱 [URI 首碼](uri-prefixes.md)。

## <a name="types-of-resource-uris"></a>資源 Uri 的類型

雖然 [*Windows Management Instrumentation (WMI)*](windows-remote-management-glossary.md) 是 Windows 作業系統之管理資料的主要來源，但也存在其他的管理架構來源。

下列清單描述 Windows 遠端管理所使用的幾種資源 Uri 類型：

-   WMI Uri

    這組 Uri 代表 [*通用訊息模型*](/windows/desktop/WmiSdk/gloss-c) 類別路徑，其中包含命名空間和類別。

    WMI Uri 可用於：

    -   [**會話**](session.md) 方法
    -   [**Iwsmansession.invoke**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession) 方法
    -   [**WSMan. CreateResourceLocator**](wsman-createresourcelocator.md) 或 [**IWSMan. CreateResourceLocator**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-createresourcelocator) 方法
    -   [**ResourceLocator**](resourcelocator.md) 或 [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) 方法

-   IPMI Uri

    這組 Uri 代表以 CIM 2.9 版為基礎的產業標準 Uri。 IPMI Uri 可以在 [**會話**](session.md) 方法中使用 [**Get**](session-get.md)、 [**Put**](session-put.md)、 [**列舉**](session-enumerate.md) 和 [**Invoke**](session-invoke.md)。

    例如 https://schemas.dmtf.org/wbem/wscim/1/cim-schema/2/CIM_NumericSensor.xsd。 此資源是根據 [DMTF.org](https://www.dmtf.org/home) CIM 架構來定義。

-   WinRM 設定 Uri

    這組 Uri [*是 WinRM 接聽*](windows-remote-management-glossary.md) 程式設定的設定作業。

    https://schemas.microsoft.com/wbem/wsman/1/config/listener 可以在 [**會話**](session.md) 方法中使用 [**Get**](session-get.md)、 [**Put**](session-put.md)、 [**Create**](session-create.md)、 [**Delete**](session-delete.md)和 [**列舉**](session-enumerate.md)。

-   [*系統事件記錄*](windows-remote-management-glossary.md) 檔 () URI 的選取專案

    這組 Uri 會訂閱來自 BMC 的事件收集器事件。 您可以使用 **Wevtutil** 命令列工具來訂閱這些事件。 如需詳細資訊，請參閱https://schemas.microsoft.com/wbem/wsman/1/logrecord/sel。

## <a name="case-sensitivity"></a>區分大小寫

[*WMI 外掛程式*](windows-remote-management-glossary.md)會保留在要求中收到的資源 URI 大小寫。 不過，為了確保與其他 WS-Management 通訊協定的執行互通性，請在資源 URI 中針對要求的資源使用正確的大小寫。 正確的大小寫是資源提供者所定義的拼寫。

雖然資源 Uri 不需要區分大小寫，但 [*片段*](windows-remote-management-glossary.md) XML 會有。 片段只會指定一個屬性，而不會指定資源的整個屬性集。 在 WMI 資源的案例中，片段語法會從資源實例取得一個屬性。 例如，從 [**Win32 \_ 作業系統**](/windows/desktop/CIMWin32Prov/win32-operatingsystem)取得 **版本** 屬性需要使用片段。 如需片段的詳細資訊，請參閱 [Windows 遠端管理和 WMI](windows-remote-management-and-wmi.md)中的「將選取器新增至 ResourceLocator 或 IWSManResourceLocator 物件」。

依照 XML 和 [*XPath*](windows-remote-management-glossary.md) 標準， [*WMI 外掛程式*](windows-remote-management-glossary.md) 會針對定義方法之輸入參數的片段和 XML 強制區分大小寫。 必須區分大小寫，才能支援 XPath 1.0/層級1標準。 若要透過 WinRM 取得 WMI 資料，區分大小寫表示 WMI 類別、屬性和方法的名稱必須符合 WMI 儲存機制中找到之名稱的大小寫。

如需詳細資訊，請參閱 [XPath 語法](/previous-versions/dotnet/netframework-4.0/ms256471(v=vs.100))。

## <a name="case-sensitivity-examples"></a>區分大小寫範例

例如，從 WMI [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service)類別的實例取得 **安全 \_ 描述項** 屬性的腳本，不能使用大寫作為片段路徑中的名稱，只使用 URI。 WinRM [*WMI 外掛程式*](windows-remote-management-glossary.md) 會傳回下列 VBScript 範例的錯誤，因為提供給 **FRAGMENTPATH** 的 XPath XML 未使用正確的大小寫。 在 WMI 儲存機制中，類別的拼寫為「Win32 \_ 服務」。


```VB
RResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_& "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_SERVICE/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



下列版本的相同範例顯示 [**Win32 \_ 服務**](/windows/desktop/CIMWin32Prov/win32-service) 類別和 **安全 \_ 描述項** 屬性的正確用法。


```VB
ResourceUri = "http://schemas.microsoft.com/wbem/wsman/1/"_
    & "wmi/root/cimv2/Win32_Service?Name=winrm"
Set WSMan = CreateObject("WSMan.Automation")
Set Locator = WSMan.CreateResourceLocator(Resourceuri)
Locator.FragmentPath = "/Win32_Service/Name"
Set Session = WSMan.Createsession
xml = Session.Get(Locator)
WScript.Echo xml
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> <dt>

[遠端硬體管理](remote-hardware-management.md)
</dt> <dt>

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 