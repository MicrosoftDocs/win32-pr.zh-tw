---
description: 從 IPv4 到 IPv6 的最明顯變更之一，就是 IP 位址的大小。 許多使用者介面提供的對話方塊，可讓使用者輸入 IP 位址，如下圖中的查詢示。
ms.assetid: e2d7fd41-297a-400b-ae59-5d67db2be6f6
title: IPv6 Winsock 應用程式的消費者介面問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03305073687cdd77e17c529d70ffe5959df40960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971546"
---
# <a name="user-interface-issues-for-ipv6-winsock-applications"></a><span data-ttu-id="1174e-104">IPv6 Winsock 應用程式的消費者介面問題</span><span class="sxs-lookup"><span data-stu-id="1174e-104">User Interface Issues for IPv6 Winsock Applications</span></span>

<span data-ttu-id="1174e-105">從 IPv4 到 IPv6 的最明顯變更之一，就是 IP 位址的大小。</span><span class="sxs-lookup"><span data-stu-id="1174e-105">One of the most obvious changes from IPv4 to IPv6 is the size of the IP address.</span></span> <span data-ttu-id="1174e-106">許多使用者介面提供的對話方塊，可讓使用者輸入 IP 位址，如下圖中的查詢示。</span><span class="sxs-lookup"><span data-stu-id="1174e-106">Many user interfaces provide dialog boxes that enable a user to enter an IP address, as exemplified in the following figure.</span></span>

![使用者介面中的一般 ipv4 位址方塊](images/portingguide001.jpg)

<span data-ttu-id="1174e-108">因為許多因素，例如長度、複雜度，以及 IPv6 位址空間內各區段的重要性等因素，所以在 IPv6 中定址不採用遭利用由使用者修改或規格。</span><span class="sxs-lookup"><span data-stu-id="1174e-108">Addressing in IPv6, due to many factors such as length, complexity, and the significance of sections within the IPv6 address space, is not conducive to modification or specification by users.</span></span> <span data-ttu-id="1174e-109">因此，讓使用者能夠指定自己的位址的需求也會降低。</span><span class="sxs-lookup"><span data-stu-id="1174e-109">Therefore, the need to provide users with the capability of specifying their own address is reduced.</span></span> <span data-ttu-id="1174e-110">此外，由於與 IPv6 定址相關的複雜度，讓系統管理員能夠指定 IPv6 位址資訊，不太可能會以每個節點為基礎。</span><span class="sxs-lookup"><span data-stu-id="1174e-110">Additionally, due to the complexity associated with IPv6 addressing, providing administrators with the capability of specifying IPv6 address information is not likely to occur on a per-node basis.</span></span>

<span data-ttu-id="1174e-111">在 UI 中顯示 IPv6 位址並不會 inconceivable，因此開發人員應該在修改應用程式以支援 IPv6 時，考慮 IPv6 位址的大小變化。</span><span class="sxs-lookup"><span data-stu-id="1174e-111">Displaying an IPv6 address in the UI is not inconceivable, and therefore developers should consider the variability in the size of an IPv6 address when modifying an application to support IPv6.</span></span>

<span data-ttu-id="1174e-112">本節的其餘部分將討論 IPv4 位址長度可預測性和 IPv6 位址長度考慮之間的差異。</span><span class="sxs-lookup"><span data-stu-id="1174e-112">The rest of this section discusses the difference between IPv4 address length predictability and IPv6 address length considerations.</span></span> <span data-ttu-id="1174e-113">本節假設 IPv6 位址會顯示在其十六進位標記法中。</span><span class="sxs-lookup"><span data-stu-id="1174e-113">This section presumes IPv6 addresses are being displayed in their hexadecimal representation.</span></span>

<span data-ttu-id="1174e-114">IPv4 位址的大小是可預測的，因為它們會以小數點的十進位標記法為依據，如下列位址範例所示：</span><span class="sxs-lookup"><span data-stu-id="1174e-114">IPv4 addresses are predictable in size, because they rigidly follow dotted decimal notation, as the following address example illustrates:</span></span>

``` syntax
10.10.256.1
```

<span data-ttu-id="1174e-115">IPv6 位址不是可預測的，因為 IPv6 位址慣例可讓您使用雙冒號 (：： ) 來代表一連串的零。</span><span class="sxs-lookup"><span data-stu-id="1174e-115">IPv6 addresses are not so predictable, due to the IPv6 address convention that enables the use of a double-colon (::) to represent a series of zeros.</span></span> <span data-ttu-id="1174e-116">因此，下列 IPv6 位址表示等同于相同的 IPv6 位址：</span><span class="sxs-lookup"><span data-stu-id="1174e-116">As such, the following IPv6 address representations equate to the same IPv6 address:</span></span>

``` syntax
1040:0:0:0:0:0:0:1
1040::1
```

<span data-ttu-id="1174e-117">以雙冒號表示一系列零的功能，會導致任何指定 IPv6 的長度無法預期，這需要程式設計人員在建立 IPv6 位址的使用者介面顯示時，將這項功能納入考慮。</span><span class="sxs-lookup"><span data-stu-id="1174e-117">The capability to represent a series of zeros with a double-colon results in an unpredictable length for any given IPv6, which requires programmers to take this capability into consideration when creating user interface displays of IPv6 addresses.</span></span> <span data-ttu-id="1174e-118">當然，開發人員應確定使用者介面能夠顯示不使用雙冒號的 IP 位址，以代表一系列的零 (第一個位址) ，以及能夠顯示以下的最長可能 IPv6 位址 (第二個位址，並在建立具備 IPv6 功能的使用者介面時) 內嵌的 IPv4 位址。</span><span class="sxs-lookup"><span data-stu-id="1174e-118">Certainly, developers should ensure that the user interface is capable of displaying IP addresses that do not use a double-colon to represent a series of zeros (first address below), as well as being capable of displaying the longest possible IPv6 address (second address below, with the embedded IPv4 address) when creating their IPv6-capable user interface.</span></span> <span data-ttu-id="1174e-119">也請注意，將範圍識別碼 (識別碼) 新增至下列位址，將會增加其長度，最多可達另一個11個字元：</span><span class="sxs-lookup"><span data-stu-id="1174e-119">Note, too, that adding the Scope identifier (ID) to the following address would increase its length by as much as another eleven characters:</span></span>

``` syntax
21DA:00D3:0010:2F3B:02AA:00FF:FE28:9C5A
0000:0000:0000:0000:0000:ffff:123.123.123.123
```

<span data-ttu-id="1174e-120">另一個重要考慮是，以名稱為基礎的位址是否更適合以數位為基礎的 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="1174e-120">Another important consideration is whether name-based addresses are more appropriate than number-based IPv6 addresses.</span></span> <span data-ttu-id="1174e-121">如果以名稱為基礎的位址更適合，則應該在使用者介面中內建命名慣例考慮，包括適用于工作的任何輸入錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="1174e-121">If name-based addresses are more appropriate, consideration for naming conventions should be built into the user interface, including any input error-checking appropriate for the task.</span></span>

<span data-ttu-id="1174e-122">當您在修改應用程式時，以及設計 IPv6 位址的使用者介面標記法時，會顯示開發人員必須考慮的 IPv6 位址，還有其他一些複雜性。</span><span class="sxs-lookup"><span data-stu-id="1174e-122">There are other complexities associated with displaying IPv6 addresses that developers must take into consideration when modifying their application, and when designing user interface representations of IPv6 addresses.</span></span> <span data-ttu-id="1174e-123">其中一些考慮如下：</span><span class="sxs-lookup"><span data-stu-id="1174e-123">Some of these considerations are the following:</span></span>

-   <span data-ttu-id="1174e-124">位址是否包含所有零的序列，或使用雙冒號標記法？</span><span class="sxs-lookup"><span data-stu-id="1174e-124">Should the address contain all sequences of zeros, or use the double-colon notation?</span></span>
-   <span data-ttu-id="1174e-125">是否更適合使用以數位為基礎的位址表示或以名稱為基礎的表示方式？</span><span class="sxs-lookup"><span data-stu-id="1174e-125">Is it more appropriate to use a number-based address representation or a name-based representation?</span></span>
-   <span data-ttu-id="1174e-126">使用者是否有興趣辨識定址配置的特定層面，例如子網首碼、範圍識別碼或其他子欄位？</span><span class="sxs-lookup"><span data-stu-id="1174e-126">Is the user interested in discerning a certain aspect of the addressing scheme, such as the subnet prefix, scope identifier, or other subfields?</span></span>
-   <span data-ttu-id="1174e-127">使用者是否有興趣決定位址的其他層面，例如 TLA 識別碼、NLA 識別碼或 SLA 識別碼？</span><span class="sxs-lookup"><span data-stu-id="1174e-127">Is the user interested in determining other aspects of the address, such as the TLA identifier, the NLA identifier, or the SLA identifier?</span></span>
-   <span data-ttu-id="1174e-128">您的使用者介面是否能夠辨識內嵌的 IPv6 位址，如果有的話，該如何處理和顯示？</span><span class="sxs-lookup"><span data-stu-id="1174e-128">Will your user interface be capable of discerning embedded IPv6 addresses, and if so, how will those be handled and displayed?</span></span> <span data-ttu-id="1174e-129">當您向使用者顯示位址資訊時，您會在 IPv4 相容的位址和 IPv4 對應的 IPv6 位址之間辨別嗎？</span><span class="sxs-lookup"><span data-stu-id="1174e-129">Will you discern between IPv4-compatible addresses and IPv4-mapped IPv6 addresses when displaying address information to the user?</span></span>

<span data-ttu-id="1174e-130">另外還有其他考慮，開發人員應在開發 IP 位址使用者介面時，仔細考慮他們的客戶物件。</span><span class="sxs-lookup"><span data-stu-id="1174e-130">There are other considerations as well, and developers should carefully consider their customer audience when developing IP address user interfaces.</span></span>

<span data-ttu-id="1174e-131">最佳做法</span><span class="sxs-lookup"><span data-stu-id="1174e-131">Best Practices</span></span>

-   <span data-ttu-id="1174e-132">在修改應用程式以支援 IPv6 時，開發人員必須針對每個使用者介面考慮適當的方法。</span><span class="sxs-lookup"><span data-stu-id="1174e-132">Developers must consider the appropriate approach to each user interface when modifying their application to support IPv6.</span></span> <span data-ttu-id="1174e-133">確定使用者介面包含足夠的長度來顯示 IPv6 位址是必要的，因為它會判斷該位址是以數位或名稱為基礎。</span><span class="sxs-lookup"><span data-stu-id="1174e-133">Ensuring that the user interface contains sufficient length to display IPv6 addresses is imperative, as is determining whether that address is number or name based.</span></span>
-   <span data-ttu-id="1174e-134">使用 IPv6 位址時，請盡可能使用現有的 Winsock 和 IP Helper 函式，而不是重新執行此邏輯。</span><span class="sxs-lookup"><span data-stu-id="1174e-134">Whenever possible, use existing Winsock and IP Helper functions when using IPv6 addresses rather than re-implementing this logic.</span></span> <span data-ttu-id="1174e-135">例如，您可以使用 [**RtlIpv6AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa)、 [**RtlIpv6AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw)、 [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)和 [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw) 函數，在 ipv6 位址和這些 ipv6 位址的字串表示之間進行轉換。</span><span class="sxs-lookup"><span data-stu-id="1174e-135">For example, the [**RtlIpv6AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa), [**RtlIpv6AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw), [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa), and [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw) functions can be used to convert between IPv6 addresses and string representations of these IPv6 addresses.</span></span>

<span data-ttu-id="1174e-136">要避免的程式碼</span><span class="sxs-lookup"><span data-stu-id="1174e-136">Code To Avoid</span></span>

-   <span data-ttu-id="1174e-137">相依于 IPv4 大小之位址的使用者介面元素必須經過審查，而該審查的一部分應該包含您在 IPv4) 提供 (的資訊是否適合 IPv6。</span><span class="sxs-lookup"><span data-stu-id="1174e-137">User interface elements that depend on an IPv4-sized address must undergo scrutiny, and part of that scrutiny should include whether the information you were providing (under IPv4) is appropriate for IPv6.</span></span>
-   <span data-ttu-id="1174e-138">指定 IP 位址的功能也應該取決於 IPv4 是否正在使用中，或 IPv6 是否可用。</span><span class="sxs-lookup"><span data-stu-id="1174e-138">The capability to specify an IP address should also depend on whether IPv4 is in use, or IPv6 is available.</span></span> <span data-ttu-id="1174e-139">如果有 IPv6 可用，是否適合指定以數位為基礎的 (十六進位) 位址或以名稱為基礎的位址？</span><span class="sxs-lookup"><span data-stu-id="1174e-139">If IPv6 is available, is it appropriate to specify number-based (hexadecimal) addresses or name-based addresses?</span></span>

<span data-ttu-id="1174e-140">編寫工作的程式碼</span><span class="sxs-lookup"><span data-stu-id="1174e-140">Coding Tasks</span></span>

<span data-ttu-id="1174e-141">**從 IPv4 將現有的程式碼基底修改為 IPv4 和 IPv6 互通性**</span><span class="sxs-lookup"><span data-stu-id="1174e-141">**To revise your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="1174e-142">執行使用者介面的視覺化查看，尋找相依于 IP 位址字串特定長度的任何元素。</span><span class="sxs-lookup"><span data-stu-id="1174e-142">Perform a visual review of the user interface, looking for any element that is dependent on a specific length for the IP address string.</span></span> <span data-ttu-id="1174e-143">具有容易識別之四個區段的小數點小數點標記法的控制項很容易找到，但其他控制項則否。</span><span class="sxs-lookup"><span data-stu-id="1174e-143">Controls with the easily identified four-section dotted decimal notation are easy to spot, but others are not.</span></span> <span data-ttu-id="1174e-144">可能會有一些可能會顯示 IP 位址的位置，例如在對話方塊中，IPv6 位址可能會用盡顯示空間。</span><span class="sxs-lookup"><span data-stu-id="1174e-144">There may be places where IP addresses could be displayed, such as in dialog boxes, where an IPv6 address might run out of display room.</span></span>
2.  <span data-ttu-id="1174e-145">在尋找任何這些控制項時，請在使用 IPv6 時，仔細確認是否適合顯示位址。</span><span class="sxs-lookup"><span data-stu-id="1174e-145">Upon finding any of these controls, scrutinize whether it is appropriate to display the address when using IPv6.</span></span> <span data-ttu-id="1174e-146">如果有可能是 IPv4 或 IPv6 正在使用中，請確定使用者介面可以容納其中一種。</span><span class="sxs-lookup"><span data-stu-id="1174e-146">If it is possible that either IPv4 or IPv6 is in use, ensure that the user interface can accommodate either.</span></span> <span data-ttu-id="1174e-147">以可顯示整個 IPv6 位址的使用者介面控制項來取代或增強任何控制項。</span><span class="sxs-lookup"><span data-stu-id="1174e-147">Replace or augment any controls with user interface controls that can display an entire IPv6 address.</span></span>
3.  <span data-ttu-id="1174e-148">追蹤使用者介面的測試，以確保在使用 IPv4 位址時，允許 IPv6 位址顯示的變更維持預期的可用性。</span><span class="sxs-lookup"><span data-stu-id="1174e-148">Follow up with testing of the user interface to ensure the changes that enable IPv6 address display maintain the intended usability when using IPv4 addresses.</span></span> <span data-ttu-id="1174e-149">此外，也請測試通訊協定位址顯示位置，例如資訊對話方塊，以確保它們能夠正確地處理 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="1174e-149">Also, test for protocol address display locations, such as informational dialog boxes, to ensure they properly handle IPv6 addresses.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1174e-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="1174e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1174e-151">適用于 Windows 通訊端應用程式的 IPv6 指南</span><span class="sxs-lookup"><span data-stu-id="1174e-151">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="1174e-152">變更 IPv6 Winsock Html5 應用程式的資料結構</span><span class="sxs-lookup"><span data-stu-id="1174e-152">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="1174e-153">IPv6 Winsock 應用程式的雙重堆疊通訊端</span><span class="sxs-lookup"><span data-stu-id="1174e-153">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="1174e-154">IPv6 Winsock 應用程式的函式呼叫</span><span class="sxs-lookup"><span data-stu-id="1174e-154">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="1174e-155">使用硬式編碼的 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="1174e-155">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="1174e-156">IPv6 Winsock 應用程式的基礎通訊協定</span><span class="sxs-lookup"><span data-stu-id="1174e-156">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
