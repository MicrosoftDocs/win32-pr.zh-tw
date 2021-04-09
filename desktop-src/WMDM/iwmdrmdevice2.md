---
title: IWMDRMDevice2 介面
description: 這個介面不是由服務提供者所執行，而是為了完成檔的目的而提供。IWMDRMDevice2 介面會藉由提供取得授權狀態和部分同步處理清單的方法，來擴充 IWMDRMDevice。
ms.assetid: dccc3a65-7ab1-48b1-b44f-eca0878763ca
keywords:
- IWMDRMDevice2 介面 windows Media 裝置管理員
- IWMDRMDevice2 interface windows Media 裝置管理員，說明
topic_type:
- apiref
api_name:
- IWMDRMDevice2
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8000c63d7e80b195a03ab4822117b871bcd989b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678788"
---
# <a name="iwmdrmdevice2-interface"></a><span data-ttu-id="ef9fa-105">IWMDRMDevice2 介面</span><span class="sxs-lookup"><span data-stu-id="ef9fa-105">IWMDRMDevice2 interface</span></span>

<span data-ttu-id="ef9fa-106">這個介面不是由服務提供者所執行，而是為了完成檔的目的而提供。</span><span class="sxs-lookup"><span data-stu-id="ef9fa-106">This interface is not intended to be implemented by a service provider, but is provided for purposes of complete documentation.</span></span>

<span data-ttu-id="ef9fa-107">**IWMDRMDevice2** 介面會藉由提供取得授權狀態和部分同步處理清單的方法，來擴充 **IWMDRMDevice** 。</span><span class="sxs-lookup"><span data-stu-id="ef9fa-107">The **IWMDRMDevice2** interface extends **IWMDRMDevice** by providing methods to get the license state and a partial synchronization list.</span></span>

## <a name="members"></a><span data-ttu-id="ef9fa-108">成員</span><span class="sxs-lookup"><span data-stu-id="ef9fa-108">Members</span></span>

<span data-ttu-id="ef9fa-109">**IWMDRMDevice2** 介面繼承自 [**IWMDRMDevice**](iwmdrmdevice.md)。</span><span class="sxs-lookup"><span data-stu-id="ef9fa-109">The **IWMDRMDevice2** interface inherits from [**IWMDRMDevice**](iwmdrmdevice.md).</span></span> <span data-ttu-id="ef9fa-110">**IWMDRMDevice2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ef9fa-110">**IWMDRMDevice2** also has these types of members:</span></span>

-   [<span data-ttu-id="ef9fa-111">方法</span><span class="sxs-lookup"><span data-stu-id="ef9fa-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ef9fa-112">方法</span><span class="sxs-lookup"><span data-stu-id="ef9fa-112">Methods</span></span>

<span data-ttu-id="ef9fa-113">**IWMDRMDevice2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ef9fa-113">The **IWMDRMDevice2** interface has these methods.</span></span>



| <span data-ttu-id="ef9fa-114">方法</span><span class="sxs-lookup"><span data-stu-id="ef9fa-114">Method</span></span>                                                         | <span data-ttu-id="ef9fa-115">描述</span><span class="sxs-lookup"><span data-stu-id="ef9fa-115">Description</span></span>                                     |
|:---------------------------------------------------------------|:------------------------------------------------|
| [<span data-ttu-id="ef9fa-116">**GetLicenseState**</span><span class="sxs-lookup"><span data-stu-id="ef9fa-116">**GetLicenseState**</span></span>](iwmdrmdevice2-getlicensestate.md)       | <span data-ttu-id="ef9fa-117">取得授權狀態。</span><span class="sxs-lookup"><span data-stu-id="ef9fa-117">Gets the license state.</span></span><br/>              |
| [<span data-ttu-id="ef9fa-118">**GetPartialSyncList**</span><span class="sxs-lookup"><span data-stu-id="ef9fa-118">**GetPartialSyncList**</span></span>](iwmdrmdevice2-getpartialsynclist.md) | <span data-ttu-id="ef9fa-119">取得部分同步處理清單。</span><span class="sxs-lookup"><span data-stu-id="ef9fa-119">Gets a partial synchronization list.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ef9fa-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ef9fa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef9fa-121">**服務提供者的介面**</span><span class="sxs-lookup"><span data-stu-id="ef9fa-121">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> <dt>

[<span data-ttu-id="ef9fa-122">**IWMDRMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="ef9fa-122">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





