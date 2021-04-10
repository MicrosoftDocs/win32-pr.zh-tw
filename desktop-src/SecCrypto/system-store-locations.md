---
description: 系統存放區是由一或多個實體同級存放區所組成的集合。
ms.assetid: 41fe9366-4c17-43bb-91d6-934c7aa87a2d
title: 系統存放區位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0863ffde8be5db67459908b1ec26ec73da029744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944363"
---
# <a name="system-store-locations"></a><span data-ttu-id="946ac-103">系統存放區位置</span><span class="sxs-lookup"><span data-stu-id="946ac-103">System Store Locations</span></span>

<span data-ttu-id="946ac-104">系統存放區是由一或多個實體同級存放區所組成的集合。</span><span class="sxs-lookup"><span data-stu-id="946ac-104">A system store is a collection that consists of one or more physical sibling stores.</span></span> <span data-ttu-id="946ac-105">每個系統存放區都有預先定義的實體同級存放區。</span><span class="sxs-lookup"><span data-stu-id="946ac-105">For each system store, there are predefined physical sibling stores.</span></span> <span data-ttu-id="946ac-106">開啟系統存放區（例如 MY at CERT \_ system \_ store 目前 \_ 的 \_ 使用者）之後，存放區提供者會呼叫 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) 來開啟系統存放區集合中的每個實體存放區。</span><span class="sxs-lookup"><span data-stu-id="946ac-106">After opening a system store such as MY at CERT\_SYSTEM\_STORE\_CURRENT\_USER, the store provider calls [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) to open each of the physical stores in the system store collection.</span></span> <span data-ttu-id="946ac-107">在開啟的進程中，每個實體存放區都會使用 [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection)新增至系統存放區集合。</span><span class="sxs-lookup"><span data-stu-id="946ac-107">In the open process, each of these physical stores is added to the system store collection using [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection).</span></span> <span data-ttu-id="946ac-108">這些實體存放區中的所有憑證都可透過邏輯系統存放區集合使用。</span><span class="sxs-lookup"><span data-stu-id="946ac-108">All certificates in those physical stores are available through the logical system store collection.</span></span>

<span data-ttu-id="946ac-109">針對每個系統存放區位置，預先定義的系統存放區為：</span><span class="sxs-lookup"><span data-stu-id="946ac-109">For each system store location, the predefined systems stores are:</span></span>

-   <span data-ttu-id="946ac-110">MY</span><span class="sxs-lookup"><span data-stu-id="946ac-110">MY</span></span>
-   <span data-ttu-id="946ac-111">Root</span><span class="sxs-lookup"><span data-stu-id="946ac-111">Root</span></span>
-   <span data-ttu-id="946ac-112">信任</span><span class="sxs-lookup"><span data-stu-id="946ac-112">Trust</span></span>
-   <span data-ttu-id="946ac-113">CA</span><span class="sxs-lookup"><span data-stu-id="946ac-113">CA</span></span>

<span data-ttu-id="946ac-114">在 CERT \_ SYSTEM \_ STORE \_ 目前的 \_ 使用者中，也有預先定義的 UserDS 存放區。</span><span class="sxs-lookup"><span data-stu-id="946ac-114">In CERT\_SYSTEM\_STORE\_CURRENT\_USER, there is also a predefined UserDS store.</span></span> <span data-ttu-id="946ac-115">已為此位置規劃智慧卡存放區。</span><span class="sxs-lookup"><span data-stu-id="946ac-115">A smart card store is planned for this location.</span></span>

<span data-ttu-id="946ac-116">以下是系統存放區，後面接著進一步的備註：</span><span class="sxs-lookup"><span data-stu-id="946ac-116">Here are the system stores followed by further remarks:</span></span>

-   [<span data-ttu-id="946ac-117">CERT \_ 系統 \_ 存放區 \_ 目前的 \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="946ac-117">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>](#cert_system_store_current_user)
-   [<span data-ttu-id="946ac-118">CERT \_ 系統 \_ 存放區 \_ 本機 \_ 電腦</span><span class="sxs-lookup"><span data-stu-id="946ac-118">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>](#cert_system_store_local_machine)
-   [<span data-ttu-id="946ac-119">CERT \_ 系統 \_ 存放區 \_ 目前的 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="946ac-119">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>](#cert_system_store_current_service)
-   [<span data-ttu-id="946ac-120">CERT \_ 系統 \_ 存放區 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="946ac-120">CERT\_SYSTEM\_STORE\_SERVICES</span></span>](#cert_system_store_services)
-   [<span data-ttu-id="946ac-121">CERT \_ 系統 \_ 存放區 \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="946ac-121">CERT\_SYSTEM\_STORE\_USERS</span></span>](#cert_system_store_users)
-   [<span data-ttu-id="946ac-122">CERT \_ 系統 \_ 目前的 \_ 使用者 \_ 組 \_ 策略</span><span class="sxs-lookup"><span data-stu-id="946ac-122">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>](#cert_system_current_user_group_policy)
-   [<span data-ttu-id="946ac-123">CERT \_ 系統 \_ 本機 \_ 電腦 \_ 組 \_ 策略</span><span class="sxs-lookup"><span data-stu-id="946ac-123">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>](#cert_system_local_machine_group_policy)
-   [<span data-ttu-id="946ac-124">CERT \_ SYSTEM \_ STORE \_ 本機 \_ 電腦 \_ ENTERPRISE</span><span class="sxs-lookup"><span data-stu-id="946ac-124">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>](#cert_system_store_local_machine_enterprise)
-   [<span data-ttu-id="946ac-125">備註</span><span class="sxs-lookup"><span data-stu-id="946ac-125">Remarks</span></span>](#remarks)

### <a name="cert_system_store_current_user"></a><span data-ttu-id="946ac-126">CERT \_ 系統 \_ 存放區 \_ 目前的 \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="946ac-126">CERT\_SYSTEM\_STORE\_CURRENT\_USER</span></span>

<span data-ttu-id="946ac-127">CERT \_ SYSTEM \_ STORE \_ 目前 \_ 的使用者系統存放區位於下列登錄位置：</span><span class="sxs-lookup"><span data-stu-id="946ac-127">CERT\_SYSTEM\_STORE\_CURRENT\_USER system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="946ac-128">與這些系統存放區相關聯的預先定義實體存放區如下所示。</span><span class="sxs-lookup"><span data-stu-id="946ac-128">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="946ac-129">系統存放區</span><span class="sxs-lookup"><span data-stu-id="946ac-129">System store</span></span> | <span data-ttu-id="946ac-130">實體存放區</span><span class="sxs-lookup"><span data-stu-id="946ac-130">Physical store</span></span>                                           |
|--------------|----------------------------------------------------------|
| <span data-ttu-id="946ac-131">MY</span><span class="sxs-lookup"><span data-stu-id="946ac-131">MY</span></span>           | <span data-ttu-id="946ac-132">.預設</span><span class="sxs-lookup"><span data-stu-id="946ac-132">.Default</span></span>                                                 |
| <span data-ttu-id="946ac-133">Root</span><span class="sxs-lookup"><span data-stu-id="946ac-133">Root</span></span>         | <span data-ttu-id="946ac-134">.預設的 LocalMachine</span><span class="sxs-lookup"><span data-stu-id="946ac-134">.Default.LocalMachine</span></span><br/> <span data-ttu-id="946ac-135">.智慧卡</span><span class="sxs-lookup"><span data-stu-id="946ac-135">.SmartCard</span></span><br/>   |
| <span data-ttu-id="946ac-136">信任</span><span class="sxs-lookup"><span data-stu-id="946ac-136">Trust</span></span>        | <span data-ttu-id="946ac-137">.預設值。 GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="946ac-137">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="946ac-138">.My</span><span class="sxs-lookup"><span data-stu-id="946ac-138">.LocalMachine</span></span><br/> |
| <span data-ttu-id="946ac-139">CA</span><span class="sxs-lookup"><span data-stu-id="946ac-139">CA</span></span>           | <span data-ttu-id="946ac-140">.預設值。 GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="946ac-140">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="946ac-141">.My</span><span class="sxs-lookup"><span data-stu-id="946ac-141">.LocalMachine</span></span><br/> |
| <span data-ttu-id="946ac-142">UserDS</span><span class="sxs-lookup"><span data-stu-id="946ac-142">UserDS</span></span>       | <span data-ttu-id="946ac-143">.UserCertificate</span><span class="sxs-lookup"><span data-stu-id="946ac-143">.UserCertificate</span></span>                                         |



 

### <a name="cert_system_store_local_machine"></a><span data-ttu-id="946ac-144">CERT \_ 系統 \_ 存放區 \_ 本機 \_ 電腦</span><span class="sxs-lookup"><span data-stu-id="946ac-144">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>

<span data-ttu-id="946ac-145">CERT \_ system \_ STORE \_ 本機 \_ 電腦系統存放區位於下列登錄位置：</span><span class="sxs-lookup"><span data-stu-id="946ac-145">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         SystemCertificates
```

<span data-ttu-id="946ac-146">預先定義的實體存放區會與這些系統存放區產生關聯，如下所示。</span><span class="sxs-lookup"><span data-stu-id="946ac-146">The predefined physical stores are associated with those system stores are as follows.</span></span>



| <span data-ttu-id="946ac-147">系統存放區</span><span class="sxs-lookup"><span data-stu-id="946ac-147">System store</span></span> | <span data-ttu-id="946ac-148">實體存放區</span><span class="sxs-lookup"><span data-stu-id="946ac-148">Physical store</span></span>                                                                                    |
|--------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="946ac-149">MY</span><span class="sxs-lookup"><span data-stu-id="946ac-149">MY</span></span>           | <span data-ttu-id="946ac-150">.預設</span><span class="sxs-lookup"><span data-stu-id="946ac-150">.Default</span></span>                                                                                          |
| <span data-ttu-id="946ac-151">Root</span><span class="sxs-lookup"><span data-stu-id="946ac-151">Root</span></span>         | <span data-ttu-id="946ac-152">.預設值。 AuthRoot</span><span class="sxs-lookup"><span data-stu-id="946ac-152">.Default.AuthRoot</span></span><br/> <span data-ttu-id="946ac-153">.GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="946ac-153">.GroupPolicy</span></span><br/> <span data-ttu-id="946ac-154">.企業</span><span class="sxs-lookup"><span data-stu-id="946ac-154">.Enterprise</span></span><br/> <span data-ttu-id="946ac-155">.智慧卡</span><span class="sxs-lookup"><span data-stu-id="946ac-155">.SmartCard</span></span><br/> |
| <span data-ttu-id="946ac-156">信任</span><span class="sxs-lookup"><span data-stu-id="946ac-156">Trust</span></span>        | <span data-ttu-id="946ac-157">.預設值。 GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="946ac-157">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="946ac-158">.企業</span><span class="sxs-lookup"><span data-stu-id="946ac-158">.Enterprise</span></span><br/>                                            |
| <span data-ttu-id="946ac-159">CA</span><span class="sxs-lookup"><span data-stu-id="946ac-159">CA</span></span>           | <span data-ttu-id="946ac-160">.預設值。 GroupPolicy</span><span class="sxs-lookup"><span data-stu-id="946ac-160">.Default.GroupPolicy</span></span><br/> <span data-ttu-id="946ac-161">.企業</span><span class="sxs-lookup"><span data-stu-id="946ac-161">.Enterprise</span></span> <br/>                                           |



 

### <a name="cert_system_store_current_service"></a><span data-ttu-id="946ac-162">CERT \_ 系統 \_ 存放區 \_ 目前的 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="946ac-162">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE</span></span>

<span data-ttu-id="946ac-163">CERT \_ SYSTEM \_ STORE \_ 目前 \_ 的服務系統存放區位於下列登錄位置：</span><span class="sxs-lookup"><span data-stu-id="946ac-163">CERT\_SYSTEM\_STORE\_CURRENT\_SERVICE system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="946ac-164">與這些系統存放區相關聯的預先定義實體存放區如下所示。</span><span class="sxs-lookup"><span data-stu-id="946ac-164">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="946ac-165">系統存放區</span><span class="sxs-lookup"><span data-stu-id="946ac-165">System store</span></span> | <span data-ttu-id="946ac-166">實體存放區</span><span class="sxs-lookup"><span data-stu-id="946ac-166">Physical store</span></span>                   |
|--------------|----------------------------------|
| <span data-ttu-id="946ac-167">MY</span><span class="sxs-lookup"><span data-stu-id="946ac-167">MY</span></span>           | <span data-ttu-id="946ac-168">.預設</span><span class="sxs-lookup"><span data-stu-id="946ac-168">.Default</span></span>                         |
| <span data-ttu-id="946ac-169">Root</span><span class="sxs-lookup"><span data-stu-id="946ac-169">Root</span></span>         | <span data-ttu-id="946ac-170">.預設的 LocalMachine</span><span class="sxs-lookup"><span data-stu-id="946ac-170">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="946ac-171">信任</span><span class="sxs-lookup"><span data-stu-id="946ac-171">Trust</span></span>        | <span data-ttu-id="946ac-172">.預設的 LocalMachine</span><span class="sxs-lookup"><span data-stu-id="946ac-172">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="946ac-173">CA</span><span class="sxs-lookup"><span data-stu-id="946ac-173">CA</span></span>           | <span data-ttu-id="946ac-174">.預設的 LocalMachine</span><span class="sxs-lookup"><span data-stu-id="946ac-174">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_services"></a><span data-ttu-id="946ac-175">CERT \_ 系統 \_ 存放區 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="946ac-175">CERT\_SYSTEM\_STORE\_SERVICES</span></span>

<span data-ttu-id="946ac-176">CERT \_ system \_ STORE \_ 服務系統存放區位於下列登錄位置：</span><span class="sxs-lookup"><span data-stu-id="946ac-176">CERT\_SYSTEM\_STORE\_SERVICES system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Cryptography
            Services
               ServiceName
                  SystemCertificates
```

<span data-ttu-id="946ac-177">與這些系統存放區相關聯的預先定義實體存放區如下所示。</span><span class="sxs-lookup"><span data-stu-id="946ac-177">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="946ac-178">系統存放區</span><span class="sxs-lookup"><span data-stu-id="946ac-178">System store</span></span>       | <span data-ttu-id="946ac-179">實體存放區</span><span class="sxs-lookup"><span data-stu-id="946ac-179">Physical store</span></span>                   |
|--------------------|----------------------------------|
| <span data-ttu-id="946ac-180">ServiceName \\ MY</span><span class="sxs-lookup"><span data-stu-id="946ac-180">ServiceName\\MY</span></span>    | <span data-ttu-id="946ac-181">.預設</span><span class="sxs-lookup"><span data-stu-id="946ac-181">.Default</span></span>                         |
| <span data-ttu-id="946ac-182">ServiceName \\ 根目錄</span><span class="sxs-lookup"><span data-stu-id="946ac-182">ServiceName\\Root</span></span>  | <span data-ttu-id="946ac-183">.預設的 LocalMachine</span><span class="sxs-lookup"><span data-stu-id="946ac-183">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="946ac-184">ServiceName \\ 信任</span><span class="sxs-lookup"><span data-stu-id="946ac-184">ServiceName\\Trust</span></span> | <span data-ttu-id="946ac-185">.預設的 LocalMachine</span><span class="sxs-lookup"><span data-stu-id="946ac-185">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="946ac-186">ServiceName \\ CA</span><span class="sxs-lookup"><span data-stu-id="946ac-186">ServiceName\\CA</span></span>    | <span data-ttu-id="946ac-187">.預設的 LocalMachine</span><span class="sxs-lookup"><span data-stu-id="946ac-187">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_store_users"></a><span data-ttu-id="946ac-188">CERT \_ 系統 \_ 存放區 \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="946ac-188">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="946ac-189">CERT \_ system \_ STORE \_ 使用者的系統存放區位於下列登錄位置：</span><span class="sxs-lookup"><span data-stu-id="946ac-189">CERT\_SYSTEM\_STORE\_USERS system stores are at the following registry location:</span></span>

```
HKEY_USERS
   UserName
      Software
         Microsoft
            SystemCertificates
```

<span data-ttu-id="946ac-190">與這些系統存放區相關聯的預先定義實體存放區如下所示。</span><span class="sxs-lookup"><span data-stu-id="946ac-190">The predefined physical stores associated with those system stores are as follows.</span></span>



| <span data-ttu-id="946ac-191">系統存放區</span><span class="sxs-lookup"><span data-stu-id="946ac-191">System store</span></span>  | <span data-ttu-id="946ac-192">實體存放區</span><span class="sxs-lookup"><span data-stu-id="946ac-192">Physical store</span></span>                   |
|---------------|----------------------------------|
| <span data-ttu-id="946ac-193">userid \\ MY</span><span class="sxs-lookup"><span data-stu-id="946ac-193">userid\\MY</span></span>    | <span data-ttu-id="946ac-194">.預設的 LocalMachine</span><span class="sxs-lookup"><span data-stu-id="946ac-194">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="946ac-195">userid \\ 根</span><span class="sxs-lookup"><span data-stu-id="946ac-195">userid\\Root</span></span>  | <span data-ttu-id="946ac-196">.預設的 LocalMachine</span><span class="sxs-lookup"><span data-stu-id="946ac-196">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="946ac-197">userid \\ 信任</span><span class="sxs-lookup"><span data-stu-id="946ac-197">userid\\Trust</span></span> | <span data-ttu-id="946ac-198">.預設的 LocalMachine</span><span class="sxs-lookup"><span data-stu-id="946ac-198">.Default.LocalMachine</span></span><br/> |
| <span data-ttu-id="946ac-199">userid \\ CA</span><span class="sxs-lookup"><span data-stu-id="946ac-199">userid\\CA</span></span>    | <span data-ttu-id="946ac-200">.預設的 LocalMachine</span><span class="sxs-lookup"><span data-stu-id="946ac-200">.Default.LocalMachine</span></span><br/> |



 

### <a name="cert_system_current_user_group_policy"></a><span data-ttu-id="946ac-201">CERT \_ 系統 \_ 目前的 \_ 使用者 \_ 組 \_ 策略</span><span class="sxs-lookup"><span data-stu-id="946ac-201">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY</span></span>

<span data-ttu-id="946ac-202">CERT \_ 系統 \_ 目前 \_ \_ 的使用者組 \_ 策略系統存放區位於下列登錄位置：</span><span class="sxs-lookup"><span data-stu-id="946ac-202">CERT\_SYSTEM\_CURRENT\_USER\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_CURRENT_USER
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_local_machine_group_policy"></a><span data-ttu-id="946ac-203">CERT \_ 系統 \_ 本機 \_ 電腦 \_ 組 \_ 策略</span><span class="sxs-lookup"><span data-stu-id="946ac-203">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>

<span data-ttu-id="946ac-204">CERT \_ 系統 \_ 本機 \_ 電腦 \_ 組 \_ 策略系統存放區位於下列登錄位置：</span><span class="sxs-lookup"><span data-stu-id="946ac-204">CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY system stores are at the following registry location:</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Policy
         Microsoft
            SystemCertificates
```

### <a name="cert_system_store_local_machine_enterprise"></a><span data-ttu-id="946ac-205">CERT \_ SYSTEM \_ STORE \_ 本機 \_ 電腦 \_ ENTERPRISE</span><span class="sxs-lookup"><span data-stu-id="946ac-205">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE</span></span>

<span data-ttu-id="946ac-206">CERT \_ SYSTEM \_ STORE \_ 本機 \_ 電腦 \_ enterprise 包含企業內跨網域共用的憑證，並從全球企業目錄下載。</span><span class="sxs-lookup"><span data-stu-id="946ac-206">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_ENTERPRISE contains certificates shared across domains in the enterprise and downloaded from the global enterprise directory.</span></span> <span data-ttu-id="946ac-207">若要同步處理用戶端的企業存放區，企業目錄會每隔8小時輪詢一次，而且會在背景自動下載憑證。</span><span class="sxs-lookup"><span data-stu-id="946ac-207">To synchronize the client's enterprise store, the enterprise directory is polled every eight hours and certificates are downloaded automatically in the background.</span></span>

<span data-ttu-id="946ac-208">與這些系統存放區相關聯的預先定義實體存放區如下所示。</span><span class="sxs-lookup"><span data-stu-id="946ac-208">The predefined physical stores associated with these system stores are as follows.</span></span>



| <span data-ttu-id="946ac-209">系統存放區</span><span class="sxs-lookup"><span data-stu-id="946ac-209">System store</span></span> | <span data-ttu-id="946ac-210">實體存放區</span><span class="sxs-lookup"><span data-stu-id="946ac-210">Physical store</span></span> |
|--------------|----------------|
| <span data-ttu-id="946ac-211">MY</span><span class="sxs-lookup"><span data-stu-id="946ac-211">MY</span></span>           | <span data-ttu-id="946ac-212">.預設</span><span class="sxs-lookup"><span data-stu-id="946ac-212">.Default</span></span>       |
| <span data-ttu-id="946ac-213">Root</span><span class="sxs-lookup"><span data-stu-id="946ac-213">Root</span></span>         | <span data-ttu-id="946ac-214">.預設</span><span class="sxs-lookup"><span data-stu-id="946ac-214">.Default</span></span>       |
| <span data-ttu-id="946ac-215">信任</span><span class="sxs-lookup"><span data-stu-id="946ac-215">Trust</span></span>        | <span data-ttu-id="946ac-216">.預設</span><span class="sxs-lookup"><span data-stu-id="946ac-216">.Default</span></span>       |
| <span data-ttu-id="946ac-217">CA</span><span class="sxs-lookup"><span data-stu-id="946ac-217">CA</span></span>           | <span data-ttu-id="946ac-218">.預設</span><span class="sxs-lookup"><span data-stu-id="946ac-218">.Default</span></span>       |



 

### <a name="remarks"></a><span data-ttu-id="946ac-219">備註</span><span class="sxs-lookup"><span data-stu-id="946ac-219">Remarks</span></span>

<span data-ttu-id="946ac-220">您可以使用 [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore)，將其他實體存放區與系統存放區相關聯。</span><span class="sxs-lookup"><span data-stu-id="946ac-220">Additional physical stores can be associated with a system store by using [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore).</span></span>

<span data-ttu-id="946ac-221">Cert \_ 系統 \_ 存放區 \_ 服務和 cert \_ 系統 \_ 存放區使用者存放區的 \_ 開啟方式是在傳遞至 *pvPara* 的字串中，以服務或使用者名稱（例如 *ServiceName* \\ **信任** 或）來附加存放區的名稱 **。預設值** 是 \\ **MY**。</span><span class="sxs-lookup"><span data-stu-id="946ac-221">CERT\_SYSTEM\_STORE\_SERVICE and CERT\_SYSTEM\_STORE\_USERS stores are opened by prefixing the name of the store in the string passed to *pvPara* with the service or user name such as *ServiceName*\\**Trust** or **.Default**\\**MY**.</span></span> <span data-ttu-id="946ac-222">CERT \_ 系統 \_ 存放區 \_ 服務或憑證 \_ 系統 \_ 存放區 \_ 使用者位置可以 \_ \_ \_ \_ \_ \_ \_ 使用目前服務或使用者的文字 [*安全性識別*](../secgloss/s-gly.md) 元 (SID) ，開啟 cert system current SERVICE 或 cert system store 目前使用者中的相同存放區。</span><span class="sxs-lookup"><span data-stu-id="946ac-222">The CERT\_SYSTEM\_STORE\_SERVICES or CERT\_SYSTEM\_STORE\_USERS location can open the same store in CERT\_SYSTEM\_CURRENT\_SERVICE or CERT\_SYSTEM\_STORE\_CURRENT\_USER by using the textual [*security identifier*](../secgloss/s-gly.md) (SID) of the current service or user.</span></span>

<span data-ttu-id="946ac-223">在 \_ \_ \_ \_ \_ \_ 電腦啟動或使用者登入期間，系統會在網路設定中，從群組原則範本 (GPT) ，將存放區的使用者群組原則和憑證系統 \_ 本機 \_ 電腦 \_ 組 \_ 策略下載到用戶端電腦。</span><span class="sxs-lookup"><span data-stu-id="946ac-223">Stores in CERT\_SYSTEM\_STORE\_USER\_GROUP\_POLICY and CERT\_SYSTEM\_LOCAL\_MACHINE\_GROUP\_POLICY in a network setting are downloaded to the client computer from the Group Policy Template (GPT) during computer startup or user logon.</span></span> <span data-ttu-id="946ac-224">當系統管理員在網域伺服器上變更 GPT 時，可以在啟動或登入之後，在用戶端電腦上更新這些存放區。</span><span class="sxs-lookup"><span data-stu-id="946ac-224">These stores can be updated on the client computer after startup or logon when the GPT is changed on the domain server by an administrator.</span></span> <span data-ttu-id="946ac-225">[**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore)函式可讓應用程式在其中一個位置的存放區變更時收到通知。</span><span class="sxs-lookup"><span data-stu-id="946ac-225">The [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore) function allows an application to be notified when stores in either of these locations have changed.</span></span>

<span data-ttu-id="946ac-226">您可以從遠端開啟下列系統存放區位置：</span><span class="sxs-lookup"><span data-stu-id="946ac-226">The following system store locations can be opened remotely:</span></span>

-   <span data-ttu-id="946ac-227">CERT \_ 系統 \_ 存放區 \_ 本機 \_ 電腦</span><span class="sxs-lookup"><span data-stu-id="946ac-227">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE</span></span>
-   <span data-ttu-id="946ac-228">CERT \_ 系統 \_ 存放區 \_ 本機 \_ 電腦 \_ 組 \_ 策略</span><span class="sxs-lookup"><span data-stu-id="946ac-228">CERT\_SYSTEM\_STORE\_LOCAL\_MACHINE\_GROUP\_POLICY</span></span>
-   <span data-ttu-id="946ac-229">CERT \_ 系統 \_ 存放區 \_ 服務</span><span class="sxs-lookup"><span data-stu-id="946ac-229">CERT\_SYSTEM\_STORE\_SERVICES</span></span>
-   <span data-ttu-id="946ac-230">CERT \_ 系統 \_ 存放區 \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="946ac-230">CERT\_SYSTEM\_STORE\_USERS</span></span>

<span data-ttu-id="946ac-231">系統存放區位置會從遠端開啟，方法是在傳遞至 *pvPara* 的字串中，將存放區名稱前面加上電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="946ac-231">System store locations are opened remotely by prefixing the store name in the string passed to *pvPara* with the computer name.</span></span> <span data-ttu-id="946ac-232">遠端系統存放區名稱的範例如下：</span><span class="sxs-lookup"><span data-stu-id="946ac-232">Examples of remote system store names are:</span></span>

-   <span data-ttu-id="946ac-233">*ComputerName* \\**CA**</span><span class="sxs-lookup"><span data-stu-id="946ac-233">*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="946ac-234">\\\\*ComputerName* \\**CA**</span><span class="sxs-lookup"><span data-stu-id="946ac-234">\\\\*ComputerName*\\**CA**</span></span>
-   <span data-ttu-id="946ac-235">*ComputerName* \\*ServiceName* \\**信任**</span><span class="sxs-lookup"><span data-stu-id="946ac-235">*ComputerName*\\*ServiceName*\\**Trust**</span></span>
-   <span data-ttu-id="946ac-236">\\\\*ComputerName* \\*ServiceName* \\**信任**</span><span class="sxs-lookup"><span data-stu-id="946ac-236">\\\\*ComputerName*\\*ServiceName*\\**Trust**</span></span>

 

 
