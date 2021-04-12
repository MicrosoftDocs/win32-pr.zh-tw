---
title: 執行裝置提供者
description: 若要執行裝置提供者，請建立公開 IUPnPDeviceProvider 介面的物件。
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462449"
---
# <a name="implementing-a-device-provider"></a><span data-ttu-id="42644-103">執行裝置提供者</span><span class="sxs-lookup"><span data-stu-id="42644-103">Implementing a Device Provider</span></span>

<span data-ttu-id="42644-104">若要執行裝置提供者，請建立公開 [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="42644-104">To implement a device provider, create an object that exposes the [**IUPnPDeviceProvider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) interface.</span></span> <span data-ttu-id="42644-105">此物件必須使用 [**IUPnPRegistrar：： RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) 方法向裝置主機註冊。</span><span class="sxs-lookup"><span data-stu-id="42644-105">This object must be registered with the device host using the [**IUPnPRegistrar::RegisterDeviceProvider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) method.</span></span> <span data-ttu-id="42644-106">這個方法會採用下列參數：</span><span class="sxs-lookup"><span data-stu-id="42644-106">This method takes the following parameters:</span></span>

-   <span data-ttu-id="42644-107">提供者的名稱，在電腦上必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="42644-107">The name of the provider, which must be unique on the computer.</span></span>
-   <span data-ttu-id="42644-108">實作為裝置提供者之類別的 ProgID。</span><span class="sxs-lookup"><span data-stu-id="42644-108">The ProgID of the class that implements the device provider.</span></span>
-   <span data-ttu-id="42644-109">啟動時傳遞給裝置提供者的初始化字串。</span><span class="sxs-lookup"><span data-stu-id="42644-109">An initialization string that is passed to the device provider when it is started.</span></span>
-   <span data-ttu-id="42644-110">容器識別碼。</span><span class="sxs-lookup"><span data-stu-id="42644-110">A container ID.</span></span> <span data-ttu-id="42644-111">容器識別碼是識別裝置所屬群組的字串。</span><span class="sxs-lookup"><span data-stu-id="42644-111">A container ID is a string that identifies the group to which the device belongs.</span></span> <span data-ttu-id="42644-112">所有具有相同容器識別碼的裝置都會裝載在相同的進程中。</span><span class="sxs-lookup"><span data-stu-id="42644-112">All devices with the same container identifier are hosted in the same process.</span></span>

 

 




