---
title: BITS Compact Server
description: 背景智慧型傳送服務 (位) Compact Server 是一種獨立的 HTTP/HTTPS 檔案伺服器，可讓您在電腦之間以非同步方式傳輸有限數量的大型檔案。
ms.assetid: ab4cf901-6d93-433c-b1b2-ffa54d10725c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40e2840c24e15379fac11a5a12ed76c225e7be5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842524"
---
# <a name="bits-compact-server"></a>BITS Compact Server

背景智慧型傳送服務 (位) Compact Server 是一種獨立的 HTTP/HTTPS 檔案伺服器，可讓您在電腦之間以非同步方式傳輸有限數量的大型檔案。 Compact Server 是以 NT 服務的形式建立，並且使用 HTTP.SYS。

在下列情況下，企業和小型企業客戶會使用 BITS Compact 伺服器：

-   預期的使用量最多可有25個 URL 群組，且每個 URL 群組都支援3個同時進行的檔案傳輸。
-   在相同網域或互相信任網域中的電腦之間進行檔案傳輸。
-   檔案傳輸並非適用于網際網路面向的用戶端。

## <a name="installing-the-bits-compact-server"></a>安裝 BITS Compact Server

BITS Compact Server 是選擇性的伺服器元件。 您可以使用下列其中一個選項來安裝 BITS Compact 伺服器：

-   伺服器管理員

-   Windows PowerShell

-   套件管理員

**使用伺服器管理員安裝 BITS Compact Server**

1.  在 **伺服器管理員** 的 [**功能摘要**] 區段中，按一下 [**新增功能**]。
2.  在 [新增功能] 嚮導中，選取 **背景智慧型傳送服務 (位)** 和 **Compact Server**。
3.  遵循 wizard 的指示，包括安裝必要的軟體（如有指定）。

如需詳細資訊，請參閱 **伺服器管理員** 線上說明。

**使用 Windows PowerShell 安裝 BITS Compact Server**

1.  在 Windows PowerShell 命令提示字元中，輸入下列命令： **Import-module ServerManager**。 然後按 Enter。
2.  輸入下列命令： **ADD-WINDOWSFEATURE BITS-Compact-Server**。 然後按 Enter。

下列以文字為基礎的範例示範如何使用 Windows PowerShell Cmdlet 來安裝 BITS Compact Server。

``` syntax
PS C:\> Import-Module ServerManager
PS C:\> Add-WindowsFeature BITS-Compact-Server

Success Restart Needed Exit Code Feature Result
------- -------------- --------- --------------
True    No             Success   {Compact Server}


PS C:\>
```

如需使用 Cmdlet 的詳細資訊，請參閱 [Windows PowerShell](https://msdn.microsoft.com/library/dd835506(v=vs.85).aspx) 檔。

如需 Import-Module Cmdlet 的詳細資訊，請參閱 Microsoft TechNet Library 中的 [import-module](/previous-versions//dd347701(v=technet.10)) 。 如需命令列的說明，請輸入 **get-help import-module**。

如需 Add-WindowsFeature Cmdlet 的詳細資訊，請參閱 Microsoft TechNet Library 中的 [add-windowsfeature](/previous-versions//dd347701(v=technet.10)) 。 如需命令列的說明，請輸入 **Get-help 附加程式**。

**使用封裝管理員安裝 BITS Compact Server**

-   輸入下列命令： **PkgMgr.exe/iu： LightweightServer**。

> [!Note]  
> 如果 Compact Server 服務已重新開機或電腦重新開機，則設定會遺失。

 

## <a name="bits-compact-server-remote-management"></a>BITS Compact Server 遠端系統管理

BITS Compact Server 搭配 BITS 遠端系統管理，可提供更安全的遠端檔案傳輸。 BITS 遠端系統管理使用 Windows Management Instrumentation (WMI) 提供者，讓系統管理員或控制器應用程式在用戶端上遠端建立 BITS 傳送工作，以及發佈要在 BITS Compact 伺服器上裝載的檔案。 BITS 提供者也可用來讓應用程式能夠從遠端使用 BITS 用戶端搭配 BITS Compact 伺服器，以將檔案從一部遠端電腦傳送到另一部遠端電腦。

如需詳細資訊，請參閱 [位提供者](/previous-versions/windows/desktop/bitsprov/bits-provider) 檔。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[位提供者](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> </dl>

 

 