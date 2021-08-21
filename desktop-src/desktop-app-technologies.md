---
description: 本文提供適用于 Windows 功能和技術的可用 Win32 api 相關檔的索引。
ms.assetid: FF115416-220F-4FCD-8690-F9C0890CD6CC
title: 桌面應用程式技術
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd764c23b38e7239cea1d4d26d018ecbf9711b22
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812213"
---
# <a name="desktop-app-technologies"></a>桌面應用程式技術

本節提供有關使用 WIN32 API 的桌面應用程式可用 Windows 功能的深入指引和程式碼範例。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述  |  
|----------------------------------|---|
| [協助工具](accessibility/accessibility.md) | 針對設計可存取應用程式 Windows 的開發人員、輔助技術開發人員（例如螢幕閱讀程式和放大鏡），以及建立自動化腳本來測試 Windows 應用程式的軟體測試工程師，提供指引。 |
| [傳統型使用者介面](windows-application-ui-development.md) | 提供可讓您為應用程式開發圖形使用者介面的資訊，包括 windows 和訊息、資源和控制項等功能。 |
| [桌面環境](user-interface.md) | 提供整合和延伸 Windows 桌面使用者面向功能的指引，包括工作列、桌上型電腦和檔案總管。 |
| [應用程式安裝和維護](application-installing-and-servicing.md) | 提供有關使用 Windows 所提供之 api 和服務的資訊，以安裝、管理和服務您的桌面應用程式。 |
| [音訊與視訊](audio-and-video.md) | 提供使用 Windows 所提供之音訊和影片功能的相關指引。 |
| [資料存取與儲存](data-access-and-storage.md) | 提供您可以在桌面應用程式中使用的資料存取和儲存功能的相關資訊，包括檔案系統管理和雲端同步引擎。  |
| [裝置](devices.md) | 說明與裝置和感應器互動的 Api。 |
| [診斷](diagnostics.md) | 提供有關偵錯工具和錯誤處理、效能分析、網路監視和其他診斷功能的指引。 |
| [檔和列印](printdocs/documents-and-printing.md) | 描述 Windows 的檔和列印功能，可讓應用程式儲存、查看和列印。  |
| [圖形和遊戲](graphics-and-multimedia.md) | 提供 Windows 之圖形和遊戲功能的相關資訊，包括 DirectX 和數位影像處理。  |
| [網路功能和網際網路](networking.md) | 提供有關 Windows 的網路和網際網路相關功能的指引，包括網路管理、HTTP api，以及 (RPC) 的遠端程序呼叫。 |
| [安全性與身分識別](security.md) | 提供有關 Windows 的驗證、授權、加密和其他安全性功能的資訊。 |
| [系統服務](system-services.md) | 提供基本作業系統功能的相關指引，例如進程和執行緒、服務、動態連結程式庫、COM、登錄等等。 |
| [AI 和機器學習服務](/windows/ai/) | 使用人工智慧的能力來轉換您的 Windows 應用程式。 Windows AI 能為複雜的問題提供智慧型的解決方案，讓您和您的企業能達成更多目標。 |

<!--
<br/>

| User Interface and accessibility | System services and fundamentals  |  Audio, video, and graphics  |
|----------------------------------|---|----|
| [Desktop User Interface](windows-application-ui-development.md)<br/>[Windows and messages](winmsg/windowing.md)<br/>[Desktop Window Manager](dwm/dwm-overview.md)<br/>[Menus and other resources](menurc/resources.md)<br/>[Dialog boxes](dlgbox/dialog-boxes.md)<br/>[Data exchange](dataxchg/data-exchange.md)<br/>[High DPI](hidpi/high-dpi-desktop-application-development-on-windows.md)<br/>[Windows controls (Win32)](controls/window-controls.md)<br/>[Desktop environment and shell](user-interface.md)<br/>[Windows Property System](properties/windows-properties-system.md)<br/>[Accessibility](accessibility.md) | [System services](system-services.md)<br/>[Component Object Model (COM)](com/component-object-model--com--portal.md)<br/>[COM+](cossdk/component-services-portal.md)<br/>[Structured storage](stg/structured-storage-start-page.md)<br/>[Dynamic-link libraries](dlls/dynamic-link-libraries.md)<br/>[Interprocess communications](ipc/interprocess-communications.md)<br/>[Memory management](memory/memory-management.md)<br/>[Power management](power/power-management-portal.md)<br/>[Processes and threads](procthread/processes-and-threads.md)<br/>[Services](services/services.md)<br/>[Synchronization](sync/synchronization.md)<br/>[Windows system information](sysinfo/windows-system-information.md) | [Audio and video technologies](audio-and-video.md)<br/>[Core Audio APIs](coreaudio/core-audio-apis-in-windows-vista.md)<br/>[DirectShow](directshow/directshow.md)<br/>[Windows Multimedia](multimedia/windows-multimedia-start-page.md)<br/>[Graphics and gaming technologies](graphics-and-multimedia.md)<br/>[DirectX](directx.md)<br/>[Direct2D](direct2d/direct2d-portal.md)<br/>[Direct3D](direct3d.md)<br/>[Windows GDI](gdi/windows-gdi.md)<br/>[GDI+](gdiplus/-gdiplus-gdi-start.md)<br/>[OpenGL](opengl/opengl.md)<br/>[Windows Imaging Component](wic/-wic-lh.md) |

<br/>

| Networking and Internet | Data access and storage  |  Devices, documents, and printing  |
|----------------------------------|---|----|
| [Networking and Internet overview](networking.md)<br/>[Remote Procedure Call](rpc/rpc-start-page.md)<br/>[Delivery optimization](delivery_optimization/delivery-optimization-portal.md)<br/>[Network interfaces](network-interfaces.md)<br/>[Network management](netmgmt/network-management.md)<br/>[Network share management](netshare/network-share-management.md)<br/>[Windows networking](wnet/windows-networking-wnet-.md)<br/>[Windows Sockets 2](winsock/windows-sockets-start-page-2.md)<br/>[Wireless networking](wireless-networking.md) | [Data access and storage overview](data-access-and-storage.md)<br/>[Local file systems](fileio/file-systems.md)<br/>[Distributed File System](dfs/distributed-file-system.md)<br/>[Projected File System](projfs/projected-file-system.md)<br/>[Cloud sync engines](cfapi/cloud-files-api-portal.md)<br/>[Virtual Storage](VStor/virtual-storage.md)<br/>[Background Intelligent Transfer Service](bits/background-intelligent-transfer-service-portal.md)<br/>[Backup](backup.md) | [Devices overview](devices.md)<br/>[Communications resources](devio/communications-resources.md)<br/>[Location API](locationapi/windows-location-api-portal.md)<br/>[Sensor API](sensorsapi/portal.md)<br/>[UPnP APIs](upnp/universal-plug-and-play-start-page.md)<br/>[Windows Portable Devices](windows-portable-devices.md)<br/>[Documents and printing](printdocs/documents-and-printing.md) |

<br/>

| Security and identity | Diagnostics and testing  |  Packaging and installation  |
|----------------------------------|---|----|
| [Security and identity overview](security.md)<br/>[Antimalware Scan Interface](amsi/antimalware-scan-interface-portal.md)<br/>[Authentication](secauthn/authentication-portal.md)<br/>[Authorization](secauthz/authorization-portal.md)<br/>[Certificate Enrollment API](seccertenroll/certenroll-portal.md)<br/>[Cryptography (CNG)](seccng/cng-portal.md)<br/>[Rights Management](SrvNodes/rights-management.md)<br/>[Security Management](secmgmt/management-portal.md)<br/>[TPM Base Services](tbs/tpm-base-services-portal.md)<br/>[Windows Biometric Framework](secbiomet/biometric-service-api-portal.md) | [Diagnostics overview](diagnostics.md)<br/>[Debugging and error handling](debugging-and-error-handling.md)<br/>[Network Monitor](netmon2/network-monitor.md)<br/>[System Monitor](sysmon/system-monitor-portal.md)<br/>[Performance counters](perfctrs/performance-counters-portal.md)<br/>[Windows error reporting](wer/windows-error-reporting.md)<br/>[Windows events](events/windows-events.md)<br/>[TraceLogging](tracelogging/trace-logging-portal.md)<br/>[Debugging tools for Windows](//docs.microsoft.com/windows-hardware/drivers/debugger/index) | [MSIX packaging](//docs.microsoft.com/windows/msix)<br/>[Application install and servicing](application-installing-and-servicing.md)<br/>[Side-by-side assemblies](sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)<br/>[Packaging and query of UWP apps](appxpkg/appx-portal.md)<br/>[Windows Installer](msi/windows-installer-portal.md)<br/>[Desktop Application Program](appxpkg/windows-desktop-application-program.md)<br/>[Windows containers](//docs.microsoft.com/virtualization/windowscontainers/about/) |

-->

<!--
:::row:::
    :::column:::
        ![User Interface and accessibility](/media/illustrations/bcs-partner-advanced-management-add-user-1.svg?branch=master)
        ### User Interface and accessibility
        * [Desktop User Interface](windows-application-ui-development.md)
        * [Windows and messages](winmsg/windowing.md)
        * [Desktop Window Manager](dwm/dwm-overview.md)
        * [Dialog boxes](dlgbox/dialog-boxes.md)
        * [Menus and other resources](menurc/resources.md)
        * [Data exchange](dataxchg/data-exchange.md)
        * [High DPI](hidpi/high-dpi-desktop-application-development-on-windows.md)
        * [Windows controls (Win32)](controls/window-controls.md)
        * [Desktop environment and shell](user-interface.md)
        * [Windows Property System](properties/windows-properties-system.md)
        * [Accessibility](accessibility.md)
    :::column-end:::
    :::column:::
        ![System and fundamentals](/media/illustrations/biztalk-get-started-get-started.svg?branch=master)
        ### System services and fundamentals
        * [System services](system-services.md)
        * [Component Object Model (COM)](com/component-object-model--com--portal.md)
        * [COM+](cossdk/component-services-portal.md)
        * [Structured storage](stg/structured-storage-start-page.md)
        * [Dynamic-link libraries](dlls/dynamic-link-libraries.md)
        * [Interprocess communications](ipc/interprocess-communications.md)
        * [Memory management](memory/memory-management.md)
        * [Power management](power/power-management-portal.md)
        * [Processes and threads](procthread/processes-and-threads.md)
        * [Services](services/services.md)
        * [Synchronization](sync/synchronization.md)
        * [Windows system information](sysinfo/windows-system-information.md)
    :::column-end:::
    :::column:::
        ![Audio, video, and graphics](/media/illustrations/virtualization-containers-samples.svg?branch=master)
        ### Audio, video, and graphics
        * [Audio and video technologies](audio-and-video.md)
        * [Core Audio APIs](coreaudio/core-audio-apis-in-windows-vista.md)
        * [DirectShow](directshow/directshow.md)
        * [Windows Multimedia](multimedia/windows-multimedia-start-page.md)
        * [Graphics and gaming technologies](graphics-and-multimedia.md)
        * [DirectX](directx.md)
        * [Direct2D](direct2d/direct2d-portal.md)
        * [Direct3D](direct3d.md)
        * [Windows GDI](gdi/windows-gdi.md)
        * [GDI+](gdiplus/-gdiplus-gdi-start.md)
        * [OpenGL](opengl/opengl.md)
        * [Windows Imaging Component](wic/-wic-lh.md)
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Networking and Internet](/media/illustrations/teams-voice-deployment.svg?branch=master)
        ### Networking and Internet
        * [Networking and Internet overview](networking.md)
        * [Remote Procedure Call](rpc/rpc-start-page.md)
        * [Delivery Optimization](delivery_optimization/delivery-optimization-portal.md)
        * [Network interfaces](network-interfaces.md)
        * [Network Management](netmgmt/network-management.md)
        * [Network Share Management](netshare/network-share-management.md)
        * [Windows Networking](wnet/windows-networking-wnet-.md)
        * [Windows Sockets 2](winsock/windows-sockets-start-page-2.md)
        * [Wireless Networking](wireless-networking.md)
    :::column-end:::
    :::column:::
        ![Data access and storage](/media/illustrations/azure-architecture-patterns.svg?branch=master)
        ### Data access and storage
        * [Data access and storage overview](data-access-and-storage.md)
        * [Local File Systems](fileio/file-systems.md)
        * [Distributed File System](dfs/distributed-file-system.md)
        * [Projected File System](projfs/projected-file-system.md)
        * [Cloud Sync Engines](cfapi/cloud-files-api-portal.md)
        * [Virtual Storage](VStor/virtual-storage.md)
        * [Background Intelligent Transfer Service](bits/background-intelligent-transfer-service-portal.md)
        * [Backup](backup.md)
    :::column-end:::
    :::column:::
        ![Devices, documents, and printing](/media/illustrations/virtualization-hperv-server-doc-archive.svg?branch=master)
        ### Devices, documents, and printing
        * [Devices overview](devices.md)
        * [Communications Resources](devio/communications-resources.md)
        * [Location API](locationapi/windows-location-api-portal.md)
        * [Sensor API](sensorsapi/portal.md)
        * [UPnP APIs](upnp/universal-plug-and-play-start-page.md)
        * [Windows Portable Devices](windows-portable-devices.md)
        * [Documents and Printing](printdocs/documents-and-printing.md)
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Security and identity](/media/illustrations/bcs-partner-advanced-management-password-3.svg?branch=master)
        ### Security and identity
        * [Security and identity overview](security.md)
        * [Antimalware Scan Interface](amsi/antimalware-scan-interface-portal.md)
        * [Authentication](secauthn/authentication-portal.md)
        * [Authorization](secauthz/authorization-portal.md)
        * [Certificate Enrollment API](seccertenroll/certenroll-portal.md)
        * [Cryptography (CNG)](seccng/cng-portal.md)
        * [Rights Management](SrvNodes/rights-management.md)
        * [Security Management](secmgmt/management-portal.md)
        * [TPM Base Services](tbs/tpm-base-services-portal.md)
        * [Windows Biometric Framework](secbiomet/biometric-service-api-portal.md)
    :::column-end:::
    :::column:::
        ![Diagnostics and testing](/media/illustrations/team-services-dev-ops-test.svg?branch=master)
        ### Diagnostics and testing
        * [Diagnostics overview](diagnostics.md)
        * [Debugging and error handling](debugging-and-error-handling.md)
        * [Network Monitor](netmon2/network-monitor.md)
        * [System Monitor](sysmon/system-monitor-portal.md)
        * [Performance counters](perfctrs/performance-counters-portal.md)
        * [Windows error reporting](wer/windows-error-reporting.md)
        * [Windows events](events/windows-events.md)
        * [TraceLogging](tracelogging/trace-logging-portal.md)
        * [Debugging tools for Windows](//docs.microsoft.com/windows-hardware/drivers/debugger/index)
    :::column-end:::
    :::column:::
        ![Packaging and installation](/media/illustrations/biztalk-host-integration-install-configure.svg?branch=master)
        ### Packaging and installation
        * [MSIX packaging and deployment](//docs.microsoft.com/windows/msix)
        * [Application Installation and Servicing](application-installing-and-servicing.md)
        * [Isolated Applications and Side-by-side Assemblies](sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
        * [Packaging, deployment, and query of UWP apps](appxpkg/appx-portal.md)
        * [Windows Installer](msi/windows-installer-portal.md)
        * [Windows Desktop Application Program](appxpkg/windows-desktop-application-program.md)
        * [Windows containers](//docs.microsoft.com/virtualization/windowscontainers/about/)
    :::column-end:::
:::row-end:::
-->
