---
title: IWMDRMNonSilentLicenseAquisition 介面
description: IWMDRMNonSilentLicenseAquisition 介面提供的方法可啟用授權取得，而需要使用者介入。您可以藉由執行非無訊息授權取得來取得這個介面。
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- IWMDRMNonSilentLicenseAquisition 介面 windows 媒體格式
- IWMDRMNonSilentLicenseAquisition 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89fce7764b755231812c761778131c159ddd860b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682710"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a><span data-ttu-id="b43fb-105">IWMDRMNonSilentLicenseAquisition 介面</span><span class="sxs-lookup"><span data-stu-id="b43fb-105">IWMDRMNonSilentLicenseAquisition interface</span></span>

<span data-ttu-id="b43fb-106">**IWMDRMNonSilentLicenseAquisition** 介面提供的方法可啟用授權取得，而需要使用者介入。</span><span class="sxs-lookup"><span data-stu-id="b43fb-106">The **IWMDRMNonSilentLicenseAquisition** interface provides methods that enable license acquisition requiring user intervention.</span></span>

<span data-ttu-id="b43fb-107">您可以藉由執行非無訊息授權取得來取得這個介面。</span><span class="sxs-lookup"><span data-stu-id="b43fb-107">This interface can be obtained by performing non-silent license acquisition.</span></span> <span data-ttu-id="b43fb-108">在您呼叫 [**IWMDRMLicenseManagement：： AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) 之後，將會產生 **MEWMDRMLicenseAcquisitionCompleted** 事件。</span><span class="sxs-lookup"><span data-stu-id="b43fb-108">After you call [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) an **MEWMDRMLicenseAcquisitionCompleted** event will be generated.</span></span> <span data-ttu-id="b43fb-109">呼叫事件的 **IMFMediaEvent：： GetValue** 方法，取得可查詢此介面之實例指標的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="b43fb-109">Call the **IMFMediaEvent::GetValue** method of the event to get a pointer to an **IUnknown** interface that can be queried for a pointer to an instance of this interface.</span></span>

## <a name="members"></a><span data-ttu-id="b43fb-110">成員</span><span class="sxs-lookup"><span data-stu-id="b43fb-110">Members</span></span>

<span data-ttu-id="b43fb-111">**IWMDRMNonSilentLicenseAquisition** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="b43fb-111">The **IWMDRMNonSilentLicenseAquisition** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b43fb-112">**IWMDRMNonSilentLicenseAquisition** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b43fb-112">**IWMDRMNonSilentLicenseAquisition** also has these types of members:</span></span>

-   [<span data-ttu-id="b43fb-113">方法</span><span class="sxs-lookup"><span data-stu-id="b43fb-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b43fb-114">方法</span><span class="sxs-lookup"><span data-stu-id="b43fb-114">Methods</span></span>

<span data-ttu-id="b43fb-115">**IWMDRMNonSilentLicenseAquisition** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b43fb-115">The **IWMDRMNonSilentLicenseAquisition** interface has these methods.</span></span>



| <span data-ttu-id="b43fb-116">方法</span><span class="sxs-lookup"><span data-stu-id="b43fb-116">Method</span></span>                                                                | <span data-ttu-id="b43fb-117">描述</span><span class="sxs-lookup"><span data-stu-id="b43fb-117">Description</span></span>                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="b43fb-118">**GetChallenge**</span><span class="sxs-lookup"><span data-stu-id="b43fb-118">**GetChallenge**</span></span>](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | <span data-ttu-id="b43fb-119">抓取應張貼至授權伺服器的授權挑戰。</span><span class="sxs-lookup"><span data-stu-id="b43fb-119">Retrieves the license challenge that should be posted to the license server.</span></span><br/> |
| [<span data-ttu-id="b43fb-120">**GetURL**</span><span class="sxs-lookup"><span data-stu-id="b43fb-120">**GetURL**</span></span>](iwmdrmnonsilentlicenseaquisition-geturl.md)             | <span data-ttu-id="b43fb-121">抓取授權挑戰應張貼至其中的 URL。</span><span class="sxs-lookup"><span data-stu-id="b43fb-121">Retrieves the URL to which the license challenge should be posted.</span></span><br/>           |



 

## <a name="see-also"></a><span data-ttu-id="b43fb-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b43fb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b43fb-123">**介面**</span><span class="sxs-lookup"><span data-stu-id="b43fb-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="b43fb-124">**取得非無訊息授權**</span><span class="sxs-lookup"><span data-stu-id="b43fb-124">**Non-Silent License Acquisition**</span></span>](non-silent-license-acquisition.md)
</dt> </dl>

 

