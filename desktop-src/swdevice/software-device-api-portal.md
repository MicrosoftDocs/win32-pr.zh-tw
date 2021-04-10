---
title: 軟體裝置 API
description: 您可以使用軟體裝置 API 從應用程式建立 PnP 裝置。
ms.assetid: 203abb2c-526f-4995-95de-4eb0ecee63d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e011d806ea21310fccc6ca96517a5465cb41add1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682959"
---
# <a name="software-device-api"></a><span data-ttu-id="b6b1d-103">軟體裝置 API</span><span class="sxs-lookup"><span data-stu-id="b6b1d-103">Software Device API</span></span>

## <a name="purpose"></a><span data-ttu-id="b6b1d-104">目的</span><span class="sxs-lookup"><span data-stu-id="b6b1d-104">Purpose</span></span>

<span data-ttu-id="b6b1d-105">您可以使用軟體裝置 API 從應用程式建立 PnP 裝置。</span><span class="sxs-lookup"><span data-stu-id="b6b1d-105">You can use the Software Device API to create a PnP device from an app.</span></span> <span data-ttu-id="b6b1d-106">API 可讓您將裝置列舉為任何現有父裝置的子系。</span><span class="sxs-lookup"><span data-stu-id="b6b1d-106">The API lets you enumerate the device as a child of any existing parent device.</span></span> <span data-ttu-id="b6b1d-107">此 API 也可讓您向列舉的裝置註冊裝置介面，以及設定裝置和介面的屬性。</span><span class="sxs-lookup"><span data-stu-id="b6b1d-107">The API also lets you register device interfaces against the enumerated devices and set properties for the devices and interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b6b1d-108">本節內容</span><span class="sxs-lookup"><span data-stu-id="b6b1d-108">In this section</span></span>



| <span data-ttu-id="b6b1d-109">主題</span><span class="sxs-lookup"><span data-stu-id="b6b1d-109">Topic</span></span>                                                                                         | <span data-ttu-id="b6b1d-110">描述</span><span class="sxs-lookup"><span data-stu-id="b6b1d-110">Description</span></span>                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6b1d-111">[軟體裝置 API 程式設計指南](/previous-versions/windows/hardware/drivers/dn315034(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b6b1d-111">[Software Device API Programming Guide](/previous-versions/windows/hardware/drivers/dn315034(v=vs.85))</span></span><br/> | <span data-ttu-id="b6b1d-112">本指南包含如何使用軟體裝置 API 來列舉 PnP 裝置的資訊。</span><span class="sxs-lookup"><span data-stu-id="b6b1d-112">This guide contains info on how to use the Software Device API to enumerate PnP devices.</span></span> <br/>                                                                               |
| [<span data-ttu-id="b6b1d-113">軟體裝置 API 參考</span><span class="sxs-lookup"><span data-stu-id="b6b1d-113">Software Device API Reference</span></span>](software-device-api-reference.md)<br/>                 | <span data-ttu-id="b6b1d-114">此參考描述用戶端應用程式所呼叫的軟體裝置 API 函式，以及用戶端應用程式所執行的回呼函式和軟體裝置 API 結構。</span><span class="sxs-lookup"><span data-stu-id="b6b1d-114">This reference describes Software Device API functions that a client app calls and a callback function that a client app implements and Software Device API structures.</span></span><br/> |



 

## <a name="developer-audience"></a><span data-ttu-id="b6b1d-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="b6b1d-115">Developer audience</span></span>

<span data-ttu-id="b6b1d-116">軟體裝置 API 的設計目的是要讓想要在 PnP 「目錄」中發佈裝置功能或載入設備磁碟機的開發人員使用。</span><span class="sxs-lookup"><span data-stu-id="b6b1d-116">The Software Device API is designed for use by developers who want to publish device functionality in the PnP "directory" or to load a device driver.</span></span>

 

 

[<span data-ttu-id="b6b1d-117">將關於本主題的意見傳送給 Microsoft</span><span class="sxs-lookup"><span data-stu-id="b6b1d-117">Send comments about this topic to Microsoft</span></span>](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bswdevice\swdevice%5D:%20Software%20Device%20API%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "將關於本主題的意見傳送給 Microsoft")