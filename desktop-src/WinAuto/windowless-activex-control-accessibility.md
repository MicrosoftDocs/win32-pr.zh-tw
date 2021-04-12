---
title: 無視窗的 ActiveX 控制項協助工具
description: 本節說明如何使用 Windows 協助工具 API，以確保可存取無視窗的 Microsoft ActiveX 控制項。
ms.assetid: 93CBCF20-DADF-4A63-BE60-F2A0D8810C62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb0489cdd5de3ac34df361bfa3e7b3624ee18f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376093"
---
# <a name="windowless-activex-control-accessibility"></a><span data-ttu-id="5ee8d-103">無視窗的 ActiveX 控制項協助工具</span><span class="sxs-lookup"><span data-stu-id="5ee8d-103">Windowless ActiveX Control Accessibility</span></span>

<span data-ttu-id="5ee8d-104">本節說明如何使用 Windows 協助工具 API，以確保可存取無視窗的 Microsoft ActiveX 控制項。</span><span class="sxs-lookup"><span data-stu-id="5ee8d-104">This section describes how to use the Windows Accessibility API to ensure that windowless Microsoft ActiveX controls are accessible.</span></span>

<span data-ttu-id="5ee8d-105">Windows 8 包含新的 Windows 協助工具 API 介面，可簡化為無視窗的 ActiveX 控制項執行協助工具的工作。</span><span class="sxs-lookup"><span data-stu-id="5ee8d-105">Windows 8 includes new Windows Accessibility API interfaces that simplify the task of implementing accessibility for windowless ActiveX controls.</span></span> <span data-ttu-id="5ee8d-106">API 包含在無視窗控制項和控制項容器上執行的介面，可讓無視窗控制項和其容器一起運作，以提供無視窗控制項的協助工具資訊。</span><span class="sxs-lookup"><span data-stu-id="5ee8d-106">The API includes interfaces that are implemented on a windowless control and on the control container, enabling the windowless control and its container to work together to provide accessibility information about the windowless control.</span></span> <span data-ttu-id="5ee8d-107">API 支援下列案例：</span><span class="sxs-lookup"><span data-stu-id="5ee8d-107">The API supports the following scenarios:</span></span>

-   <span data-ttu-id="5ee8d-108">Microsoft Active Accessibility 裝載于 Microsoft Active Accessibility 控制項容器中的無視窗控制項。</span><span class="sxs-lookup"><span data-stu-id="5ee8d-108">Microsoft Active Accessibility windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="5ee8d-109">Microsoft Active Accessibility 裝載于 Microsoft 消費者介面自動化控制項容器中的無視窗控制項。</span><span class="sxs-lookup"><span data-stu-id="5ee8d-109">Microsoft Active Accessibility windowless controls hosted in a Microsoft UI Automation control container.</span></span>
-   <span data-ttu-id="5ee8d-110">消費者介面自動化裝載于 Microsoft Active Accessibility 控制項容器中的無視窗控制項。</span><span class="sxs-lookup"><span data-stu-id="5ee8d-110">UI Automation windowless controls hosted in a Microsoft Active Accessibility control container.</span></span>
-   <span data-ttu-id="5ee8d-111">消費者介面自動化裝載于消費者介面自動化控制項容器中的無視窗控制項。</span><span class="sxs-lookup"><span data-stu-id="5ee8d-111">UI Automation windowless controls hosted in a UI Automation control container.</span></span>

<span data-ttu-id="5ee8d-112">下表列出支援無視窗的 ActiveX 控制項，以及識別執行介面之物件的介面。</span><span class="sxs-lookup"><span data-stu-id="5ee8d-112">The following table lists the interfaces that support windowless ActiveX controls and identifies the objects that implement the interfaces.</span></span>



| <span data-ttu-id="5ee8d-113">Object</span><span class="sxs-lookup"><span data-stu-id="5ee8d-113">Object</span></span>              | <span data-ttu-id="5ee8d-114">MSAA</span><span class="sxs-lookup"><span data-stu-id="5ee8d-114">MSAA</span></span>                                                                             | <span data-ttu-id="5ee8d-115">UI 自動化</span><span class="sxs-lookup"><span data-stu-id="5ee8d-115">UI automation</span></span>                                                                                     |
|---------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee8d-116">Control 物件</span><span class="sxs-lookup"><span data-stu-id="5ee8d-116">Control object</span></span>      | [<span data-ttu-id="5ee8d-117">**IAccessibleHandler**</span><span class="sxs-lookup"><span data-stu-id="5ee8d-117">**IAccessibleHandler**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblehandler)                                 |                                                                                                   |
| <span data-ttu-id="5ee8d-118">控制網站</span><span class="sxs-lookup"><span data-stu-id="5ee8d-118">Control site</span></span>        | [<span data-ttu-id="5ee8d-119">**IAccessibleWindowlessSite**</span><span class="sxs-lookup"><span data-stu-id="5ee8d-119">**IAccessibleWindowlessSite**</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite)        | [<span data-ttu-id="5ee8d-120">**IRawElementProviderWindowlessSite**</span><span class="sxs-lookup"><span data-stu-id="5ee8d-120">**IRawElementProviderWindowlessSite**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite)         |
| <span data-ttu-id="5ee8d-121">主機視窗的根目錄</span><span class="sxs-lookup"><span data-stu-id="5ee8d-121">Root of host window</span></span> | [<span data-ttu-id="5ee8d-122">**IAccessibleHostingElementProviders**</span><span class="sxs-lookup"><span data-stu-id="5ee8d-122">**IAccessibleHostingElementProviders**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessiblehostingelementproviders) | [<span data-ttu-id="5ee8d-123">**IRawElementProviderHostingAccessibles**</span><span class="sxs-lookup"><span data-stu-id="5ee8d-123">**IRawElementProviderHostingAccessibles**</span></span>](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles) |



 

## <a name="in-this-section"></a><span data-ttu-id="5ee8d-124">本節內容</span><span class="sxs-lookup"><span data-stu-id="5ee8d-124">In this section</span></span>

-   [<span data-ttu-id="5ee8d-125">如何使用消費者介面自動化使無視窗的 ActiveX 控制項可供存取</span><span class="sxs-lookup"><span data-stu-id="5ee8d-125">How to Use UI Automation to Make a Windowless ActiveX Control Accessible</span></span>](use-ui-automation-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="5ee8d-126">如何使用 MSAA 讓無視窗的 ActiveX 控制項可供存取</span><span class="sxs-lookup"><span data-stu-id="5ee8d-126">How to Use MSAA to Make a Windowless ActiveX Control Accessible</span></span>](use-msaa-to-make-an-windowless-activex-control-accessible.md)
-   [<span data-ttu-id="5ee8d-127">如何裝載消費者介面自動化無視窗的 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="5ee8d-127">How to Host a UI Automation Windowless ActiveX Control</span></span>](host-a-ui-automation-windowless-activex-control.md)
-   [<span data-ttu-id="5ee8d-128">如何裝載 MSAA 無視窗 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="5ee8d-128">How to Host an MSAA Windowless ActiveX Control</span></span>](host-an-msaa-windowless-activex-control.md)

 

 