---
description: 瞭解如何在裝置上執行 web 服務 (WSD) 。 瞭解其用途、適用的位置、開發人員物件和執行時間需求。
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: 裝置上的 Web 服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 267f8dba0fd56c383dd3cecabb3c00959aa0d90c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405751"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="e3596-104">裝置上的 Web 服務</span><span class="sxs-lookup"><span data-stu-id="e3596-104">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="e3596-105">目的</span><span class="sxs-lookup"><span data-stu-id="e3596-105">Purpose</span></span>

<span data-ttu-id="e3596-106">Microsoft Web Services on Devices API (WSDAPI) 支援執行用戶端控制的裝置和服務，以及符合 Web 服務 (DPWS) 之 [裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) 的裝置主機。</span><span class="sxs-lookup"><span data-stu-id="e3596-106">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="e3596-107">WSDAPI 使用 [WS 探索](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) 進行裝置探索。</span><span class="sxs-lookup"><span data-stu-id="e3596-107">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="e3596-108">WSDAPI 可用於用戶端和服務的開發。</span><span class="sxs-lookup"><span data-stu-id="e3596-108">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="e3596-109">適用時</span><span class="sxs-lookup"><span data-stu-id="e3596-109">Where applicable</span></span>

<span data-ttu-id="e3596-110">裝置上的 Web 服務可讓用戶端在網路上探索及存取遠端裝置及其相關聯的服務。</span><span class="sxs-lookup"><span data-stu-id="e3596-110">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="e3596-111">它支援裝置探索、描述、控制項和事件。</span><span class="sxs-lookup"><span data-stu-id="e3596-111">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="e3596-112">開發人員可以為裝置主機建立 WSDAPI 用戶端 proxy 和對應的存根。</span><span class="sxs-lookup"><span data-stu-id="e3596-112">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e3596-113">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="e3596-113">Developer audience</span></span>

<span data-ttu-id="e3596-114">[裝置上的 Web 服務] 檔適用于 C/c + + 程式設計人員，以及建立符合 DPWS 規範之產品的裝置廠商。</span><span class="sxs-lookup"><span data-stu-id="e3596-114">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e3596-115">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="e3596-115">Run-time requirements</span></span>

<span data-ttu-id="e3596-116">從 Windows Vista 和 Windows Server 2008 開始，支援使用 WSDAPI 的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="e3596-116">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e3596-117">本節內容</span><span class="sxs-lookup"><span data-stu-id="e3596-117">In this section</span></span>



| <span data-ttu-id="e3596-118">主題</span><span class="sxs-lookup"><span data-stu-id="e3596-118">Topic</span></span>                                                                                  | <span data-ttu-id="e3596-119">描述</span><span class="sxs-lookup"><span data-stu-id="e3596-119">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e3596-120">關於裝置上的 Web 服務</span><span class="sxs-lookup"><span data-stu-id="e3596-120">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="e3596-121">有關裝置上 Web 服務的架構和一般資訊。</span><span class="sxs-lookup"><span data-stu-id="e3596-121">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="e3596-122">在裝置上使用 Web 服務</span><span class="sxs-lookup"><span data-stu-id="e3596-122">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="e3596-123">產生程式碼、設定應用程式和疑難排解的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e3596-123">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="e3596-124">裝置上的 Web 服務參考</span><span class="sxs-lookup"><span data-stu-id="e3596-124">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="e3596-125">Web Services on Devices API 的參考檔。</span><span class="sxs-lookup"><span data-stu-id="e3596-125">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="e3596-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3596-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3596-127">Dan Driscoll 的 Blog</span><span class="sxs-lookup"><span data-stu-id="e3596-127">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 

