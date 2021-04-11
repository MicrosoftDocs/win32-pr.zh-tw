---
description: 此設定會在相同子網上的兩部主機之間建立 IPsec 安全性關聯 (SA) ，以使用驗證標頭 (AH) 和訊息摘要 5 (MD5) 雜湊演算法來執行驗證。
ms.assetid: ed88d8ee-ac65-4310-a988-ead50ff743fd
title: 設定3：在兩個本機連結主機之間使用 IPsec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994e7a760b6ae1ba87678d6061881e5eb80faf88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113100"
---
# <a name="configuration-3-using-ipsec-between-two-local-link-hosts"></a><span data-ttu-id="9808f-103">設定3：在兩個本機連結主機之間使用 IPsec</span><span class="sxs-lookup"><span data-stu-id="9808f-103">Configuration 3: Using IPsec Between Two Local-link Hosts</span></span>

<span data-ttu-id="9808f-104">此設定會在相同子網上的兩部主機之間建立 IPsec 安全性關聯 (SA) ，以使用驗證標頭 (AH) 和訊息摘要 5 (MD5) 雜湊演算法來執行驗證。</span><span class="sxs-lookup"><span data-stu-id="9808f-104">This configuration creates an IPsec Security Association (SA) between two hosts on the same subnet to perform authentication using the Authentication Header (AH) and the Message Digest 5 (MD5) hashing algorithm.</span></span> <span data-ttu-id="9808f-105">在此範例中，所顯示的設定會使用連結-本機位址 FE80：：2AA： FF： FE53： A92C 和主機2來保護兩個相鄰主機之間的所有流量，並使用連結-本機位址 FE80：：2AA： FF： FE92： D0F1。</span><span class="sxs-lookup"><span data-stu-id="9808f-105">In this example, the configuration shown secures all traffic between two neighboring hosts: Host 1, with the link-local address FE80::2AA:FF:FE53:A92C, and Host 2, with the link-local address FE80::2AA:FF:FE92:D0F1.</span></span>

<span data-ttu-id="9808f-106">**在兩個本機連結主機之間使用 IPsec**</span><span class="sxs-lookup"><span data-stu-id="9808f-106">**To use IPsec between two local-link hosts**</span></span>

1.  <span data-ttu-id="9808f-107">在主機1上，使用 ipsec6 c 命令 (SPD) 檔建立空白安全性關聯 (悲傷) 和安全性原則。</span><span class="sxs-lookup"><span data-stu-id="9808f-107">On Host 1, create blank security association (SAD) and security policy (SPD) files by using the ipsec6 c command.</span></span> <span data-ttu-id="9808f-108">在此範例中，Ipsec6.exe 命令是 ipsec6 c test。</span><span class="sxs-lookup"><span data-stu-id="9808f-108">In this example, the Ipsec6.exe command is ipsec6 c test.</span></span> <span data-ttu-id="9808f-109">這會建立兩個檔案，以手動方式設定安全性關聯 (測試) 和安全性原則 (Test. spd) 。</span><span class="sxs-lookup"><span data-stu-id="9808f-109">This creates two files to manually configure security associations (Test.sad) and security policies (Test.spd).</span></span>
2.  <span data-ttu-id="9808f-110">在主機1上，編輯 SPD 檔案以新增安全性原則，以保護主機1和主機2之間的所有流量。</span><span class="sxs-lookup"><span data-stu-id="9808f-110">On Host 1, edit the SPD file to add a security policy that secures all traffic between Host 1 and Host 2.</span></span>

    <span data-ttu-id="9808f-111">下表顯示在此範例中，第一個專案之前加入至測試. spd 檔案的安全性原則 (未修改) 中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="9808f-111">The following table shows the security policy added to the Test.spd file before the first entry for this example (the first entry in the Test.spd file was not modified).</span></span>

    | <span data-ttu-id="9808f-112">SPD 檔案功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="9808f-112">SPD file field name</span></span> | <span data-ttu-id="9808f-113">範例值</span><span class="sxs-lookup"><span data-stu-id="9808f-113">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="9808f-114">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-114">**Policy**</span></span>          | <span data-ttu-id="9808f-115">2</span><span class="sxs-lookup"><span data-stu-id="9808f-115">2</span></span>                          |
    | <span data-ttu-id="9808f-116">**RemoteIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-116">**RemoteIPAddr**</span></span>    | <span data-ttu-id="9808f-117">**FE80：：2AA： FF： FE92： D0F1**</span><span class="sxs-lookup"><span data-stu-id="9808f-117">**FE80::2AA:FF:FE92:D0F1**</span></span> |
    | <span data-ttu-id="9808f-118">**LocalIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-118">**LocalIPAddr**</span></span>     | \*                         |
    | <span data-ttu-id="9808f-119">**Server.remoteport**</span><span class="sxs-lookup"><span data-stu-id="9808f-119">**RemotePort**</span></span>      | \*                         |
    | <span data-ttu-id="9808f-120">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="9808f-120">**Protocol**</span></span>        | \*                         |
    | <span data-ttu-id="9808f-121">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="9808f-121">**LocalPort**</span></span>       | \*                         |
    | <span data-ttu-id="9808f-122">**IPSecProtocol**</span><span class="sxs-lookup"><span data-stu-id="9808f-122">**IPSecProtocol**</span></span>   | <span data-ttu-id="9808f-123">**啊**</span><span class="sxs-lookup"><span data-stu-id="9808f-123">**AH**</span></span>                     |
    | <span data-ttu-id="9808f-124">**IPSecMode**</span><span class="sxs-lookup"><span data-stu-id="9808f-124">**IPSecMode**</span></span>       | <span data-ttu-id="9808f-125">**運輸**</span><span class="sxs-lookup"><span data-stu-id="9808f-125">**TRANSPORT**</span></span>              |
    | <span data-ttu-id="9808f-126">**RemoteGWIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-126">**RemoteGWIPAddr**</span></span>  | \*                         |
    | <span data-ttu-id="9808f-127">**SABundleIndex**</span><span class="sxs-lookup"><span data-stu-id="9808f-127">**SABundleIndex**</span></span>   | <span data-ttu-id="9808f-128">**NONE**</span><span class="sxs-lookup"><span data-stu-id="9808f-128">**NONE**</span></span>                   |
    | <span data-ttu-id="9808f-129">[方向]</span><span class="sxs-lookup"><span data-stu-id="9808f-129">**Direction**</span></span>       | <span data-ttu-id="9808f-130">**BIDIRECT**</span><span class="sxs-lookup"><span data-stu-id="9808f-130">**BIDIRECT**</span></span>               |
    | <span data-ttu-id="9808f-131">**動作**</span><span class="sxs-lookup"><span data-stu-id="9808f-131">**Action**</span></span>          | <span data-ttu-id="9808f-132">**應用**</span><span class="sxs-lookup"><span data-stu-id="9808f-132">**APPLY**</span></span>                  |
    | <span data-ttu-id="9808f-133">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="9808f-133">**InterfaceIndex**</span></span>  | <span data-ttu-id="9808f-134">0</span><span class="sxs-lookup"><span data-stu-id="9808f-134">0</span></span>                          |

    

     

    <span data-ttu-id="9808f-135">將分號放在設定此安全性原則的行尾。</span><span class="sxs-lookup"><span data-stu-id="9808f-135">Place a semicolon at the end of the line configuring this security policy.</span></span> <span data-ttu-id="9808f-136">原則專案必須以遞減的數值順序放置。</span><span class="sxs-lookup"><span data-stu-id="9808f-136">The policy entries must be placed in decreasing numerical order.</span></span>

3.  <span data-ttu-id="9808f-137">在主機1上，編輯悲傷檔案，新增 SA 專案以保護主機1和主機2之間的所有流量。</span><span class="sxs-lookup"><span data-stu-id="9808f-137">On Host 1, edit the SAD file, adding SA entries to secure all traffic between Host 1 and Host 2.</span></span> <span data-ttu-id="9808f-138">必須建立兩個安全性關聯，一個用於主機2的流量，另一個用於主機2的流量。</span><span class="sxs-lookup"><span data-stu-id="9808f-138">Two security associations must be created, one for traffic to Host 2 and one for traffic from Host 2.</span></span>

    <span data-ttu-id="9808f-139">下表顯示此範例 (的第一個 SA 專案加入至主機 2) 的流量。</span><span class="sxs-lookup"><span data-stu-id="9808f-139">The following table shows the first SA entry added to the Test.sad file for this example (for traffic to Host 2).</span></span>

    | <span data-ttu-id="9808f-140">悲傷的檔案功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="9808f-140">SAD file field name</span></span> | <span data-ttu-id="9808f-141">範例值</span><span class="sxs-lookup"><span data-stu-id="9808f-141">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="9808f-142">**SAEntry**</span><span class="sxs-lookup"><span data-stu-id="9808f-142">**SAEntry**</span></span>         | <span data-ttu-id="9808f-143">2</span><span class="sxs-lookup"><span data-stu-id="9808f-143">2</span></span>                          |
    | <span data-ttu-id="9808f-144">**SPI**</span><span class="sxs-lookup"><span data-stu-id="9808f-144">**SPI**</span></span>             | <span data-ttu-id="9808f-145">3001</span><span class="sxs-lookup"><span data-stu-id="9808f-145">3001</span></span>                       |
    | <span data-ttu-id="9808f-146">**SADestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-146">**SADestIPAddr**</span></span>    | <span data-ttu-id="9808f-147">**FE80：：2AA： FF： FE92： D0F1**</span><span class="sxs-lookup"><span data-stu-id="9808f-147">**FE80::2AA:FF:FE92:D0F1**</span></span> |
    | <span data-ttu-id="9808f-148">**DestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-148">**DestIPAddr**</span></span>      | <span data-ttu-id="9808f-149">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-149">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-150">**SrcIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-150">**SrcIPAddr**</span></span>       | <span data-ttu-id="9808f-151">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-151">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-152">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="9808f-152">**Protocol**</span></span>        | <span data-ttu-id="9808f-153">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-153">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-154">**DestPort**</span><span class="sxs-lookup"><span data-stu-id="9808f-154">**DestPort**</span></span>        | <span data-ttu-id="9808f-155">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-155">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-156">**SrcPort**</span><span class="sxs-lookup"><span data-stu-id="9808f-156">**SrcPort**</span></span>         | <span data-ttu-id="9808f-157">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-157">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-158">**AuthAlg**</span><span class="sxs-lookup"><span data-stu-id="9808f-158">**AuthAlg**</span></span>         | <span data-ttu-id="9808f-159">**HMAC-MD5**</span><span class="sxs-lookup"><span data-stu-id="9808f-159">**HMAC-MD5**</span></span>               |
    | <span data-ttu-id="9808f-160">**KeyFile**</span><span class="sxs-lookup"><span data-stu-id="9808f-160">**KeyFile**</span></span>         | <span data-ttu-id="9808f-161">**測試金鑰**</span><span class="sxs-lookup"><span data-stu-id="9808f-161">**Test.key**</span></span>               |
    | <span data-ttu-id="9808f-162">[方向]</span><span class="sxs-lookup"><span data-stu-id="9808f-162">**Direction**</span></span>       | <span data-ttu-id="9808f-163">**出境**</span><span class="sxs-lookup"><span data-stu-id="9808f-163">**OUTBOUND**</span></span>               |
    | <span data-ttu-id="9808f-164">**SecPolicyIndex**</span><span class="sxs-lookup"><span data-stu-id="9808f-164">**SecPolicyIndex**</span></span>  | <span data-ttu-id="9808f-165">2</span><span class="sxs-lookup"><span data-stu-id="9808f-165">2</span></span>                          |

    

     

    <span data-ttu-id="9808f-166">在設定此 SA 的行尾放置分號。</span><span class="sxs-lookup"><span data-stu-id="9808f-166">Place a semicolon at the end of the line configuring this SA.</span></span>

    <span data-ttu-id="9808f-167">下表顯示在此範例中，針對來自主機 2) 的流量，將第二個 SA 專案新增至測試的 (。</span><span class="sxs-lookup"><span data-stu-id="9808f-167">The following table shows the second SA entry added to the Test.sad file for this example (for traffic from Host 2).</span></span>

    | <span data-ttu-id="9808f-168">悲傷的檔案功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="9808f-168">SAD file field name</span></span> | <span data-ttu-id="9808f-169">範例值</span><span class="sxs-lookup"><span data-stu-id="9808f-169">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="9808f-170">**SAEntry**</span><span class="sxs-lookup"><span data-stu-id="9808f-170">**SAEntry**</span></span>         | <span data-ttu-id="9808f-171">1</span><span class="sxs-lookup"><span data-stu-id="9808f-171">1</span></span>                          |
    | <span data-ttu-id="9808f-172">**SPI**</span><span class="sxs-lookup"><span data-stu-id="9808f-172">**SPI**</span></span>             | <span data-ttu-id="9808f-173">3000</span><span class="sxs-lookup"><span data-stu-id="9808f-173">3000</span></span>                       |
    | <span data-ttu-id="9808f-174">**SADestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-174">**SADestIPAddr**</span></span>    | <span data-ttu-id="9808f-175">**FE80：：2AA： FF： FE53： A92C**</span><span class="sxs-lookup"><span data-stu-id="9808f-175">**FE80::2AA:FF:FE53:A92C**</span></span> |
    | <span data-ttu-id="9808f-176">**DestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-176">**DestIPAddr**</span></span>      | <span data-ttu-id="9808f-177">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-177">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-178">**SrcIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-178">**SrcIPAddr**</span></span>       | <span data-ttu-id="9808f-179">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-179">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-180">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="9808f-180">**Protocol**</span></span>        | <span data-ttu-id="9808f-181">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-181">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-182">**DestPort**</span><span class="sxs-lookup"><span data-stu-id="9808f-182">**DestPort**</span></span>        | <span data-ttu-id="9808f-183">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-183">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-184">**SrcPort**</span><span class="sxs-lookup"><span data-stu-id="9808f-184">**SrcPort**</span></span>         | <span data-ttu-id="9808f-185">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-185">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-186">**AuthAlg**</span><span class="sxs-lookup"><span data-stu-id="9808f-186">**AuthAlg**</span></span>         | <span data-ttu-id="9808f-187">**HMAC-MD5**</span><span class="sxs-lookup"><span data-stu-id="9808f-187">**HMAC-MD5**</span></span>               |
    | <span data-ttu-id="9808f-188">**KeyFile**</span><span class="sxs-lookup"><span data-stu-id="9808f-188">**KeyFile**</span></span>         | <span data-ttu-id="9808f-189">**測試金鑰**</span><span class="sxs-lookup"><span data-stu-id="9808f-189">**Test.key**</span></span>               |
    | <span data-ttu-id="9808f-190">[方向]</span><span class="sxs-lookup"><span data-stu-id="9808f-190">**Direction**</span></span>       | <span data-ttu-id="9808f-191">**入境**</span><span class="sxs-lookup"><span data-stu-id="9808f-191">**INBOUND**</span></span>                |
    | <span data-ttu-id="9808f-192">**SecPolicyIndex**</span><span class="sxs-lookup"><span data-stu-id="9808f-192">**SecPolicyIndex**</span></span>  | <span data-ttu-id="9808f-193">2</span><span class="sxs-lookup"><span data-stu-id="9808f-193">2</span></span>                          |

    

     

    <span data-ttu-id="9808f-194">在設定此 SA 的行尾放置分號。</span><span class="sxs-lookup"><span data-stu-id="9808f-194">Place a semicolon at the end of the line configuring this SA.</span></span> <span data-ttu-id="9808f-195">SA 專案必須以遞減的數位順序放置。</span><span class="sxs-lookup"><span data-stu-id="9808f-195">The SA entries must be placed in decreasing numerical order.</span></span>

4.  <span data-ttu-id="9808f-196">在主機1上，建立一個文字檔，其中包含用來驗證主機2所建立之 SAs 的文字字串。</span><span class="sxs-lookup"><span data-stu-id="9808f-196">On Host 1, create a text file that contains a text string used to authenticate the SAs created with Host 2.</span></span> <span data-ttu-id="9808f-197">在此範例中，會使用「這是測試」內容來建立檔案測試。</span><span class="sxs-lookup"><span data-stu-id="9808f-197">In this example, the file Test.key is created with the contents "This is a test".</span></span> <span data-ttu-id="9808f-198">您必須在索引鍵字串前後加上雙引號，才能讓 ipsec6 工具讀取金鑰。</span><span class="sxs-lookup"><span data-stu-id="9808f-198">You must include double quotes around the key string in order for the key to be read by the ipsec6 tool.</span></span>

    <span data-ttu-id="9808f-199">Microsoft IPv6 技術預覽僅支援手動設定的金鑰來驗證 IPsec SAs。</span><span class="sxs-lookup"><span data-stu-id="9808f-199">The Microsoft IPv6 Technology Preview only supports manually configured keys for the authentication of IPsec SAs.</span></span> <span data-ttu-id="9808f-200">手動金鑰的設定方式是建立文字檔，其中包含手動按鍵的文字字串。</span><span class="sxs-lookup"><span data-stu-id="9808f-200">The manual keys are configured by creating text files that contain the text string of the manual key.</span></span> <span data-ttu-id="9808f-201">在此範例中，會在兩個方向使用相同的 SAs 金鑰。</span><span class="sxs-lookup"><span data-stu-id="9808f-201">In this example, the same key for the SAs is used in both directions.</span></span> <span data-ttu-id="9808f-202">您可以使用不同的金鑰來處理輸入和輸出 SAs，方法是建立不同的金鑰檔，然後使用 SAD 檔案中的 KeyFile 欄位來參考它們。</span><span class="sxs-lookup"><span data-stu-id="9808f-202">You can use different keys for inbound and outbound SAs by creating different key files and referencing them with the KeyFile field in the SAD file.</span></span>

5.  <span data-ttu-id="9808f-203">在主機2上，使用 ipsec6 c 命令 (SPD) 檔建立空白安全性關聯 (悲傷) 和安全性原則。</span><span class="sxs-lookup"><span data-stu-id="9808f-203">On Host 2, create blank security association (SAD) and security policy (SPD) files by using the ipsec6 c command.</span></span> <span data-ttu-id="9808f-204">在此範例中，Ipsec6.exe 命令是 ipsec6 c test。</span><span class="sxs-lookup"><span data-stu-id="9808f-204">In this example, the Ipsec6.exe command is ipsec6 c test.</span></span> <span data-ttu-id="9808f-205">這會建立兩個具有空白專案的檔案，以便手動設定安全性關聯 (測試) 和安全性原則 (Test. spd) 。</span><span class="sxs-lookup"><span data-stu-id="9808f-205">This creates two files with blank entries for manually configuring security associations (Test.sad) and security policies (Test.spd).</span></span>

    <span data-ttu-id="9808f-206">為了簡化此範例，會在主機2上使用相同的悲傷和 SPD 檔案檔案名。</span><span class="sxs-lookup"><span data-stu-id="9808f-206">To simplify the example, the same file names for the SAD and SPD files are used on Host 2.</span></span> <span data-ttu-id="9808f-207">您可以選擇在每部主機上使用不同的檔案名。</span><span class="sxs-lookup"><span data-stu-id="9808f-207">You can choose to use different file names on each host.</span></span>

6.  <span data-ttu-id="9808f-208">在主機2上，編輯 SPD 檔案以新增安全性原則，以保護主機2和主機1之間的所有流量。</span><span class="sxs-lookup"><span data-stu-id="9808f-208">On Host 2, edit the SPD file to add a security policy that secures all traffic between Host 2 and Host 1.</span></span>

    <span data-ttu-id="9808f-209">下表顯示在此範例中，將第一個專案加入至測試的測試檔中之前加入的安全性原則專案 (測試中的第一個專案未) 修改。</span><span class="sxs-lookup"><span data-stu-id="9808f-209">The following table shows the security policy entry added before the first entry to the Test.spd file for this example (the first entry in the Test.spd file was not modified).</span></span>

    | <span data-ttu-id="9808f-210">SPD 檔案功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="9808f-210">SPD file field name</span></span> | <span data-ttu-id="9808f-211">範例值</span><span class="sxs-lookup"><span data-stu-id="9808f-211">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="9808f-212">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-212">**Policy**</span></span>          | <span data-ttu-id="9808f-213">2</span><span class="sxs-lookup"><span data-stu-id="9808f-213">2</span></span>                          |
    | <span data-ttu-id="9808f-214">**RemoteIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-214">**RemoteIPAddr**</span></span>    | <span data-ttu-id="9808f-215">**FE80：：2AA： FF： FE53： A92C**</span><span class="sxs-lookup"><span data-stu-id="9808f-215">**FE80::2AA:FF:FE53:A92C**</span></span> |
    | <span data-ttu-id="9808f-216">**LocalIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-216">**LocalIPAddr**</span></span>     | \*                         |
    | <span data-ttu-id="9808f-217">**Server.remoteport**</span><span class="sxs-lookup"><span data-stu-id="9808f-217">**RemotePort**</span></span>      | \*                         |
    | <span data-ttu-id="9808f-218">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="9808f-218">**Protocol**</span></span>        | \*                         |
    | <span data-ttu-id="9808f-219">**LocalPort**</span><span class="sxs-lookup"><span data-stu-id="9808f-219">**LocalPort**</span></span>       | \*                         |
    | <span data-ttu-id="9808f-220">**IPSecProtocol**</span><span class="sxs-lookup"><span data-stu-id="9808f-220">**IPSecProtocol**</span></span>   | <span data-ttu-id="9808f-221">**啊**</span><span class="sxs-lookup"><span data-stu-id="9808f-221">**AH**</span></span>                     |
    | <span data-ttu-id="9808f-222">**IPSecMode**</span><span class="sxs-lookup"><span data-stu-id="9808f-222">**IPSecMode**</span></span>       | <span data-ttu-id="9808f-223">**運輸**</span><span class="sxs-lookup"><span data-stu-id="9808f-223">**TRANSPORT**</span></span>              |
    | <span data-ttu-id="9808f-224">**RemoteGWIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-224">**RemoteGWIPAddr**</span></span>  | \*                         |
    | <span data-ttu-id="9808f-225">**SABundleIndex**</span><span class="sxs-lookup"><span data-stu-id="9808f-225">**SABundleIndex**</span></span>   | <span data-ttu-id="9808f-226">**NONE**</span><span class="sxs-lookup"><span data-stu-id="9808f-226">**NONE**</span></span>                   |
    | <span data-ttu-id="9808f-227">[方向]</span><span class="sxs-lookup"><span data-stu-id="9808f-227">**Direction**</span></span>       | <span data-ttu-id="9808f-228">**BIDIRECT**</span><span class="sxs-lookup"><span data-stu-id="9808f-228">**BIDIRECT**</span></span>               |
    | <span data-ttu-id="9808f-229">**動作**</span><span class="sxs-lookup"><span data-stu-id="9808f-229">**Action**</span></span>          | <span data-ttu-id="9808f-230">**應用**</span><span class="sxs-lookup"><span data-stu-id="9808f-230">**APPLY**</span></span>                  |
    | <span data-ttu-id="9808f-231">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="9808f-231">**InterfaceIndex**</span></span>  | <span data-ttu-id="9808f-232">0</span><span class="sxs-lookup"><span data-stu-id="9808f-232">0</span></span>                          |

    

     

    <span data-ttu-id="9808f-233">將分號放在設定此安全性原則的行尾。</span><span class="sxs-lookup"><span data-stu-id="9808f-233">Place a semicolon at the end of the line configuring this security policy.</span></span> <span data-ttu-id="9808f-234">原則專案必須以遞減的數值順序放置。</span><span class="sxs-lookup"><span data-stu-id="9808f-234">The policy entries must be placed in decreasing numerical order.</span></span>

7.  <span data-ttu-id="9808f-235">在主機2上，編輯悲傷檔案，新增 SA 專案以保護主機2與主機1之間的所有流量。</span><span class="sxs-lookup"><span data-stu-id="9808f-235">On Host 2, edit the SAD file, adding SA entries to secure all traffic between Host 2 and Host 1.</span></span> <span data-ttu-id="9808f-236">必須建立兩個安全性關聯-一個用於主機1的流量，另一個用於主機1的流量。</span><span class="sxs-lookup"><span data-stu-id="9808f-236">Two security associations must be created-one for traffic to Host 1 and one for traffic from Host 1.</span></span>

    <span data-ttu-id="9808f-237">下表顯示在此範例中，針對來自主機 1) 的流量，將第一個 SA 新增至測試的 (。</span><span class="sxs-lookup"><span data-stu-id="9808f-237">The following table shows the first SA added to the Test.sad file for this example (for traffic from Host 1).</span></span>

    | <span data-ttu-id="9808f-238">悲傷的檔案功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="9808f-238">SAD file field name</span></span> | <span data-ttu-id="9808f-239">範例值</span><span class="sxs-lookup"><span data-stu-id="9808f-239">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="9808f-240">**SAEntry**</span><span class="sxs-lookup"><span data-stu-id="9808f-240">**SAEntry**</span></span>         | <span data-ttu-id="9808f-241">2</span><span class="sxs-lookup"><span data-stu-id="9808f-241">2</span></span>                          |
    | <span data-ttu-id="9808f-242">**SPI**</span><span class="sxs-lookup"><span data-stu-id="9808f-242">**SPI**</span></span>             | <span data-ttu-id="9808f-243">3001</span><span class="sxs-lookup"><span data-stu-id="9808f-243">3001</span></span>                       |
    | <span data-ttu-id="9808f-244">**SADestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-244">**SADestIPAddr**</span></span>    | <span data-ttu-id="9808f-245">**FE80：：2AA： FF： FE92： D0F1**</span><span class="sxs-lookup"><span data-stu-id="9808f-245">**FE80::2AA:FF:FE92:D0F1**</span></span> |
    | <span data-ttu-id="9808f-246">**DestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-246">**DestIPAddr**</span></span>      | <span data-ttu-id="9808f-247">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-247">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-248">**SrcIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-248">**SrcIPAddr**</span></span>       | <span data-ttu-id="9808f-249">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-249">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-250">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="9808f-250">**Protocol**</span></span>        | <span data-ttu-id="9808f-251">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-251">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-252">**DestPort**</span><span class="sxs-lookup"><span data-stu-id="9808f-252">**DestPort**</span></span>        | <span data-ttu-id="9808f-253">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-253">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-254">**SrcPort**</span><span class="sxs-lookup"><span data-stu-id="9808f-254">**SrcPort**</span></span>         | <span data-ttu-id="9808f-255">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-255">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-256">**AuthAlg**</span><span class="sxs-lookup"><span data-stu-id="9808f-256">**AuthAlg**</span></span>         | <span data-ttu-id="9808f-257">**HMAC-MD5**</span><span class="sxs-lookup"><span data-stu-id="9808f-257">**HMAC-MD5**</span></span>               |
    | <span data-ttu-id="9808f-258">**KeyFile**</span><span class="sxs-lookup"><span data-stu-id="9808f-258">**KeyFile**</span></span>         | <span data-ttu-id="9808f-259">**測試金鑰**</span><span class="sxs-lookup"><span data-stu-id="9808f-259">**Test.key**</span></span>               |
    | <span data-ttu-id="9808f-260">[方向]</span><span class="sxs-lookup"><span data-stu-id="9808f-260">**Direction**</span></span>       | <span data-ttu-id="9808f-261">**入境**</span><span class="sxs-lookup"><span data-stu-id="9808f-261">**INBOUND**</span></span>                |
    | <span data-ttu-id="9808f-262">**SecPolicyIndex**</span><span class="sxs-lookup"><span data-stu-id="9808f-262">**SecPolicyIndex**</span></span>  | <span data-ttu-id="9808f-263">2</span><span class="sxs-lookup"><span data-stu-id="9808f-263">2</span></span>                          |

    

     

    <span data-ttu-id="9808f-264">在設定此 SA 的行尾放置分號。</span><span class="sxs-lookup"><span data-stu-id="9808f-264">Place a semicolon at the end of the line configuring this SA.</span></span>

    <span data-ttu-id="9808f-265">下表顯示在此範例中，新增至測試的測試悲傷檔案的第二個 SA 專案 (用於裝載 1) 的流量。</span><span class="sxs-lookup"><span data-stu-id="9808f-265">The following table shows the second SA entry added to the Test.sad file for this example (for traffic to Host 1).</span></span>

    | <span data-ttu-id="9808f-266">悲傷的檔案功能變數名稱</span><span class="sxs-lookup"><span data-stu-id="9808f-266">SAD file field name</span></span> | <span data-ttu-id="9808f-267">範例值</span><span class="sxs-lookup"><span data-stu-id="9808f-267">Example value</span></span>              |
    |---------------------|----------------------------|
    | <span data-ttu-id="9808f-268">**SAEntry**</span><span class="sxs-lookup"><span data-stu-id="9808f-268">**SAEntry**</span></span>         | <span data-ttu-id="9808f-269">1</span><span class="sxs-lookup"><span data-stu-id="9808f-269">1</span></span>                          |
    | <span data-ttu-id="9808f-270">**SPI**</span><span class="sxs-lookup"><span data-stu-id="9808f-270">**SPI**</span></span>             | <span data-ttu-id="9808f-271">3000</span><span class="sxs-lookup"><span data-stu-id="9808f-271">3000</span></span>                       |
    | <span data-ttu-id="9808f-272">**SADestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-272">**SADestIPAddr**</span></span>    | <span data-ttu-id="9808f-273">**FE80：：2AA： FF： FE53： A92C**</span><span class="sxs-lookup"><span data-stu-id="9808f-273">**FE80::2AA:FF:FE53:A92C**</span></span> |
    | <span data-ttu-id="9808f-274">**DestIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-274">**DestIPAddr**</span></span>      | <span data-ttu-id="9808f-275">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-275">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-276">**SrcIPAddr**</span><span class="sxs-lookup"><span data-stu-id="9808f-276">**SrcIPAddr**</span></span>       | <span data-ttu-id="9808f-277">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-277">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-278">**通訊協定**</span><span class="sxs-lookup"><span data-stu-id="9808f-278">**Protocol**</span></span>        | <span data-ttu-id="9808f-279">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-279">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-280">**DestPort**</span><span class="sxs-lookup"><span data-stu-id="9808f-280">**DestPort**</span></span>        | <span data-ttu-id="9808f-281">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-281">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-282">**SrcPort**</span><span class="sxs-lookup"><span data-stu-id="9808f-282">**SrcPort**</span></span>         | <span data-ttu-id="9808f-283">**原則**</span><span class="sxs-lookup"><span data-stu-id="9808f-283">**POLICY**</span></span>                 |
    | <span data-ttu-id="9808f-284">**AuthAlg**</span><span class="sxs-lookup"><span data-stu-id="9808f-284">**AuthAlg**</span></span>         | <span data-ttu-id="9808f-285">**HMAC-MD5**</span><span class="sxs-lookup"><span data-stu-id="9808f-285">**HMAC-MD5**</span></span>               |
    | <span data-ttu-id="9808f-286">**KeyFile**</span><span class="sxs-lookup"><span data-stu-id="9808f-286">**KeyFile**</span></span>         | <span data-ttu-id="9808f-287">**測試金鑰**</span><span class="sxs-lookup"><span data-stu-id="9808f-287">**Test.key**</span></span>               |
    | <span data-ttu-id="9808f-288">[方向]</span><span class="sxs-lookup"><span data-stu-id="9808f-288">**Direction**</span></span>       | <span data-ttu-id="9808f-289">**出境**</span><span class="sxs-lookup"><span data-stu-id="9808f-289">**OUTBOUND**</span></span>               |
    | <span data-ttu-id="9808f-290">**SecPolicyIndex**</span><span class="sxs-lookup"><span data-stu-id="9808f-290">**SecPolicyIndex**</span></span>  | <span data-ttu-id="9808f-291">2</span><span class="sxs-lookup"><span data-stu-id="9808f-291">2</span></span>                          |

    

     

    <span data-ttu-id="9808f-292">在設定此 SA 的行尾放置分號。</span><span class="sxs-lookup"><span data-stu-id="9808f-292">Place a semicolon at the end of the line configuring this SA.</span></span> <span data-ttu-id="9808f-293">SA 專案必須以遞減的數位順序放置。</span><span class="sxs-lookup"><span data-stu-id="9808f-293">The SA entries must be placed in decreasing numerical order.</span></span>

8.  <span data-ttu-id="9808f-294">在主機2上，建立一個文字檔，其中包含用來驗證以主機1建立之 SAs 的文字字串。</span><span class="sxs-lookup"><span data-stu-id="9808f-294">On Host 2, create a text file that contains a text string used to authenticate the SAs created with Host 1.</span></span> <span data-ttu-id="9808f-295">在此範例中，會使用「這是測試」內容來建立檔案測試。</span><span class="sxs-lookup"><span data-stu-id="9808f-295">In this example, the file Test.key is created with the contents "This is a test".</span></span> <span data-ttu-id="9808f-296">您必須在索引鍵字串前後加上雙引號，才能讓 ipsec6 工具讀取金鑰。</span><span class="sxs-lookup"><span data-stu-id="9808f-296">You must include double quotes around the key string in order for the key to be read by the ipsec6 tool.</span></span>
9.  <span data-ttu-id="9808f-297">在主機1上，使用 ipsec6 命令，從 SPD 和悲傷檔案新增設定的安全性原則和 SAs。</span><span class="sxs-lookup"><span data-stu-id="9808f-297">On Host 1, add the configured security policies and SAs from the SPD and SAD files using the ipsec6 a command.</span></span> <span data-ttu-id="9808f-298">在此範例中，ipsec6 會在主機1上執行測試命令。</span><span class="sxs-lookup"><span data-stu-id="9808f-298">In this example, the ipsec6 a test command is run on Host 1.</span></span>
10. <span data-ttu-id="9808f-299">在主機2上，使用 ipsec6 命令，從 SPD 和悲傷檔案新增設定的安全性原則和 SAs。</span><span class="sxs-lookup"><span data-stu-id="9808f-299">On Host 2, add the configured security policies and SAs from the SPD and SAD files by using the ipsec6 a command.</span></span> <span data-ttu-id="9808f-300">在此範例中，ipsec6 會在主機2上執行測試命令。</span><span class="sxs-lookup"><span data-stu-id="9808f-300">In this example, the ipsec6 a test command is run on Host 2.</span></span>
11. <span data-ttu-id="9808f-301">使用 ping6 命令從主機2偵測主機1。</span><span class="sxs-lookup"><span data-stu-id="9808f-301">Ping Host 1 from Host 2 with the ping6 command.</span></span>

    <span data-ttu-id="9808f-302">如果您使用 Microsoft 網路監視器或另一個封包探測器來捕捉流量，您應該會看到 ICMPv6 Echo 要求和回應訊息的交換，以及 IPv6 標頭與 ICMPv6 標頭之間的驗證標頭。</span><span class="sxs-lookup"><span data-stu-id="9808f-302">If you capture the traffic using Microsoft Network Monitor or another packet sniffer, you should see the exchange of ICMPv6 Echo Request and Echo Reply messages with an Authentication Header between the IPv6 header and the ICMPv6 header.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9808f-303">相關主題</span><span class="sxs-lookup"><span data-stu-id="9808f-303">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9808f-304">IPv6 的建議設定</span><span class="sxs-lookup"><span data-stu-id="9808f-304">Recommended Configurations for IPv6</span></span>](recommended-configurations-2.md)
</dt> <dt>

[<span data-ttu-id="9808f-305">具有連結-本機位址的單一子網</span><span class="sxs-lookup"><span data-stu-id="9808f-305">Single subnet with link-local addresses</span></span>](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="9808f-306">IPv4 網路上不同子網節點之間的 IPv6 流量 (6to4) </span><span class="sxs-lookup"><span data-stu-id="9808f-306">IPv6 traffic between nodes on different subnets of an IPv4 internetwork (6to4)</span></span>](configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4--2.md)
</dt> </dl>

 

 



