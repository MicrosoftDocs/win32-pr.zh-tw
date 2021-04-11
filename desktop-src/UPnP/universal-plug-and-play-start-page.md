---
title: UPnP API
description: UPnP 架構可啟用智慧型設備、無線裝置及電腦的動態網路功能。
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104093463"
---
# <a name="upnp-apis"></a><span data-ttu-id="bbe7e-104">UPnP API</span><span class="sxs-lookup"><span data-stu-id="bbe7e-104">UPnP APIs</span></span>

## <a name="purpose"></a><span data-ttu-id="bbe7e-105">目的</span><span class="sxs-lookup"><span data-stu-id="bbe7e-105">Purpose</span></span>

<span data-ttu-id="bbe7e-106">UPnP 架構可啟用智慧型設備、無線裝置及電腦的動態網路功能。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-106">The UPnP  framework enables dynamic networking of intelligent appliances, wireless devices, and PCs.</span></span> <span data-ttu-id="bbe7e-107">有兩個 Api 可搭配使用 UPnP 認證的裝置：</span><span class="sxs-lookup"><span data-stu-id="bbe7e-107">There are two APIs for working with UPnP-certified devices:</span></span>

-   <span data-ttu-id="bbe7e-108">控制點 API，由用來尋找及控制裝置的一組 COM 介面所組成。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-108">The Control Point API, which consists of a set of COM interfaces used to find and control devices.</span></span>
-   <span data-ttu-id="bbe7e-109">裝置主機 API，包含一組用來執行電腦所裝載之裝置的 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-109">The Device Host API, which consists of a set of COM interfaces used to implement devices that are hosted by a computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="bbe7e-110">適用時</span><span class="sxs-lookup"><span data-stu-id="bbe7e-110">Where applicable</span></span>

<span data-ttu-id="bbe7e-111">控制點 API 可讓開發人員撰寫應用程式，以搜尋及控制 UPnP 認證的裝置。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-111">The Control Point API enables developers to write applications that search for and control UPnP-certified devices.</span></span> <span data-ttu-id="bbe7e-112">裝置主機 API 可讓開發人員執行 UPnP 認證裝置的功能，並使用裝置主機管理 UPnP 認證裝置的探索、描述、控制、簡報和事件功能。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-112">The Device Host API enables developers to implement the functionality of UPnP-certified devices, and use the device host to manage the discovery, description, control, presentation, and eventing functions of a UPnP-certified device.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="bbe7e-113">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="bbe7e-113">Developer audience</span></span>

<span data-ttu-id="bbe7e-114">使用控制點 Api 和裝置主機 Api 的開發人員必須熟悉 UPnP 裝置架構。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-114">Developers using the Control Point APIs and Device Host APIs must be familiar with the UPnP device architecture.</span></span> <span data-ttu-id="bbe7e-115">如需詳細資訊，請參閱 [Upnp 執行檔](https://openconnectivity.org/resources/upnpresources.zip) 和 [upnp 論壇](https://openconnectivity.org/)。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-115">For more information, see the [UPnP Implementation Documentation](https://openconnectivity.org/resources/upnpresources.zip) and the [UPnP Forum](https://openconnectivity.org/).</span></span>

<span data-ttu-id="bbe7e-116">使用裝置主機 Api 的開發人員應該熟悉 Active Template Library (ATL) 和 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-116">Developers who are using the Device Host APIs should be familiar with the Active Template Library (ATL) and COM interfaces.</span></span>

<span data-ttu-id="bbe7e-117">控制點 Api 和裝置主機 Api 是由各種應用程式所使用，從 HTML 網頁中內嵌的腳本到完備的 c + + 和 Microsoft Visual Basic 程式。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-117">The Control Point APIs and Device Host APIs are used by a variety of applications, from scripts embedded in HTML pages to full-fledged C++ and Microsoft Visual Basic programs.</span></span>

<span data-ttu-id="bbe7e-118">只有控制點 API 支援 Visual Basic Scripting Edition (VBScript) 。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-118">Only the Control Point API supports Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="bbe7e-119">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="bbe7e-119">Run-time requirements</span></span>

<span data-ttu-id="bbe7e-120">控制點 API 是在執行 Microsoft Windows Millennium Edition、Windows XP、Windows XP Professional 和 Windows CE .NET 的電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-120">The Control Point API is used on computers running Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="bbe7e-121">裝置主機 API 是在執行 Windows XP、Windows XP Professional 和 Windows CE .NET 的電腦上使用。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-121">The Device Host API is used on computers running Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="bbe7e-122">如需有關哪些作業系統支援特定功能的詳細資訊，請參閱檔中的「需求」。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-122">For more specific information about which operating systems support a particular function, refer to "Requirements" in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bbe7e-123">本節內容</span><span class="sxs-lookup"><span data-stu-id="bbe7e-123">In this section</span></span>



| <span data-ttu-id="bbe7e-124">主題</span><span class="sxs-lookup"><span data-stu-id="bbe7e-124">Topic</span></span>                                                                                          | <span data-ttu-id="bbe7e-125">描述</span><span class="sxs-lookup"><span data-stu-id="bbe7e-125">Description</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbe7e-126">UPnP 架構總覽</span><span class="sxs-lookup"><span data-stu-id="bbe7e-126">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)<br/>            | <span data-ttu-id="bbe7e-127">一般資訊和背景。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-127">General information and background.</span></span><br/>                                                     |
| [<span data-ttu-id="bbe7e-128">控制點總覽</span><span class="sxs-lookup"><span data-stu-id="bbe7e-128">Control Point Overview</span></span>](control-point-api.md)<br/>                                     | <span data-ttu-id="bbe7e-129">指向控制點 API 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-129">General information about the Control Point API.</span></span><br/>                                        |
| [<span data-ttu-id="bbe7e-130">使用控制點 API</span><span class="sxs-lookup"><span data-stu-id="bbe7e-130">Using the Control Point API</span></span>](using-the-control-point-api-with-upnp-technology.md)<br/> | <span data-ttu-id="bbe7e-131">示範如何開發可控制 UPnP 認證裝置之應用程式的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-131">Sample code that shows how to develop applications that control UPnP-certified devices.</span></span><br/> |
| [<span data-ttu-id="bbe7e-132">控制點 API 參考</span><span class="sxs-lookup"><span data-stu-id="bbe7e-132">Control Point API Reference</span></span>](control-point-api-with-upnp-technology-reference.md)<br/> | <span data-ttu-id="bbe7e-133">控制點元件介面、方法和事件的檔。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-133">Documentation of Control Point component interfaces, methods, and events.</span></span><br/>               |
| [<span data-ttu-id="bbe7e-134">裝置主機 API 總覽</span><span class="sxs-lookup"><span data-stu-id="bbe7e-134">Device Host API Overview</span></span>](device-host-api.md)<br/>                                     | <span data-ttu-id="bbe7e-135">裝置主機 API 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-135">General information about the Device Host API.</span></span><br/>                                          |
| [<span data-ttu-id="bbe7e-136">使用裝置主機 API</span><span class="sxs-lookup"><span data-stu-id="bbe7e-136">Using the Device Host API</span></span>](using-the-device-host-api-with-upnp-technology.md)<br/>     | <span data-ttu-id="bbe7e-137">示範如何針對 UPnP 認證的裝置開發應用程式的範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-137">Sample code that shows how to develop an application for UPnP-certified devices.</span></span><br/>        |
| [<span data-ttu-id="bbe7e-138">裝置主機 API 參考</span><span class="sxs-lookup"><span data-stu-id="bbe7e-138">Device Host API Reference</span></span>](device-host-api-with-upnp-technology-reference.md)<br/>     | <span data-ttu-id="bbe7e-139">裝置主機元件介面、方法和事件的檔。</span><span class="sxs-lookup"><span data-stu-id="bbe7e-139">Documentation of Device Host component interfaces, methods, and events.</span></span><br/>                 |



 

 

 





