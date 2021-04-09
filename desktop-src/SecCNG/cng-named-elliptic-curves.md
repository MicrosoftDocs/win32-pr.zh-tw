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
# <a name="cng-named-elliptic-curves"></a><span data-ttu-id="13c30-103">CNG 命名橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="13c30-103">CNG Named Elliptic Curves</span></span>

<span data-ttu-id="13c30-104">從 Windows 10 開始，CNG 提供下列命名橢圓曲線的支援 (ANSI X x9.62、X 9.63、FIPS 186-2) 。</span><span class="sxs-lookup"><span data-stu-id="13c30-104">Beginning in Windows 10, CNG provides support for the following named elliptic curves (ANSI X9.62, X9.63, FIPS 186-2).</span></span>

<dl> <span data-ttu-id="13c30-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT \_ ECC \_ 曲線 \_ 25519**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT\_ECC\_CURVE\_25519**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-106">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-106">Requirement</span></span> | <span data-ttu-id="13c30-107">值</span><span class="sxs-lookup"><span data-stu-id="13c30-107">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="13c30-108">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-108">Name</span></span>              | <span data-ttu-id="13c30-109">curve25519</span><span class="sxs-lookup"><span data-stu-id="13c30-109">curve25519</span></span>                                                  |
| <span data-ttu-id="13c30-110">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-110">Standard</span></span>          | [<span data-ttu-id="13c30-111">曲線25519</span><span class="sxs-lookup"><span data-stu-id="13c30-111">Curve 25519</span></span>](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| <span data-ttu-id="13c30-112">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-112">Key size (bits)</span></span>   | <span data-ttu-id="13c30-113">255</span><span class="sxs-lookup"><span data-stu-id="13c30-113">255</span></span>                                                         |
| <span data-ttu-id="13c30-114">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-114">TLS capable</span></span>       |                                                             |
| <span data-ttu-id="13c30-115">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-115">Object identifier</span></span> | <span data-ttu-id="13c30-116">無</span><span class="sxs-lookup"><span data-stu-id="13c30-116">None</span></span>                                                        |



 

<span data-ttu-id="13c30-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-118">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-118">Requirement</span></span> | <span data-ttu-id="13c30-119">值</span><span class="sxs-lookup"><span data-stu-id="13c30-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-120">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-120">Name</span></span>              | <span data-ttu-id="13c30-121">brainpoolP160r1</span><span class="sxs-lookup"><span data-stu-id="13c30-121">brainpoolP160r1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-122">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-122">Standard</span></span>          | [<span data-ttu-id="13c30-123">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-123">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-124">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-124">Key size (bits)</span></span>   | <span data-ttu-id="13c30-125">160</span><span class="sxs-lookup"><span data-stu-id="13c30-125">160</span></span>                                                                                                               |
| <span data-ttu-id="13c30-126">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-126">TLS capable</span></span>       | <span data-ttu-id="13c30-127">No</span><span class="sxs-lookup"><span data-stu-id="13c30-127">No</span></span>                                                                                                                |
| <span data-ttu-id="13c30-128">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-128">Object identifier</span></span> | <span data-ttu-id="13c30-129">1.3.36.3.3.2.8.1.1.1</span><span class="sxs-lookup"><span data-stu-id="13c30-129">1.3.36.3.3.2.8.1.1.1</span></span>                                                                                              |



 

<span data-ttu-id="13c30-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ BRAINPOOLP160T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-131">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-131">Requirement</span></span> | <span data-ttu-id="13c30-132">值</span><span class="sxs-lookup"><span data-stu-id="13c30-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-133">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-133">Name</span></span>              | <span data-ttu-id="13c30-134">brainpoolP160t1</span><span class="sxs-lookup"><span data-stu-id="13c30-134">brainpoolP160t1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-135">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-135">Standard</span></span>          | [<span data-ttu-id="13c30-136">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-136">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-137">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-137">Key size (bits)</span></span>   | <span data-ttu-id="13c30-138">160</span><span class="sxs-lookup"><span data-stu-id="13c30-138">160</span></span>                                                                                                               |
| <span data-ttu-id="13c30-139">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-139">TLS capable</span></span>       | <span data-ttu-id="13c30-140">No</span><span class="sxs-lookup"><span data-stu-id="13c30-140">No</span></span>                                                                                                                |
| <span data-ttu-id="13c30-141">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-141">Object identifier</span></span> | <span data-ttu-id="13c30-142">1.3.36.3.3.2.8.1.1.2</span><span class="sxs-lookup"><span data-stu-id="13c30-142">1.3.36.3.3.2.8.1.1.2</span></span>                                                                                              |



 

<span data-ttu-id="13c30-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP192R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-144">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-144">Requirement</span></span> | <span data-ttu-id="13c30-145">值</span><span class="sxs-lookup"><span data-stu-id="13c30-145">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-146">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-146">Name</span></span>              | <span data-ttu-id="13c30-147">brainpoolP192r1</span><span class="sxs-lookup"><span data-stu-id="13c30-147">brainpoolP192r1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-148">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-148">Standard</span></span>          | [<span data-ttu-id="13c30-149">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-149">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-150">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-150">Key size (bits)</span></span>   | <span data-ttu-id="13c30-151">192</span><span class="sxs-lookup"><span data-stu-id="13c30-151">192</span></span>                                                                                                               |
| <span data-ttu-id="13c30-152">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-152">TLS capable</span></span>       | <span data-ttu-id="13c30-153">No</span><span class="sxs-lookup"><span data-stu-id="13c30-153">No</span></span>                                                                                                                |
| <span data-ttu-id="13c30-154">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-154">Object identifier</span></span> | <span data-ttu-id="13c30-155">1.3.36.3.3.2.8.1.1.3</span><span class="sxs-lookup"><span data-stu-id="13c30-155">1.3.36.3.3.2.8.1.1.3</span></span>                                                                                              |



 

<span data-ttu-id="13c30-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP192T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-157">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-157">Requirement</span></span> | <span data-ttu-id="13c30-158">值</span><span class="sxs-lookup"><span data-stu-id="13c30-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-159">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-159">Name</span></span>              | <span data-ttu-id="13c30-160">brainpoolP192t1</span><span class="sxs-lookup"><span data-stu-id="13c30-160">brainpoolP192t1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-161">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-161">Standard</span></span>          | [<span data-ttu-id="13c30-162">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-162">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-163">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-163">Key size (bits)</span></span>   | <span data-ttu-id="13c30-164">192</span><span class="sxs-lookup"><span data-stu-id="13c30-164">192</span></span>                                                                                                               |
| <span data-ttu-id="13c30-165">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-165">TLS capable</span></span>       | <span data-ttu-id="13c30-166">No</span><span class="sxs-lookup"><span data-stu-id="13c30-166">No</span></span>                                                                                                                |
| <span data-ttu-id="13c30-167">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-167">Object identifier</span></span> | <span data-ttu-id="13c30-168">1.3.36.3.3.2.8.1.1.4</span><span class="sxs-lookup"><span data-stu-id="13c30-168">1.3.36.3.3.2.8.1.1.4</span></span>                                                                                              |



 

<span data-ttu-id="13c30-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP224R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-170">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-170">Requirement</span></span> | <span data-ttu-id="13c30-171">值</span><span class="sxs-lookup"><span data-stu-id="13c30-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-172">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-172">Name</span></span>              | <span data-ttu-id="13c30-173">brainpoolP224r1</span><span class="sxs-lookup"><span data-stu-id="13c30-173">brainpoolP224r1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-174">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-174">Standard</span></span>          | [<span data-ttu-id="13c30-175">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-175">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-176">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-176">Key size (bits)</span></span>   | <span data-ttu-id="13c30-177">224</span><span class="sxs-lookup"><span data-stu-id="13c30-177">224</span></span>                                                                                                               |
| <span data-ttu-id="13c30-178">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-178">TLS capable</span></span>       | <span data-ttu-id="13c30-179">No</span><span class="sxs-lookup"><span data-stu-id="13c30-179">No</span></span>                                                                                                                |
| <span data-ttu-id="13c30-180">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-180">Object identifier</span></span> | <span data-ttu-id="13c30-181">1.3.36.3.3.2.8.1.1.5</span><span class="sxs-lookup"><span data-stu-id="13c30-181">1.3.36.3.3.2.8.1.1.5</span></span>                                                                                              |



 

<span data-ttu-id="13c30-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP224T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-183">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-183">Requirement</span></span> | <span data-ttu-id="13c30-184">值</span><span class="sxs-lookup"><span data-stu-id="13c30-184">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-185">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-185">Name</span></span>              | <span data-ttu-id="13c30-186">brainpoolP224t1</span><span class="sxs-lookup"><span data-stu-id="13c30-186">brainpoolP224t1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-187">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-187">Standard</span></span>          | [<span data-ttu-id="13c30-188">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-188">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-189">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-189">Key size (bits)</span></span>   | <span data-ttu-id="13c30-190">224</span><span class="sxs-lookup"><span data-stu-id="13c30-190">224</span></span>                                                                                                               |
| <span data-ttu-id="13c30-191">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-191">TLS capable</span></span>       | <span data-ttu-id="13c30-192">No</span><span class="sxs-lookup"><span data-stu-id="13c30-192">No</span></span>                                                                                                                |
| <span data-ttu-id="13c30-193">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-193">Object identifier</span></span> | <span data-ttu-id="13c30-194">1.3.36.3.3.2.8.1.1.6</span><span class="sxs-lookup"><span data-stu-id="13c30-194">1.3.36.3.3.2.8.1.1.6</span></span>                                                                                              |



 

<span data-ttu-id="13c30-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP256R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-196">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-196">Requirement</span></span> | <span data-ttu-id="13c30-197">值</span><span class="sxs-lookup"><span data-stu-id="13c30-197">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-198">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-198">Name</span></span>              | <span data-ttu-id="13c30-199">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="13c30-199">brainpoolP256r1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-200">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-200">Standard</span></span>          | [<span data-ttu-id="13c30-201">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-201">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-202">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-202">Key size (bits)</span></span>   | <span data-ttu-id="13c30-203">256</span><span class="sxs-lookup"><span data-stu-id="13c30-203">256</span></span>                                                                                                               |
| <span data-ttu-id="13c30-204">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-204">TLS capable</span></span>       | <span data-ttu-id="13c30-205">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-205">Yes</span></span>                                                                                                               |
| <span data-ttu-id="13c30-206">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-206">Object identifier</span></span> | <span data-ttu-id="13c30-207">1.3.36.3.3.2.8.1.1.7</span><span class="sxs-lookup"><span data-stu-id="13c30-207">1.3.36.3.3.2.8.1.1.7</span></span>                                                                                              |



 

<span data-ttu-id="13c30-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP256T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-209">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-209">Requirement</span></span> | <span data-ttu-id="13c30-210">值</span><span class="sxs-lookup"><span data-stu-id="13c30-210">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-211">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-211">Name</span></span>              | <span data-ttu-id="13c30-212">brainpoolP256t1</span><span class="sxs-lookup"><span data-stu-id="13c30-212">brainpoolP256t1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-213">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-213">Standard</span></span>          | [<span data-ttu-id="13c30-214">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-214">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-215">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-215">Key size (bits)</span></span>   | <span data-ttu-id="13c30-216">256</span><span class="sxs-lookup"><span data-stu-id="13c30-216">256</span></span>                                                                                                               |
| <span data-ttu-id="13c30-217">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-217">TLS capable</span></span>       | <span data-ttu-id="13c30-218">No</span><span class="sxs-lookup"><span data-stu-id="13c30-218">No</span></span>                                                                                                                |
| <span data-ttu-id="13c30-219">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-219">Object identifier</span></span> | <span data-ttu-id="13c30-220">1.3.36.3.3.2.8.1.1.8</span><span class="sxs-lookup"><span data-stu-id="13c30-220">1.3.36.3.3.2.8.1.1.8</span></span>                                                                                              |



 

<span data-ttu-id="13c30-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP320R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP320R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-222">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-222">Requirement</span></span> | <span data-ttu-id="13c30-223">值</span><span class="sxs-lookup"><span data-stu-id="13c30-223">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-224">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-224">Name</span></span>              | <span data-ttu-id="13c30-225">brainpoolP320r1</span><span class="sxs-lookup"><span data-stu-id="13c30-225">brainpoolP320r1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-226">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-226">Standard</span></span>          | [<span data-ttu-id="13c30-227">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-227">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-228">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-228">Key size (bits)</span></span>   | <span data-ttu-id="13c30-229">320</span><span class="sxs-lookup"><span data-stu-id="13c30-229">320</span></span>                                                                                                               |
| <span data-ttu-id="13c30-230">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-230">TLS capable</span></span>       | <span data-ttu-id="13c30-231">No</span><span class="sxs-lookup"><span data-stu-id="13c30-231">No</span></span>                                                                                                                |
| <span data-ttu-id="13c30-232">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-232">Object identifier</span></span> | <span data-ttu-id="13c30-233">1.3.36.3.3.2.8.1.1.9</span><span class="sxs-lookup"><span data-stu-id="13c30-233">1.3.36.3.3.2.8.1.1.9</span></span>                                                                                              |



 

<span data-ttu-id="13c30-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP32 0T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP32 0T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-235">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-235">Requirement</span></span> | <span data-ttu-id="13c30-236">值</span><span class="sxs-lookup"><span data-stu-id="13c30-236">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-237">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-237">Name</span></span>              | <span data-ttu-id="13c30-238">brainpoolP320t1</span><span class="sxs-lookup"><span data-stu-id="13c30-238">brainpoolP320t1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-239">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-239">Standard</span></span>          | [<span data-ttu-id="13c30-240">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-240">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-241">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-241">Key size (bits)</span></span>   | <span data-ttu-id="13c30-242">320</span><span class="sxs-lookup"><span data-stu-id="13c30-242">320</span></span>                                                                                                               |
| <span data-ttu-id="13c30-243">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-243">TLS capable</span></span>       | <span data-ttu-id="13c30-244">No</span><span class="sxs-lookup"><span data-stu-id="13c30-244">No</span></span>                                                                                                                |
| <span data-ttu-id="13c30-245">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-245">Object identifier</span></span> | <span data-ttu-id="13c30-246">1.3.36.3.3.2.8.1.1.10</span><span class="sxs-lookup"><span data-stu-id="13c30-246">1.3.36.3.3.2.8.1.1.10</span></span>                                                                                             |



 

<span data-ttu-id="13c30-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ BRAINPOOLP384R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-248">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-248">Requirement</span></span> | <span data-ttu-id="13c30-249">值</span><span class="sxs-lookup"><span data-stu-id="13c30-249">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-250">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-250">Name</span></span>              | <span data-ttu-id="13c30-251">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="13c30-251">brainpoolP384r1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-252">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-252">Standard</span></span>          | [<span data-ttu-id="13c30-253">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-253">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-254">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-254">Key size (bits)</span></span>   | <span data-ttu-id="13c30-255">384</span><span class="sxs-lookup"><span data-stu-id="13c30-255">384</span></span>                                                                                                               |
| <span data-ttu-id="13c30-256">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-256">TLS capable</span></span>       | <span data-ttu-id="13c30-257">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-257">Yes</span></span>                                                                                                               |
| <span data-ttu-id="13c30-258">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-258">Object identifier</span></span> | <span data-ttu-id="13c30-259">1.3.36.3.3.2.8.1.1.11</span><span class="sxs-lookup"><span data-stu-id="13c30-259">1.3.36.3.3.2.8.1.1.11</span></span>                                                                                             |



 

<span data-ttu-id="13c30-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP384T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-261">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-261">Requirement</span></span> | <span data-ttu-id="13c30-262">值</span><span class="sxs-lookup"><span data-stu-id="13c30-262">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-263">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-263">Name</span></span>              | <span data-ttu-id="13c30-264">brainpoolP384t1</span><span class="sxs-lookup"><span data-stu-id="13c30-264">brainpoolP384t1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-265">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-265">Standard</span></span>          | [<span data-ttu-id="13c30-266">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-266">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-267">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-267">Key size (bits)</span></span>   | <span data-ttu-id="13c30-268">384</span><span class="sxs-lookup"><span data-stu-id="13c30-268">384</span></span>                                                                                                               |
| <span data-ttu-id="13c30-269">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-269">TLS capable</span></span>       | <span data-ttu-id="13c30-270">No</span><span class="sxs-lookup"><span data-stu-id="13c30-270">No</span></span>                                                                                                                |
| <span data-ttu-id="13c30-271">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-271">Object identifier</span></span> | <span data-ttu-id="13c30-272">1.3.36.3.3.2.8.1.1.12</span><span class="sxs-lookup"><span data-stu-id="13c30-272">1.3.36.3.3.2.8.1.1.12</span></span>                                                                                             |



 

<span data-ttu-id="13c30-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP512R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-274">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-274">Requirement</span></span> | <span data-ttu-id="13c30-275">值</span><span class="sxs-lookup"><span data-stu-id="13c30-275">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-276">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-276">Name</span></span>              | <span data-ttu-id="13c30-277">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="13c30-277">brainpoolP512r1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-278">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-278">Standard</span></span>          | [<span data-ttu-id="13c30-279">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-279">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-280">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-280">Key size (bits)</span></span>   | <span data-ttu-id="13c30-281">512</span><span class="sxs-lookup"><span data-stu-id="13c30-281">512</span></span>                                                                                                               |
| <span data-ttu-id="13c30-282">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-282">TLS capable</span></span>       | <span data-ttu-id="13c30-283">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-283">Yes</span></span>                                                                                                               |
| <span data-ttu-id="13c30-284">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-284">Object identifier</span></span> | <span data-ttu-id="13c30-285">1.3.36.3.3.2.8.1.1.13</span><span class="sxs-lookup"><span data-stu-id="13c30-285">1.3.36.3.3.2.8.1.1.13</span></span>                                                                                             |



 

<span data-ttu-id="13c30-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP512T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-287">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-287">Requirement</span></span> | <span data-ttu-id="13c30-288">值</span><span class="sxs-lookup"><span data-stu-id="13c30-288">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-289">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-289">Name</span></span>              | <span data-ttu-id="13c30-290">brainpoolP512t1</span><span class="sxs-lookup"><span data-stu-id="13c30-290">brainpoolP512t1</span></span>                                                                                                   |
| <span data-ttu-id="13c30-291">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-291">Standard</span></span>          | [<span data-ttu-id="13c30-292">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="13c30-292">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="13c30-293">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-293">Key size (bits)</span></span>   | <span data-ttu-id="13c30-294">512</span><span class="sxs-lookup"><span data-stu-id="13c30-294">512</span></span>                                                                                                               |
| <span data-ttu-id="13c30-295">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-295">TLS capable</span></span>       | <span data-ttu-id="13c30-296">No</span><span class="sxs-lookup"><span data-stu-id="13c30-296">No</span></span>                                                                                                                |
| <span data-ttu-id="13c30-297">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-297">Object identifier</span></span> | <span data-ttu-id="13c30-298">1.3.36.3.3.2.8.1.1.14</span><span class="sxs-lookup"><span data-stu-id="13c30-298">1.3.36.3.3.2.8.1.1.14</span></span>                                                                                             |



 

<span data-ttu-id="13c30-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ECC \_ 曲線 \_ EC192WAPI**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT\_ECC\_CURVE\_EC192WAPI** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-300">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-300">Requirement</span></span> | <span data-ttu-id="13c30-301">值</span><span class="sxs-lookup"><span data-stu-id="13c30-301">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="13c30-302">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-302">Name</span></span>              | <span data-ttu-id="13c30-303">ec192wapi</span><span class="sxs-lookup"><span data-stu-id="13c30-303">ec192wapi</span></span>                                                      |
| <span data-ttu-id="13c30-304">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-304">Standard</span></span>          | <span data-ttu-id="13c30-305">國際區域網路的中文標準 (GB 15629.11-2003) </span><span class="sxs-lookup"><span data-stu-id="13c30-305">Chinese National Standard for Wireless LANs (GB 15629.11-2003)</span></span> |
| <span data-ttu-id="13c30-306">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-306">Key size (bits)</span></span>   | <span data-ttu-id="13c30-307">192</span><span class="sxs-lookup"><span data-stu-id="13c30-307">192</span></span>                                                            |
| <span data-ttu-id="13c30-308">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-308">TLS capable</span></span>       | <span data-ttu-id="13c30-309">No</span><span class="sxs-lookup"><span data-stu-id="13c30-309">No</span></span>                                                             |
| <span data-ttu-id="13c30-310">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-310">Object identifier</span></span> | <span data-ttu-id="13c30-311">1.2.156.11235.1.1.2.1</span><span class="sxs-lookup"><span data-stu-id="13c30-311">1.2.156.11235.1.1.2.1</span></span>                                          |



 

<span data-ttu-id="13c30-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP192**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT\_ECC\_CURVE\_NISTP192**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-313">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-313">Requirement</span></span> | <span data-ttu-id="13c30-314">值</span><span class="sxs-lookup"><span data-stu-id="13c30-314">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-315">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-315">Name</span></span>              | <span data-ttu-id="13c30-316">nistP192</span><span class="sxs-lookup"><span data-stu-id="13c30-316">nistP192</span></span>                                                                                                                     |
| <span data-ttu-id="13c30-317">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-317">Standard</span></span>          | [<span data-ttu-id="13c30-318">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="13c30-318">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="13c30-319">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-319">Key size (bits)</span></span>   | <span data-ttu-id="13c30-320">192</span><span class="sxs-lookup"><span data-stu-id="13c30-320">192</span></span>                                                                                                                          |
| <span data-ttu-id="13c30-321">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-321">TLS capable</span></span>       | <span data-ttu-id="13c30-322">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-322">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="13c30-323">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-323">Object identifier</span></span> | <span data-ttu-id="13c30-324">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="13c30-324">1.2.840.10045.3.1.1</span></span>                                                                                                          |



 

<span data-ttu-id="13c30-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ECC \_ 曲線 \_ NISTP224**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT\_ECC\_CURVE\_NISTP224** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-326">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-326">Requirement</span></span> | <span data-ttu-id="13c30-327">值</span><span class="sxs-lookup"><span data-stu-id="13c30-327">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-328">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-328">Name</span></span>              | <span data-ttu-id="13c30-329">nistP224</span><span class="sxs-lookup"><span data-stu-id="13c30-329">nistP224</span></span>                                                                                                                     |
| <span data-ttu-id="13c30-330">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-330">Standard</span></span>          | [<span data-ttu-id="13c30-331">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="13c30-331">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="13c30-332">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-332">Key size (bits)</span></span>   | <span data-ttu-id="13c30-333">224</span><span class="sxs-lookup"><span data-stu-id="13c30-333">224</span></span>                                                                                                                          |
| <span data-ttu-id="13c30-334">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-334">TLS capable</span></span>       | <span data-ttu-id="13c30-335">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-335">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="13c30-336">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-336">Object identifier</span></span> | <span data-ttu-id="13c30-337">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="13c30-337">1.3.132.0.33</span></span>                                                                                                                 |



 

<span data-ttu-id="13c30-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP256**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT\_ECC\_CURVE\_NISTP256**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-339">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-339">Requirement</span></span> | <span data-ttu-id="13c30-340">值</span><span class="sxs-lookup"><span data-stu-id="13c30-340">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-341">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-341">Name</span></span>              | <span data-ttu-id="13c30-342">nistP256</span><span class="sxs-lookup"><span data-stu-id="13c30-342">nistP256</span></span>                                                                                                                     |
| <span data-ttu-id="13c30-343">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-343">Standard</span></span>          | [<span data-ttu-id="13c30-344">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="13c30-344">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="13c30-345">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-345">Key size (bits)</span></span>   | <span data-ttu-id="13c30-346">256</span><span class="sxs-lookup"><span data-stu-id="13c30-346">256</span></span>                                                                                                                          |
| <span data-ttu-id="13c30-347">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-347">TLS capable</span></span>       | <span data-ttu-id="13c30-348">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-348">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="13c30-349">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-349">Object identifier</span></span> | <span data-ttu-id="13c30-350">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="13c30-350">1.2.840.10045.3.1.7</span></span>                                                                                                          |



 

<span data-ttu-id="13c30-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ECC \_ 曲線 \_ NISTP384**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT\_ECC\_CURVE\_NISTP384** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-352">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-352">Requirement</span></span> | <span data-ttu-id="13c30-353">值</span><span class="sxs-lookup"><span data-stu-id="13c30-353">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-354">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-354">Name</span></span>              | <span data-ttu-id="13c30-355">nistP384</span><span class="sxs-lookup"><span data-stu-id="13c30-355">nistP384</span></span>                                                                                                                     |
| <span data-ttu-id="13c30-356">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-356">Standard</span></span>          | [<span data-ttu-id="13c30-357">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="13c30-357">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="13c30-358">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-358">Key size (bits)</span></span>   | <span data-ttu-id="13c30-359">384</span><span class="sxs-lookup"><span data-stu-id="13c30-359">384</span></span>                                                                                                                          |
| <span data-ttu-id="13c30-360">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-360">TLS capable</span></span>       | <span data-ttu-id="13c30-361">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-361">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="13c30-362">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-362">Object identifier</span></span> | <span data-ttu-id="13c30-363">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="13c30-363">1.3.132.0.34</span></span>                                                                                                                 |



 

<span data-ttu-id="13c30-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP521**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT\_ECC\_CURVE\_NISTP521**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-365">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-365">Requirement</span></span> | <span data-ttu-id="13c30-366">值</span><span class="sxs-lookup"><span data-stu-id="13c30-366">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-367">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-367">Name</span></span>              | <span data-ttu-id="13c30-368">nistP521</span><span class="sxs-lookup"><span data-stu-id="13c30-368">nistP521</span></span>                                                                                                                     |
| <span data-ttu-id="13c30-369">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-369">Standard</span></span>          | [<span data-ttu-id="13c30-370">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="13c30-370">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="13c30-371">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-371">Key size (bits)</span></span>   | <span data-ttu-id="13c30-372">521</span><span class="sxs-lookup"><span data-stu-id="13c30-372">521</span></span>                                                                                                                          |
| <span data-ttu-id="13c30-373">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-373">TLS capable</span></span>       | <span data-ttu-id="13c30-374">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-374">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="13c30-375">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-375">Object identifier</span></span> | <span data-ttu-id="13c30-376">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="13c30-376">1.3.132.0.35</span></span>                                                                                                                 |



 

<span data-ttu-id="13c30-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ NUMSP256T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP256T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-378">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-378">Requirement</span></span> | <span data-ttu-id="13c30-379">值</span><span class="sxs-lookup"><span data-stu-id="13c30-379">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-380">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-380">Name</span></span>              | <span data-ttu-id="13c30-381">numsP256t1</span><span class="sxs-lookup"><span data-stu-id="13c30-381">numsP256t1</span></span>                                                                                                                              |
| <span data-ttu-id="13c30-382">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-382">Standard</span></span>          | [<span data-ttu-id="13c30-383">MSR ECCLib 中的曲線選取和支援曲線參數規格</span><span class="sxs-lookup"><span data-stu-id="13c30-383">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="13c30-384">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-384">Key size (bits)</span></span>   | <span data-ttu-id="13c30-385">256</span><span class="sxs-lookup"><span data-stu-id="13c30-385">256</span></span>                                                                                                                                     |
| <span data-ttu-id="13c30-386">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-386">TLS capable</span></span>       | <span data-ttu-id="13c30-387">No</span><span class="sxs-lookup"><span data-stu-id="13c30-387">No</span></span>                                                                                                                                      |
| <span data-ttu-id="13c30-388">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-388">Object identifier</span></span> | <span data-ttu-id="13c30-389">無</span><span class="sxs-lookup"><span data-stu-id="13c30-389">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="13c30-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ NUMSP384T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP384T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-391">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-391">Requirement</span></span> | <span data-ttu-id="13c30-392">值</span><span class="sxs-lookup"><span data-stu-id="13c30-392">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-393">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-393">Name</span></span>              | <span data-ttu-id="13c30-394">numsP384t1</span><span class="sxs-lookup"><span data-stu-id="13c30-394">numsP384t1</span></span>                                                                                                                              |
| <span data-ttu-id="13c30-395">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-395">Standard</span></span>          | [<span data-ttu-id="13c30-396">MSR ECCLib 中的曲線選取和支援曲線參數規格</span><span class="sxs-lookup"><span data-stu-id="13c30-396">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="13c30-397">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-397">Key size (bits)</span></span>   | <span data-ttu-id="13c30-398">384</span><span class="sxs-lookup"><span data-stu-id="13c30-398">384</span></span>                                                                                                                                     |
| <span data-ttu-id="13c30-399">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-399">TLS capable</span></span>       | <span data-ttu-id="13c30-400">No</span><span class="sxs-lookup"><span data-stu-id="13c30-400">No</span></span>                                                                                                                                      |
| <span data-ttu-id="13c30-401">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-401">Object identifier</span></span> | <span data-ttu-id="13c30-402">無</span><span class="sxs-lookup"><span data-stu-id="13c30-402">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="13c30-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ NUMSP512T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT\_ECC\_CURVE\_NUMSP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-404">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-404">Requirement</span></span> | <span data-ttu-id="13c30-405">值</span><span class="sxs-lookup"><span data-stu-id="13c30-405">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-406">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-406">Name</span></span>              | <span data-ttu-id="13c30-407">numsP512t1</span><span class="sxs-lookup"><span data-stu-id="13c30-407">numsP512t1</span></span>                                                                                                                              |
| <span data-ttu-id="13c30-408">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-408">Standard</span></span>          | [<span data-ttu-id="13c30-409">MSR ECCLib 中的曲線選取和支援曲線參數規格</span><span class="sxs-lookup"><span data-stu-id="13c30-409">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="13c30-410">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-410">Key size (bits)</span></span>   | <span data-ttu-id="13c30-411">512</span><span class="sxs-lookup"><span data-stu-id="13c30-411">512</span></span>                                                                                                                                     |
| <span data-ttu-id="13c30-412">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-412">TLS capable</span></span>       | <span data-ttu-id="13c30-413">No</span><span class="sxs-lookup"><span data-stu-id="13c30-413">No</span></span>                                                                                                                                      |
| <span data-ttu-id="13c30-414">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-414">Object identifier</span></span> | <span data-ttu-id="13c30-415">無</span><span class="sxs-lookup"><span data-stu-id="13c30-415">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="13c30-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160K1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-417">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-417">Requirement</span></span> | <span data-ttu-id="13c30-418">值</span><span class="sxs-lookup"><span data-stu-id="13c30-418">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-419">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-419">Name</span></span>              | <span data-ttu-id="13c30-420">secP160k1</span><span class="sxs-lookup"><span data-stu-id="13c30-420">secP160k1</span></span>                                                                       |
| <span data-ttu-id="13c30-421">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-421">Standard</span></span>          | [<span data-ttu-id="13c30-422">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="13c30-422">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="13c30-423">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-423">Key size (bits)</span></span>   | <span data-ttu-id="13c30-424">160</span><span class="sxs-lookup"><span data-stu-id="13c30-424">160</span></span>                                                                             |
| <span data-ttu-id="13c30-425">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-425">TLS capable</span></span>       | <span data-ttu-id="13c30-426">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-426">Yes</span></span>                                                                             |
| <span data-ttu-id="13c30-427">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-427">Object identifier</span></span> | <span data-ttu-id="13c30-428">1.3.132.0.9</span><span class="sxs-lookup"><span data-stu-id="13c30-428">1.3.132.0.9</span></span>                                                                     |



 

<span data-ttu-id="13c30-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-430">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-430">Requirement</span></span> | <span data-ttu-id="13c30-431">值</span><span class="sxs-lookup"><span data-stu-id="13c30-431">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-432">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-432">Name</span></span>              | <span data-ttu-id="13c30-433">secP160r1</span><span class="sxs-lookup"><span data-stu-id="13c30-433">secP160r1</span></span>                                                                       |
| <span data-ttu-id="13c30-434">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-434">Standard</span></span>          | [<span data-ttu-id="13c30-435">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="13c30-435">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="13c30-436">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-436">Key size (bits)</span></span>   | <span data-ttu-id="13c30-437">160</span><span class="sxs-lookup"><span data-stu-id="13c30-437">160</span></span>                                                                             |
| <span data-ttu-id="13c30-438">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-438">TLS capable</span></span>       | <span data-ttu-id="13c30-439">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-439">Yes</span></span>                                                                             |
| <span data-ttu-id="13c30-440">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-440">Object identifier</span></span> | <span data-ttu-id="13c30-441">1.3.132.0.8</span><span class="sxs-lookup"><span data-stu-id="13c30-441">1.3.132.0.8</span></span>                                                                     |



 

<span data-ttu-id="13c30-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-443">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-443">Requirement</span></span> | <span data-ttu-id="13c30-444">值</span><span class="sxs-lookup"><span data-stu-id="13c30-444">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-445">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-445">Name</span></span>              | <span data-ttu-id="13c30-446">secP160r2</span><span class="sxs-lookup"><span data-stu-id="13c30-446">secP160r2</span></span>                                                                       |
| <span data-ttu-id="13c30-447">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-447">Standard</span></span>          | [<span data-ttu-id="13c30-448">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="13c30-448">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="13c30-449">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-449">Key size (bits)</span></span>   | <span data-ttu-id="13c30-450">160</span><span class="sxs-lookup"><span data-stu-id="13c30-450">160</span></span>                                                                             |
| <span data-ttu-id="13c30-451">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-451">TLS capable</span></span>       | <span data-ttu-id="13c30-452">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-452">Yes</span></span>                                                                             |
| <span data-ttu-id="13c30-453">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-453">Object identifier</span></span> | <span data-ttu-id="13c30-454">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="13c30-454">1.3.132.0.30</span></span>                                                                    |



 

<span data-ttu-id="13c30-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP192K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT\_ECC\_CURVE\_SECP192K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-456">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-456">Requirement</span></span> | <span data-ttu-id="13c30-457">值</span><span class="sxs-lookup"><span data-stu-id="13c30-457">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-458">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-458">Name</span></span>              | <span data-ttu-id="13c30-459">secP192k1</span><span class="sxs-lookup"><span data-stu-id="13c30-459">secP192k1</span></span>                                                                       |
| <span data-ttu-id="13c30-460">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-460">Standard</span></span>          | [<span data-ttu-id="13c30-461">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="13c30-461">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="13c30-462">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-462">Key size (bits)</span></span>   | <span data-ttu-id="13c30-463">192</span><span class="sxs-lookup"><span data-stu-id="13c30-463">192</span></span>                                                                             |
| <span data-ttu-id="13c30-464">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-464">TLS capable</span></span>       | <span data-ttu-id="13c30-465">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-465">Yes</span></span>                                                                             |
| <span data-ttu-id="13c30-466">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-466">Object identifier</span></span> | <span data-ttu-id="13c30-467">1.3.132.0.31</span><span class="sxs-lookup"><span data-stu-id="13c30-467">1.3.132.0.31</span></span>                                                                    |



 

<span data-ttu-id="13c30-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP192R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP192R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-469">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-469">Requirement</span></span> | <span data-ttu-id="13c30-470">值</span><span class="sxs-lookup"><span data-stu-id="13c30-470">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-471">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-471">Name</span></span>              | <span data-ttu-id="13c30-472">secP192r1</span><span class="sxs-lookup"><span data-stu-id="13c30-472">secP192r1</span></span>                                                                       |
| <span data-ttu-id="13c30-473">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-473">Standard</span></span>          | [<span data-ttu-id="13c30-474">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="13c30-474">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="13c30-475">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-475">Key size (bits)</span></span>   | <span data-ttu-id="13c30-476">192</span><span class="sxs-lookup"><span data-stu-id="13c30-476">192</span></span>                                                                             |
| <span data-ttu-id="13c30-477">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-477">TLS capable</span></span>       | <span data-ttu-id="13c30-478">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-478">Yes</span></span>                                                                             |
| <span data-ttu-id="13c30-479">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-479">Object identifier</span></span> | <span data-ttu-id="13c30-480">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="13c30-480">1.2.840.10045.3.1.1</span></span>                                                             |



 

<span data-ttu-id="13c30-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP224K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT\_ECC\_CURVE\_SECP224K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-482">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-482">Requirement</span></span> | <span data-ttu-id="13c30-483">值</span><span class="sxs-lookup"><span data-stu-id="13c30-483">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-484">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-484">Name</span></span>              | <span data-ttu-id="13c30-485">secP224k1</span><span class="sxs-lookup"><span data-stu-id="13c30-485">secP224k1</span></span>                                                                       |
| <span data-ttu-id="13c30-486">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-486">Standard</span></span>          | [<span data-ttu-id="13c30-487">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="13c30-487">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="13c30-488">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-488">Key size (bits)</span></span>   | <span data-ttu-id="13c30-489">224</span><span class="sxs-lookup"><span data-stu-id="13c30-489">224</span></span>                                                                             |
| <span data-ttu-id="13c30-490">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-490">TLS capable</span></span>       | <span data-ttu-id="13c30-491">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-491">Yes</span></span>                                                                             |
| <span data-ttu-id="13c30-492">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-492">Object identifier</span></span> | <span data-ttu-id="13c30-493">1.3.132.0.32</span><span class="sxs-lookup"><span data-stu-id="13c30-493">1.3.132.0.32</span></span>                                                                    |



 

<span data-ttu-id="13c30-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP224R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT\_ECC\_CURVE\_SECP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-495">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-495">Requirement</span></span> | <span data-ttu-id="13c30-496">值</span><span class="sxs-lookup"><span data-stu-id="13c30-496">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-497">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-497">Name</span></span>              | <span data-ttu-id="13c30-498">secP224r1</span><span class="sxs-lookup"><span data-stu-id="13c30-498">secP224r1</span></span>                                                                       |
| <span data-ttu-id="13c30-499">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-499">Standard</span></span>          | [<span data-ttu-id="13c30-500">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="13c30-500">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="13c30-501">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-501">Key size (bits)</span></span>   | <span data-ttu-id="13c30-502">224</span><span class="sxs-lookup"><span data-stu-id="13c30-502">224</span></span>                                                                             |
| <span data-ttu-id="13c30-503">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-503">TLS capable</span></span>       | <span data-ttu-id="13c30-504">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-504">Yes</span></span>                                                                             |
| <span data-ttu-id="13c30-505">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-505">Object identifier</span></span> | <span data-ttu-id="13c30-506">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="13c30-506">1.3.132.0.33</span></span>                                                                    |



 

<span data-ttu-id="13c30-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP256K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT\_ECC\_CURVE\_SECP256K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-508">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-508">Requirement</span></span> | <span data-ttu-id="13c30-509">值</span><span class="sxs-lookup"><span data-stu-id="13c30-509">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-510">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-510">Name</span></span>              | <span data-ttu-id="13c30-511">secP256k1</span><span class="sxs-lookup"><span data-stu-id="13c30-511">secP256k1</span></span>                                                                       |
| <span data-ttu-id="13c30-512">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-512">Standard</span></span>          | [<span data-ttu-id="13c30-513">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="13c30-513">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="13c30-514">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-514">Key size (bits)</span></span>   | <span data-ttu-id="13c30-515">256</span><span class="sxs-lookup"><span data-stu-id="13c30-515">256</span></span>                                                                             |
| <span data-ttu-id="13c30-516">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-516">TLS capable</span></span>       | <span data-ttu-id="13c30-517">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-517">Yes</span></span>                                                                             |
| <span data-ttu-id="13c30-518">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-518">Object identifier</span></span> | <span data-ttu-id="13c30-519">1.3.132.0.10</span><span class="sxs-lookup"><span data-stu-id="13c30-519">1.3.132.0.10</span></span>                                                                    |



 

<span data-ttu-id="13c30-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP256R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT\_ECC\_CURVE\_SECP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-521">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-521">Requirement</span></span> | <span data-ttu-id="13c30-522">值</span><span class="sxs-lookup"><span data-stu-id="13c30-522">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-523">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-523">Name</span></span>              | <span data-ttu-id="13c30-524">secP256r1</span><span class="sxs-lookup"><span data-stu-id="13c30-524">secP256r1</span></span>                                                                       |
| <span data-ttu-id="13c30-525">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-525">Standard</span></span>          | [<span data-ttu-id="13c30-526">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="13c30-526">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="13c30-527">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-527">Key size (bits)</span></span>   | <span data-ttu-id="13c30-528">256</span><span class="sxs-lookup"><span data-stu-id="13c30-528">256</span></span>                                                                             |
| <span data-ttu-id="13c30-529">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-529">TLS capable</span></span>       | <span data-ttu-id="13c30-530">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-530">Yes</span></span>                                                                             |
| <span data-ttu-id="13c30-531">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-531">Object identifier</span></span> | <span data-ttu-id="13c30-532">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="13c30-532">1.2.840.10045.3.1.7</span></span>                                                             |



 

<span data-ttu-id="13c30-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP384R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-534">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-534">Requirement</span></span> | <span data-ttu-id="13c30-535">值</span><span class="sxs-lookup"><span data-stu-id="13c30-535">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-536">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-536">Name</span></span>              | <span data-ttu-id="13c30-537">secP384r1</span><span class="sxs-lookup"><span data-stu-id="13c30-537">secP384r1</span></span>                                                                       |
| <span data-ttu-id="13c30-538">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-538">Standard</span></span>          | [<span data-ttu-id="13c30-539">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="13c30-539">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="13c30-540">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-540">Key size (bits)</span></span>   | <span data-ttu-id="13c30-541">384</span><span class="sxs-lookup"><span data-stu-id="13c30-541">384</span></span>                                                                             |
| <span data-ttu-id="13c30-542">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-542">TLS capable</span></span>       | <span data-ttu-id="13c30-543">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-543">Yes</span></span>                                                                             |
| <span data-ttu-id="13c30-544">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-544">Object identifier</span></span> | <span data-ttu-id="13c30-545">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="13c30-545">1.3.132.0.34</span></span>                                                                    |



 

<span data-ttu-id="13c30-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP521R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT\_ECC\_CURVE\_SECP521R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-547">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-547">Requirement</span></span> | <span data-ttu-id="13c30-548">值</span><span class="sxs-lookup"><span data-stu-id="13c30-548">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-549">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-549">Name</span></span>              | <span data-ttu-id="13c30-550">secP521r1</span><span class="sxs-lookup"><span data-stu-id="13c30-550">secP521r1</span></span>                                                                       |
| <span data-ttu-id="13c30-551">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-551">Standard</span></span>          | [<span data-ttu-id="13c30-552">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="13c30-552">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="13c30-553">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-553">Key size (bits)</span></span>   | <span data-ttu-id="13c30-554">521</span><span class="sxs-lookup"><span data-stu-id="13c30-554">521</span></span>                                                                             |
| <span data-ttu-id="13c30-555">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-555">TLS capable</span></span>       | <span data-ttu-id="13c30-556">Yes</span><span class="sxs-lookup"><span data-stu-id="13c30-556">Yes</span></span>                                                                             |
| <span data-ttu-id="13c30-557">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-557">Object identifier</span></span> | <span data-ttu-id="13c30-558">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="13c30-558">1.3.132.0.35</span></span>                                                                    |



 

<span data-ttu-id="13c30-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT \_ ECC \_ 曲線 \_ WTLS12**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT\_ECC\_CURVE\_WTLS12**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-560">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-560">Requirement</span></span> | <span data-ttu-id="13c30-561">值</span><span class="sxs-lookup"><span data-stu-id="13c30-561">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="13c30-562">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-562">Name</span></span>              | <span data-ttu-id="13c30-563">wtls12</span><span class="sxs-lookup"><span data-stu-id="13c30-563">wtls12</span></span>       |
| <span data-ttu-id="13c30-564">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-564">Standard</span></span>          | <span data-ttu-id="13c30-565">WTLS</span><span class="sxs-lookup"><span data-stu-id="13c30-565">WTLS</span></span>         |
| <span data-ttu-id="13c30-566">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-566">Key size (bits)</span></span>   | <span data-ttu-id="13c30-567">224</span><span class="sxs-lookup"><span data-stu-id="13c30-567">224</span></span>          |
| <span data-ttu-id="13c30-568">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-568">TLS capable</span></span>       | <span data-ttu-id="13c30-569">No</span><span class="sxs-lookup"><span data-stu-id="13c30-569">No</span></span>           |
| <span data-ttu-id="13c30-570">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-570">Object identifier</span></span> | <span data-ttu-id="13c30-571">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="13c30-571">1.3.132.0.33</span></span> |



 

<span data-ttu-id="13c30-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT \_ ECC \_ 曲線 \_ WTLS7**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT\_ECC\_CURVE\_WTLS7**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-573">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-573">Requirement</span></span> | <span data-ttu-id="13c30-574">值</span><span class="sxs-lookup"><span data-stu-id="13c30-574">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="13c30-575">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-575">Name</span></span>              | <span data-ttu-id="13c30-576">wtls7</span><span class="sxs-lookup"><span data-stu-id="13c30-576">wtls7</span></span>        |
| <span data-ttu-id="13c30-577">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-577">Standard</span></span>          | <span data-ttu-id="13c30-578">WTLS</span><span class="sxs-lookup"><span data-stu-id="13c30-578">WTLS</span></span>         |
| <span data-ttu-id="13c30-579">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-579">Key size (bits)</span></span>   | <span data-ttu-id="13c30-580">160</span><span class="sxs-lookup"><span data-stu-id="13c30-580">160</span></span>          |
| <span data-ttu-id="13c30-581">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-581">TLS capable</span></span>       | <span data-ttu-id="13c30-582">No</span><span class="sxs-lookup"><span data-stu-id="13c30-582">No</span></span>           |
| <span data-ttu-id="13c30-583">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-583">Object identifier</span></span> | <span data-ttu-id="13c30-584">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="13c30-584">1.3.132.0.30</span></span> |



 

<span data-ttu-id="13c30-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ECC \_ 曲線 \_ WTLS9**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT\_ECC\_CURVE\_WTLS9** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-586">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-586">Requirement</span></span> | <span data-ttu-id="13c30-587">值</span><span class="sxs-lookup"><span data-stu-id="13c30-587">Value</span></span> |
|-------------------|---------------|
| <span data-ttu-id="13c30-588">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-588">Name</span></span>              | <span data-ttu-id="13c30-589">wtls9</span><span class="sxs-lookup"><span data-stu-id="13c30-589">wtls9</span></span>         |
| <span data-ttu-id="13c30-590">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-590">Standard</span></span>          | <span data-ttu-id="13c30-591">WTLS</span><span class="sxs-lookup"><span data-stu-id="13c30-591">WTLS</span></span>          |
| <span data-ttu-id="13c30-592">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-592">Key size (bits)</span></span>   | <span data-ttu-id="13c30-593">160</span><span class="sxs-lookup"><span data-stu-id="13c30-593">160</span></span>           |
| <span data-ttu-id="13c30-594">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-594">TLS capable</span></span>       | <span data-ttu-id="13c30-595">No</span><span class="sxs-lookup"><span data-stu-id="13c30-595">No</span></span>            |
| <span data-ttu-id="13c30-596">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-596">Object identifier</span></span> | <span data-ttu-id="13c30-597">2.23.43.1.4.9</span><span class="sxs-lookup"><span data-stu-id="13c30-597">2.23.43.1.4.9</span></span> |



 

<span data-ttu-id="13c30-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P192V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT\_ECC\_CURVE\_X962P192V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-599">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-599">Requirement</span></span> | <span data-ttu-id="13c30-600">值</span><span class="sxs-lookup"><span data-stu-id="13c30-600">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="13c30-601">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-601">Name</span></span>              | <span data-ttu-id="13c30-602">x962P192v1</span><span class="sxs-lookup"><span data-stu-id="13c30-602">x962P192v1</span></span>          |
| <span data-ttu-id="13c30-603">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-603">Standard</span></span>          | <span data-ttu-id="13c30-604">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="13c30-604">ANSI X9.62</span></span>          |
| <span data-ttu-id="13c30-605">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-605">Key size (bits)</span></span>   | <span data-ttu-id="13c30-606">192</span><span class="sxs-lookup"><span data-stu-id="13c30-606">192</span></span>                 |
| <span data-ttu-id="13c30-607">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-607">TLS capable</span></span>       | <span data-ttu-id="13c30-608">No</span><span class="sxs-lookup"><span data-stu-id="13c30-608">No</span></span>                  |
| <span data-ttu-id="13c30-609">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-609">Object identifier</span></span> | <span data-ttu-id="13c30-610">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="13c30-610">1.2.840.10045.3.1.1</span></span> |



 

<span data-ttu-id="13c30-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P192V2**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P192V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-612">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-612">Requirement</span></span> | <span data-ttu-id="13c30-613">值</span><span class="sxs-lookup"><span data-stu-id="13c30-613">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="13c30-614">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-614">Name</span></span>              | <span data-ttu-id="13c30-615">x962P192v2</span><span class="sxs-lookup"><span data-stu-id="13c30-615">x962P192v2</span></span>          |
| <span data-ttu-id="13c30-616">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-616">Standard</span></span>          | <span data-ttu-id="13c30-617">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="13c30-617">ANSI X9.62</span></span>          |
| <span data-ttu-id="13c30-618">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-618">Key size (bits)</span></span>   | <span data-ttu-id="13c30-619">192</span><span class="sxs-lookup"><span data-stu-id="13c30-619">192</span></span>                 |
| <span data-ttu-id="13c30-620">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-620">TLS capable</span></span>       | <span data-ttu-id="13c30-621">No</span><span class="sxs-lookup"><span data-stu-id="13c30-621">No</span></span>                  |
| <span data-ttu-id="13c30-622">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-622">Object identifier</span></span> | <span data-ttu-id="13c30-623">1.2.840.10045.3.1.2</span><span class="sxs-lookup"><span data-stu-id="13c30-623">1.2.840.10045.3.1.2</span></span> |



 

<span data-ttu-id="13c30-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P192V3**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT\_ECC\_CURVE\_X962P192V3**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-625">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-625">Requirement</span></span> | <span data-ttu-id="13c30-626">值</span><span class="sxs-lookup"><span data-stu-id="13c30-626">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="13c30-627">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-627">Name</span></span>              | <span data-ttu-id="13c30-628">x962P192v3</span><span class="sxs-lookup"><span data-stu-id="13c30-628">x962P192v3</span></span>          |
| <span data-ttu-id="13c30-629">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-629">Standard</span></span>          | <span data-ttu-id="13c30-630">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="13c30-630">ANSI X9.62</span></span>          |
| <span data-ttu-id="13c30-631">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-631">Key size (bits)</span></span>   | <span data-ttu-id="13c30-632">192</span><span class="sxs-lookup"><span data-stu-id="13c30-632">192</span></span>                 |
| <span data-ttu-id="13c30-633">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-633">TLS capable</span></span>       | <span data-ttu-id="13c30-634">No</span><span class="sxs-lookup"><span data-stu-id="13c30-634">No</span></span>                  |
| <span data-ttu-id="13c30-635">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-635">Object identifier</span></span> | <span data-ttu-id="13c30-636">1.2.840.10045.3.1.3</span><span class="sxs-lookup"><span data-stu-id="13c30-636">1.2.840.10045.3.1.3</span></span> |



 

<span data-ttu-id="13c30-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-638">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-638">Requirement</span></span> | <span data-ttu-id="13c30-639">值</span><span class="sxs-lookup"><span data-stu-id="13c30-639">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="13c30-640">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-640">Name</span></span>              | <span data-ttu-id="13c30-641">x962P239v1</span><span class="sxs-lookup"><span data-stu-id="13c30-641">x962P239v1</span></span>          |
| <span data-ttu-id="13c30-642">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-642">Standard</span></span>          | <span data-ttu-id="13c30-643">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="13c30-643">ANSI X9.62</span></span>          |
| <span data-ttu-id="13c30-644">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-644">Key size (bits)</span></span>   | <span data-ttu-id="13c30-645">239</span><span class="sxs-lookup"><span data-stu-id="13c30-645">239</span></span>                 |
| <span data-ttu-id="13c30-646">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-646">TLS capable</span></span>       | <span data-ttu-id="13c30-647">No</span><span class="sxs-lookup"><span data-stu-id="13c30-647">No</span></span>                  |
| <span data-ttu-id="13c30-648">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-648">Object identifier</span></span> | <span data-ttu-id="13c30-649">1.2.840.10045.3.1.4</span><span class="sxs-lookup"><span data-stu-id="13c30-649">1.2.840.10045.3.1.4</span></span> |



 

<span data-ttu-id="13c30-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V2**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-651">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-651">Requirement</span></span> | <span data-ttu-id="13c30-652">值</span><span class="sxs-lookup"><span data-stu-id="13c30-652">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="13c30-653">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-653">Name</span></span>              | <span data-ttu-id="13c30-654">x962P239v2</span><span class="sxs-lookup"><span data-stu-id="13c30-654">x962P239v2</span></span>          |
| <span data-ttu-id="13c30-655">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-655">Standard</span></span>          | <span data-ttu-id="13c30-656">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="13c30-656">ANSI X9.62</span></span>          |
| <span data-ttu-id="13c30-657">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-657">Key size (bits)</span></span>   | <span data-ttu-id="13c30-658">239</span><span class="sxs-lookup"><span data-stu-id="13c30-658">239</span></span>                 |
| <span data-ttu-id="13c30-659">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-659">TLS capable</span></span>       | <span data-ttu-id="13c30-660">No</span><span class="sxs-lookup"><span data-stu-id="13c30-660">No</span></span>                  |
| <span data-ttu-id="13c30-661">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-661">Object identifier</span></span> | <span data-ttu-id="13c30-662">1.2.840.10045.3.1.5</span><span class="sxs-lookup"><span data-stu-id="13c30-662">1.2.840.10045.3.1.5</span></span> |



 

<span data-ttu-id="13c30-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V3**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V3** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-664">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-664">Requirement</span></span> | <span data-ttu-id="13c30-665">值</span><span class="sxs-lookup"><span data-stu-id="13c30-665">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="13c30-666">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-666">Name</span></span>              | <span data-ttu-id="13c30-667">x962P239v3</span><span class="sxs-lookup"><span data-stu-id="13c30-667">x962P239v3</span></span>          |
| <span data-ttu-id="13c30-668">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-668">Standard</span></span>          | <span data-ttu-id="13c30-669">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="13c30-669">ANSI X9.62</span></span>          |
| <span data-ttu-id="13c30-670">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-670">Key size (bits)</span></span>   | <span data-ttu-id="13c30-671">239</span><span class="sxs-lookup"><span data-stu-id="13c30-671">239</span></span>                 |
| <span data-ttu-id="13c30-672">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-672">TLS capable</span></span>       | <span data-ttu-id="13c30-673">No</span><span class="sxs-lookup"><span data-stu-id="13c30-673">No</span></span>                  |
| <span data-ttu-id="13c30-674">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-674">Object identifier</span></span> | <span data-ttu-id="13c30-675">1.2.840.10045.3.1.6</span><span class="sxs-lookup"><span data-stu-id="13c30-675">1.2.840.10045.3.1.6</span></span> |



 

<span data-ttu-id="13c30-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P256V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="13c30-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT\_ECC\_CURVE\_X962P256V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="13c30-677">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-677">Requirement</span></span> | <span data-ttu-id="13c30-678">值</span><span class="sxs-lookup"><span data-stu-id="13c30-678">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="13c30-679">名稱</span><span class="sxs-lookup"><span data-stu-id="13c30-679">Name</span></span>              | <span data-ttu-id="13c30-680">x962P256v1</span><span class="sxs-lookup"><span data-stu-id="13c30-680">x962P256v1</span></span>          |
| <span data-ttu-id="13c30-681">標準</span><span class="sxs-lookup"><span data-stu-id="13c30-681">Standard</span></span>          | <span data-ttu-id="13c30-682">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="13c30-682">ANSI X9.62</span></span>          |
| <span data-ttu-id="13c30-683">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="13c30-683">Key size (bits)</span></span>   | <span data-ttu-id="13c30-684">256</span><span class="sxs-lookup"><span data-stu-id="13c30-684">256</span></span>                 |
| <span data-ttu-id="13c30-685">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="13c30-685">TLS capable</span></span>       | <span data-ttu-id="13c30-686">No</span><span class="sxs-lookup"><span data-stu-id="13c30-686">No</span></span>                  |
| <span data-ttu-id="13c30-687">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="13c30-687">Object identifier</span></span> | <span data-ttu-id="13c30-688">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="13c30-688">1.2.840.10045.3.1.7</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13c30-689">備註</span><span class="sxs-lookup"><span data-stu-id="13c30-689">Remarks</span></span>

<span data-ttu-id="13c30-690">若要使用命名曲線，請使用 **BCRYPT \_ ECDSA \_ 演算法** 或 **BCRYPT \_ ECDH \_ 演算法** 來呼叫 [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) ，作為演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="13c30-690">To use a named curve, call [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) using either the **BCRYPT\_ECDSA\_ALGORITHM** or the **BCRYPT\_ECDH\_ALGORITHM** as the algorithm ID.</span></span> <span data-ttu-id="13c30-691">然後，呼叫 [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) ，並將 [ **BCRYPT \_ ECC \_ 曲線 \_ 名稱** ] 屬性設定為上述其中一個曲線或任何已在電腦上註冊的命名曲線，如命令所示 `certutil -displayEccCurve` 。</span><span class="sxs-lookup"><span data-stu-id="13c30-691">Then, call [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) and set the **BCRYPT\_ECC\_CURVE\_NAME** property to one of the above curves or any named curves registered on the computer as shown by the `certutil -displayEccCurve` command.</span></span>

## <a name="requirements"></a><span data-ttu-id="13c30-692">規格需求</span><span class="sxs-lookup"><span data-stu-id="13c30-692">Requirements</span></span>



| <span data-ttu-id="13c30-693">需求</span><span class="sxs-lookup"><span data-stu-id="13c30-693">Requirement</span></span> | <span data-ttu-id="13c30-694">值</span><span class="sxs-lookup"><span data-stu-id="13c30-694">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="13c30-695">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13c30-695">Minimum supported client</span></span><br/> | <span data-ttu-id="13c30-696">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13c30-696">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="13c30-697">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13c30-697">Minimum supported server</span></span><br/> | <span data-ttu-id="13c30-698">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13c30-698">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="13c30-699">標頭</span><span class="sxs-lookup"><span data-stu-id="13c30-699">Header</span></span><br/>                   | <dl> <span data-ttu-id="13c30-700"><dt>Bcrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="13c30-700"><dt>Bcrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13c30-701">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13c30-701">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c30-702">**BCryptOpenAlgorithmProvider**</span><span class="sxs-lookup"><span data-stu-id="13c30-702">**BCryptOpenAlgorithmProvider**</span></span>](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[<span data-ttu-id="13c30-703">**NCryptCreatePersistedKey**</span><span class="sxs-lookup"><span data-stu-id="13c30-703">**NCryptCreatePersistedKey**</span></span>](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




