---
description: 這些方法必須由衍生類別覆寫。
ms.assetid: 68402cff-effd-4a2b-b9f9-f13f233b1555
title: CMSPAddress 純虛擬方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a93c9b2a995554dd2f7412c8fa5bf153ea8871e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985458"
---
# <a name="cmspaddress-pure-virtual-methods"></a><span data-ttu-id="1bd69-103">CMSPAddress 純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="1bd69-103">CMSPAddress Pure Virtual Methods</span></span>

<span data-ttu-id="1bd69-104">這些方法必須由衍生類別覆寫。</span><span class="sxs-lookup"><span data-stu-id="1bd69-104">These methods must be overridden by derived classes.</span></span>



| <span data-ttu-id="1bd69-105">CMSPAddress 純虛擬方法</span><span class="sxs-lookup"><span data-stu-id="1bd69-105">CMSPAddress pure virtual methods</span></span>                           | <span data-ttu-id="1bd69-106">Description</span><span class="sxs-lookup"><span data-stu-id="1bd69-106">Description</span></span>                                                                                                                                                                            |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1bd69-107">**MSPAddressAddRef**</span><span class="sxs-lookup"><span data-stu-id="1bd69-107">**MSPAddressAddRef**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref)   | <span data-ttu-id="1bd69-108">位址的私用 AddRef 方法。</span><span class="sxs-lookup"><span data-stu-id="1bd69-108">Private AddRef method for the address.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="1bd69-109">**MSPAddressRelease**</span><span class="sxs-lookup"><span data-stu-id="1bd69-109">**MSPAddressRelease**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-mspaddressrelease) | <span data-ttu-id="1bd69-110">位址的私用版本方法。</span><span class="sxs-lookup"><span data-stu-id="1bd69-110">Private Release method for the address.</span></span>                                                                                                                                                |
| [<span data-ttu-id="1bd69-111">**CreateMSPCall**</span><span class="sxs-lookup"><span data-stu-id="1bd69-111">**CreateMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall)        | <span data-ttu-id="1bd69-112">由 TAPI 呼叫以建立呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="1bd69-112">Called by TAPI to create a call object.</span></span> <span data-ttu-id="1bd69-113">衍生類別中的實應只呼叫 [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) 函數。</span><span class="sxs-lookup"><span data-stu-id="1bd69-113">The implementation in the derived class should simply call the [**CreateMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-createmspcallhelper) function.</span></span>        |
| [<span data-ttu-id="1bd69-114">**ShutdownMSPCall**</span><span class="sxs-lookup"><span data-stu-id="1bd69-114">**ShutdownMSPCall**</span></span>](/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall)    | <span data-ttu-id="1bd69-115">由 TAPI 呼叫以關閉呼叫物件。</span><span class="sxs-lookup"><span data-stu-id="1bd69-115">Called by TAPI to shut down a call object.</span></span> <span data-ttu-id="1bd69-116">衍生類別中的實應只呼叫 [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) 函數。</span><span class="sxs-lookup"><span data-stu-id="1bd69-116">The implementation in the derived class should simply call the [**ShutdownMSPCallHelper**](/windows/desktop/api/Mspaddr/nf-mspaddr-shutdownmspcallhelper) function.</span></span> |
| [<span data-ttu-id="1bd69-117">**GetCallMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="1bd69-117">**GetCallMediaTypes**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getcallmediatypes) | <span data-ttu-id="1bd69-118">取得 MSP 所支援的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="1bd69-118">Gets media types supported by the MSP.</span></span>                                                                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="1bd69-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="1bd69-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1bd69-120">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="1bd69-120">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 



