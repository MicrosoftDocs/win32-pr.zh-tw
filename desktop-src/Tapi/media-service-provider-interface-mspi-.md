---
description: 媒體服務提供者介面 (MSPI) 是一組由 MSP 所執行的介面和方法，可在通訊會話期間，讓 TAPI 3 應用程式能控制媒體傳輸。
ms.assetid: 53b7bcbd-571a-44da-a6db-10d4c3e5d30a
title: '媒體服務提供者介面 (MSPI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b1ce09e626ede14515c0abbbd5c3a35921026d6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106991394"
---
# <a name="media-service-provider-interface-mspi"></a><span data-ttu-id="43795-103">媒體服務提供者介面 (MSPI) </span><span class="sxs-lookup"><span data-stu-id="43795-103">Media Service Provider Interface (MSPI)</span></span>

<span data-ttu-id="43795-104">媒體服務提供者介面 (MSPI) 是一組由 MSP 所執行的介面和方法，可在通訊會話期間，讓 TAPI 3 應用程式能控制媒體傳輸。</span><span class="sxs-lookup"><span data-stu-id="43795-104">The Media Service Provider Interface (MSPI) is a set of interfaces and methods implemented by an MSP to allow a TAPI 3 application control over media transport during a communications session.</span></span> <span data-ttu-id="43795-105">MSP 會處理制定這些控制項所需的裝置特定和通訊協定特定機制，並透過使用 MSPI 中提供的方法，與其配對的 TSP 或應用程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="43795-105">An MSP handles the device-specific and protocol-specific mechanisms needed to enact these controls, and communicates with its paired TSP or an application through use of the methods provided in the MSPI.</span></span>

<span data-ttu-id="43795-106">下一節 ( [媒體服務提供者介面 (MSPI) 參考](media-service-provider-interface-mspi-reference.md)) 詳述 MSP 公開的介面，以便與 Microsoft 電話語音環境互動。</span><span class="sxs-lookup"><span data-stu-id="43795-106">The following section ( [Media Service Provider Interface (MSPI) Reference](media-service-provider-interface-mspi-reference.md)) details the interfaces an MSP exposes in order to interact with the Microsoft Telephony environment.</span></span>

<span data-ttu-id="43795-107">此外，MSP 可能會公開提供者專屬的私用介面和方法，以進一步協助媒體控制項。</span><span class="sxs-lookup"><span data-stu-id="43795-107">In addition, an MSP may expose provider-specific private interfaces and methods to further assist in media control.</span></span> <span data-ttu-id="43795-108">例如， [IP 會議 MSP](ipconf-msp.md) 會公開提供參與者控制項的介面。</span><span class="sxs-lookup"><span data-stu-id="43795-108">For example, the [IP Conference MSP](ipconf-msp.md) exposes interfaces that provide participant control.</span></span> <span data-ttu-id="43795-109">請參閱 [提供者特定介面](provider-specific-interfaces.md) ，以取得私用物件如何運作的資訊，以及 [IPConf MSP 介面](ipconf-msp-interfaces.md) 以取得 IPConf 的參考清單。</span><span class="sxs-lookup"><span data-stu-id="43795-109">See [Provider-Specific Interfaces](provider-specific-interfaces.md) for information on how private objects work and [IPConf MSP Interfaces](ipconf-msp-interfaces.md) for a reference listing of IPConf.</span></span>

<span data-ttu-id="43795-110">建立 MSP 的大部分程式設計工作，對指定的平臺、裝置和傳輸通訊協定而言都是高度專屬的，而且不在本檔的範圍內。</span><span class="sxs-lookup"><span data-stu-id="43795-110">The majority of the programming effort in creating an MSP is highly specific to a given platform, device, and transport protocol, and is outside the scope of this document.</span></span> <span data-ttu-id="43795-111">不過，Microsoft 會提供一組 MSP 基類，這對大多數 MSP 作者很有用。</span><span class="sxs-lookup"><span data-stu-id="43795-111">However, Microsoft supplies a set of MSP base classes, which will be useful to most MSP authors.</span></span> <span data-ttu-id="43795-112">如需使用這些類別的詳細資訊，請參閱 [TAPI 3 MSP 基類](tapi-3-msp-base-classes.md) 。</span><span class="sxs-lookup"><span data-stu-id="43795-112">See [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md) for information on using these classes.</span></span>

<span data-ttu-id="43795-113">[**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress)介面代表 TAPI DLL 的媒體服務提供者。</span><span class="sxs-lookup"><span data-stu-id="43795-113">The [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress) interface represents a media service provider to the TAPI DLL.</span></span> <span data-ttu-id="43795-114">此介面不會由或公開給使用者應用程式。</span><span class="sxs-lookup"><span data-stu-id="43795-114">This interface is not used by or exposed to an end-user application.</span></span> <span data-ttu-id="43795-115">TAPI 3 DLL 會呼叫此介面上的 **CoCreateInstance** 來建立主要 MSP 物件。</span><span class="sxs-lookup"><span data-stu-id="43795-115">The TAPI 3 DLL calls **CoCreateInstance** on this interface to create the main MSP object.</span></span> <span data-ttu-id="43795-116">此物件上的方法可讓應用程式載入和卸載 MSP、接收 TSP 的資訊，以及建立 [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) 介面，此介面會在呼叫物件上公開。</span><span class="sxs-lookup"><span data-stu-id="43795-116">Methods on this object allow an application to load and unload the MSP, receive information from a TSP, and create the [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol) interface, which is exposed on the call object.</span></span>

<span data-ttu-id="43795-117">[**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol)和 [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)介面提供與子串流相關的平行方法。</span><span class="sxs-lookup"><span data-stu-id="43795-117">The [**ITSubStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstreamcontrol) and [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces provide parallel methods with respect to substreams.</span></span> <span data-ttu-id="43795-118">子流支援是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="43795-118">Substream support is optional.</span></span> <span data-ttu-id="43795-119">所有其他介面都必須由 MSP 來執行。</span><span class="sxs-lookup"><span data-stu-id="43795-119">All other interfaces must be implemented by an MSP.</span></span>

> [!Note]  
> <span data-ttu-id="43795-120">TSP/MSP 組所實行的作業必須位於一個 DLL 中，才能讓使用者更新服務提供者，而不需要重新開機其系統。</span><span class="sxs-lookup"><span data-stu-id="43795-120">Operations implemented by a TSP/MSP pair must be located in one DLL to allow a user to update the service provider without rebooting his or her system.</span></span>

 

 

 
