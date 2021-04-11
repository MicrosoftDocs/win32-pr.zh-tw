---
description: CNG 提供私密金鑰儲存的模型，可讓您根據目前和未來建立使用加密功能（例如公用或私密金鑰加密）的應用程式，以及儲存金鑰資料的需求。
ms.assetid: 95e5750f-fdc5-41f3-a4ce-9593a7081e95
title: 金鑰儲存和抓取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5abfd6319353440c580d53990075a71613a1eba9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320079"
---
# <a name="key-storage-and-retrieval"></a><span data-ttu-id="a2952-103">金鑰儲存和抓取</span><span class="sxs-lookup"><span data-stu-id="a2952-103">Key Storage and Retrieval</span></span>

-   [<span data-ttu-id="a2952-104">金鑰儲存架構</span><span class="sxs-lookup"><span data-stu-id="a2952-104">Key Storage Architecture</span></span>](#key-storage-architecture)
-   [<span data-ttu-id="a2952-105">金鑰類型</span><span class="sxs-lookup"><span data-stu-id="a2952-105">Key Types</span></span>](#key-types)
-   [<span data-ttu-id="a2952-106">支援的演算法</span><span class="sxs-lookup"><span data-stu-id="a2952-106">Supported Algorithms</span></span>](#supported-algorithms)
-   [<span data-ttu-id="a2952-107">金鑰目錄和檔案</span><span class="sxs-lookup"><span data-stu-id="a2952-107">Key Directories and Files</span></span>](#key-directories-and-files)

## <a name="key-storage-architecture"></a><span data-ttu-id="a2952-108">金鑰儲存架構</span><span class="sxs-lookup"><span data-stu-id="a2952-108">Key Storage Architecture</span></span>

<span data-ttu-id="a2952-109">CNG 提供私密金鑰儲存的模型，可讓您根據目前和未來建立使用加密功能（例如公用或私密金鑰加密）的應用程式，以及儲存金鑰資料的需求。</span><span class="sxs-lookup"><span data-stu-id="a2952-109">CNG provides a model for private key storage that allows adapting to the current and future demands of creating applications that use cryptography features such as public or private key encryption, as well as the demands of the storage of key material.</span></span> <span data-ttu-id="a2952-110">金鑰儲存路由器是此模型中的中央常式，並在 Ncrypt.dll 中執行。</span><span class="sxs-lookup"><span data-stu-id="a2952-110">The key storage router is the central routine in this model and is implemented in Ncrypt.dll.</span></span> <span data-ttu-id="a2952-111">應用程式會透過金鑰儲存路由器 (在系統上 Ksp) 來存取金鑰儲存提供者，這會從應用程式和存放裝置提供者本身隱藏詳細資料，例如金鑰隔離。</span><span class="sxs-lookup"><span data-stu-id="a2952-111">An application accesses the key storage providers (KSPs) on the system through the key storage router, which conceals details, such as key isolation, from both the application and the storage provider itself.</span></span> <span data-ttu-id="a2952-112">下圖顯示 CNG 金鑰隔離架構的設計和功能。</span><span class="sxs-lookup"><span data-stu-id="a2952-112">The following illustration shows the design and function of the CNG key isolation architecture.</span></span>

![cng 金鑰儲存提供者](images/cng-key-storage-provider.png)

<span data-ttu-id="a2952-114">為了符合 (CC) 需求的通用準則，必須隔離長時間的金鑰，使其永遠不會出現在應用程式進程中。</span><span class="sxs-lookup"><span data-stu-id="a2952-114">To comply with common criteria (CC) requirements, the long-lived keys must be isolated so that they are never present in the application process.</span></span> <span data-ttu-id="a2952-115">CNG 目前支援使用 Windows Server 2008 和 Windows Vista 隨附的 Microsoft 軟體 KSP 儲存非對稱式私密金鑰，並預設會安裝這些金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-115">CNG currently supports the storage of asymmetric private keys by using the Microsoft software KSP that is included with Windows Server 2008 and Windows Vista and installed by default.</span></span>

<span data-ttu-id="a2952-116">Windows Server 2008 和 Windows Vista 中預設會啟用金鑰隔離。</span><span class="sxs-lookup"><span data-stu-id="a2952-116">Key isolation is enabled by default in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="a2952-117">在這些平臺之前，您無法在平臺上使用金鑰隔離功能。</span><span class="sxs-lookup"><span data-stu-id="a2952-117">The key isolation feature is not available on platforms prior to these.</span></span> <span data-ttu-id="a2952-118">此外，協力廠商 Ksp 不會載入 (LSA 進程) 的金鑰隔離服務中。</span><span class="sxs-lookup"><span data-stu-id="a2952-118">Also, third party KSPs are not loaded in the key isolation service (LSA process).</span></span> <span data-ttu-id="a2952-119">只有 Microsoft KSP 會在金鑰隔離服務中載入。</span><span class="sxs-lookup"><span data-stu-id="a2952-119">Only the Microsoft KSP is loaded in the key isolation service.</span></span>

<span data-ttu-id="a2952-120">LSA 處理常式是用來將效能最大化的金鑰隔離程式。</span><span class="sxs-lookup"><span data-stu-id="a2952-120">The LSA process is used as the key isolation process to maximize performance.</span></span> <span data-ttu-id="a2952-121">私密金鑰的所有存取都是透過金鑰儲存路由器，它會公開一組完整的功能來管理和使用私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-121">All access to private keys goes through the key storage router, which exposes a comprehensive set of functions for managing and using private keys.</span></span>

<span data-ttu-id="a2952-122">CNG 會將預存金鑰的公開部分與私用部分分開儲存。</span><span class="sxs-lookup"><span data-stu-id="a2952-122">CNG stores the public portion of the stored key separately from the private portion.</span></span> <span data-ttu-id="a2952-123">金鑰組的公開部分也會在金鑰隔離服務中維護，並且使用本機遠端程序呼叫 (LRPC) 來存取。</span><span class="sxs-lookup"><span data-stu-id="a2952-123">The public portion of a key pair is also maintained in the key isolation service and is accessed by using local remote procedure call (LRPC).</span></span> <span data-ttu-id="a2952-124">在呼叫金鑰隔離程式時，金鑰儲存路由器會使用 LRPC。</span><span class="sxs-lookup"><span data-stu-id="a2952-124">The key storage router uses LRPC when calling into the key isolation process.</span></span> <span data-ttu-id="a2952-125">私密金鑰的所有存取都是透過私密金鑰路由器，並且由 CNG 進行審核。</span><span class="sxs-lookup"><span data-stu-id="a2952-125">All access to private keys goes through the private key router and is audited by CNG.</span></span>

<span data-ttu-id="a2952-126">如上所述，您可以支援各種不同的硬體儲存體裝置。</span><span class="sxs-lookup"><span data-stu-id="a2952-126">As described above, a wide range of hardware storage devices can be supported.</span></span> <span data-ttu-id="a2952-127">在每個案例中，所有這些儲存裝置的介面都相同。</span><span class="sxs-lookup"><span data-stu-id="a2952-127">In each case, the interface to all of these storage devices is identical.</span></span> <span data-ttu-id="a2952-128">它包含執行各種私密金鑰作業的函式，以及與金鑰儲存和管理相關的功能。</span><span class="sxs-lookup"><span data-stu-id="a2952-128">It includes functions to perform various private key operations as well as functions that pertain to key storage and management.</span></span>

<span data-ttu-id="a2952-129">CNG 提供一組 Api，可用來建立、儲存和取出密碼編譯金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-129">CNG provides a set of APIs that are used to create, store, and retrieve cryptographic keys.</span></span> <span data-ttu-id="a2952-130">如需這些 Api 的清單，請參閱 [CNG 金鑰儲存功能](cng-key-storage-functions.md)。</span><span class="sxs-lookup"><span data-stu-id="a2952-130">For a list of these APIs, see [CNG Key Storage Functions](cng-key-storage-functions.md).</span></span>

## <a name="key-types"></a><span data-ttu-id="a2952-131">索引鍵類型</span><span class="sxs-lookup"><span data-stu-id="a2952-131">Key Types</span></span>

<span data-ttu-id="a2952-132">CNG 支援下列金鑰類型：</span><span class="sxs-lookup"><span data-stu-id="a2952-132">CNG supports the following key types:</span></span>

-   <span data-ttu-id="a2952-133">Diffie-Hellman 公開和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-133">Diffie-Hellman public and private keys.</span></span>
-   <span data-ttu-id="a2952-134">數位簽章演算法 (DSA、FIPS 186-2) 公開和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-134">Digital Signature Algorithm (DSA, FIPS 186-2) public and private keys.</span></span>
-   <span data-ttu-id="a2952-135">RSA (PKCS \# 1) 公開和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-135">RSA (PKCS \#1) public and private keys.</span></span>
-   <span data-ttu-id="a2952-136">有幾個舊版 (CryptoAPI) 公開和私用金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-136">Several legacy (CryptoAPI) public and private keys.</span></span>
-   <span data-ttu-id="a2952-137">橢圓曲線密碼編譯公用和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-137">Elliptic Curve Cryptography public and private keys.</span></span>

## <a name="supported-algorithms"></a><span data-ttu-id="a2952-138">支援的演算法</span><span class="sxs-lookup"><span data-stu-id="a2952-138">Supported Algorithms</span></span>

<span data-ttu-id="a2952-139">CNG 支援下列金鑰演算法。</span><span class="sxs-lookup"><span data-stu-id="a2952-139">CNG supports the following key algorithms.</span></span>

| <span data-ttu-id="a2952-140">演算法</span><span class="sxs-lookup"><span data-stu-id="a2952-140">Algorithm</span></span> | <span data-ttu-id="a2952-141">金鑰/雜湊長度 (位) </span><span class="sxs-lookup"><span data-stu-id="a2952-141">Key/hash length (bits)</span></span>             |
|-----------|------------------------------------|
| <span data-ttu-id="a2952-142">RSA</span><span class="sxs-lookup"><span data-stu-id="a2952-142">RSA</span></span>       | <span data-ttu-id="a2952-143">512至16384，以64位遞增</span><span class="sxs-lookup"><span data-stu-id="a2952-143">512 to 16384, in 64 bit increments</span></span> |
| <span data-ttu-id="a2952-144">DH</span><span class="sxs-lookup"><span data-stu-id="a2952-144">DH</span></span>        | <span data-ttu-id="a2952-145">512至16384，以64位遞增</span><span class="sxs-lookup"><span data-stu-id="a2952-145">512 to 16384, in 64 bit increments</span></span> |
| <span data-ttu-id="a2952-146">DSA</span><span class="sxs-lookup"><span data-stu-id="a2952-146">DSA</span></span>       | <span data-ttu-id="a2952-147">512至1024，以64位遞增</span><span class="sxs-lookup"><span data-stu-id="a2952-147">512 to 1024, in 64 bit increments</span></span>  |
| <span data-ttu-id="a2952-148">ECDSA</span><span class="sxs-lookup"><span data-stu-id="a2952-148">ECDSA</span></span>     | <span data-ttu-id="a2952-149">P-256、P-384、P-521 (NIST 曲線) </span><span class="sxs-lookup"><span data-stu-id="a2952-149">P-256, P-384, P-521 (NIST Curves)</span></span>  |
| <span data-ttu-id="a2952-150">ECDH</span><span class="sxs-lookup"><span data-stu-id="a2952-150">ECDH</span></span>      | <span data-ttu-id="a2952-151">P-256、P-384、P-521 (NIST 曲線) </span><span class="sxs-lookup"><span data-stu-id="a2952-151">P-256, P-384, P-521 (NIST Curves)</span></span>  |
| <span data-ttu-id="a2952-152">MD2</span><span class="sxs-lookup"><span data-stu-id="a2952-152">MD2</span></span>       | <span data-ttu-id="a2952-153">128</span><span class="sxs-lookup"><span data-stu-id="a2952-153">128</span></span>                                |
| <span data-ttu-id="a2952-154">MD4</span><span class="sxs-lookup"><span data-stu-id="a2952-154">MD4</span></span>       | <span data-ttu-id="a2952-155">128</span><span class="sxs-lookup"><span data-stu-id="a2952-155">128</span></span>                                |
| <span data-ttu-id="a2952-156">MD5</span><span class="sxs-lookup"><span data-stu-id="a2952-156">MD5</span></span>       | <span data-ttu-id="a2952-157">128</span><span class="sxs-lookup"><span data-stu-id="a2952-157">128</span></span>                                |
| <span data-ttu-id="a2952-158">SHA-1</span><span class="sxs-lookup"><span data-stu-id="a2952-158">SHA-1</span></span>     | <span data-ttu-id="a2952-159">160</span><span class="sxs-lookup"><span data-stu-id="a2952-159">160</span></span>                                |
| <span data-ttu-id="a2952-160">SHA-256</span><span class="sxs-lookup"><span data-stu-id="a2952-160">SHA-256</span></span>   | <span data-ttu-id="a2952-161">256</span><span class="sxs-lookup"><span data-stu-id="a2952-161">256</span></span>                                |
| <span data-ttu-id="a2952-162">SHA-384</span><span class="sxs-lookup"><span data-stu-id="a2952-162">SHA-384</span></span>   | <span data-ttu-id="a2952-163">384</span><span class="sxs-lookup"><span data-stu-id="a2952-163">384</span></span>                                |
| <span data-ttu-id="a2952-164">SHA-512</span><span class="sxs-lookup"><span data-stu-id="a2952-164">SHA-512</span></span>   | <span data-ttu-id="a2952-165">512</span><span class="sxs-lookup"><span data-stu-id="a2952-165">512</span></span>                                |



 

## <a name="key-directories-and-files"></a><span data-ttu-id="a2952-166">金鑰目錄和檔案</span><span class="sxs-lookup"><span data-stu-id="a2952-166">Key Directories and Files</span></span>

<span data-ttu-id="a2952-167">Microsoft 舊版 CryptoAPI Csp 將私密金鑰儲存在下列目錄中。</span><span class="sxs-lookup"><span data-stu-id="a2952-167">The Microsoft legacy CryptoAPI CSPs store private keys in the following directories.</span></span>

| <span data-ttu-id="a2952-168">金鑰類型</span><span class="sxs-lookup"><span data-stu-id="a2952-168">Key type</span></span>                | <span data-ttu-id="a2952-169">目錄</span><span class="sxs-lookup"><span data-stu-id="a2952-169">Directories</span></span>                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2952-170">使用者私用</span><span class="sxs-lookup"><span data-stu-id="a2952-170">User private</span></span>            | <span data-ttu-id="a2952-171">% APPDATA% \\ Microsoft \\ 加密 \\ RSA \\ *使用者 SID*</span><span class="sxs-lookup"><span data-stu-id="a2952-171">%APPDATA%\\Microsoft\\Crypto\\RSA\\*User SID*</span></span>\\<br/><span data-ttu-id="a2952-172">% APPDATA% \\ Microsoft \\ 加密 \\ DSS \\ *使用者 SID*</span><span class="sxs-lookup"><span data-stu-id="a2952-172">%APPDATA%\\Microsoft\\Crypto\\DSS\\*User SID*</span></span>\\<br/>                                                   |
| <span data-ttu-id="a2952-173">本機系統私用</span><span class="sxs-lookup"><span data-stu-id="a2952-173">Local system private</span></span>    | <span data-ttu-id="a2952-174">% ALLUSERSPROFILE% \\ 應用程式資料 \\ Microsoft \\ 加密 \\ RSA \\ S-1-5-18</span><span class="sxs-lookup"><span data-stu-id="a2952-174">%ALLUSERSPROFILE%\\Application Data\\Microsoft\\Crypto\\RSA\\S-1-5-18</span></span>\\<br/><span data-ttu-id="a2952-175">% ALLUSERSPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ 加密 \\ DSS \\ S-1-5-18</span><span class="sxs-lookup"><span data-stu-id="a2952-175">%ALLUSERSPROFILE%\\Application Data\\Microsoft\\Crypto\\DSS\\S-1-5-18</span></span>\\<br/>   |
| <span data-ttu-id="a2952-176">本機服務私用</span><span class="sxs-lookup"><span data-stu-id="a2952-176">Local service private</span></span>   | <span data-ttu-id="a2952-177">% ALLUSERSPROFILE% \\ 應用程式資料 \\ Microsoft \\ 加密 \\ RSA \\ S-1-5-19</span><span class="sxs-lookup"><span data-stu-id="a2952-177">%ALLUSERSPROFILE%\\Application Data\\Microsoft\\Crypto\\RSA\\S-1-5-19</span></span>\\<br/><span data-ttu-id="a2952-178">% ALLUSERSPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ 加密 \\ DSS \\ S-1-5-19</span><span class="sxs-lookup"><span data-stu-id="a2952-178">%ALLUSERSPROFILE%\\Application Data\\Microsoft\\Crypto\\DSS\\S-1-5-19</span></span>\\<br/>   |
| <span data-ttu-id="a2952-179">網路服務私用</span><span class="sxs-lookup"><span data-stu-id="a2952-179">Network service private</span></span> | <span data-ttu-id="a2952-180">% ALLUSERSPROFILE% \\ 應用程式資料 \\ Microsoft \\ 加密 \\ RSA \\ S-1-5-20</span><span class="sxs-lookup"><span data-stu-id="a2952-180">%ALLUSERSPROFILE%\\Application Data\\Microsoft\\Crypto\\RSA\\S-1-5-20</span></span>\\<br/><span data-ttu-id="a2952-181">% ALLUSERSPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ 加密 \\ DSS \\ S-1-5-20</span><span class="sxs-lookup"><span data-stu-id="a2952-181">%ALLUSERSPROFILE%\\Application Data\\Microsoft\\Crypto\\DSS\\S-1-5-20</span></span>\\<br/>   |
| <span data-ttu-id="a2952-182">共用私用</span><span class="sxs-lookup"><span data-stu-id="a2952-182">Shared private</span></span>          | <span data-ttu-id="a2952-183">% ALLUSERSPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ 加密 \\ RSA \\ MachineKeys</span><span class="sxs-lookup"><span data-stu-id="a2952-183">%ALLUSERSPROFILE%\\Application Data\\Microsoft\\Crypto\\RSA\\MachineKeys</span></span><br/><span data-ttu-id="a2952-184">% ALLUSERSPROFILE% \\ \\ Microsoft \\ 加密 \\ DSS \\ MachineKeys 的應用程式資料</span><span class="sxs-lookup"><span data-stu-id="a2952-184">%ALLUSERSPROFILE%\\Application Data\\Microsoft\\Crypto\\DSS\\MachineKeys</span></span><br/> |



 

<span data-ttu-id="a2952-185">CNG 將私密金鑰儲存在下列目錄中。</span><span class="sxs-lookup"><span data-stu-id="a2952-185">CNG stores private keys in the following directories.</span></span>

| <span data-ttu-id="a2952-186">金鑰類型</span><span class="sxs-lookup"><span data-stu-id="a2952-186">Key type</span></span>                | <span data-ttu-id="a2952-187">目錄</span><span class="sxs-lookup"><span data-stu-id="a2952-187">Directory</span></span>                                                          |
|-------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="a2952-188">使用者私用</span><span class="sxs-lookup"><span data-stu-id="a2952-188">User private</span></span>            | <span data-ttu-id="a2952-189">% APPDATA% \\ Microsoft \\ 加密 \\ 金鑰</span><span class="sxs-lookup"><span data-stu-id="a2952-189">%APPDATA%\\Microsoft\\Crypto\\Keys</span></span>                                 |
| <span data-ttu-id="a2952-190">本機系統私用</span><span class="sxs-lookup"><span data-stu-id="a2952-190">Local system private</span></span>    | <span data-ttu-id="a2952-191">% ALLUSERSPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ 加密 \\ SystemKeys</span><span class="sxs-lookup"><span data-stu-id="a2952-191">%ALLUSERSPROFILE%\\Application Data\\Microsoft\\Crypto\\SystemKeys</span></span> |
| <span data-ttu-id="a2952-192">本機服務私用</span><span class="sxs-lookup"><span data-stu-id="a2952-192">Local service private</span></span>   | <span data-ttu-id="a2952-193">% WINDIR% \\ ServiceProfiles \\ LocalService</span><span class="sxs-lookup"><span data-stu-id="a2952-193">%WINDIR%\\ServiceProfiles\\LocalService</span></span>                            |
| <span data-ttu-id="a2952-194">網路服務私用</span><span class="sxs-lookup"><span data-stu-id="a2952-194">Network service private</span></span> | <span data-ttu-id="a2952-195">% WINDIR% \\ ServiceProfiles \\ NetworkService</span><span class="sxs-lookup"><span data-stu-id="a2952-195">%WINDIR%\\ServiceProfiles\\NetworkService</span></span>                          |
| <span data-ttu-id="a2952-196">共用私用</span><span class="sxs-lookup"><span data-stu-id="a2952-196">Shared private</span></span>          | <span data-ttu-id="a2952-197">% ALLUSERSPROFILE% 的 \\ 應用程式資料 \\ Microsoft \\ 加密 \\ 金鑰</span><span class="sxs-lookup"><span data-stu-id="a2952-197">%ALLUSERSPROFILE%\\Application Data\\Microsoft\\Crypto\\Keys</span></span>       |



 

<span data-ttu-id="a2952-198">以下是 CryptoAPI 和 CNG 金鑰容器之間的一些差異。</span><span class="sxs-lookup"><span data-stu-id="a2952-198">The following are some of the differences between the CryptoAPI and CNG key containers.</span></span>

-   <span data-ttu-id="a2952-199">CNG 使用的金鑰檔名稱，與 Rsaenh.dll 和 Dssenh.dll 舊版 Csp 所建立的金鑰檔不同。</span><span class="sxs-lookup"><span data-stu-id="a2952-199">CNG uses different file names for key files than key files that are created by the Rsaenh.dll and Dssenh.dll legacy CSPs.</span></span> <span data-ttu-id="a2952-200">舊版金鑰檔的副檔名也是副檔名，但是 CNG 金鑰檔沒有副檔名。</span><span class="sxs-lookup"><span data-stu-id="a2952-200">The legacy key files also have the .key extension, but CNG key files do not have the .key extension.</span></span>
-   <span data-ttu-id="a2952-201">CNG 完全支援 Unicode 金鑰容器名稱;CNG 使用 Unicode 容器名稱的雜湊，而 CryptoAPI 則使用 ANSI 容器名稱的雜湊。</span><span class="sxs-lookup"><span data-stu-id="a2952-201">CNG fully supports Unicode key container names; CNG uses a hash of the Unicode container name, whereas CryptoAPI uses a hash of the ANSI container name.</span></span>
-   <span data-ttu-id="a2952-202">CNG 對於 RSA 金鑰組有更大的彈性。</span><span class="sxs-lookup"><span data-stu-id="a2952-202">CNG is more flexible with regard to RSA key pairs.</span></span> <span data-ttu-id="a2952-203">例如，CNG 支援大於32位的公用指數長度，並支援 p 和 q 的長度不同的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a2952-203">For example, CNG supports public exponents larger than 32-bits in length, and it supports keys in which p and q are different lengths.</span></span>
-   <span data-ttu-id="a2952-204">在 CryptoAPI 中，金鑰容器檔案儲存在目錄中，其名稱是與使用者 SID 相等的文字。</span><span class="sxs-lookup"><span data-stu-id="a2952-204">In CryptoAPI, the key container file is stored in a directory whose name is the textual equivalent of the user's SID.</span></span> <span data-ttu-id="a2952-205">這不再是 CNG 中的情況，因此不會遺失所有私用金鑰，因而免除將使用者從某個網域移到另一個網域的困難。</span><span class="sxs-lookup"><span data-stu-id="a2952-205">This is no longer the case in CNG, which removes the difficulty of moving users from one domain to another without losing all of their private keys.</span></span>
-   <span data-ttu-id="a2952-206">CNG KSP 和金鑰名稱會限制為 **最大 \_ 路徑** Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="a2952-206">The CNG KSP and key names are limited to **MAX\_PATH** Unicode characters.</span></span> <span data-ttu-id="a2952-207">CryptoAPI CSP 和金鑰名稱會限制為 **最大 \_ 路徑** ANSI 字元。</span><span class="sxs-lookup"><span data-stu-id="a2952-207">The CryptoAPI CSP and key names are limited to **MAX\_PATH** ANSI characters.</span></span>
-   <span data-ttu-id="a2952-208">CNG 提供使用者定義索引鍵屬性的功能。</span><span class="sxs-lookup"><span data-stu-id="a2952-208">CNG offers the capability of user-defined key properties.</span></span> <span data-ttu-id="a2952-209">使用者可以建立自訂屬性並將其與金鑰建立關聯，並以保存的金鑰儲存它們。</span><span class="sxs-lookup"><span data-stu-id="a2952-209">Users can create and associate custom properties with keys, and have them stored with persisted keys.</span></span>

<span data-ttu-id="a2952-210">保存金鑰時，CNG 可以建立兩個檔案。</span><span class="sxs-lookup"><span data-stu-id="a2952-210">When persisting a key, CNG can create two files.</span></span> <span data-ttu-id="a2952-211">第一個檔案包含新的 CNG 格式的私密金鑰，而且一律會建立此金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-211">The first file contains the private key in the new CNG format and is always created.</span></span> <span data-ttu-id="a2952-212">舊版 CryptoAPI Csp 無法使用這個檔案。</span><span class="sxs-lookup"><span data-stu-id="a2952-212">This file is not usable by the legacy CryptoAPI CSPs.</span></span> <span data-ttu-id="a2952-213">第二個檔案包含舊版 CryptoAPI 金鑰容器中的相同私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-213">The second file contains the same private key in the legacy CryptoAPI key container.</span></span> <span data-ttu-id="a2952-214">第二個檔案符合 Rsaenh.dll 所使用的格式和位置。</span><span class="sxs-lookup"><span data-stu-id="a2952-214">The second file conforms to the format and location used by Rsaenh.dll.</span></span> <span data-ttu-id="a2952-215">當呼叫 [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey)函式來完成 RSA 金鑰時，如果指定了 **NCRYPT \_ 寫入 \_ 金鑰 \_ 至 \_ 舊版 \_ 存放區 \_ 旗** 標旗標，就會建立第二個檔案。</span><span class="sxs-lookup"><span data-stu-id="a2952-215">Creation of the second file only occurs if the **NCRYPT\_WRITE\_KEY\_TO\_LEGACY\_STORE\_FLAG** flag is specified when the [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) function is called to finalize an RSA key.</span></span> <span data-ttu-id="a2952-216">這項功能不支援 DSA 和 DH 金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-216">This feature is not supported for DSA and DH keys.</span></span>

<span data-ttu-id="a2952-217">當應用程式嘗試開啟現有的保存金鑰時，CNG 會先嘗試開啟原生的 CNG 檔。</span><span class="sxs-lookup"><span data-stu-id="a2952-217">When an application attempts to open an existing persisted key, CNG first attempts to open the native CNG file.</span></span> <span data-ttu-id="a2952-218">如果此檔案不存在，則 CNG 會嘗試在舊版 CryptoAPI 金鑰容器中找出相符的金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-218">If this file does not exist, then CNG attempts to locate a matching key in the legacy CryptoAPI key container.</span></span>

<span data-ttu-id="a2952-219">當您從來源電腦移動或複製 CryptoAPI 金鑰至具有 Windows 消費者狀態移轉工具 (USMT) 的目的電腦時，CNG 將無法存取目的電腦上的金鑰。</span><span class="sxs-lookup"><span data-stu-id="a2952-219">When you move or copy CryptoAPI keys from a source machine to a target machine with Windows User State Migration Tool (USMT), CNG will fail to access the keys on the target machine.</span></span> <span data-ttu-id="a2952-220">若要存取這類已遷移的金鑰，您必須使用 CryptoAPI。</span><span class="sxs-lookup"><span data-stu-id="a2952-220">To access such migrated keys, you must use the CryptoAPI.</span></span>

 

 




