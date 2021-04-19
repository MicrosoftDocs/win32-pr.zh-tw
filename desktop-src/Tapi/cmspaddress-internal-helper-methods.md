---
description: 下列清單包含內部 CMSP 位址方法。
ms.assetid: 2016a776-1464-46b5-96b9-b045834f9e38
title: CMSPAddress 內部 Helper 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17064d161e2a073addb2e8eef6d9d290b41278b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991944"
---
# <a name="cmspaddress-internal-helper-methods"></a><span data-ttu-id="ad2cc-103">CMSPAddress 內部 Helper 方法</span><span class="sxs-lookup"><span data-stu-id="ad2cc-103">CMSPAddress Internal Helper Methods</span></span>



| <span data-ttu-id="ad2cc-104">CMSPAddress 內部 helper 方法</span><span class="sxs-lookup"><span data-stu-id="ad2cc-104">CMSPAddress internal helper methods</span></span>                                        | <span data-ttu-id="ad2cc-105">Description</span><span class="sxs-lookup"><span data-stu-id="ad2cc-105">Description</span></span>                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ad2cc-106">**GetStaticTerminals**</span><span class="sxs-lookup"><span data-stu-id="ad2cc-106">**GetStaticTerminals**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getstaticterminals)               | <span data-ttu-id="ad2cc-107">由 [**get \_ StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) 和 [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) 呼叫，以取得可用於此位址的靜態終端陣列。</span><span class="sxs-lookup"><span data-stu-id="ad2cc-107">Called by [**get\_StaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals) and [**EnumerateStaticTerminals**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals) to get an array of static terminals that can be used on this address.</span></span>                                     |
| [<span data-ttu-id="ad2cc-108">**GetDynamicTerminalClasses**</span><span class="sxs-lookup"><span data-stu-id="ad2cc-108">**GetDynamicTerminalClasses**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-getdynamicterminalclasses) | <span data-ttu-id="ad2cc-109">由 [**get \_ DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) 和 [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) 呼叫，以取得可在此位址上使用的動態終端機類別陣列。</span><span class="sxs-lookup"><span data-stu-id="ad2cc-109">Called by [**get\_DynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-get_dynamicterminalclasses) and [**EnumerateDynamicTerminalClasses**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratedynamicterminalclasses) to get an array of dynamic terminal classes that can be used on this address.</span></span> |
| [<span data-ttu-id="ad2cc-110">**UpdateTerminalList**</span><span class="sxs-lookup"><span data-stu-id="ad2cc-110">**UpdateTerminalList**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-updateterminallist)               | <span data-ttu-id="ad2cc-111">填入 MSP 的靜態終端機清單。</span><span class="sxs-lookup"><span data-stu-id="ad2cc-111">Populates the MSP's list of static terminals.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="ad2cc-112">**ReceiveTSPAddressData**</span><span class="sxs-lookup"><span data-stu-id="ad2cc-112">**ReceiveTSPAddressData**</span></span>](/windows/desktop/api/Mspaddr/nf-mspaddr-cmspaddress-receivetspaddressdata)         | <span data-ttu-id="ad2cc-113">當 TSP 資料訊息要由位址處理，而不是由特定呼叫來處理時呼叫。</span><span class="sxs-lookup"><span data-stu-id="ad2cc-113">Called when a TSP data message is intended to be processed by the address rather than by a specific call.</span></span>                                                                                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="ad2cc-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="ad2cc-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad2cc-115">**CMSPAddress**</span><span class="sxs-lookup"><span data-stu-id="ad2cc-115">**CMSPAddress**</span></span>](/windows/desktop/api/Mspaddr/nl-mspaddr-cmspaddress)
</dt> </dl>

 

 
