---
description: CMSPAddress 純虛擬方法-這些方法必須由衍生類別覆寫。
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: CMSPAddress 純虛擬方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d9b9494e4ee42972d97433927fd587034af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084206"
---
# <a name="cmspaddress-pure-virtual-methods"></a><span data-ttu-id="ee477-103">CMSPAddress 純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="ee477-103">CMSPAddress Pure Virtual Methods</span></span>

<span data-ttu-id="ee477-104">這些方法必須由衍生類別覆寫。</span><span class="sxs-lookup"><span data-stu-id="ee477-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="ee477-105">CMSPAddress 純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="ee477-105">CMSPAddress pure virtual methods</span></span>                           | <span data-ttu-id="ee477-106">Description</span><span class="sxs-lookup"><span data-stu-id="ee477-106">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ee477-107">**MSPAddressAddRef**</span><span class="sxs-lookup"><span data-stu-id="ee477-107">**MSPAddressAddRef**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | <span data-ttu-id="ee477-108">位址的私用 AddRef 方法。</span><span class="sxs-lookup"><span data-stu-id="ee477-108">Private AddRef method for the address.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="ee477-109">**MSPAddressRelease**</span><span class="sxs-lookup"><span data-stu-id="ee477-109">**MSPAddressRelease**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | <span data-ttu-id="ee477-110">位址的私用版本方法。</span><span class="sxs-lookup"><span data-stu-id="ee477-110">Private Release method for the address.</span></span>                                                                                                                                                |
| [<span data-ttu-id="ee477-111">**CreateMSPCall**</span><span class="sxs-lookup"><span data-stu-id="ee477-111">**CreateMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | <span data-ttu-id="ee477-112">由 TAPI 呼叫以建立呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="ee477-112">Called by TAPI to create a call object.</span></span> <span data-ttu-id="ee477-113">衍生類別中的實應只呼叫 [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) 函數。</span><span class="sxs-lookup"><span data-stu-id="ee477-113">The implementation in the derived class should simply call the [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) function.</span></span>        |
| [<span data-ttu-id="ee477-114">**ShutdownMSPCall**</span><span class="sxs-lookup"><span data-stu-id="ee477-114">**ShutdownMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | <span data-ttu-id="ee477-115">由 TAPI 呼叫以關閉呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="ee477-115">Called by TAPI to shut down a call object.</span></span> <span data-ttu-id="ee477-116">衍生類別中的實應只呼叫 [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) 函數。</span><span class="sxs-lookup"><span data-stu-id="ee477-116">The implementation in the derived class should simply call the [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) function.</span></span> |
| [<span data-ttu-id="ee477-117">**GetCallMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="ee477-117">**GetCallMediaTypes**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | <span data-ttu-id="ee477-118">取得 MSP 所支援的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="ee477-118">Gets media types supported by the MSP.</span></span>                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="ee477-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="ee477-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee477-120">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="ee477-120">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



