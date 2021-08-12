---
title: 無視窗 ActiveX 控制項協助工具
description: 本節說明如何使用 Windows 協助工具 API，以確保可存取無視窗的 Microsoft ActiveX 控制項。
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3842dd6b9ec18b745e043841936dd811afd1580779d276290057c2fe6d2194cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118563453"
---
# <a name="windowless-activex-control-accessibility"></a>無視窗 ActiveX 控制項協助工具

本節說明如何使用 Windows 協助工具 API，以確保可存取無視窗的 Microsoft ActiveX 控制項。

Windows 8 包含新的 Windows 協助工具 API 介面，可簡化無視窗 ActiveX 控制項之協助工具的執行工作。 API 包含在無視窗控制項和控制項容器上執行的介面，可讓無視窗控制項和其容器一起運作，以提供無視窗控制項的協助工具資訊。 API 支援下列案例：

-   Microsoft Active Accessibility 裝載于 Microsoft Active Accessibility 控制項容器中的無視窗控制項。
-   Microsoft Active Accessibility 裝載于 Microsoft 消費者介面自動化控制項容器中的無視窗控制項。
-   消費者介面自動化裝載于 Microsoft Active Accessibility 控制項容器中的無視窗控制項。
-   消費者介面自動化裝載于消費者介面自動化控制項容器中的無視窗控制項。

下表列出支援無視窗 ActiveX 控制項的介面，並識別執行介面的物件。



| Object              | MSAA                                                                             | UI 自動化                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| Control 物件      | [**IAccessibleHandler**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| 控制網站        | [**IAccessibleWindowlessSite**](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [**IRawElementProviderWindowlessSite**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| 主機視窗的根目錄 | [**IAccessibleHostingElementProviders**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [**IRawElementProviderHostingAccessibles**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a>本節內容

-   [如何使用消費者介面自動化使無視窗 ActiveX 控制項可供存取](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [如何使用 MSAA 讓無視窗 ActiveX 控制項可供存取](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [如何裝載消費者介面自動化無視窗 ActiveX 控制項](host-a-ui-automation-windowless-activex-control.md)
-   [如何裝載 MSAA 無視窗 ActiveX 控制項](host-an-msaa-windowless-activex-control.md)

 

 