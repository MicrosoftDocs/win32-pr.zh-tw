---
description: MTP/藍牙連接介面
ms.assetid: 7bbd5fe3-85f1-4f0a-9d3e-22746bd23aae
title: MTP/藍牙連接介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e5194b8a6ababc05c36590ef30ae19ab185efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027403"
---
# <a name="mtpbluetooth-connection-interfaces"></a><span data-ttu-id="26ab6-103">MTP/藍牙連接介面</span><span class="sxs-lookup"><span data-stu-id="26ab6-103">MTP/Bluetooth Connection Interfaces</span></span>

<span data-ttu-id="26ab6-104">下列介面可讓應用程式僅列舉支援媒體傳輸通訊協定的裝置，並將其連線到透過藍牙 (MTP/藍牙)  (MTP) 。</span><span class="sxs-lookup"><span data-stu-id="26ab6-104">The following interfaces allow applications to enumerate and connect only to devices that support the Media Transfer Protocol (MTP) over Bluetooth (MTP/Bluetooth).</span></span> <span data-ttu-id="26ab6-105">WPD 驅動程式（、集合和用戶端介面）不受 MTP/Bluetooth 通訊協定限制。</span><span class="sxs-lookup"><span data-stu-id="26ab6-105">The WPD driver-, collection-, and client-interfaces are not restricted to the MTP/ Bluetooth protocol.</span></span>



| <span data-ttu-id="26ab6-106">介面</span><span class="sxs-lookup"><span data-stu-id="26ab6-106">Interface</span></span>                                                              | <span data-ttu-id="26ab6-107">描述</span><span class="sxs-lookup"><span data-stu-id="26ab6-107">Description</span></span>                                                                                                         |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26ab6-108">**IConnectionRequestCallback**</span><span class="sxs-lookup"><span data-stu-id="26ab6-108">**IConnectionRequestCallback**</span></span>](iconnectionrequestcallback.md)       | <span data-ttu-id="26ab6-109">定義單一回呼方法，讓應用程式用來接收已完成和已取消之要求的通知。</span><span class="sxs-lookup"><span data-stu-id="26ab6-109">Defines a single callback method that applications use to receive notification of completed and cancelled requests.</span></span> |
| [<span data-ttu-id="26ab6-110">**IEnumPortableDeviceConnectors**</span><span class="sxs-lookup"><span data-stu-id="26ab6-110">**IEnumPortableDeviceConnectors**</span></span>](ienumportabledeviceconnectors.md) | <span data-ttu-id="26ab6-111">列舉 **IPortableDeviceConnector** 介面。</span><span class="sxs-lookup"><span data-stu-id="26ab6-111">Enumerates **IPortableDeviceConnector** interfaces.</span></span>                                                                 |
| [<span data-ttu-id="26ab6-112">**IPortableDeviceConnector**</span><span class="sxs-lookup"><span data-stu-id="26ab6-112">**IPortableDeviceConnector**</span></span>](/windows/desktop/api/portabledeviceconnectapi/nn-portabledeviceconnectapi-iportabledeviceconnector)           | <span data-ttu-id="26ab6-113">支援應用程式呼叫的方法，以建立與 MTP 藍牙裝置的連線。</span><span class="sxs-lookup"><span data-stu-id="26ab6-113">Supports methods that applications call to establish connections to MTP Bluetooth devices.</span></span>                          |



 

## <a name="related-topics"></a><span data-ttu-id="26ab6-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="26ab6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26ab6-115">**程式設計參考**</span><span class="sxs-lookup"><span data-stu-id="26ab6-115">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



