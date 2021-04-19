---
description: Microsoft Web Services on Devices API (WSDAPI) 支援執行用戶端控制的裝置和服務，以及符合 Web 服務 (DPWS) 之裝置設定檔的裝置主機。
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: 裝置上的 Web 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d8b5812983e7102093234458c94b475bb6a503
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986830"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="82baf-103">裝置上的 Web 服務</span><span class="sxs-lookup"><span data-stu-id="82baf-103">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="82baf-104">目的</span><span class="sxs-lookup"><span data-stu-id="82baf-104">Purpose</span></span>

<span data-ttu-id="82baf-105">Microsoft Web Services on Devices API (WSDAPI) 支援執行用戶端控制的裝置和服務，以及符合 Web 服務 (DPWS) 之 [裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) 的裝置主機。</span><span class="sxs-lookup"><span data-stu-id="82baf-105">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="82baf-106">WSDAPI 使用 [WS 探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) 進行裝置探索。</span><span class="sxs-lookup"><span data-stu-id="82baf-106">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="82baf-107">WSDAPI 可用於用戶端和服務的開發。</span><span class="sxs-lookup"><span data-stu-id="82baf-107">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="82baf-108">適用時</span><span class="sxs-lookup"><span data-stu-id="82baf-108">Where applicable</span></span>

<span data-ttu-id="82baf-109">裝置上的 Web 服務可讓用戶端在網路上探索及存取遠端裝置及其相關聯的服務。</span><span class="sxs-lookup"><span data-stu-id="82baf-109">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="82baf-110">它支援裝置探索、描述、控制項和事件。</span><span class="sxs-lookup"><span data-stu-id="82baf-110">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="82baf-111">開發人員可以為裝置主機建立 WSDAPI 用戶端 proxy 和對應的存根。</span><span class="sxs-lookup"><span data-stu-id="82baf-111">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="82baf-112">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="82baf-112">Developer audience</span></span>

<span data-ttu-id="82baf-113">[裝置上的 Web 服務] 檔適用于 C/c + + 程式設計人員，以及建立符合 DPWS 規範之產品的裝置廠商。</span><span class="sxs-lookup"><span data-stu-id="82baf-113">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="82baf-114">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="82baf-114">Run-time requirements</span></span>

<span data-ttu-id="82baf-115">從 Windows Vista 和 Windows Server 2008 開始，支援使用 WSDAPI 的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="82baf-115">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="82baf-116">本節內容</span><span class="sxs-lookup"><span data-stu-id="82baf-116">In this section</span></span>



| <span data-ttu-id="82baf-117">主題</span><span class="sxs-lookup"><span data-stu-id="82baf-117">Topic</span></span>                                                                                  | <span data-ttu-id="82baf-118">描述</span><span class="sxs-lookup"><span data-stu-id="82baf-118">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="82baf-119">關於裝置上的 Web 服務</span><span class="sxs-lookup"><span data-stu-id="82baf-119">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="82baf-120">有關裝置上 Web 服務的架構和一般資訊。</span><span class="sxs-lookup"><span data-stu-id="82baf-120">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="82baf-121">在裝置上使用 Web 服務</span><span class="sxs-lookup"><span data-stu-id="82baf-121">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="82baf-122">產生程式碼、設定應用程式和疑難排解的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="82baf-122">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="82baf-123">裝置上的 Web 服務參考</span><span class="sxs-lookup"><span data-stu-id="82baf-123">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="82baf-124">Web Services on Devices API 的參考檔。</span><span class="sxs-lookup"><span data-stu-id="82baf-124">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="82baf-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="82baf-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82baf-126">Dan Driscoll 的 Blog</span><span class="sxs-lookup"><span data-stu-id="82baf-126">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 

