---
description: 下列詞彙有助於瞭解 TAPI 技術。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b4256a4a-c19e-4431-b62f-9e9fef4b5827
title: 'S (電話語音 API) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f33f4d2c16110ad6c79a02401c6a63ad0fb8f4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992202"
---
# <a name="s-telephony-api"></a><span data-ttu-id="a0d33-103">S (電話語音 API) </span><span class="sxs-lookup"><span data-stu-id="a0d33-103">S (Telephony API)</span></span>

<span data-ttu-id="a0d33-104">[](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F [](u-tapgloss.md) [](v-tapgloss.md) G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="a0d33-104">[A](a-tapgloss.md) [B](b-tapgloss.md) [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) S [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="a0d33-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**服務提供者**</span><span class="sxs-lookup"><span data-stu-id="a0d33-105"><span id="tapi2.service_provider_tapgloss"></span><span id="TAPI2.SERVICE_PROVIDER_TAPGLOSS"></span>**service provider**</span></span>
</dt> <dd>

<span data-ttu-id="a0d33-106">動態連結程式庫，可透過一組匯出的服務功能，支援透過電話網絡進行通訊。</span><span class="sxs-lookup"><span data-stu-id="a0d33-106">A dynamic-link library that supports communications over a telephone network through a set of exported service functions.</span></span> <span data-ttu-id="a0d33-107">服務提供者會執行透過電話網絡進行通訊所需的低層級工作，以回應由 TAPI 動態連結程式庫傳送的電話語音要求。</span><span class="sxs-lookup"><span data-stu-id="a0d33-107">The service provider responds to telephony requests, sent to it by the TAPI dynamic-link library, by carrying out the low-level tasks necessary to communicate over the telephone network.</span></span> <span data-ttu-id="a0d33-108">如此一來，服務提供者與 TAPI 結合，可防止應用程式與電話網絡通訊的服務和技術相關的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a0d33-108">In this way, the service provider, in conjunction with TAPI, shields applications from the service- and technology-dependent details of the telephone network communication.</span></span>

</dd> <dt>

<span data-ttu-id="a0d33-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**subaddressing**</span><span class="sxs-lookup"><span data-stu-id="a0d33-109"><span id="tapi2.subaddressing_tapgloss"></span><span id="TAPI2.SUBADDRESSING_TAPGLOSS"></span>**subaddressing**</span></span>
</dt> <dd>

<span data-ttu-id="a0d33-110">在 ISDN 線路上提供的一項功能，可讓您比撥入時使用的單一電話號碼更多的資訊。</span><span class="sxs-lookup"><span data-stu-id="a0d33-110">A capability provided on ISDN lines that allows more information than just a single telephone number to be used when dialing.</span></span>

</dd> <dt>

<span data-ttu-id="a0d33-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**補充電話語音**</span><span class="sxs-lookup"><span data-stu-id="a0d33-111"><span id="tapi2.supplementary_telephony_tapgloss"></span><span id="TAPI2.SUPPLEMENTARY_TELEPHONY_TAPGLOSS"></span>**Supplementary Telephony**</span></span>
</dt> <dd>

<span data-ttu-id="a0d33-112">提供 advanced switch 功能的服務層級，例如保存、傳輸等等。</span><span class="sxs-lookup"><span data-stu-id="a0d33-112">Level of service that provides advanced switch features such as hold, transfer, and so on.</span></span> <span data-ttu-id="a0d33-113">所有補充服務都是選擇性的;也就是說，服務提供者不需要支援它們。</span><span class="sxs-lookup"><span data-stu-id="a0d33-113">All supplementary services are optional; that is, the service provider is not required to support them.</span></span> <span data-ttu-id="a0d33-114">請參閱 [*輔助電話語音*](a-tapgloss.md)、 [*基本電話語音*](b-tapgloss.md)、 [*擴充電話語音*](e-tapgloss.md#tapi2.extended_telephony_tapgloss)。</span><span class="sxs-lookup"><span data-stu-id="a0d33-114">See [*Assisted Telephony*](a-tapgloss.md), [*Basic Telephony*](b-tapgloss.md), [*Extended Telephony*](e-tapgloss.md#tapi2.extended_telephony_tapgloss).</span></span>

</dd> <dt>

<span data-ttu-id="a0d33-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**切換56**</span><span class="sxs-lookup"><span data-stu-id="a0d33-115"><span id="tapi2.switched_56_tapgloss"></span><span id="TAPI2.SWITCHED_56_TAPGLOSS"></span>**Switched 56**</span></span>
</dt> <dd>

<span data-ttu-id="a0d33-116">一種切換的資料服務，可讓使用者撥打電話給其他人，並以全雙工傳輸、數位同步 56 Kbps 來撥打通話的價格。</span><span class="sxs-lookup"><span data-stu-id="a0d33-116">A switched data service that lets the user dial someone else and transmit at full duplex, digital synchronous 56 Kbps for the price of a phone call.</span></span>

</dd> <dt>

<span data-ttu-id="a0d33-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**同步**</span><span class="sxs-lookup"><span data-stu-id="a0d33-117"><span id="tapi2.synchronous_tapgloss"></span><span id="TAPI2.SYNCHRONOUS_TAPGLOSS"></span>**synchronous**</span></span>
</dt> <dd>

<span data-ttu-id="a0d33-118">在連續的位、字元或事件之間有固定時間的資料傳輸方法。</span><span class="sxs-lookup"><span data-stu-id="a0d33-118">Data transmission method in which there is constant time between successive bits, characters, or events.</span></span> <span data-ttu-id="a0d33-119">時間是藉由共用單一時鐘來達成。</span><span class="sxs-lookup"><span data-stu-id="a0d33-119">The timing is achieved by the sharing of a single clock.</span></span> <span data-ttu-id="a0d33-120">傳輸的每個結束都會與傳送的資料一起使用時鐘和資訊進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="a0d33-120">Each end of the transmission synchronizes itself with the use of clocks and information sent along with the transmitted data.</span></span> <span data-ttu-id="a0d33-121">字元會以時間為單位，而不是依開始和停止位。</span><span class="sxs-lookup"><span data-stu-id="a0d33-121">Characters are spaced by time, not by start and stop bits.</span></span> <span data-ttu-id="a0d33-122">請參閱 [*非同步*](a-tapgloss.md)。</span><span class="sxs-lookup"><span data-stu-id="a0d33-122">See [*asynchronous*](a-tapgloss.md).</span></span>

</dd> </dl>

 

 



