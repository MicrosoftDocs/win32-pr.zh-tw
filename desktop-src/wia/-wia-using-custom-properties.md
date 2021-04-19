---
description: 使用自訂屬性。
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: 使用自訂屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca9f8092afa5b8af22080b154fff79a32a6f304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971008"
---
# <a name="using-custom-properties"></a><span data-ttu-id="9ecd5-103">使用自訂屬性</span><span class="sxs-lookup"><span data-stu-id="9ecd5-103">Using Custom Properties</span></span>

<span data-ttu-id="9ecd5-104">**使用自訂屬性**。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-104">**Using Custom Properties**.</span></span>

<span data-ttu-id="9ecd5-105">Windows 映像取得 (WIA) 驅動程式可以定義自己的自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-105">A Windows Image Acquisition (WIA) driver can define its own custom properties.</span></span> <span data-ttu-id="9ecd5-106">呼叫端可以操作自訂屬性，就像一般的 WIA 屬性一樣。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-106">Callers can manipulate custom properties just as they would normal WIA properties.</span></span> <span data-ttu-id="9ecd5-107">不過，只有您的應用程式或自訂 UI 模組可以存取這些自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-107">However, only your application or custom UI module can access these custom properties.</span></span>

<span data-ttu-id="9ecd5-108">WIA 驅動程式應該將自訂屬性定義為具有裝置屬性的 WIA 私用 DEVPROP 所位移的屬性識別碼 \_ \_ ，並 \_ \_ 針對一般專案屬性使用 wia 私用 ITEMPROP，例如 [IWiaMiniDrv 內：:d rvinititemproperties](https://msdn.microsoft.com/library/ms794131.aspx)。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-108">WIA drivers should define the custom properties to have property identifiers that are offset by WIA\_PRIVATE\_DEVPROP for device properties, and use WIA\_PRIVATE\_ITEMPROP for normal item properties, such as inside [IWiaMiniDrv::drvInitItemProperties](https://msdn.microsoft.com/library/ms794131.aspx).</span></span> <span data-ttu-id="9ecd5-109">如需詳細資訊，請參閱 [定義自訂屬性](-wia-defining-custom-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-109">For more information, see [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="9ecd5-110">有兩種方式可以將自訂參數傳遞給 WIA 驅動程式。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-110">There are two ways to pass custom parameters to WIA drivers.</span></span>

<span data-ttu-id="9ecd5-111">第一個選項是使用 **IWiaItemExtras：： Escape** 方法 () 的 Platform SDK 檔中所述。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-111">The first option is to use the **IWiaItemExtras::Escape** method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="9ecd5-112">這類似于 [IStiUSD：： Escape](https://msdn.microsoft.com/library/ms794396.aspx) 方法，但它可讓呼叫者直接使用 WIA，而不是使用 STI 方法。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-112">This is similar to the [IStiUSD::Escape](https://msdn.microsoft.com/library/ms794396.aspx) method, but it allows callers to use WIA directly, instead of using STI methods.</span></span> <span data-ttu-id="9ecd5-113">您可以使用 **IWiaItemExtras：： Escape** 將任何資訊傳遞至驅動程式，而驅動程式可以將任何資訊傳遞回來。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-113">Using **IWiaItemExtras::Escape**, you can pass any information to the driver, and the driver can pass any information back.</span></span> <span data-ttu-id="9ecd5-114">WIA 服務只會管理呼叫端與驅動程式之間傳遞的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-114">The WIA service manages only those buffers passed between the caller and the driver.</span></span>

<span data-ttu-id="9ecd5-115">第二個選項是使用自訂屬性。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-115">The second option is to use custom properties.</span></span> <span data-ttu-id="9ecd5-116">使用 **IWiaItemExtras：： Escape** 方法比使用自訂 wia 屬性更有彈性，但自訂 wia 屬性可讓您將資訊儲存在專案的屬性資料流程中，以便驅動程式可以在其他時間讀取資訊。</span><span class="sxs-lookup"><span data-stu-id="9ecd5-116">Using the **IWiaItemExtras::Escape** method is more flexible than using custom WIA properties, but custom WIA properties allow you to store information in the item's property stream so that the driver can read the information at another time.</span></span>

 

 



