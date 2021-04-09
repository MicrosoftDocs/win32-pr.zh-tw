---
description: 從 Windows 10 開始，CNG 提供下列命名橢圓曲線的支援 (ANSI X x9.62、X 9.63、FIPS 186-2) 。
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: CNG 命名橢圓曲線 (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35092d463e6f83917d231a87659e690ffeb59fe3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847718"
---
# <a name="cng-named-elliptic-curves"></a><span data-ttu-id="03267-103">CNG 命名橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="03267-103">CNG Named Elliptic Curves</span></span>

<span data-ttu-id="03267-104">從 Windows 10 開始，CNG 提供下列命名橢圓曲線的支援 (ANSI X x9.62、X 9.63、FIPS 186-2) 。</span><span class="sxs-lookup"><span data-stu-id="03267-104">Beginning in Windows 10, CNG provides support for the following named elliptic curves (ANSI X9.62, X9.63, FIPS 186-2).</span></span>

<dl> <span data-ttu-id="03267-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT \_ ECC \_ 曲線 \_ 25519**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT\_ECC\_CURVE\_25519**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-106">需求</span><span class="sxs-lookup"><span data-stu-id="03267-106">Requirement</span></span> | <span data-ttu-id="03267-107">值</span><span class="sxs-lookup"><span data-stu-id="03267-107">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="03267-108">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-108">Name</span></span>              | <span data-ttu-id="03267-109">curve25519</span><span class="sxs-lookup"><span data-stu-id="03267-109">curve25519</span></span>                                                  |
| <span data-ttu-id="03267-110">標準</span><span class="sxs-lookup"><span data-stu-id="03267-110">Standard</span></span>          | [<span data-ttu-id="03267-111">曲線25519</span><span class="sxs-lookup"><span data-stu-id="03267-111">Curve 25519</span></span>](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| <span data-ttu-id="03267-112">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-112">Key size (bits)</span></span>   | <span data-ttu-id="03267-113">255</span><span class="sxs-lookup"><span data-stu-id="03267-113">255</span></span>                                                         |
| <span data-ttu-id="03267-114">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-114">TLS capable</span></span>       |                                                             |
| <span data-ttu-id="03267-115">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-115">Object identifier</span></span> | <span data-ttu-id="03267-116">無</span><span class="sxs-lookup"><span data-stu-id="03267-116">None</span></span>                                                        |



 

<span data-ttu-id="03267-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-118">需求</span><span class="sxs-lookup"><span data-stu-id="03267-118">Requirement</span></span> | <span data-ttu-id="03267-119">值</span><span class="sxs-lookup"><span data-stu-id="03267-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-120">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-120">Name</span></span>              | <span data-ttu-id="03267-121">brainpoolP160r1</span><span class="sxs-lookup"><span data-stu-id="03267-121">brainpoolP160r1</span></span>                                                                                                   |
| <span data-ttu-id="03267-122">標準</span><span class="sxs-lookup"><span data-stu-id="03267-122">Standard</span></span>          | [<span data-ttu-id="03267-123">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-123">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-124">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-124">Key size (bits)</span></span>   | <span data-ttu-id="03267-125">160</span><span class="sxs-lookup"><span data-stu-id="03267-125">160</span></span>                                                                                                               |
| <span data-ttu-id="03267-126">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-126">TLS capable</span></span>       | <span data-ttu-id="03267-127">No</span><span class="sxs-lookup"><span data-stu-id="03267-127">No</span></span>                                                                                                                |
| <span data-ttu-id="03267-128">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-128">Object identifier</span></span> | <span data-ttu-id="03267-129">1.3.36.3.3.2.8.1.1.1</span><span class="sxs-lookup"><span data-stu-id="03267-129">1.3.36.3.3.2.8.1.1.1</span></span>                                                                                              |



 

<span data-ttu-id="03267-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ BRAINPOOLP160T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-131">需求</span><span class="sxs-lookup"><span data-stu-id="03267-131">Requirement</span></span> | <span data-ttu-id="03267-132">值</span><span class="sxs-lookup"><span data-stu-id="03267-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-133">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-133">Name</span></span>              | <span data-ttu-id="03267-134">brainpoolP160t1</span><span class="sxs-lookup"><span data-stu-id="03267-134">brainpoolP160t1</span></span>                                                                                                   |
| <span data-ttu-id="03267-135">標準</span><span class="sxs-lookup"><span data-stu-id="03267-135">Standard</span></span>          | [<span data-ttu-id="03267-136">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-136">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-137">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-137">Key size (bits)</span></span>   | <span data-ttu-id="03267-138">160</span><span class="sxs-lookup"><span data-stu-id="03267-138">160</span></span>                                                                                                               |
| <span data-ttu-id="03267-139">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-139">TLS capable</span></span>       | <span data-ttu-id="03267-140">No</span><span class="sxs-lookup"><span data-stu-id="03267-140">No</span></span>                                                                                                                |
| <span data-ttu-id="03267-141">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-141">Object identifier</span></span> | <span data-ttu-id="03267-142">1.3.36.3.3.2.8.1.1.2</span><span class="sxs-lookup"><span data-stu-id="03267-142">1.3.36.3.3.2.8.1.1.2</span></span>                                                                                              |



 

<span data-ttu-id="03267-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP192R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-144">需求</span><span class="sxs-lookup"><span data-stu-id="03267-144">Requirement</span></span> | <span data-ttu-id="03267-145">值</span><span class="sxs-lookup"><span data-stu-id="03267-145">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-146">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-146">Name</span></span>              | <span data-ttu-id="03267-147">brainpoolP192r1</span><span class="sxs-lookup"><span data-stu-id="03267-147">brainpoolP192r1</span></span>                                                                                                   |
| <span data-ttu-id="03267-148">標準</span><span class="sxs-lookup"><span data-stu-id="03267-148">Standard</span></span>          | [<span data-ttu-id="03267-149">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-149">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-150">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-150">Key size (bits)</span></span>   | <span data-ttu-id="03267-151">192</span><span class="sxs-lookup"><span data-stu-id="03267-151">192</span></span>                                                                                                               |
| <span data-ttu-id="03267-152">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-152">TLS capable</span></span>       | <span data-ttu-id="03267-153">No</span><span class="sxs-lookup"><span data-stu-id="03267-153">No</span></span>                                                                                                                |
| <span data-ttu-id="03267-154">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-154">Object identifier</span></span> | <span data-ttu-id="03267-155">1.3.36.3.3.2.8.1.1.3</span><span class="sxs-lookup"><span data-stu-id="03267-155">1.3.36.3.3.2.8.1.1.3</span></span>                                                                                              |



 

<span data-ttu-id="03267-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP192T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-157">需求</span><span class="sxs-lookup"><span data-stu-id="03267-157">Requirement</span></span> | <span data-ttu-id="03267-158">值</span><span class="sxs-lookup"><span data-stu-id="03267-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-159">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-159">Name</span></span>              | <span data-ttu-id="03267-160">brainpoolP192t1</span><span class="sxs-lookup"><span data-stu-id="03267-160">brainpoolP192t1</span></span>                                                                                                   |
| <span data-ttu-id="03267-161">標準</span><span class="sxs-lookup"><span data-stu-id="03267-161">Standard</span></span>          | [<span data-ttu-id="03267-162">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-162">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-163">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-163">Key size (bits)</span></span>   | <span data-ttu-id="03267-164">192</span><span class="sxs-lookup"><span data-stu-id="03267-164">192</span></span>                                                                                                               |
| <span data-ttu-id="03267-165">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-165">TLS capable</span></span>       | <span data-ttu-id="03267-166">No</span><span class="sxs-lookup"><span data-stu-id="03267-166">No</span></span>                                                                                                                |
| <span data-ttu-id="03267-167">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-167">Object identifier</span></span> | <span data-ttu-id="03267-168">1.3.36.3.3.2.8.1.1.4</span><span class="sxs-lookup"><span data-stu-id="03267-168">1.3.36.3.3.2.8.1.1.4</span></span>                                                                                              |



 

<span data-ttu-id="03267-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP224R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-170">需求</span><span class="sxs-lookup"><span data-stu-id="03267-170">Requirement</span></span> | <span data-ttu-id="03267-171">值</span><span class="sxs-lookup"><span data-stu-id="03267-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-172">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-172">Name</span></span>              | <span data-ttu-id="03267-173">brainpoolP224r1</span><span class="sxs-lookup"><span data-stu-id="03267-173">brainpoolP224r1</span></span>                                                                                                   |
| <span data-ttu-id="03267-174">標準</span><span class="sxs-lookup"><span data-stu-id="03267-174">Standard</span></span>          | [<span data-ttu-id="03267-175">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-175">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-176">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-176">Key size (bits)</span></span>   | <span data-ttu-id="03267-177">224</span><span class="sxs-lookup"><span data-stu-id="03267-177">224</span></span>                                                                                                               |
| <span data-ttu-id="03267-178">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-178">TLS capable</span></span>       | <span data-ttu-id="03267-179">No</span><span class="sxs-lookup"><span data-stu-id="03267-179">No</span></span>                                                                                                                |
| <span data-ttu-id="03267-180">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-180">Object identifier</span></span> | <span data-ttu-id="03267-181">1.3.36.3.3.2.8.1.1.5</span><span class="sxs-lookup"><span data-stu-id="03267-181">1.3.36.3.3.2.8.1.1.5</span></span>                                                                                              |



 

<span data-ttu-id="03267-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP224T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-183">需求</span><span class="sxs-lookup"><span data-stu-id="03267-183">Requirement</span></span> | <span data-ttu-id="03267-184">值</span><span class="sxs-lookup"><span data-stu-id="03267-184">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-185">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-185">Name</span></span>              | <span data-ttu-id="03267-186">brainpoolP224t1</span><span class="sxs-lookup"><span data-stu-id="03267-186">brainpoolP224t1</span></span>                                                                                                   |
| <span data-ttu-id="03267-187">標準</span><span class="sxs-lookup"><span data-stu-id="03267-187">Standard</span></span>          | [<span data-ttu-id="03267-188">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-188">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-189">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-189">Key size (bits)</span></span>   | <span data-ttu-id="03267-190">224</span><span class="sxs-lookup"><span data-stu-id="03267-190">224</span></span>                                                                                                               |
| <span data-ttu-id="03267-191">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-191">TLS capable</span></span>       | <span data-ttu-id="03267-192">No</span><span class="sxs-lookup"><span data-stu-id="03267-192">No</span></span>                                                                                                                |
| <span data-ttu-id="03267-193">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-193">Object identifier</span></span> | <span data-ttu-id="03267-194">1.3.36.3.3.2.8.1.1.6</span><span class="sxs-lookup"><span data-stu-id="03267-194">1.3.36.3.3.2.8.1.1.6</span></span>                                                                                              |



 

<span data-ttu-id="03267-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP256R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-196">需求</span><span class="sxs-lookup"><span data-stu-id="03267-196">Requirement</span></span> | <span data-ttu-id="03267-197">值</span><span class="sxs-lookup"><span data-stu-id="03267-197">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-198">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-198">Name</span></span>              | <span data-ttu-id="03267-199">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="03267-199">brainpoolP256r1</span></span>                                                                                                   |
| <span data-ttu-id="03267-200">標準</span><span class="sxs-lookup"><span data-stu-id="03267-200">Standard</span></span>          | [<span data-ttu-id="03267-201">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-201">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-202">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-202">Key size (bits)</span></span>   | <span data-ttu-id="03267-203">256</span><span class="sxs-lookup"><span data-stu-id="03267-203">256</span></span>                                                                                                               |
| <span data-ttu-id="03267-204">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-204">TLS capable</span></span>       | <span data-ttu-id="03267-205">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-205">Yes</span></span>                                                                                                               |
| <span data-ttu-id="03267-206">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-206">Object identifier</span></span> | <span data-ttu-id="03267-207">1.3.36.3.3.2.8.1.1.7</span><span class="sxs-lookup"><span data-stu-id="03267-207">1.3.36.3.3.2.8.1.1.7</span></span>                                                                                              |



 

<span data-ttu-id="03267-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP256T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-209">需求</span><span class="sxs-lookup"><span data-stu-id="03267-209">Requirement</span></span> | <span data-ttu-id="03267-210">值</span><span class="sxs-lookup"><span data-stu-id="03267-210">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-211">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-211">Name</span></span>              | <span data-ttu-id="03267-212">brainpoolP256t1</span><span class="sxs-lookup"><span data-stu-id="03267-212">brainpoolP256t1</span></span>                                                                                                   |
| <span data-ttu-id="03267-213">標準</span><span class="sxs-lookup"><span data-stu-id="03267-213">Standard</span></span>          | [<span data-ttu-id="03267-214">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-214">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-215">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-215">Key size (bits)</span></span>   | <span data-ttu-id="03267-216">256</span><span class="sxs-lookup"><span data-stu-id="03267-216">256</span></span>                                                                                                               |
| <span data-ttu-id="03267-217">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-217">TLS capable</span></span>       | <span data-ttu-id="03267-218">No</span><span class="sxs-lookup"><span data-stu-id="03267-218">No</span></span>                                                                                                                |
| <span data-ttu-id="03267-219">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-219">Object identifier</span></span> | <span data-ttu-id="03267-220">1.3.36.3.3.2.8.1.1.8</span><span class="sxs-lookup"><span data-stu-id="03267-220">1.3.36.3.3.2.8.1.1.8</span></span>                                                                                              |



 

<span data-ttu-id="03267-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP320R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP320R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-222">需求</span><span class="sxs-lookup"><span data-stu-id="03267-222">Requirement</span></span> | <span data-ttu-id="03267-223">值</span><span class="sxs-lookup"><span data-stu-id="03267-223">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-224">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-224">Name</span></span>              | <span data-ttu-id="03267-225">brainpoolP320r1</span><span class="sxs-lookup"><span data-stu-id="03267-225">brainpoolP320r1</span></span>                                                                                                   |
| <span data-ttu-id="03267-226">標準</span><span class="sxs-lookup"><span data-stu-id="03267-226">Standard</span></span>          | [<span data-ttu-id="03267-227">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-227">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-228">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-228">Key size (bits)</span></span>   | <span data-ttu-id="03267-229">320</span><span class="sxs-lookup"><span data-stu-id="03267-229">320</span></span>                                                                                                               |
| <span data-ttu-id="03267-230">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-230">TLS capable</span></span>       | <span data-ttu-id="03267-231">No</span><span class="sxs-lookup"><span data-stu-id="03267-231">No</span></span>                                                                                                                |
| <span data-ttu-id="03267-232">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-232">Object identifier</span></span> | <span data-ttu-id="03267-233">1.3.36.3.3.2.8.1.1.9</span><span class="sxs-lookup"><span data-stu-id="03267-233">1.3.36.3.3.2.8.1.1.9</span></span>                                                                                              |



 

<span data-ttu-id="03267-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP32 0T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP32 0T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-235">需求</span><span class="sxs-lookup"><span data-stu-id="03267-235">Requirement</span></span> | <span data-ttu-id="03267-236">值</span><span class="sxs-lookup"><span data-stu-id="03267-236">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-237">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-237">Name</span></span>              | <span data-ttu-id="03267-238">brainpoolP320t1</span><span class="sxs-lookup"><span data-stu-id="03267-238">brainpoolP320t1</span></span>                                                                                                   |
| <span data-ttu-id="03267-239">標準</span><span class="sxs-lookup"><span data-stu-id="03267-239">Standard</span></span>          | [<span data-ttu-id="03267-240">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-240">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-241">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-241">Key size (bits)</span></span>   | <span data-ttu-id="03267-242">320</span><span class="sxs-lookup"><span data-stu-id="03267-242">320</span></span>                                                                                                               |
| <span data-ttu-id="03267-243">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-243">TLS capable</span></span>       | <span data-ttu-id="03267-244">No</span><span class="sxs-lookup"><span data-stu-id="03267-244">No</span></span>                                                                                                                |
| <span data-ttu-id="03267-245">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-245">Object identifier</span></span> | <span data-ttu-id="03267-246">1.3.36.3.3.2.8.1.1.10</span><span class="sxs-lookup"><span data-stu-id="03267-246">1.3.36.3.3.2.8.1.1.10</span></span>                                                                                             |



 

<span data-ttu-id="03267-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ BRAINPOOLP384R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-248">需求</span><span class="sxs-lookup"><span data-stu-id="03267-248">Requirement</span></span> | <span data-ttu-id="03267-249">值</span><span class="sxs-lookup"><span data-stu-id="03267-249">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-250">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-250">Name</span></span>              | <span data-ttu-id="03267-251">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="03267-251">brainpoolP384r1</span></span>                                                                                                   |
| <span data-ttu-id="03267-252">標準</span><span class="sxs-lookup"><span data-stu-id="03267-252">Standard</span></span>          | [<span data-ttu-id="03267-253">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-253">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-254">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-254">Key size (bits)</span></span>   | <span data-ttu-id="03267-255">384</span><span class="sxs-lookup"><span data-stu-id="03267-255">384</span></span>                                                                                                               |
| <span data-ttu-id="03267-256">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-256">TLS capable</span></span>       | <span data-ttu-id="03267-257">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-257">Yes</span></span>                                                                                                               |
| <span data-ttu-id="03267-258">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-258">Object identifier</span></span> | <span data-ttu-id="03267-259">1.3.36.3.3.2.8.1.1.11</span><span class="sxs-lookup"><span data-stu-id="03267-259">1.3.36.3.3.2.8.1.1.11</span></span>                                                                                             |



 

<span data-ttu-id="03267-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP384T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-261">需求</span><span class="sxs-lookup"><span data-stu-id="03267-261">Requirement</span></span> | <span data-ttu-id="03267-262">值</span><span class="sxs-lookup"><span data-stu-id="03267-262">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-263">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-263">Name</span></span>              | <span data-ttu-id="03267-264">brainpoolP384t1</span><span class="sxs-lookup"><span data-stu-id="03267-264">brainpoolP384t1</span></span>                                                                                                   |
| <span data-ttu-id="03267-265">標準</span><span class="sxs-lookup"><span data-stu-id="03267-265">Standard</span></span>          | [<span data-ttu-id="03267-266">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-266">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-267">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-267">Key size (bits)</span></span>   | <span data-ttu-id="03267-268">384</span><span class="sxs-lookup"><span data-stu-id="03267-268">384</span></span>                                                                                                               |
| <span data-ttu-id="03267-269">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-269">TLS capable</span></span>       | <span data-ttu-id="03267-270">No</span><span class="sxs-lookup"><span data-stu-id="03267-270">No</span></span>                                                                                                                |
| <span data-ttu-id="03267-271">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-271">Object identifier</span></span> | <span data-ttu-id="03267-272">1.3.36.3.3.2.8.1.1.12</span><span class="sxs-lookup"><span data-stu-id="03267-272">1.3.36.3.3.2.8.1.1.12</span></span>                                                                                             |



 

<span data-ttu-id="03267-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP512R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-274">需求</span><span class="sxs-lookup"><span data-stu-id="03267-274">Requirement</span></span> | <span data-ttu-id="03267-275">值</span><span class="sxs-lookup"><span data-stu-id="03267-275">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-276">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-276">Name</span></span>              | <span data-ttu-id="03267-277">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="03267-277">brainpoolP512r1</span></span>                                                                                                   |
| <span data-ttu-id="03267-278">標準</span><span class="sxs-lookup"><span data-stu-id="03267-278">Standard</span></span>          | [<span data-ttu-id="03267-279">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-279">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-280">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-280">Key size (bits)</span></span>   | <span data-ttu-id="03267-281">512</span><span class="sxs-lookup"><span data-stu-id="03267-281">512</span></span>                                                                                                               |
| <span data-ttu-id="03267-282">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-282">TLS capable</span></span>       | <span data-ttu-id="03267-283">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-283">Yes</span></span>                                                                                                               |
| <span data-ttu-id="03267-284">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-284">Object identifier</span></span> | <span data-ttu-id="03267-285">1.3.36.3.3.2.8.1.1.13</span><span class="sxs-lookup"><span data-stu-id="03267-285">1.3.36.3.3.2.8.1.1.13</span></span>                                                                                             |



 

<span data-ttu-id="03267-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP512T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-287">需求</span><span class="sxs-lookup"><span data-stu-id="03267-287">Requirement</span></span> | <span data-ttu-id="03267-288">值</span><span class="sxs-lookup"><span data-stu-id="03267-288">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-289">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-289">Name</span></span>              | <span data-ttu-id="03267-290">brainpoolP512t1</span><span class="sxs-lookup"><span data-stu-id="03267-290">brainpoolP512t1</span></span>                                                                                                   |
| <span data-ttu-id="03267-291">標準</span><span class="sxs-lookup"><span data-stu-id="03267-291">Standard</span></span>          | [<span data-ttu-id="03267-292">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="03267-292">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="03267-293">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-293">Key size (bits)</span></span>   | <span data-ttu-id="03267-294">512</span><span class="sxs-lookup"><span data-stu-id="03267-294">512</span></span>                                                                                                               |
| <span data-ttu-id="03267-295">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-295">TLS capable</span></span>       | <span data-ttu-id="03267-296">No</span><span class="sxs-lookup"><span data-stu-id="03267-296">No</span></span>                                                                                                                |
| <span data-ttu-id="03267-297">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-297">Object identifier</span></span> | <span data-ttu-id="03267-298">1.3.36.3.3.2.8.1.1.14</span><span class="sxs-lookup"><span data-stu-id="03267-298">1.3.36.3.3.2.8.1.1.14</span></span>                                                                                             |



 

<span data-ttu-id="03267-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ECC \_ 曲線 \_ EC192WAPI**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT\_ECC\_CURVE\_EC192WAPI** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-300">需求</span><span class="sxs-lookup"><span data-stu-id="03267-300">Requirement</span></span> | <span data-ttu-id="03267-301">值</span><span class="sxs-lookup"><span data-stu-id="03267-301">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="03267-302">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-302">Name</span></span>              | <span data-ttu-id="03267-303">ec192wapi</span><span class="sxs-lookup"><span data-stu-id="03267-303">ec192wapi</span></span>                                                      |
| <span data-ttu-id="03267-304">標準</span><span class="sxs-lookup"><span data-stu-id="03267-304">Standard</span></span>          | <span data-ttu-id="03267-305">國際區域網路的中文標準 (GB 15629.11-2003) </span><span class="sxs-lookup"><span data-stu-id="03267-305">Chinese National Standard for Wireless LANs (GB 15629.11-2003)</span></span> |
| <span data-ttu-id="03267-306">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-306">Key size (bits)</span></span>   | <span data-ttu-id="03267-307">192</span><span class="sxs-lookup"><span data-stu-id="03267-307">192</span></span>                                                            |
| <span data-ttu-id="03267-308">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-308">TLS capable</span></span>       | <span data-ttu-id="03267-309">No</span><span class="sxs-lookup"><span data-stu-id="03267-309">No</span></span>                                                             |
| <span data-ttu-id="03267-310">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-310">Object identifier</span></span> | <span data-ttu-id="03267-311">1.2.156.11235.1.1.2.1</span><span class="sxs-lookup"><span data-stu-id="03267-311">1.2.156.11235.1.1.2.1</span></span>                                          |



 

<span data-ttu-id="03267-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP192**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT\_ECC\_CURVE\_NISTP192**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-313">需求</span><span class="sxs-lookup"><span data-stu-id="03267-313">Requirement</span></span> | <span data-ttu-id="03267-314">值</span><span class="sxs-lookup"><span data-stu-id="03267-314">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-315">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-315">Name</span></span>              | <span data-ttu-id="03267-316">nistP192</span><span class="sxs-lookup"><span data-stu-id="03267-316">nistP192</span></span>                                                                                                                     |
| <span data-ttu-id="03267-317">標準</span><span class="sxs-lookup"><span data-stu-id="03267-317">Standard</span></span>          | [<span data-ttu-id="03267-318">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="03267-318">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="03267-319">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-319">Key size (bits)</span></span>   | <span data-ttu-id="03267-320">192</span><span class="sxs-lookup"><span data-stu-id="03267-320">192</span></span>                                                                                                                          |
| <span data-ttu-id="03267-321">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-321">TLS capable</span></span>       | <span data-ttu-id="03267-322">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-322">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="03267-323">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-323">Object identifier</span></span> | <span data-ttu-id="03267-324">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="03267-324">1.2.840.10045.3.1.1</span></span>                                                                                                          |



 

<span data-ttu-id="03267-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ECC \_ 曲線 \_ NISTP224**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT\_ECC\_CURVE\_NISTP224** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-326">需求</span><span class="sxs-lookup"><span data-stu-id="03267-326">Requirement</span></span> | <span data-ttu-id="03267-327">值</span><span class="sxs-lookup"><span data-stu-id="03267-327">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-328">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-328">Name</span></span>              | <span data-ttu-id="03267-329">nistP224</span><span class="sxs-lookup"><span data-stu-id="03267-329">nistP224</span></span>                                                                                                                     |
| <span data-ttu-id="03267-330">標準</span><span class="sxs-lookup"><span data-stu-id="03267-330">Standard</span></span>          | [<span data-ttu-id="03267-331">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="03267-331">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="03267-332">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-332">Key size (bits)</span></span>   | <span data-ttu-id="03267-333">224</span><span class="sxs-lookup"><span data-stu-id="03267-333">224</span></span>                                                                                                                          |
| <span data-ttu-id="03267-334">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-334">TLS capable</span></span>       | <span data-ttu-id="03267-335">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-335">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="03267-336">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-336">Object identifier</span></span> | <span data-ttu-id="03267-337">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="03267-337">1.3.132.0.33</span></span>                                                                                                                 |



 

<span data-ttu-id="03267-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP256**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT\_ECC\_CURVE\_NISTP256**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-339">需求</span><span class="sxs-lookup"><span data-stu-id="03267-339">Requirement</span></span> | <span data-ttu-id="03267-340">值</span><span class="sxs-lookup"><span data-stu-id="03267-340">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-341">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-341">Name</span></span>              | <span data-ttu-id="03267-342">nistP256</span><span class="sxs-lookup"><span data-stu-id="03267-342">nistP256</span></span>                                                                                                                     |
| <span data-ttu-id="03267-343">標準</span><span class="sxs-lookup"><span data-stu-id="03267-343">Standard</span></span>          | [<span data-ttu-id="03267-344">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="03267-344">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="03267-345">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-345">Key size (bits)</span></span>   | <span data-ttu-id="03267-346">256</span><span class="sxs-lookup"><span data-stu-id="03267-346">256</span></span>                                                                                                                          |
| <span data-ttu-id="03267-347">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-347">TLS capable</span></span>       | <span data-ttu-id="03267-348">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-348">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="03267-349">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-349">Object identifier</span></span> | <span data-ttu-id="03267-350">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="03267-350">1.2.840.10045.3.1.7</span></span>                                                                                                          |



 

<span data-ttu-id="03267-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ECC \_ 曲線 \_ NISTP384**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT\_ECC\_CURVE\_NISTP384** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-352">需求</span><span class="sxs-lookup"><span data-stu-id="03267-352">Requirement</span></span> | <span data-ttu-id="03267-353">值</span><span class="sxs-lookup"><span data-stu-id="03267-353">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-354">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-354">Name</span></span>              | <span data-ttu-id="03267-355">nistP384</span><span class="sxs-lookup"><span data-stu-id="03267-355">nistP384</span></span>                                                                                                                     |
| <span data-ttu-id="03267-356">標準</span><span class="sxs-lookup"><span data-stu-id="03267-356">Standard</span></span>          | [<span data-ttu-id="03267-357">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="03267-357">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="03267-358">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-358">Key size (bits)</span></span>   | <span data-ttu-id="03267-359">384</span><span class="sxs-lookup"><span data-stu-id="03267-359">384</span></span>                                                                                                                          |
| <span data-ttu-id="03267-360">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-360">TLS capable</span></span>       | <span data-ttu-id="03267-361">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-361">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="03267-362">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-362">Object identifier</span></span> | <span data-ttu-id="03267-363">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="03267-363">1.3.132.0.34</span></span>                                                                                                                 |



 

<span data-ttu-id="03267-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP521**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT\_ECC\_CURVE\_NISTP521**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-365">需求</span><span class="sxs-lookup"><span data-stu-id="03267-365">Requirement</span></span> | <span data-ttu-id="03267-366">值</span><span class="sxs-lookup"><span data-stu-id="03267-366">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-367">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-367">Name</span></span>              | <span data-ttu-id="03267-368">nistP521</span><span class="sxs-lookup"><span data-stu-id="03267-368">nistP521</span></span>                                                                                                                     |
| <span data-ttu-id="03267-369">標準</span><span class="sxs-lookup"><span data-stu-id="03267-369">Standard</span></span>          | [<span data-ttu-id="03267-370">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="03267-370">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="03267-371">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-371">Key size (bits)</span></span>   | <span data-ttu-id="03267-372">521</span><span class="sxs-lookup"><span data-stu-id="03267-372">521</span></span>                                                                                                                          |
| <span data-ttu-id="03267-373">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-373">TLS capable</span></span>       | <span data-ttu-id="03267-374">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-374">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="03267-375">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-375">Object identifier</span></span> | <span data-ttu-id="03267-376">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="03267-376">1.3.132.0.35</span></span>                                                                                                                 |



 

<span data-ttu-id="03267-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ NUMSP256T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP256T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-378">需求</span><span class="sxs-lookup"><span data-stu-id="03267-378">Requirement</span></span> | <span data-ttu-id="03267-379">值</span><span class="sxs-lookup"><span data-stu-id="03267-379">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-380">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-380">Name</span></span>              | <span data-ttu-id="03267-381">numsP256t1</span><span class="sxs-lookup"><span data-stu-id="03267-381">numsP256t1</span></span>                                                                                                                              |
| <span data-ttu-id="03267-382">標準</span><span class="sxs-lookup"><span data-stu-id="03267-382">Standard</span></span>          | [<span data-ttu-id="03267-383">MSR ECCLib 中的曲線選取和支援曲線參數規格</span><span class="sxs-lookup"><span data-stu-id="03267-383">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="03267-384">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-384">Key size (bits)</span></span>   | <span data-ttu-id="03267-385">256</span><span class="sxs-lookup"><span data-stu-id="03267-385">256</span></span>                                                                                                                                     |
| <span data-ttu-id="03267-386">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-386">TLS capable</span></span>       | <span data-ttu-id="03267-387">No</span><span class="sxs-lookup"><span data-stu-id="03267-387">No</span></span>                                                                                                                                      |
| <span data-ttu-id="03267-388">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-388">Object identifier</span></span> | <span data-ttu-id="03267-389">無</span><span class="sxs-lookup"><span data-stu-id="03267-389">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="03267-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ NUMSP384T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP384T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-391">需求</span><span class="sxs-lookup"><span data-stu-id="03267-391">Requirement</span></span> | <span data-ttu-id="03267-392">值</span><span class="sxs-lookup"><span data-stu-id="03267-392">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-393">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-393">Name</span></span>              | <span data-ttu-id="03267-394">numsP384t1</span><span class="sxs-lookup"><span data-stu-id="03267-394">numsP384t1</span></span>                                                                                                                              |
| <span data-ttu-id="03267-395">標準</span><span class="sxs-lookup"><span data-stu-id="03267-395">Standard</span></span>          | [<span data-ttu-id="03267-396">MSR ECCLib 中的曲線選取和支援曲線參數規格</span><span class="sxs-lookup"><span data-stu-id="03267-396">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="03267-397">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-397">Key size (bits)</span></span>   | <span data-ttu-id="03267-398">384</span><span class="sxs-lookup"><span data-stu-id="03267-398">384</span></span>                                                                                                                                     |
| <span data-ttu-id="03267-399">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-399">TLS capable</span></span>       | <span data-ttu-id="03267-400">No</span><span class="sxs-lookup"><span data-stu-id="03267-400">No</span></span>                                                                                                                                      |
| <span data-ttu-id="03267-401">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-401">Object identifier</span></span> | <span data-ttu-id="03267-402">無</span><span class="sxs-lookup"><span data-stu-id="03267-402">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="03267-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ NUMSP512T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT\_ECC\_CURVE\_NUMSP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-404">需求</span><span class="sxs-lookup"><span data-stu-id="03267-404">Requirement</span></span> | <span data-ttu-id="03267-405">值</span><span class="sxs-lookup"><span data-stu-id="03267-405">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-406">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-406">Name</span></span>              | <span data-ttu-id="03267-407">numsP512t1</span><span class="sxs-lookup"><span data-stu-id="03267-407">numsP512t1</span></span>                                                                                                                              |
| <span data-ttu-id="03267-408">標準</span><span class="sxs-lookup"><span data-stu-id="03267-408">Standard</span></span>          | [<span data-ttu-id="03267-409">MSR ECCLib 中的曲線選取和支援曲線參數規格</span><span class="sxs-lookup"><span data-stu-id="03267-409">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="03267-410">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-410">Key size (bits)</span></span>   | <span data-ttu-id="03267-411">512</span><span class="sxs-lookup"><span data-stu-id="03267-411">512</span></span>                                                                                                                                     |
| <span data-ttu-id="03267-412">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-412">TLS capable</span></span>       | <span data-ttu-id="03267-413">No</span><span class="sxs-lookup"><span data-stu-id="03267-413">No</span></span>                                                                                                                                      |
| <span data-ttu-id="03267-414">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-414">Object identifier</span></span> | <span data-ttu-id="03267-415">無</span><span class="sxs-lookup"><span data-stu-id="03267-415">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="03267-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160K1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-417">需求</span><span class="sxs-lookup"><span data-stu-id="03267-417">Requirement</span></span> | <span data-ttu-id="03267-418">值</span><span class="sxs-lookup"><span data-stu-id="03267-418">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="03267-419">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-419">Name</span></span>              | <span data-ttu-id="03267-420">secP160k1</span><span class="sxs-lookup"><span data-stu-id="03267-420">secP160k1</span></span>                                                                       |
| <span data-ttu-id="03267-421">標準</span><span class="sxs-lookup"><span data-stu-id="03267-421">Standard</span></span>          | [<span data-ttu-id="03267-422">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="03267-422">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="03267-423">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-423">Key size (bits)</span></span>   | <span data-ttu-id="03267-424">160</span><span class="sxs-lookup"><span data-stu-id="03267-424">160</span></span>                                                                             |
| <span data-ttu-id="03267-425">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-425">TLS capable</span></span>       | <span data-ttu-id="03267-426">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-426">Yes</span></span>                                                                             |
| <span data-ttu-id="03267-427">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-427">Object identifier</span></span> | <span data-ttu-id="03267-428">1.3.132.0.9</span><span class="sxs-lookup"><span data-stu-id="03267-428">1.3.132.0.9</span></span>                                                                     |



 

<span data-ttu-id="03267-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-430">需求</span><span class="sxs-lookup"><span data-stu-id="03267-430">Requirement</span></span> | <span data-ttu-id="03267-431">值</span><span class="sxs-lookup"><span data-stu-id="03267-431">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="03267-432">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-432">Name</span></span>              | <span data-ttu-id="03267-433">secP160r1</span><span class="sxs-lookup"><span data-stu-id="03267-433">secP160r1</span></span>                                                                       |
| <span data-ttu-id="03267-434">標準</span><span class="sxs-lookup"><span data-stu-id="03267-434">Standard</span></span>          | [<span data-ttu-id="03267-435">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="03267-435">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="03267-436">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-436">Key size (bits)</span></span>   | <span data-ttu-id="03267-437">160</span><span class="sxs-lookup"><span data-stu-id="03267-437">160</span></span>                                                                             |
| <span data-ttu-id="03267-438">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-438">TLS capable</span></span>       | <span data-ttu-id="03267-439">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-439">Yes</span></span>                                                                             |
| <span data-ttu-id="03267-440">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-440">Object identifier</span></span> | <span data-ttu-id="03267-441">1.3.132.0.8</span><span class="sxs-lookup"><span data-stu-id="03267-441">1.3.132.0.8</span></span>                                                                     |



 

<span data-ttu-id="03267-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-443">需求</span><span class="sxs-lookup"><span data-stu-id="03267-443">Requirement</span></span> | <span data-ttu-id="03267-444">值</span><span class="sxs-lookup"><span data-stu-id="03267-444">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="03267-445">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-445">Name</span></span>              | <span data-ttu-id="03267-446">secP160r2</span><span class="sxs-lookup"><span data-stu-id="03267-446">secP160r2</span></span>                                                                       |
| <span data-ttu-id="03267-447">標準</span><span class="sxs-lookup"><span data-stu-id="03267-447">Standard</span></span>          | [<span data-ttu-id="03267-448">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="03267-448">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="03267-449">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-449">Key size (bits)</span></span>   | <span data-ttu-id="03267-450">160</span><span class="sxs-lookup"><span data-stu-id="03267-450">160</span></span>                                                                             |
| <span data-ttu-id="03267-451">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-451">TLS capable</span></span>       | <span data-ttu-id="03267-452">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-452">Yes</span></span>                                                                             |
| <span data-ttu-id="03267-453">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-453">Object identifier</span></span> | <span data-ttu-id="03267-454">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="03267-454">1.3.132.0.30</span></span>                                                                    |



 

<span data-ttu-id="03267-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP192K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT\_ECC\_CURVE\_SECP192K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-456">需求</span><span class="sxs-lookup"><span data-stu-id="03267-456">Requirement</span></span> | <span data-ttu-id="03267-457">值</span><span class="sxs-lookup"><span data-stu-id="03267-457">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="03267-458">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-458">Name</span></span>              | <span data-ttu-id="03267-459">secP192k1</span><span class="sxs-lookup"><span data-stu-id="03267-459">secP192k1</span></span>                                                                       |
| <span data-ttu-id="03267-460">標準</span><span class="sxs-lookup"><span data-stu-id="03267-460">Standard</span></span>          | [<span data-ttu-id="03267-461">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="03267-461">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="03267-462">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-462">Key size (bits)</span></span>   | <span data-ttu-id="03267-463">192</span><span class="sxs-lookup"><span data-stu-id="03267-463">192</span></span>                                                                             |
| <span data-ttu-id="03267-464">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-464">TLS capable</span></span>       | <span data-ttu-id="03267-465">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-465">Yes</span></span>                                                                             |
| <span data-ttu-id="03267-466">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-466">Object identifier</span></span> | <span data-ttu-id="03267-467">1.3.132.0.31</span><span class="sxs-lookup"><span data-stu-id="03267-467">1.3.132.0.31</span></span>                                                                    |



 

<span data-ttu-id="03267-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP192R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP192R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-469">需求</span><span class="sxs-lookup"><span data-stu-id="03267-469">Requirement</span></span> | <span data-ttu-id="03267-470">值</span><span class="sxs-lookup"><span data-stu-id="03267-470">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="03267-471">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-471">Name</span></span>              | <span data-ttu-id="03267-472">secP192r1</span><span class="sxs-lookup"><span data-stu-id="03267-472">secP192r1</span></span>                                                                       |
| <span data-ttu-id="03267-473">標準</span><span class="sxs-lookup"><span data-stu-id="03267-473">Standard</span></span>          | [<span data-ttu-id="03267-474">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="03267-474">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="03267-475">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-475">Key size (bits)</span></span>   | <span data-ttu-id="03267-476">192</span><span class="sxs-lookup"><span data-stu-id="03267-476">192</span></span>                                                                             |
| <span data-ttu-id="03267-477">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-477">TLS capable</span></span>       | <span data-ttu-id="03267-478">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-478">Yes</span></span>                                                                             |
| <span data-ttu-id="03267-479">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-479">Object identifier</span></span> | <span data-ttu-id="03267-480">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="03267-480">1.2.840.10045.3.1.1</span></span>                                                             |



 

<span data-ttu-id="03267-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP224K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT\_ECC\_CURVE\_SECP224K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-482">需求</span><span class="sxs-lookup"><span data-stu-id="03267-482">Requirement</span></span> | <span data-ttu-id="03267-483">值</span><span class="sxs-lookup"><span data-stu-id="03267-483">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="03267-484">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-484">Name</span></span>              | <span data-ttu-id="03267-485">secP224k1</span><span class="sxs-lookup"><span data-stu-id="03267-485">secP224k1</span></span>                                                                       |
| <span data-ttu-id="03267-486">標準</span><span class="sxs-lookup"><span data-stu-id="03267-486">Standard</span></span>          | [<span data-ttu-id="03267-487">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="03267-487">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="03267-488">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-488">Key size (bits)</span></span>   | <span data-ttu-id="03267-489">224</span><span class="sxs-lookup"><span data-stu-id="03267-489">224</span></span>                                                                             |
| <span data-ttu-id="03267-490">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-490">TLS capable</span></span>       | <span data-ttu-id="03267-491">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-491">Yes</span></span>                                                                             |
| <span data-ttu-id="03267-492">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-492">Object identifier</span></span> | <span data-ttu-id="03267-493">1.3.132.0.32</span><span class="sxs-lookup"><span data-stu-id="03267-493">1.3.132.0.32</span></span>                                                                    |



 

<span data-ttu-id="03267-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP224R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT\_ECC\_CURVE\_SECP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-495">需求</span><span class="sxs-lookup"><span data-stu-id="03267-495">Requirement</span></span> | <span data-ttu-id="03267-496">值</span><span class="sxs-lookup"><span data-stu-id="03267-496">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="03267-497">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-497">Name</span></span>              | <span data-ttu-id="03267-498">secP224r1</span><span class="sxs-lookup"><span data-stu-id="03267-498">secP224r1</span></span>                                                                       |
| <span data-ttu-id="03267-499">標準</span><span class="sxs-lookup"><span data-stu-id="03267-499">Standard</span></span>          | [<span data-ttu-id="03267-500">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="03267-500">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="03267-501">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-501">Key size (bits)</span></span>   | <span data-ttu-id="03267-502">224</span><span class="sxs-lookup"><span data-stu-id="03267-502">224</span></span>                                                                             |
| <span data-ttu-id="03267-503">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-503">TLS capable</span></span>       | <span data-ttu-id="03267-504">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-504">Yes</span></span>                                                                             |
| <span data-ttu-id="03267-505">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-505">Object identifier</span></span> | <span data-ttu-id="03267-506">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="03267-506">1.3.132.0.33</span></span>                                                                    |



 

<span data-ttu-id="03267-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP256K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT\_ECC\_CURVE\_SECP256K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-508">需求</span><span class="sxs-lookup"><span data-stu-id="03267-508">Requirement</span></span> | <span data-ttu-id="03267-509">值</span><span class="sxs-lookup"><span data-stu-id="03267-509">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="03267-510">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-510">Name</span></span>              | <span data-ttu-id="03267-511">secP256k1</span><span class="sxs-lookup"><span data-stu-id="03267-511">secP256k1</span></span>                                                                       |
| <span data-ttu-id="03267-512">標準</span><span class="sxs-lookup"><span data-stu-id="03267-512">Standard</span></span>          | [<span data-ttu-id="03267-513">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="03267-513">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="03267-514">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-514">Key size (bits)</span></span>   | <span data-ttu-id="03267-515">256</span><span class="sxs-lookup"><span data-stu-id="03267-515">256</span></span>                                                                             |
| <span data-ttu-id="03267-516">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-516">TLS capable</span></span>       | <span data-ttu-id="03267-517">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-517">Yes</span></span>                                                                             |
| <span data-ttu-id="03267-518">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-518">Object identifier</span></span> | <span data-ttu-id="03267-519">1.3.132.0.10</span><span class="sxs-lookup"><span data-stu-id="03267-519">1.3.132.0.10</span></span>                                                                    |



 

<span data-ttu-id="03267-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP256R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT\_ECC\_CURVE\_SECP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-521">需求</span><span class="sxs-lookup"><span data-stu-id="03267-521">Requirement</span></span> | <span data-ttu-id="03267-522">值</span><span class="sxs-lookup"><span data-stu-id="03267-522">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="03267-523">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-523">Name</span></span>              | <span data-ttu-id="03267-524">secP256r1</span><span class="sxs-lookup"><span data-stu-id="03267-524">secP256r1</span></span>                                                                       |
| <span data-ttu-id="03267-525">標準</span><span class="sxs-lookup"><span data-stu-id="03267-525">Standard</span></span>          | [<span data-ttu-id="03267-526">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="03267-526">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="03267-527">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-527">Key size (bits)</span></span>   | <span data-ttu-id="03267-528">256</span><span class="sxs-lookup"><span data-stu-id="03267-528">256</span></span>                                                                             |
| <span data-ttu-id="03267-529">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-529">TLS capable</span></span>       | <span data-ttu-id="03267-530">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-530">Yes</span></span>                                                                             |
| <span data-ttu-id="03267-531">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-531">Object identifier</span></span> | <span data-ttu-id="03267-532">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="03267-532">1.2.840.10045.3.1.7</span></span>                                                             |



 

<span data-ttu-id="03267-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP384R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-534">需求</span><span class="sxs-lookup"><span data-stu-id="03267-534">Requirement</span></span> | <span data-ttu-id="03267-535">值</span><span class="sxs-lookup"><span data-stu-id="03267-535">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="03267-536">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-536">Name</span></span>              | <span data-ttu-id="03267-537">secP384r1</span><span class="sxs-lookup"><span data-stu-id="03267-537">secP384r1</span></span>                                                                       |
| <span data-ttu-id="03267-538">標準</span><span class="sxs-lookup"><span data-stu-id="03267-538">Standard</span></span>          | [<span data-ttu-id="03267-539">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="03267-539">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="03267-540">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-540">Key size (bits)</span></span>   | <span data-ttu-id="03267-541">384</span><span class="sxs-lookup"><span data-stu-id="03267-541">384</span></span>                                                                             |
| <span data-ttu-id="03267-542">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-542">TLS capable</span></span>       | <span data-ttu-id="03267-543">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-543">Yes</span></span>                                                                             |
| <span data-ttu-id="03267-544">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-544">Object identifier</span></span> | <span data-ttu-id="03267-545">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="03267-545">1.3.132.0.34</span></span>                                                                    |



 

<span data-ttu-id="03267-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP521R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT\_ECC\_CURVE\_SECP521R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-547">需求</span><span class="sxs-lookup"><span data-stu-id="03267-547">Requirement</span></span> | <span data-ttu-id="03267-548">值</span><span class="sxs-lookup"><span data-stu-id="03267-548">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="03267-549">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-549">Name</span></span>              | <span data-ttu-id="03267-550">secP521r1</span><span class="sxs-lookup"><span data-stu-id="03267-550">secP521r1</span></span>                                                                       |
| <span data-ttu-id="03267-551">標準</span><span class="sxs-lookup"><span data-stu-id="03267-551">Standard</span></span>          | [<span data-ttu-id="03267-552">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="03267-552">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="03267-553">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-553">Key size (bits)</span></span>   | <span data-ttu-id="03267-554">521</span><span class="sxs-lookup"><span data-stu-id="03267-554">521</span></span>                                                                             |
| <span data-ttu-id="03267-555">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-555">TLS capable</span></span>       | <span data-ttu-id="03267-556">Yes</span><span class="sxs-lookup"><span data-stu-id="03267-556">Yes</span></span>                                                                             |
| <span data-ttu-id="03267-557">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-557">Object identifier</span></span> | <span data-ttu-id="03267-558">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="03267-558">1.3.132.0.35</span></span>                                                                    |



 

<span data-ttu-id="03267-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT \_ ECC \_ 曲線 \_ WTLS12**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT\_ECC\_CURVE\_WTLS12**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-560">需求</span><span class="sxs-lookup"><span data-stu-id="03267-560">Requirement</span></span> | <span data-ttu-id="03267-561">值</span><span class="sxs-lookup"><span data-stu-id="03267-561">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="03267-562">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-562">Name</span></span>              | <span data-ttu-id="03267-563">wtls12</span><span class="sxs-lookup"><span data-stu-id="03267-563">wtls12</span></span>       |
| <span data-ttu-id="03267-564">標準</span><span class="sxs-lookup"><span data-stu-id="03267-564">Standard</span></span>          | <span data-ttu-id="03267-565">WTLS</span><span class="sxs-lookup"><span data-stu-id="03267-565">WTLS</span></span>         |
| <span data-ttu-id="03267-566">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-566">Key size (bits)</span></span>   | <span data-ttu-id="03267-567">224</span><span class="sxs-lookup"><span data-stu-id="03267-567">224</span></span>          |
| <span data-ttu-id="03267-568">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-568">TLS capable</span></span>       | <span data-ttu-id="03267-569">No</span><span class="sxs-lookup"><span data-stu-id="03267-569">No</span></span>           |
| <span data-ttu-id="03267-570">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-570">Object identifier</span></span> | <span data-ttu-id="03267-571">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="03267-571">1.3.132.0.33</span></span> |



 

<span data-ttu-id="03267-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT \_ ECC \_ 曲線 \_ WTLS7**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT\_ECC\_CURVE\_WTLS7**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-573">需求</span><span class="sxs-lookup"><span data-stu-id="03267-573">Requirement</span></span> | <span data-ttu-id="03267-574">值</span><span class="sxs-lookup"><span data-stu-id="03267-574">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="03267-575">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-575">Name</span></span>              | <span data-ttu-id="03267-576">wtls7</span><span class="sxs-lookup"><span data-stu-id="03267-576">wtls7</span></span>        |
| <span data-ttu-id="03267-577">標準</span><span class="sxs-lookup"><span data-stu-id="03267-577">Standard</span></span>          | <span data-ttu-id="03267-578">WTLS</span><span class="sxs-lookup"><span data-stu-id="03267-578">WTLS</span></span>         |
| <span data-ttu-id="03267-579">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-579">Key size (bits)</span></span>   | <span data-ttu-id="03267-580">160</span><span class="sxs-lookup"><span data-stu-id="03267-580">160</span></span>          |
| <span data-ttu-id="03267-581">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-581">TLS capable</span></span>       | <span data-ttu-id="03267-582">No</span><span class="sxs-lookup"><span data-stu-id="03267-582">No</span></span>           |
| <span data-ttu-id="03267-583">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-583">Object identifier</span></span> | <span data-ttu-id="03267-584">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="03267-584">1.3.132.0.30</span></span> |



 

<span data-ttu-id="03267-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ECC \_ 曲線 \_ WTLS9**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT\_ECC\_CURVE\_WTLS9** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-586">需求</span><span class="sxs-lookup"><span data-stu-id="03267-586">Requirement</span></span> | <span data-ttu-id="03267-587">值</span><span class="sxs-lookup"><span data-stu-id="03267-587">Value</span></span> |
|-------------------|---------------|
| <span data-ttu-id="03267-588">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-588">Name</span></span>              | <span data-ttu-id="03267-589">wtls9</span><span class="sxs-lookup"><span data-stu-id="03267-589">wtls9</span></span>         |
| <span data-ttu-id="03267-590">標準</span><span class="sxs-lookup"><span data-stu-id="03267-590">Standard</span></span>          | <span data-ttu-id="03267-591">WTLS</span><span class="sxs-lookup"><span data-stu-id="03267-591">WTLS</span></span>          |
| <span data-ttu-id="03267-592">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-592">Key size (bits)</span></span>   | <span data-ttu-id="03267-593">160</span><span class="sxs-lookup"><span data-stu-id="03267-593">160</span></span>           |
| <span data-ttu-id="03267-594">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-594">TLS capable</span></span>       | <span data-ttu-id="03267-595">No</span><span class="sxs-lookup"><span data-stu-id="03267-595">No</span></span>            |
| <span data-ttu-id="03267-596">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-596">Object identifier</span></span> | <span data-ttu-id="03267-597">2.23.43.1.4.9</span><span class="sxs-lookup"><span data-stu-id="03267-597">2.23.43.1.4.9</span></span> |



 

<span data-ttu-id="03267-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P192V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT\_ECC\_CURVE\_X962P192V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-599">需求</span><span class="sxs-lookup"><span data-stu-id="03267-599">Requirement</span></span> | <span data-ttu-id="03267-600">值</span><span class="sxs-lookup"><span data-stu-id="03267-600">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="03267-601">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-601">Name</span></span>              | <span data-ttu-id="03267-602">x962P192v1</span><span class="sxs-lookup"><span data-stu-id="03267-602">x962P192v1</span></span>          |
| <span data-ttu-id="03267-603">標準</span><span class="sxs-lookup"><span data-stu-id="03267-603">Standard</span></span>          | <span data-ttu-id="03267-604">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="03267-604">ANSI X9.62</span></span>          |
| <span data-ttu-id="03267-605">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-605">Key size (bits)</span></span>   | <span data-ttu-id="03267-606">192</span><span class="sxs-lookup"><span data-stu-id="03267-606">192</span></span>                 |
| <span data-ttu-id="03267-607">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-607">TLS capable</span></span>       | <span data-ttu-id="03267-608">No</span><span class="sxs-lookup"><span data-stu-id="03267-608">No</span></span>                  |
| <span data-ttu-id="03267-609">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-609">Object identifier</span></span> | <span data-ttu-id="03267-610">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="03267-610">1.2.840.10045.3.1.1</span></span> |



 

<span data-ttu-id="03267-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P192V2**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P192V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-612">需求</span><span class="sxs-lookup"><span data-stu-id="03267-612">Requirement</span></span> | <span data-ttu-id="03267-613">值</span><span class="sxs-lookup"><span data-stu-id="03267-613">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="03267-614">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-614">Name</span></span>              | <span data-ttu-id="03267-615">x962P192v2</span><span class="sxs-lookup"><span data-stu-id="03267-615">x962P192v2</span></span>          |
| <span data-ttu-id="03267-616">標準</span><span class="sxs-lookup"><span data-stu-id="03267-616">Standard</span></span>          | <span data-ttu-id="03267-617">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="03267-617">ANSI X9.62</span></span>          |
| <span data-ttu-id="03267-618">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-618">Key size (bits)</span></span>   | <span data-ttu-id="03267-619">192</span><span class="sxs-lookup"><span data-stu-id="03267-619">192</span></span>                 |
| <span data-ttu-id="03267-620">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-620">TLS capable</span></span>       | <span data-ttu-id="03267-621">No</span><span class="sxs-lookup"><span data-stu-id="03267-621">No</span></span>                  |
| <span data-ttu-id="03267-622">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-622">Object identifier</span></span> | <span data-ttu-id="03267-623">1.2.840.10045.3.1.2</span><span class="sxs-lookup"><span data-stu-id="03267-623">1.2.840.10045.3.1.2</span></span> |



 

<span data-ttu-id="03267-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P192V3**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT\_ECC\_CURVE\_X962P192V3**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-625">需求</span><span class="sxs-lookup"><span data-stu-id="03267-625">Requirement</span></span> | <span data-ttu-id="03267-626">值</span><span class="sxs-lookup"><span data-stu-id="03267-626">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="03267-627">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-627">Name</span></span>              | <span data-ttu-id="03267-628">x962P192v3</span><span class="sxs-lookup"><span data-stu-id="03267-628">x962P192v3</span></span>          |
| <span data-ttu-id="03267-629">標準</span><span class="sxs-lookup"><span data-stu-id="03267-629">Standard</span></span>          | <span data-ttu-id="03267-630">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="03267-630">ANSI X9.62</span></span>          |
| <span data-ttu-id="03267-631">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-631">Key size (bits)</span></span>   | <span data-ttu-id="03267-632">192</span><span class="sxs-lookup"><span data-stu-id="03267-632">192</span></span>                 |
| <span data-ttu-id="03267-633">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-633">TLS capable</span></span>       | <span data-ttu-id="03267-634">No</span><span class="sxs-lookup"><span data-stu-id="03267-634">No</span></span>                  |
| <span data-ttu-id="03267-635">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-635">Object identifier</span></span> | <span data-ttu-id="03267-636">1.2.840.10045.3.1.3</span><span class="sxs-lookup"><span data-stu-id="03267-636">1.2.840.10045.3.1.3</span></span> |



 

<span data-ttu-id="03267-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-638">需求</span><span class="sxs-lookup"><span data-stu-id="03267-638">Requirement</span></span> | <span data-ttu-id="03267-639">值</span><span class="sxs-lookup"><span data-stu-id="03267-639">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="03267-640">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-640">Name</span></span>              | <span data-ttu-id="03267-641">x962P239v1</span><span class="sxs-lookup"><span data-stu-id="03267-641">x962P239v1</span></span>          |
| <span data-ttu-id="03267-642">標準</span><span class="sxs-lookup"><span data-stu-id="03267-642">Standard</span></span>          | <span data-ttu-id="03267-643">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="03267-643">ANSI X9.62</span></span>          |
| <span data-ttu-id="03267-644">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-644">Key size (bits)</span></span>   | <span data-ttu-id="03267-645">239</span><span class="sxs-lookup"><span data-stu-id="03267-645">239</span></span>                 |
| <span data-ttu-id="03267-646">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-646">TLS capable</span></span>       | <span data-ttu-id="03267-647">No</span><span class="sxs-lookup"><span data-stu-id="03267-647">No</span></span>                  |
| <span data-ttu-id="03267-648">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-648">Object identifier</span></span> | <span data-ttu-id="03267-649">1.2.840.10045.3.1.4</span><span class="sxs-lookup"><span data-stu-id="03267-649">1.2.840.10045.3.1.4</span></span> |



 

<span data-ttu-id="03267-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V2**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-651">需求</span><span class="sxs-lookup"><span data-stu-id="03267-651">Requirement</span></span> | <span data-ttu-id="03267-652">值</span><span class="sxs-lookup"><span data-stu-id="03267-652">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="03267-653">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-653">Name</span></span>              | <span data-ttu-id="03267-654">x962P239v2</span><span class="sxs-lookup"><span data-stu-id="03267-654">x962P239v2</span></span>          |
| <span data-ttu-id="03267-655">標準</span><span class="sxs-lookup"><span data-stu-id="03267-655">Standard</span></span>          | <span data-ttu-id="03267-656">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="03267-656">ANSI X9.62</span></span>          |
| <span data-ttu-id="03267-657">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-657">Key size (bits)</span></span>   | <span data-ttu-id="03267-658">239</span><span class="sxs-lookup"><span data-stu-id="03267-658">239</span></span>                 |
| <span data-ttu-id="03267-659">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-659">TLS capable</span></span>       | <span data-ttu-id="03267-660">No</span><span class="sxs-lookup"><span data-stu-id="03267-660">No</span></span>                  |
| <span data-ttu-id="03267-661">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-661">Object identifier</span></span> | <span data-ttu-id="03267-662">1.2.840.10045.3.1.5</span><span class="sxs-lookup"><span data-stu-id="03267-662">1.2.840.10045.3.1.5</span></span> |



 

<span data-ttu-id="03267-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V3**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V3** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-664">需求</span><span class="sxs-lookup"><span data-stu-id="03267-664">Requirement</span></span> | <span data-ttu-id="03267-665">值</span><span class="sxs-lookup"><span data-stu-id="03267-665">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="03267-666">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-666">Name</span></span>              | <span data-ttu-id="03267-667">x962P239v3</span><span class="sxs-lookup"><span data-stu-id="03267-667">x962P239v3</span></span>          |
| <span data-ttu-id="03267-668">標準</span><span class="sxs-lookup"><span data-stu-id="03267-668">Standard</span></span>          | <span data-ttu-id="03267-669">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="03267-669">ANSI X9.62</span></span>          |
| <span data-ttu-id="03267-670">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-670">Key size (bits)</span></span>   | <span data-ttu-id="03267-671">239</span><span class="sxs-lookup"><span data-stu-id="03267-671">239</span></span>                 |
| <span data-ttu-id="03267-672">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-672">TLS capable</span></span>       | <span data-ttu-id="03267-673">No</span><span class="sxs-lookup"><span data-stu-id="03267-673">No</span></span>                  |
| <span data-ttu-id="03267-674">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-674">Object identifier</span></span> | <span data-ttu-id="03267-675">1.2.840.10045.3.1.6</span><span class="sxs-lookup"><span data-stu-id="03267-675">1.2.840.10045.3.1.6</span></span> |



 

<span data-ttu-id="03267-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P256V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="03267-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT\_ECC\_CURVE\_X962P256V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="03267-677">需求</span><span class="sxs-lookup"><span data-stu-id="03267-677">Requirement</span></span> | <span data-ttu-id="03267-678">值</span><span class="sxs-lookup"><span data-stu-id="03267-678">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="03267-679">名稱</span><span class="sxs-lookup"><span data-stu-id="03267-679">Name</span></span>              | <span data-ttu-id="03267-680">x962P256v1</span><span class="sxs-lookup"><span data-stu-id="03267-680">x962P256v1</span></span>          |
| <span data-ttu-id="03267-681">標準</span><span class="sxs-lookup"><span data-stu-id="03267-681">Standard</span></span>          | <span data-ttu-id="03267-682">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="03267-682">ANSI X9.62</span></span>          |
| <span data-ttu-id="03267-683">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="03267-683">Key size (bits)</span></span>   | <span data-ttu-id="03267-684">256</span><span class="sxs-lookup"><span data-stu-id="03267-684">256</span></span>                 |
| <span data-ttu-id="03267-685">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="03267-685">TLS capable</span></span>       | <span data-ttu-id="03267-686">No</span><span class="sxs-lookup"><span data-stu-id="03267-686">No</span></span>                  |
| <span data-ttu-id="03267-687">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="03267-687">Object identifier</span></span> | <span data-ttu-id="03267-688">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="03267-688">1.2.840.10045.3.1.7</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="03267-689">備註</span><span class="sxs-lookup"><span data-stu-id="03267-689">Remarks</span></span>

<span data-ttu-id="03267-690">若要使用命名曲線，請使用 **BCRYPT \_ ECDSA \_ 演算法** 或 **BCRYPT \_ ECDH \_ 演算法** 來呼叫 [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) ，作為演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="03267-690">To use a named curve, call [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) using either the **BCRYPT\_ECDSA\_ALGORITHM** or the **BCRYPT\_ECDH\_ALGORITHM** as the algorithm ID.</span></span> <span data-ttu-id="03267-691">然後，呼叫 [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) ，並將 [ **BCRYPT \_ ECC \_ 曲線 \_ 名稱** ] 屬性設定為上述其中一個曲線或任何已在電腦上註冊的命名曲線，如命令所示 `certutil -displayEccCurve` 。</span><span class="sxs-lookup"><span data-stu-id="03267-691">Then, call [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) and set the **BCRYPT\_ECC\_CURVE\_NAME** property to one of the above curves or any named curves registered on the computer as shown by the `certutil -displayEccCurve` command.</span></span>

## <a name="requirements"></a><span data-ttu-id="03267-692">規格需求</span><span class="sxs-lookup"><span data-stu-id="03267-692">Requirements</span></span>



| <span data-ttu-id="03267-693">需求</span><span class="sxs-lookup"><span data-stu-id="03267-693">Requirement</span></span> | <span data-ttu-id="03267-694">值</span><span class="sxs-lookup"><span data-stu-id="03267-694">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="03267-695">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03267-695">Minimum supported client</span></span><br/> | <span data-ttu-id="03267-696">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03267-696">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="03267-697">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03267-697">Minimum supported server</span></span><br/> | <span data-ttu-id="03267-698">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="03267-698">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="03267-699">標頭</span><span class="sxs-lookup"><span data-stu-id="03267-699">Header</span></span><br/>                   | <dl> <span data-ttu-id="03267-700"><dt>Bcrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="03267-700"><dt>Bcrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03267-701">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03267-701">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03267-702">**BCryptOpenAlgorithmProvider**</span><span class="sxs-lookup"><span data-stu-id="03267-702">**BCryptOpenAlgorithmProvider**</span></span>](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[<span data-ttu-id="03267-703">**NCryptCreatePersistedKey**</span><span class="sxs-lookup"><span data-stu-id="03267-703">**NCryptCreatePersistedKey**</span></span>](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




