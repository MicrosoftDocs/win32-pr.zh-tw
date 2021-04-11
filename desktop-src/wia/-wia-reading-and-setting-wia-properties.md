---
description: IWiaPropertyStorage 介面會提供方法，以讀取和寫入 Windows 映像取得 (WIA) 專案的屬性。 專案屬性包括裝置命令、專案格式資訊和裝置資訊。
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: 讀取及設定 WIA 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113285"
---
# <a name="reading-and-setting-wia-properties"></a><span data-ttu-id="3f69f-104">讀取及設定 WIA 屬性</span><span class="sxs-lookup"><span data-stu-id="3f69f-104">Reading and Setting WIA Properties</span></span>

<span data-ttu-id="3f69f-105">[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)介面會提供方法，以讀取和寫入 Windows 映像取得 (WIA) 專案的屬性。</span><span class="sxs-lookup"><span data-stu-id="3f69f-105">The [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface provides methods for reading and writing a Windows Image Acquisition (WIA) item's properties.</span></span> <span data-ttu-id="3f69f-106">專案屬性包括裝置命令、專案格式資訊和裝置資訊。</span><span class="sxs-lookup"><span data-stu-id="3f69f-106">Item properties include device commands, item format information, and device information.</span></span>

<span data-ttu-id="3f69f-107">應用程式可以藉由呼叫 [**IWiaItem：： EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities)或 [**IWiaItem：： EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) ，或藉由查詢專案的 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)介面，來取得專案之 [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="3f69f-107">An application can obtain a pointer to an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface of an item either by enumerating the item's device information or event information by calling [**IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) or [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) or by querying the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface of the item.</span></span> <span data-ttu-id="3f69f-108"> (在 WIA 2.0 中，藉由呼叫 [**IWiaItem2：： EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) 或 [**IWiaItem2：： EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) 或查詢專案的 [**IWiaItem2**](-wia-iwiaitem2.md) 介面來執行此作業。 ) </span><span class="sxs-lookup"><span data-stu-id="3f69f-108">(In WIA 2.0, do this by calling [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) or [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) or by querying the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item.)</span></span>

<span data-ttu-id="3f69f-109">[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) 繼承自 [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) ，且繼承的方法會依照 Windows 軟體開發套件 (SDK) 中結構化儲存體的參考一節所述的方式執行。</span><span class="sxs-lookup"><span data-stu-id="3f69f-109">[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) inherits from [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) and the inherited methods are implemented as described in the reference section of Structured Storage in the Windows Software Development Kit (SDK).</span></span>

> [!Note]
>
> <span data-ttu-id="3f69f-110">WIA 應用程式應該一律讀取影像資料標頭，以取得正確的影像資訊。</span><span class="sxs-lookup"><span data-stu-id="3f69f-110">WIA applications should always read image data headers for accurate image information.</span></span> <span data-ttu-id="3f69f-111">WIA 驅動程式可以在資料傳輸期間改變 WIA 屬性和影像資料標頭。</span><span class="sxs-lookup"><span data-stu-id="3f69f-111">The WIA driver can alter the WIA properties and image data headers during data transfer.</span></span>
>
> <span data-ttu-id="3f69f-112">如果未提供指定格式的影像資料標頭，則 WIA 應用程式應該使用 WIA 屬性作為資料傳輸的相關資訊來源。</span><span class="sxs-lookup"><span data-stu-id="3f69f-112">If there is no image data header supplied with the specified format, the WIA application should use the WIA properties as an information source about the data transfer.</span></span> <span data-ttu-id="3f69f-113">當掃描或抓取完成之後，WIA 應用程式應該重新讀取所需的 WIA 屬性，以取得更新的設定。</span><span class="sxs-lookup"><span data-stu-id="3f69f-113">The WIA application should reread the needed WIA properties after the scan or capture completes to get the updated settings.</span></span>

 

<span data-ttu-id="3f69f-114">下列各節說明各種 WIA 屬性：</span><span class="sxs-lookup"><span data-stu-id="3f69f-114">The following sections describe the various WIA properties:</span></span>

-   [<span data-ttu-id="3f69f-115">WIA 屬性驗證</span><span class="sxs-lookup"><span data-stu-id="3f69f-115">WIA Property Validation</span></span>](-wia-wia-property-validation.md)
-   [<span data-ttu-id="3f69f-116">裝置資訊屬性</span><span class="sxs-lookup"><span data-stu-id="3f69f-116">Device Information Properties</span></span>](-wia-device-information-properties-wia-dip-xxxx.md)
-   [<span data-ttu-id="3f69f-117">裝置內容</span><span class="sxs-lookup"><span data-stu-id="3f69f-117">Device Properties</span></span>](-wia-device-properties.md)
-   [<span data-ttu-id="3f69f-118">項目屬性</span><span class="sxs-lookup"><span data-stu-id="3f69f-118">Item Properties</span></span>](-wia-item-properties.md)
-   [<span data-ttu-id="3f69f-119">其他 WIA 屬性</span><span class="sxs-lookup"><span data-stu-id="3f69f-119">Additional WIA Properties</span></span>](-wia-additional-wia-properties.md)
-   [<span data-ttu-id="3f69f-120">定義自訂屬性</span><span class="sxs-lookup"><span data-stu-id="3f69f-120">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
-   [<span data-ttu-id="3f69f-121">使用自訂屬性</span><span class="sxs-lookup"><span data-stu-id="3f69f-121">Using Custom Properties</span></span>](-wia-using-custom-properties.md)
-   [<span data-ttu-id="3f69f-122">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="3f69f-122">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)

 

 
