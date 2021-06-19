---
description: 瞭解如何在裝置上使用 Microsoft Web 服務 (WSD) API (WSDAPI) 來執行用戶端控制的裝置和服務，以及符合 DPWS 的裝置主機。
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Windows 上的 WSD 應用程式開發
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167cd1ad013ea387a6e33b6de449f3f84d49db13
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405781"
---
# <a name="wsd-application-development-on-windows"></a><span data-ttu-id="98fd1-103">Windows 上的 WSD 應用程式開發</span><span class="sxs-lookup"><span data-stu-id="98fd1-103">WSD Application Development on Windows</span></span>

<span data-ttu-id="98fd1-104">Microsoft Web Services on Devices API (WSDAPI) 支援執行用戶端控制的裝置和服務，以及符合 Web 服務 (DPWS) 之 [裝置設定檔](https://specs.xmlsoap.org/ws/2006/02/devprof/) 的裝置主機。</span><span class="sxs-lookup"><span data-stu-id="98fd1-104">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="98fd1-105">您可以使用 WSDAPI 來開發用戶端和伺服器 (裝置) 的實施。</span><span class="sxs-lookup"><span data-stu-id="98fd1-105">WSDAPI may be used for the development of both client and server (device) implementations.</span></span>

<span data-ttu-id="98fd1-106">通常會使用 [WsdCodeGen](web-services-for-devices-code-generator.md)來產生這些應用程式的 WSDAPI 程式碼。</span><span class="sxs-lookup"><span data-stu-id="98fd1-106">Quite often, WSDAPI code for these applications is generated using [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="98fd1-107">某些 WSDAPI 函式和方法僅供產生的程式碼呼叫。</span><span class="sxs-lookup"><span data-stu-id="98fd1-107">Some WSDAPI functions and methods are intended to be called only by generated code.</span></span> <span data-ttu-id="98fd1-108">API 參考檔會指出應該使用或只由產生的程式碼來執行函式或方法。</span><span class="sxs-lookup"><span data-stu-id="98fd1-108">The API reference documentation indicates when a function or method should be used or implemented only by generated code.</span></span>

<span data-ttu-id="98fd1-109">Windows SDK 包含一些範例 WSDL 檔案、WsdCodeGen 設定檔案和產生的程式碼。</span><span class="sxs-lookup"><span data-stu-id="98fd1-109">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="98fd1-110">如需詳細資訊，請參閱 [WSDAPI 範例](wsdapi-samples.md)。</span><span class="sxs-lookup"><span data-stu-id="98fd1-110">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

<span data-ttu-id="98fd1-111">如果您想要使用 WSD 通訊協定來列舉裝置，並查詢 WSD 裝置中繼資料，您可以改用函式 [探索](/previous-versions/windows/desktop/fundisc/fd-portal) API。</span><span class="sxs-lookup"><span data-stu-id="98fd1-111">If you want to enumerate devices using the WSD protocol and query WSD device metadata, you can use the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API instead.</span></span>

<span data-ttu-id="98fd1-112">如果您想要執行不會執行 Windows 的 WSD 裝置，請參閱 [Wsd 裝置開發](wsd-device-development.md)。</span><span class="sxs-lookup"><span data-stu-id="98fd1-112">If you want to implement a WSD device that does not run Windows, see [WSD Device Development](wsd-device-development.md).</span></span>
