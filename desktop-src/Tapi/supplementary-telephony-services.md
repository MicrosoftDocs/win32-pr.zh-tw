---
description: 補充的電話語音服務是由 API 定義的所有服務的集合，而不是基本電話語音子集中包含的所有服務。
ms.assetid: a2a30a0d-fbfd-4317-8e3a-d1e1e8b86ae0
title: 補充電話語音服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d93a7d12840e2001c6a2742e6bbd870d291e836
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849227"
---
# <a name="supplementary-telephony-services"></a><span data-ttu-id="7331b-103">補充電話語音服務</span><span class="sxs-lookup"><span data-stu-id="7331b-103">Supplementary Telephony Services</span></span>

<span data-ttu-id="7331b-104">補充的電話語音服務是由 API 定義的所有服務的集合，而不是基本電話語音子集中包含的所有服務。</span><span class="sxs-lookup"><span data-stu-id="7331b-104">Supplementary Telephony services are the collection of all the services defined by the API other than those included in the Basic Telephony subset.</span></span> <span data-ttu-id="7331b-105">它包含在新式 Pbx 上找到的所有所謂的補充功能，例如保存、傳輸、會議、公園等等。</span><span class="sxs-lookup"><span data-stu-id="7331b-105">It includes all so-called supplementary features found on modern PBXs, such as hold, transfer, conference, park, and so on.</span></span> <span data-ttu-id="7331b-106">所有增補功能都會被視為選擇性;也就是說，服務提供者會決定其所執行或未提供的服務。</span><span class="sxs-lookup"><span data-stu-id="7331b-106">All supplementary features are considered optional; that is, the service provider decides which of these services it does or does not provide.</span></span>

<span data-ttu-id="7331b-107">應用程式可以使用 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) 或 [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps)等函式，為它所提供的一組補充服務查詢線路或電話裝置。</span><span class="sxs-lookup"><span data-stu-id="7331b-107">An application can query a line or phone device for the set of supplementary services it provides using functions such as [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) or [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps).</span></span> <span data-ttu-id="7331b-108">單一補充服務可能包含多個函式呼叫和訊息。</span><span class="sxs-lookup"><span data-stu-id="7331b-108">A single supplementary service may consist of multiple function calls and messages.</span></span> <span data-ttu-id="7331b-109">電話語音 API （而不是服務提供者開發人員）會定義每個補充功能的行為。</span><span class="sxs-lookup"><span data-stu-id="7331b-109">The Telephony API, and not the service provider developer, defines the behavior of each of these supplementary features.</span></span> <span data-ttu-id="7331b-110">只有當服務提供者可以依照 API 所定義的確切意義來執行時，才會提供補充的電話語音服務。</span><span class="sxs-lookup"><span data-stu-id="7331b-110">A service provider should provide a Supplementary Telephony service only if it can implement the exact meaning as defined by the API.</span></span> <span data-ttu-id="7331b-111">如果沒有，則應以擴充電話語音服務的形式提供此功能。</span><span class="sxs-lookup"><span data-stu-id="7331b-111">If not, the feature should be provided as an Extended Telephony service.</span></span>

<span data-ttu-id="7331b-112">如基本電話語音服務所述，手機裝置服務會視為選擇性。</span><span class="sxs-lookup"><span data-stu-id="7331b-112">As mentioned in Basic Telephony services, phone-device services are considered optional.</span></span> <span data-ttu-id="7331b-113">因此，所有的電話裝置服務都是補充電話語音的一部分。</span><span class="sxs-lookup"><span data-stu-id="7331b-113">Therefore, all phone-device services are part of Supplementary Telephony.</span></span> <span data-ttu-id="7331b-114">如需補充電話語音的功能清單，請參閱 [TAPI 快速功能參考](./tapi-quick-function-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="7331b-114">For a list of the functions of Supplementary Telephony, see [TAPI Quick Function Reference](./tapi-quick-function-reference.md).</span></span>

 

 
