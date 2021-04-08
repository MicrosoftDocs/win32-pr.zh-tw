---
description: 撥號作業可讓應用程式在先前建立的會話上傳送額外的數位。 部分撥號的使用範例是撥打延伸模組。 部分撥號有時稱為「增量撥號」或「延遲撥號」。
ms.assetid: 1dfaefd7-f8dd-451e-af18-249c89bdb517
title: 撥號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c603d8e846694b4728d1b5ad4c887be34fbac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690067"
---
# <a name="dial"></a><span data-ttu-id="2947c-105">撥號</span><span class="sxs-lookup"><span data-stu-id="2947c-105">Dial</span></span>

<span data-ttu-id="2947c-106">撥號作業可讓應用程式在先前建立的會話上傳送額外的數位。</span><span class="sxs-lookup"><span data-stu-id="2947c-106">Dial operations allow an application to send additional digits on a previously created session.</span></span> <span data-ttu-id="2947c-107">部分撥號的使用範例是撥打延伸模組。</span><span class="sxs-lookup"><span data-stu-id="2947c-107">An example use of partial dialing is to dial an extension.</span></span> <span data-ttu-id="2947c-108">部分撥號有時稱為「增量撥號」或「延遲撥號」。</span><span class="sxs-lookup"><span data-stu-id="2947c-108">Partial dialing is sometimes referred to as incremental dialing or delayed dialing.</span></span>

<span data-ttu-id="2947c-109">當提供的位址未完成時，可能會藉由將分號 ( 來撥接部分數位，) 在數位的結尾。</span><span class="sxs-lookup"><span data-stu-id="2947c-109">When the address provided is incomplete, dialing some of the digits may be delayed by placing a semicolon (;) at the end of the number.</span></span> <span data-ttu-id="2947c-110">接著會使用撥號操作，在現有的會話上傳送額外的位址資料，例如撥打將傳送呼叫的合作物件位址。</span><span class="sxs-lookup"><span data-stu-id="2947c-110">A dial operation is then used to send additional address data on the existing session, such as dialing the address of a party to which the call will be transferred.</span></span>

<span data-ttu-id="2947c-111">每個服務提供者都應該拒絕包含的撥號字串 **？**</span><span class="sxs-lookup"><span data-stu-id="2947c-111">Every service provider should reject a dial string that contains the **?**</span></span> <span data-ttu-id="2947c-112">字元，並讓應用程式適當地處理它。</span><span class="sxs-lookup"><span data-stu-id="2947c-112">character and let the application deal with it as appropriate.</span></span> <span data-ttu-id="2947c-113">例如，應用程式可以使用部分撥號來撥號字串，最多（但不包括） **？**</span><span class="sxs-lookup"><span data-stu-id="2947c-113">For example, the application could use partial dialing to dial the string, up to, but not including the **?**</span></span> <span data-ttu-id="2947c-114">字元，然後顯示對話方塊，讓使用者在撥接其他的撥號字串時發出信號。</span><span class="sxs-lookup"><span data-stu-id="2947c-114">character, and then display a dialog to let the user signal when the rest of the dial string should be dialed.</span></span>

<span data-ttu-id="2947c-115">如果服務提供者不支援一或多個呼叫進度偵測控制字元，則應用程式使用部分撥號的另一個原因是該服務提供者。</span><span class="sxs-lookup"><span data-stu-id="2947c-115">An additional reason for an application to use partial dialing is if the service provider does not support one or more of the call progress detection control characters.</span></span> <span data-ttu-id="2947c-116">這些字元可能發生在可撥撥的位址，是 W (等候撥號音) ;@ (等候無訊息回應) ;和 $ (等候電話卡提示語氣) 。</span><span class="sxs-lookup"><span data-stu-id="2947c-116">These characters, which can occur in a dialable address, are W (wait for dial tone); @ (wait for quiet answer); and $ (wait for calling-card prompt tone).</span></span> <span data-ttu-id="2947c-117">位址字串中使用的這些字元和其他所有字元，會在可 [撥](address-ovr.md)入的位址中更詳細地討論。</span><span class="sxs-lookup"><span data-stu-id="2947c-117">These and all other characters used in address strings are discussed in greater detail in [Dialable Addresses](address-ovr.md).</span></span>

<span data-ttu-id="2947c-118">提供者會指出它所支援的「等候」撥號字串修飾詞。</span><span class="sxs-lookup"><span data-stu-id="2947c-118">The provider indicates which "wait for" dial string modifiers it supports.</span></span> <span data-ttu-id="2947c-119">TAPI 2 應用程式會在 [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)所傳回之 [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps)結構的 **dwDevCapFlags** 成員中尋找這項資料。</span><span class="sxs-lookup"><span data-stu-id="2947c-119">A TAPI 2 application finds this data in the **dwDevCapFlags** member of the [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) structure returned by [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps).</span></span> <span data-ttu-id="2947c-120">TAPI 3 應用程式會呼叫 [**ITAddressCapabilities：： \_ get AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) ，並將 *AddressCap* 設定為 [**ADDRESS \_ 功能**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)的 **AC \_ DEVCAPFLAGS** 成員。</span><span class="sxs-lookup"><span data-stu-id="2947c-120">A TAPI 3 application calls [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) with *AddressCap* set to the **AC\_DEVCAPFLAGS** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).</span></span>

<span data-ttu-id="2947c-121">應用程式可以選擇針對不支援的字元 prescan.exe 可撥打的字串，或者可以在起始會話的過程中傳遞「原始」字串。</span><span class="sxs-lookup"><span data-stu-id="2947c-121">The application can choose to prescan dialable strings for unsupported characters or it can pass the "raw" string as part of initiating a session.</span></span> <span data-ttu-id="2947c-122">如果字串包含不受支援的修飾詞或 "？"，則提供者會傳回錯誤，指出在字串中第一個發生的違規修飾詞：</span><span class="sxs-lookup"><span data-stu-id="2947c-122">If the string contains an unsupported modifier or a "?", the provider will return an error indicating which offending modifier occurred first within the string:</span></span>

-   <span data-ttu-id="2947c-123">LINEERR \_ DIALBILLING</span><span class="sxs-lookup"><span data-stu-id="2947c-123">LINEERR\_DIALBILLING</span></span>
-   <span data-ttu-id="2947c-124">LINEERR \_ DIALQUIET</span><span class="sxs-lookup"><span data-stu-id="2947c-124">LINEERR\_DIALQUIET</span></span>
-   <span data-ttu-id="2947c-125">LINEERR \_ DIALDIALTONE</span><span class="sxs-lookup"><span data-stu-id="2947c-125">LINEERR\_DIALDIALTONE</span></span>
-   <span data-ttu-id="2947c-126">LINEERR \_ DIALPROMPT</span><span class="sxs-lookup"><span data-stu-id="2947c-126">LINEERR\_DIALPROMPT</span></span>

<span data-ttu-id="2947c-127">然後，應用程式可以在字串中找出違規的修飾詞、取得修飾詞左邊的數位、附加分號，然後使用部分位址初始化會話。</span><span class="sxs-lookup"><span data-stu-id="2947c-127">The application can then locate the offending modifier in the string, take the digits to the left of the modifier, append a semicolon, and initiate a session using the partial address.</span></span> <span data-ttu-id="2947c-128">您可以使用撥號操作來傳送字串的其餘部分。</span><span class="sxs-lookup"><span data-stu-id="2947c-128">The remainder of the string can be sent using the dial operation.</span></span>

<span data-ttu-id="2947c-129">並非所有服務提供者都支援使用這項作業。</span><span class="sxs-lookup"><span data-stu-id="2947c-129">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="2947c-130">**TAPI 2.x：** 請參閱 [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial)。</span><span class="sxs-lookup"><span data-stu-id="2947c-130">**TAPI 2.x:** See [**lineDial**](/windows/win32/api/tapi/nf-tapi-linedial).</span></span>

<span data-ttu-id="2947c-131">**TAPI 3.x：** 請參閱 [**ITBasicCallControl：:D ial**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-dial)。</span><span class="sxs-lookup"><span data-stu-id="2947c-131">**TAPI 3.x:** See [**ITBasicCallControl::Dial**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-dial).</span></span>

 

 
