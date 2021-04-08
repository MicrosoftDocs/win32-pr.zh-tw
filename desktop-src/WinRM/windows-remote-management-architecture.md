---
title: Windows 遠端管理架構
description: Windows 遠端管理的架構是由用戶端和伺服器電腦上的元件所組成。
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682829"
---
# <a name="windows-remote-management-architecture"></a>Windows 遠端管理架構

Windows 遠端管理的架構是由用戶端和伺服器電腦上的元件所組成。 下圖顯示兩部電腦上的元件、元件與其他元件的互動方式，以及用來在電腦之間通訊的通訊協定。

![winrm 架構](images/winrm-architecture.png)

## <a name="requesting-client"></a>要求用戶端

下列 WinRM 元件位於執行要求資料之腳本的電腦上。

-   WinRM 應用程式

    這是腳本或 **winrm** 命令列工具，使用 WINRM 腳本 API 對要求資料進行呼叫，或執行方法。 如需詳細資訊，請參閱 [WinRM 腳本 API](winrm-scripting-api.md)。

-   WSMAuto.dll

    提供腳本支援的自動化層。

-   WsmCL.dll

    作業系統內的 C API 層。

-   HTTP API

    WinRM 需要 HTTP 和 HTTPS 傳輸的支援。

## <a name="responding-server"></a>回應伺服器

下列 WinRM 元件位於回應的電腦上。

-   HTTP API

    WinRM 需要 HTTP 和 HTTPS 傳輸的支援。

-   WSMAuto.dll

    提供腳本支援的自動化層。

-   WsmCL.dll

    作業系統內的 C API 層。

-   WsmSvc.dll

    WinRM [*接聽*](windows-remote-management-glossary.md) 程式服務。

-   WsmProv.dll

    提供者子系統。

-   WsmRes.dll

    資源檔。

-   WsmWmiPl.dll

    [*WMI 外掛程式*](windows-remote-management-glossary.md)。 這可讓您透過 WinRM 取得 WMI 資料。

-   智慧型平臺管理介面 (IPMI) 驅動程式和 WMI IPMI 提供者

    這些元件提供使用 IPMI 類別要求的任何硬體資料。 如需詳細資訊，請參閱 [IPMI 提供者](/previous-versions/windows/desktop/ipmiprv/ipmi-provider)。 您必須透過載入驅動程式，以手動方式在 SMBIOS 或裝置上偵測到 BMC 硬體。 如需詳細資訊，請參閱 [Windows 遠端管理的安裝和](installation-and-configuration-for-windows-remote-management.md)設定。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於 Windows 遠端管理](about-windows-remote-management.md)
</dt> </dl>

 

 