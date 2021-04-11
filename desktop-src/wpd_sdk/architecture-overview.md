---
description: 架構概觀
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: 架構概觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f911a14e60465efc8f8f8d798b7ddf527bf4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852155"
---
# <a name="architecture-overview"></a><span data-ttu-id="be4cc-103">架構概觀</span><span class="sxs-lookup"><span data-stu-id="be4cc-103">Architecture Overview</span></span>

<span data-ttu-id="be4cc-104">WPD 架構可以分為三個進程。</span><span class="sxs-lookup"><span data-stu-id="be4cc-104">The WPD architecture can be divided into three processes.</span></span> <span data-ttu-id="be4cc-105">在這些程式中，WPD 的三個主要元件： API、序列化程式和驅動程式。</span><span class="sxs-lookup"><span data-stu-id="be4cc-105">Within these processes are the three primary components of WPD: the API, the serializer, and the driver.</span></span> <span data-ttu-id="be4cc-106">下圖說明構成 WPD 架構的處理常式和元件。</span><span class="sxs-lookup"><span data-stu-id="be4cc-106">The following illustration depicts the processes and components that constitute the WPD architecture.</span></span>

![顯示 wpd api、序列化程式和驅動程式元件的圖例](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a><span data-ttu-id="be4cc-108">WPD 應用程式設計介面</span><span class="sxs-lookup"><span data-stu-id="be4cc-108">The WPD Application Programming Interface</span></span>

<span data-ttu-id="be4cc-109">WPD API 會實作為同進程的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="be4cc-109">The WPD API is implemented as an in-proc COM server.</span></span> <span data-ttu-id="be4cc-110">API 會使用標準 Microsoft Win32 Api 來與適當的 WPD 驅動程式通訊。</span><span class="sxs-lookup"><span data-stu-id="be4cc-110">The API uses standard Microsoft Win32 APIs to communicate with the appropriate WPD driver.</span></span> <span data-ttu-id="be4cc-111">API 物件和驅動程式會使用稱為 WPD 序列化程式的元件，將參數封裝或解除封裝至 Windows Driver Foundation (WDF) -使用者模式驅動程式架構 (的 UMDF) 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="be4cc-111">A component called the WPD serializer is used by both API objects and the driver to pack or unpack parameters to or from Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) buffers.</span></span>

## <a name="the-wpd-serializer"></a><span data-ttu-id="be4cc-112">WPD 序列化程式</span><span class="sxs-lookup"><span data-stu-id="be4cc-112">The WPD Serializer</span></span>

<span data-ttu-id="be4cc-113">WPD 序列化程式會實作為同進程的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="be4cc-113">The WPD serializer is implemented as an in-proc COM server.</span></span> <span data-ttu-id="be4cc-114">WPD API 會使用序列化程式，將命令和參數封裝至傳送至驅動程式的訊息緩衝區。</span><span class="sxs-lookup"><span data-stu-id="be4cc-114">The WPD API uses the serializer to pack commands and parameters into message buffers that are sent to the driver.</span></span> <span data-ttu-id="be4cc-115">驅動程式會使用序列化程式將這些訊息緩衝區解壓縮以進行處理。</span><span class="sxs-lookup"><span data-stu-id="be4cc-115">The driver uses the serializer to unpack these message buffers for processing.</span></span> <span data-ttu-id="be4cc-116">驅動程式也會使用序列化程式將資料和參數封裝至傳回給 WPD API 的回應緩衝區，而 WPD API 會使用序列化程式來將這些回應緩衝區解壓縮，以傳回給呼叫端。</span><span class="sxs-lookup"><span data-stu-id="be4cc-116">The driver also uses the serializer to pack data and parameters into response buffers that are returned to the WPD API, and the WPD API uses the serializer to unpack these response buffers to return to callers.</span></span>

## <a name="wpd-driver"></a><span data-ttu-id="be4cc-117">WPD 驅動程式</span><span class="sxs-lookup"><span data-stu-id="be4cc-117">WPD Driver</span></span>

<span data-ttu-id="be4cc-118">WPD 驅動程式會實作為標準 Windows Driver Foundation (WDF) -使用者模式驅動程式架構 (的 UMDF) 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="be4cc-118">The WPD driver is implemented as a standard Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) driver.</span></span> <span data-ttu-id="be4cc-119">WPD 驅動程式是由 UMDF 在稱為驅動程式主機的個別進程中裝載。</span><span class="sxs-lookup"><span data-stu-id="be4cc-119">WPD drivers are hosted by UMDF in a separate process called the Driver Host.</span></span>

<span data-ttu-id="be4cc-120">驅動程式會接收來自 UMDF 反映程式的訊息 (這不會顯示在圖表中，因為接收緩衝區對驅動程式而言並不重要。</span><span class="sxs-lookup"><span data-stu-id="be4cc-120">The driver receives messages from the UMDF reflector (this is not shown in the diagram, since how the buffers are received is not important to the driver.</span></span> <span data-ttu-id="be4cc-121">如需) 的詳細資訊，請參閱 UMDF 檔。</span><span class="sxs-lookup"><span data-stu-id="be4cc-121">See UMDF documentation for more information).</span></span> <span data-ttu-id="be4cc-122">驅動程式會執行 WPD 特定的 i/o 控制項程式碼， (IOCL) 處理常式來處理 WPD API 所接收的 WPD 訊息。</span><span class="sxs-lookup"><span data-stu-id="be4cc-122">The driver implements a WPD-specific I/O Control code (IOCL) handler to process WPD messages received by the WPD API.</span></span> <span data-ttu-id="be4cc-123">驅動程式會使用 WPD 序列化程式，將命令和參數解壓縮至這些訊息緩衝區，並將回應封裝至傳回緩衝區。</span><span class="sxs-lookup"><span data-stu-id="be4cc-123">The driver uses the WPD serializer to unpack commands and parameters from these message buffers, and to pack the response into the return buffer.</span></span>

<span data-ttu-id="be4cc-124">WPD 驅動程式可以通過核心模式驅動程式來與其裝置通訊，通常是透過 Win32 檔案作業來存取， (也就是 CreateFile、ReadFile、WriteFile 等) 。</span><span class="sxs-lookup"><span data-stu-id="be4cc-124">WPD drivers may communicate with their devices by going through a kernel-mode driver, typically accessed via Win32 file operations (that is, CreateFile, ReadFile, WriteFile, and so on).</span></span> <span data-ttu-id="be4cc-125">針對常見的匯流排，Microsoft 會提供標準核心驅動程式供廠商使用，這可讓廠商寄送僅限使用者模式的驅動程式解決方案。</span><span class="sxs-lookup"><span data-stu-id="be4cc-125">For the common buses, Microsoft will provide standard kernel drivers for vendors to use, which will allow vendors to ship a user-mode-only driver solution.</span></span> <span data-ttu-id="be4cc-126">此外，針對媒體傳輸通訊協定 (MTP) 和大型儲存類別 (SERVICES.MSC) 裝置，Microsoft 將提供 WPD 類別的驅動程式。</span><span class="sxs-lookup"><span data-stu-id="be4cc-126">In addition, for Media Transfer Protocol (MTP) and Mass Storage Class (MSC) devices, Microsoft will provide WPD class drivers.</span></span>

<span data-ttu-id="be4cc-127">如需有關 WPD 驅動程式的詳細資訊，請參閱 Windows 驅動程式套件中的 Windows 便攜裝置驅動程式檔集。</span><span class="sxs-lookup"><span data-stu-id="be4cc-127">For more information about WPD drivers, see the Windows Portable Devices Driver documentation in the Windows Driver Kit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="be4cc-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="be4cc-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be4cc-129">**應用程式總覽**</span><span class="sxs-lookup"><span data-stu-id="be4cc-129">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



