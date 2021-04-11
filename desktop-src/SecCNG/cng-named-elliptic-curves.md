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
# <a name="cng-named-elliptic-curves"></a><span data-ttu-id="8ca0e-103">CNG 命名橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="8ca0e-103">CNG Named Elliptic Curves</span></span>

<span data-ttu-id="8ca0e-104">從 Windows 10 開始，CNG 提供下列命名橢圓曲線的支援 (ANSI X x9.62、X 9.63、FIPS 186-2) 。</span><span class="sxs-lookup"><span data-stu-id="8ca0e-104">Beginning in Windows 10, CNG provides support for the following named elliptic curves (ANSI X9.62, X9.63, FIPS 186-2).</span></span>

<dl> <span data-ttu-id="8ca0e-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT \_ ECC \_ 曲線 \_ 25519**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT\_ECC\_CURVE\_25519**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-106">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-106">Requirement</span></span> | <span data-ttu-id="8ca0e-107">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-107">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="8ca0e-108">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-108">Name</span></span>              | <span data-ttu-id="8ca0e-109">curve25519</span><span class="sxs-lookup"><span data-stu-id="8ca0e-109">curve25519</span></span>                                                  |
| <span data-ttu-id="8ca0e-110">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-110">Standard</span></span>          | [<span data-ttu-id="8ca0e-111">曲線25519</span><span class="sxs-lookup"><span data-stu-id="8ca0e-111">Curve 25519</span></span>](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| <span data-ttu-id="8ca0e-112">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-112">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-113">255</span><span class="sxs-lookup"><span data-stu-id="8ca0e-113">255</span></span>                                                         |
| <span data-ttu-id="8ca0e-114">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-114">TLS capable</span></span>       |                                                             |
| <span data-ttu-id="8ca0e-115">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-115">Object identifier</span></span> | <span data-ttu-id="8ca0e-116">無</span><span class="sxs-lookup"><span data-stu-id="8ca0e-116">None</span></span>                                                        |



 

<span data-ttu-id="8ca0e-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-118">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-118">Requirement</span></span> | <span data-ttu-id="8ca0e-119">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-120">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-120">Name</span></span>              | <span data-ttu-id="8ca0e-121">brainpoolP160r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-121">brainpoolP160r1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-122">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-122">Standard</span></span>          | [<span data-ttu-id="8ca0e-123">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-123">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-124">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-124">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-125">160</span><span class="sxs-lookup"><span data-stu-id="8ca0e-125">160</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-126">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-126">TLS capable</span></span>       | <span data-ttu-id="8ca0e-127">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-127">No</span></span>                                                                                                                |
| <span data-ttu-id="8ca0e-128">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-128">Object identifier</span></span> | <span data-ttu-id="8ca0e-129">1.3.36.3.3.2.8.1.1.1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-129">1.3.36.3.3.2.8.1.1.1</span></span>                                                                                              |



 

<span data-ttu-id="8ca0e-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ BRAINPOOLP160T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-131">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-131">Requirement</span></span> | <span data-ttu-id="8ca0e-132">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-133">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-133">Name</span></span>              | <span data-ttu-id="8ca0e-134">brainpoolP160t1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-134">brainpoolP160t1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-135">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-135">Standard</span></span>          | [<span data-ttu-id="8ca0e-136">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-136">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-137">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-137">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-138">160</span><span class="sxs-lookup"><span data-stu-id="8ca0e-138">160</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-139">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-139">TLS capable</span></span>       | <span data-ttu-id="8ca0e-140">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-140">No</span></span>                                                                                                                |
| <span data-ttu-id="8ca0e-141">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-141">Object identifier</span></span> | <span data-ttu-id="8ca0e-142">1.3.36.3.3.2.8.1.1.2</span><span class="sxs-lookup"><span data-stu-id="8ca0e-142">1.3.36.3.3.2.8.1.1.2</span></span>                                                                                              |



 

<span data-ttu-id="8ca0e-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP192R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-144">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-144">Requirement</span></span> | <span data-ttu-id="8ca0e-145">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-145">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-146">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-146">Name</span></span>              | <span data-ttu-id="8ca0e-147">brainpoolP192r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-147">brainpoolP192r1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-148">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-148">Standard</span></span>          | [<span data-ttu-id="8ca0e-149">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-149">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-150">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-150">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-151">192</span><span class="sxs-lookup"><span data-stu-id="8ca0e-151">192</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-152">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-152">TLS capable</span></span>       | <span data-ttu-id="8ca0e-153">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-153">No</span></span>                                                                                                                |
| <span data-ttu-id="8ca0e-154">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-154">Object identifier</span></span> | <span data-ttu-id="8ca0e-155">1.3.36.3.3.2.8.1.1.3</span><span class="sxs-lookup"><span data-stu-id="8ca0e-155">1.3.36.3.3.2.8.1.1.3</span></span>                                                                                              |



 

<span data-ttu-id="8ca0e-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP192T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-157">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-157">Requirement</span></span> | <span data-ttu-id="8ca0e-158">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-159">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-159">Name</span></span>              | <span data-ttu-id="8ca0e-160">brainpoolP192t1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-160">brainpoolP192t1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-161">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-161">Standard</span></span>          | [<span data-ttu-id="8ca0e-162">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-162">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-163">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-163">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-164">192</span><span class="sxs-lookup"><span data-stu-id="8ca0e-164">192</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-165">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-165">TLS capable</span></span>       | <span data-ttu-id="8ca0e-166">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-166">No</span></span>                                                                                                                |
| <span data-ttu-id="8ca0e-167">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-167">Object identifier</span></span> | <span data-ttu-id="8ca0e-168">1.3.36.3.3.2.8.1.1.4</span><span class="sxs-lookup"><span data-stu-id="8ca0e-168">1.3.36.3.3.2.8.1.1.4</span></span>                                                                                              |



 

<span data-ttu-id="8ca0e-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP224R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-170">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-170">Requirement</span></span> | <span data-ttu-id="8ca0e-171">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-172">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-172">Name</span></span>              | <span data-ttu-id="8ca0e-173">brainpoolP224r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-173">brainpoolP224r1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-174">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-174">Standard</span></span>          | [<span data-ttu-id="8ca0e-175">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-175">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-176">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-176">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-177">224</span><span class="sxs-lookup"><span data-stu-id="8ca0e-177">224</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-178">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-178">TLS capable</span></span>       | <span data-ttu-id="8ca0e-179">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-179">No</span></span>                                                                                                                |
| <span data-ttu-id="8ca0e-180">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-180">Object identifier</span></span> | <span data-ttu-id="8ca0e-181">1.3.36.3.3.2.8.1.1.5</span><span class="sxs-lookup"><span data-stu-id="8ca0e-181">1.3.36.3.3.2.8.1.1.5</span></span>                                                                                              |



 

<span data-ttu-id="8ca0e-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP224T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-183">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-183">Requirement</span></span> | <span data-ttu-id="8ca0e-184">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-184">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-185">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-185">Name</span></span>              | <span data-ttu-id="8ca0e-186">brainpoolP224t1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-186">brainpoolP224t1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-187">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-187">Standard</span></span>          | [<span data-ttu-id="8ca0e-188">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-188">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-189">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-189">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-190">224</span><span class="sxs-lookup"><span data-stu-id="8ca0e-190">224</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-191">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-191">TLS capable</span></span>       | <span data-ttu-id="8ca0e-192">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-192">No</span></span>                                                                                                                |
| <span data-ttu-id="8ca0e-193">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-193">Object identifier</span></span> | <span data-ttu-id="8ca0e-194">1.3.36.3.3.2.8.1.1.6</span><span class="sxs-lookup"><span data-stu-id="8ca0e-194">1.3.36.3.3.2.8.1.1.6</span></span>                                                                                              |



 

<span data-ttu-id="8ca0e-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP256R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-196">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-196">Requirement</span></span> | <span data-ttu-id="8ca0e-197">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-197">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-198">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-198">Name</span></span>              | <span data-ttu-id="8ca0e-199">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-199">brainpoolP256r1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-200">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-200">Standard</span></span>          | [<span data-ttu-id="8ca0e-201">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-201">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-202">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-202">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-203">256</span><span class="sxs-lookup"><span data-stu-id="8ca0e-203">256</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-204">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-204">TLS capable</span></span>       | <span data-ttu-id="8ca0e-205">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-205">Yes</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-206">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-206">Object identifier</span></span> | <span data-ttu-id="8ca0e-207">1.3.36.3.3.2.8.1.1.7</span><span class="sxs-lookup"><span data-stu-id="8ca0e-207">1.3.36.3.3.2.8.1.1.7</span></span>                                                                                              |



 

<span data-ttu-id="8ca0e-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP256T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-209">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-209">Requirement</span></span> | <span data-ttu-id="8ca0e-210">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-210">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-211">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-211">Name</span></span>              | <span data-ttu-id="8ca0e-212">brainpoolP256t1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-212">brainpoolP256t1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-213">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-213">Standard</span></span>          | [<span data-ttu-id="8ca0e-214">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-214">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-215">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-215">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-216">256</span><span class="sxs-lookup"><span data-stu-id="8ca0e-216">256</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-217">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-217">TLS capable</span></span>       | <span data-ttu-id="8ca0e-218">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-218">No</span></span>                                                                                                                |
| <span data-ttu-id="8ca0e-219">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-219">Object identifier</span></span> | <span data-ttu-id="8ca0e-220">1.3.36.3.3.2.8.1.1.8</span><span class="sxs-lookup"><span data-stu-id="8ca0e-220">1.3.36.3.3.2.8.1.1.8</span></span>                                                                                              |



 

<span data-ttu-id="8ca0e-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP320R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP320R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-222">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-222">Requirement</span></span> | <span data-ttu-id="8ca0e-223">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-223">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-224">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-224">Name</span></span>              | <span data-ttu-id="8ca0e-225">brainpoolP320r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-225">brainpoolP320r1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-226">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-226">Standard</span></span>          | [<span data-ttu-id="8ca0e-227">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-227">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-228">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-228">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-229">320</span><span class="sxs-lookup"><span data-stu-id="8ca0e-229">320</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-230">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-230">TLS capable</span></span>       | <span data-ttu-id="8ca0e-231">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-231">No</span></span>                                                                                                                |
| <span data-ttu-id="8ca0e-232">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-232">Object identifier</span></span> | <span data-ttu-id="8ca0e-233">1.3.36.3.3.2.8.1.1.9</span><span class="sxs-lookup"><span data-stu-id="8ca0e-233">1.3.36.3.3.2.8.1.1.9</span></span>                                                                                              |



 

<span data-ttu-id="8ca0e-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP32 0T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP32 0T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-235">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-235">Requirement</span></span> | <span data-ttu-id="8ca0e-236">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-236">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-237">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-237">Name</span></span>              | <span data-ttu-id="8ca0e-238">brainpoolP320t1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-238">brainpoolP320t1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-239">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-239">Standard</span></span>          | [<span data-ttu-id="8ca0e-240">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-240">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-241">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-241">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-242">320</span><span class="sxs-lookup"><span data-stu-id="8ca0e-242">320</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-243">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-243">TLS capable</span></span>       | <span data-ttu-id="8ca0e-244">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-244">No</span></span>                                                                                                                |
| <span data-ttu-id="8ca0e-245">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-245">Object identifier</span></span> | <span data-ttu-id="8ca0e-246">1.3.36.3.3.2.8.1.1.10</span><span class="sxs-lookup"><span data-stu-id="8ca0e-246">1.3.36.3.3.2.8.1.1.10</span></span>                                                                                             |



 

<span data-ttu-id="8ca0e-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ BRAINPOOLP384R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-248">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-248">Requirement</span></span> | <span data-ttu-id="8ca0e-249">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-249">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-250">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-250">Name</span></span>              | <span data-ttu-id="8ca0e-251">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-251">brainpoolP384r1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-252">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-252">Standard</span></span>          | [<span data-ttu-id="8ca0e-253">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-253">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-254">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-254">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-255">384</span><span class="sxs-lookup"><span data-stu-id="8ca0e-255">384</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-256">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-256">TLS capable</span></span>       | <span data-ttu-id="8ca0e-257">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-257">Yes</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-258">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-258">Object identifier</span></span> | <span data-ttu-id="8ca0e-259">1.3.36.3.3.2.8.1.1.11</span><span class="sxs-lookup"><span data-stu-id="8ca0e-259">1.3.36.3.3.2.8.1.1.11</span></span>                                                                                             |



 

<span data-ttu-id="8ca0e-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP384T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-261">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-261">Requirement</span></span> | <span data-ttu-id="8ca0e-262">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-262">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-263">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-263">Name</span></span>              | <span data-ttu-id="8ca0e-264">brainpoolP384t1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-264">brainpoolP384t1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-265">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-265">Standard</span></span>          | [<span data-ttu-id="8ca0e-266">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-266">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-267">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-267">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-268">384</span><span class="sxs-lookup"><span data-stu-id="8ca0e-268">384</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-269">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-269">TLS capable</span></span>       | <span data-ttu-id="8ca0e-270">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-270">No</span></span>                                                                                                                |
| <span data-ttu-id="8ca0e-271">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-271">Object identifier</span></span> | <span data-ttu-id="8ca0e-272">1.3.36.3.3.2.8.1.1.12</span><span class="sxs-lookup"><span data-stu-id="8ca0e-272">1.3.36.3.3.2.8.1.1.12</span></span>                                                                                             |



 

<span data-ttu-id="8ca0e-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP512R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-274">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-274">Requirement</span></span> | <span data-ttu-id="8ca0e-275">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-275">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-276">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-276">Name</span></span>              | <span data-ttu-id="8ca0e-277">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-277">brainpoolP512r1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-278">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-278">Standard</span></span>          | [<span data-ttu-id="8ca0e-279">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-279">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-280">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-280">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-281">512</span><span class="sxs-lookup"><span data-stu-id="8ca0e-281">512</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-282">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-282">TLS capable</span></span>       | <span data-ttu-id="8ca0e-283">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-283">Yes</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-284">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-284">Object identifier</span></span> | <span data-ttu-id="8ca0e-285">1.3.36.3.3.2.8.1.1.13</span><span class="sxs-lookup"><span data-stu-id="8ca0e-285">1.3.36.3.3.2.8.1.1.13</span></span>                                                                                             |



 

<span data-ttu-id="8ca0e-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP512T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-287">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-287">Requirement</span></span> | <span data-ttu-id="8ca0e-288">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-288">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-289">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-289">Name</span></span>              | <span data-ttu-id="8ca0e-290">brainpoolP512t1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-290">brainpoolP512t1</span></span>                                                                                                   |
| <span data-ttu-id="8ca0e-291">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-291">Standard</span></span>          | [<span data-ttu-id="8ca0e-292">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="8ca0e-292">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="8ca0e-293">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-293">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-294">512</span><span class="sxs-lookup"><span data-stu-id="8ca0e-294">512</span></span>                                                                                                               |
| <span data-ttu-id="8ca0e-295">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-295">TLS capable</span></span>       | <span data-ttu-id="8ca0e-296">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-296">No</span></span>                                                                                                                |
| <span data-ttu-id="8ca0e-297">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-297">Object identifier</span></span> | <span data-ttu-id="8ca0e-298">1.3.36.3.3.2.8.1.1.14</span><span class="sxs-lookup"><span data-stu-id="8ca0e-298">1.3.36.3.3.2.8.1.1.14</span></span>                                                                                             |



 

<span data-ttu-id="8ca0e-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ECC \_ 曲線 \_ EC192WAPI**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT\_ECC\_CURVE\_EC192WAPI** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-300">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-300">Requirement</span></span> | <span data-ttu-id="8ca0e-301">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-301">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="8ca0e-302">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-302">Name</span></span>              | <span data-ttu-id="8ca0e-303">ec192wapi</span><span class="sxs-lookup"><span data-stu-id="8ca0e-303">ec192wapi</span></span>                                                      |
| <span data-ttu-id="8ca0e-304">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-304">Standard</span></span>          | <span data-ttu-id="8ca0e-305">國際區域網路的中文標準 (GB 15629.11-2003) </span><span class="sxs-lookup"><span data-stu-id="8ca0e-305">Chinese National Standard for Wireless LANs (GB 15629.11-2003)</span></span> |
| <span data-ttu-id="8ca0e-306">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-306">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-307">192</span><span class="sxs-lookup"><span data-stu-id="8ca0e-307">192</span></span>                                                            |
| <span data-ttu-id="8ca0e-308">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-308">TLS capable</span></span>       | <span data-ttu-id="8ca0e-309">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-309">No</span></span>                                                             |
| <span data-ttu-id="8ca0e-310">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-310">Object identifier</span></span> | <span data-ttu-id="8ca0e-311">1.2.156.11235.1.1.2.1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-311">1.2.156.11235.1.1.2.1</span></span>                                          |



 

<span data-ttu-id="8ca0e-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP192**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT\_ECC\_CURVE\_NISTP192**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-313">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-313">Requirement</span></span> | <span data-ttu-id="8ca0e-314">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-314">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-315">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-315">Name</span></span>              | <span data-ttu-id="8ca0e-316">nistP192</span><span class="sxs-lookup"><span data-stu-id="8ca0e-316">nistP192</span></span>                                                                                                                     |
| <span data-ttu-id="8ca0e-317">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-317">Standard</span></span>          | [<span data-ttu-id="8ca0e-318">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="8ca0e-318">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="8ca0e-319">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-319">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-320">192</span><span class="sxs-lookup"><span data-stu-id="8ca0e-320">192</span></span>                                                                                                                          |
| <span data-ttu-id="8ca0e-321">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-321">TLS capable</span></span>       | <span data-ttu-id="8ca0e-322">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-322">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="8ca0e-323">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-323">Object identifier</span></span> | <span data-ttu-id="8ca0e-324">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-324">1.2.840.10045.3.1.1</span></span>                                                                                                          |



 

<span data-ttu-id="8ca0e-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ECC \_ 曲線 \_ NISTP224**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT\_ECC\_CURVE\_NISTP224** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-326">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-326">Requirement</span></span> | <span data-ttu-id="8ca0e-327">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-327">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-328">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-328">Name</span></span>              | <span data-ttu-id="8ca0e-329">nistP224</span><span class="sxs-lookup"><span data-stu-id="8ca0e-329">nistP224</span></span>                                                                                                                     |
| <span data-ttu-id="8ca0e-330">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-330">Standard</span></span>          | [<span data-ttu-id="8ca0e-331">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="8ca0e-331">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="8ca0e-332">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-332">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-333">224</span><span class="sxs-lookup"><span data-stu-id="8ca0e-333">224</span></span>                                                                                                                          |
| <span data-ttu-id="8ca0e-334">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-334">TLS capable</span></span>       | <span data-ttu-id="8ca0e-335">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-335">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="8ca0e-336">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-336">Object identifier</span></span> | <span data-ttu-id="8ca0e-337">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="8ca0e-337">1.3.132.0.33</span></span>                                                                                                                 |



 

<span data-ttu-id="8ca0e-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP256**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT\_ECC\_CURVE\_NISTP256**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-339">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-339">Requirement</span></span> | <span data-ttu-id="8ca0e-340">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-340">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-341">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-341">Name</span></span>              | <span data-ttu-id="8ca0e-342">nistP256</span><span class="sxs-lookup"><span data-stu-id="8ca0e-342">nistP256</span></span>                                                                                                                     |
| <span data-ttu-id="8ca0e-343">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-343">Standard</span></span>          | [<span data-ttu-id="8ca0e-344">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="8ca0e-344">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="8ca0e-345">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-345">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-346">256</span><span class="sxs-lookup"><span data-stu-id="8ca0e-346">256</span></span>                                                                                                                          |
| <span data-ttu-id="8ca0e-347">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-347">TLS capable</span></span>       | <span data-ttu-id="8ca0e-348">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-348">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="8ca0e-349">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-349">Object identifier</span></span> | <span data-ttu-id="8ca0e-350">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="8ca0e-350">1.2.840.10045.3.1.7</span></span>                                                                                                          |



 

<span data-ttu-id="8ca0e-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ECC \_ 曲線 \_ NISTP384**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT\_ECC\_CURVE\_NISTP384** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-352">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-352">Requirement</span></span> | <span data-ttu-id="8ca0e-353">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-353">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-354">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-354">Name</span></span>              | <span data-ttu-id="8ca0e-355">nistP384</span><span class="sxs-lookup"><span data-stu-id="8ca0e-355">nistP384</span></span>                                                                                                                     |
| <span data-ttu-id="8ca0e-356">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-356">Standard</span></span>          | [<span data-ttu-id="8ca0e-357">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="8ca0e-357">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="8ca0e-358">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-358">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-359">384</span><span class="sxs-lookup"><span data-stu-id="8ca0e-359">384</span></span>                                                                                                                          |
| <span data-ttu-id="8ca0e-360">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-360">TLS capable</span></span>       | <span data-ttu-id="8ca0e-361">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-361">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="8ca0e-362">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-362">Object identifier</span></span> | <span data-ttu-id="8ca0e-363">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="8ca0e-363">1.3.132.0.34</span></span>                                                                                                                 |



 

<span data-ttu-id="8ca0e-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP521**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT\_ECC\_CURVE\_NISTP521**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-365">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-365">Requirement</span></span> | <span data-ttu-id="8ca0e-366">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-366">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-367">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-367">Name</span></span>              | <span data-ttu-id="8ca0e-368">nistP521</span><span class="sxs-lookup"><span data-stu-id="8ca0e-368">nistP521</span></span>                                                                                                                     |
| <span data-ttu-id="8ca0e-369">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-369">Standard</span></span>          | [<span data-ttu-id="8ca0e-370">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="8ca0e-370">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="8ca0e-371">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-371">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-372">521</span><span class="sxs-lookup"><span data-stu-id="8ca0e-372">521</span></span>                                                                                                                          |
| <span data-ttu-id="8ca0e-373">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-373">TLS capable</span></span>       | <span data-ttu-id="8ca0e-374">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-374">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="8ca0e-375">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-375">Object identifier</span></span> | <span data-ttu-id="8ca0e-376">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="8ca0e-376">1.3.132.0.35</span></span>                                                                                                                 |



 

<span data-ttu-id="8ca0e-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ NUMSP256T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP256T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-378">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-378">Requirement</span></span> | <span data-ttu-id="8ca0e-379">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-379">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-380">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-380">Name</span></span>              | <span data-ttu-id="8ca0e-381">numsP256t1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-381">numsP256t1</span></span>                                                                                                                              |
| <span data-ttu-id="8ca0e-382">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-382">Standard</span></span>          | [<span data-ttu-id="8ca0e-383">MSR ECCLib 中的曲線選取和支援曲線參數規格</span><span class="sxs-lookup"><span data-stu-id="8ca0e-383">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="8ca0e-384">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-384">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-385">256</span><span class="sxs-lookup"><span data-stu-id="8ca0e-385">256</span></span>                                                                                                                                     |
| <span data-ttu-id="8ca0e-386">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-386">TLS capable</span></span>       | <span data-ttu-id="8ca0e-387">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-387">No</span></span>                                                                                                                                      |
| <span data-ttu-id="8ca0e-388">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-388">Object identifier</span></span> | <span data-ttu-id="8ca0e-389">無</span><span class="sxs-lookup"><span data-stu-id="8ca0e-389">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="8ca0e-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ NUMSP384T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP384T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-391">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-391">Requirement</span></span> | <span data-ttu-id="8ca0e-392">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-392">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-393">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-393">Name</span></span>              | <span data-ttu-id="8ca0e-394">numsP384t1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-394">numsP384t1</span></span>                                                                                                                              |
| <span data-ttu-id="8ca0e-395">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-395">Standard</span></span>          | [<span data-ttu-id="8ca0e-396">MSR ECCLib 中的曲線選取和支援曲線參數規格</span><span class="sxs-lookup"><span data-stu-id="8ca0e-396">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="8ca0e-397">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-397">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-398">384</span><span class="sxs-lookup"><span data-stu-id="8ca0e-398">384</span></span>                                                                                                                                     |
| <span data-ttu-id="8ca0e-399">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-399">TLS capable</span></span>       | <span data-ttu-id="8ca0e-400">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-400">No</span></span>                                                                                                                                      |
| <span data-ttu-id="8ca0e-401">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-401">Object identifier</span></span> | <span data-ttu-id="8ca0e-402">無</span><span class="sxs-lookup"><span data-stu-id="8ca0e-402">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="8ca0e-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ NUMSP512T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT\_ECC\_CURVE\_NUMSP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-404">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-404">Requirement</span></span> | <span data-ttu-id="8ca0e-405">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-405">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-406">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-406">Name</span></span>              | <span data-ttu-id="8ca0e-407">numsP512t1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-407">numsP512t1</span></span>                                                                                                                              |
| <span data-ttu-id="8ca0e-408">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-408">Standard</span></span>          | [<span data-ttu-id="8ca0e-409">MSR ECCLib 中的曲線選取和支援曲線參數規格</span><span class="sxs-lookup"><span data-stu-id="8ca0e-409">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="8ca0e-410">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-410">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-411">512</span><span class="sxs-lookup"><span data-stu-id="8ca0e-411">512</span></span>                                                                                                                                     |
| <span data-ttu-id="8ca0e-412">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-412">TLS capable</span></span>       | <span data-ttu-id="8ca0e-413">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-413">No</span></span>                                                                                                                                      |
| <span data-ttu-id="8ca0e-414">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-414">Object identifier</span></span> | <span data-ttu-id="8ca0e-415">無</span><span class="sxs-lookup"><span data-stu-id="8ca0e-415">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="8ca0e-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160K1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-417">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-417">Requirement</span></span> | <span data-ttu-id="8ca0e-418">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-418">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-419">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-419">Name</span></span>              | <span data-ttu-id="8ca0e-420">secP160k1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-420">secP160k1</span></span>                                                                       |
| <span data-ttu-id="8ca0e-421">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-421">Standard</span></span>          | [<span data-ttu-id="8ca0e-422">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="8ca0e-422">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="8ca0e-423">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-423">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-424">160</span><span class="sxs-lookup"><span data-stu-id="8ca0e-424">160</span></span>                                                                             |
| <span data-ttu-id="8ca0e-425">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-425">TLS capable</span></span>       | <span data-ttu-id="8ca0e-426">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-426">Yes</span></span>                                                                             |
| <span data-ttu-id="8ca0e-427">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-427">Object identifier</span></span> | <span data-ttu-id="8ca0e-428">1.3.132.0.9</span><span class="sxs-lookup"><span data-stu-id="8ca0e-428">1.3.132.0.9</span></span>                                                                     |



 

<span data-ttu-id="8ca0e-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-430">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-430">Requirement</span></span> | <span data-ttu-id="8ca0e-431">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-431">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-432">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-432">Name</span></span>              | <span data-ttu-id="8ca0e-433">secP160r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-433">secP160r1</span></span>                                                                       |
| <span data-ttu-id="8ca0e-434">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-434">Standard</span></span>          | [<span data-ttu-id="8ca0e-435">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="8ca0e-435">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="8ca0e-436">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-436">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-437">160</span><span class="sxs-lookup"><span data-stu-id="8ca0e-437">160</span></span>                                                                             |
| <span data-ttu-id="8ca0e-438">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-438">TLS capable</span></span>       | <span data-ttu-id="8ca0e-439">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-439">Yes</span></span>                                                                             |
| <span data-ttu-id="8ca0e-440">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-440">Object identifier</span></span> | <span data-ttu-id="8ca0e-441">1.3.132.0.8</span><span class="sxs-lookup"><span data-stu-id="8ca0e-441">1.3.132.0.8</span></span>                                                                     |



 

<span data-ttu-id="8ca0e-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-443">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-443">Requirement</span></span> | <span data-ttu-id="8ca0e-444">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-444">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-445">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-445">Name</span></span>              | <span data-ttu-id="8ca0e-446">secP160r2</span><span class="sxs-lookup"><span data-stu-id="8ca0e-446">secP160r2</span></span>                                                                       |
| <span data-ttu-id="8ca0e-447">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-447">Standard</span></span>          | [<span data-ttu-id="8ca0e-448">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="8ca0e-448">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="8ca0e-449">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-449">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-450">160</span><span class="sxs-lookup"><span data-stu-id="8ca0e-450">160</span></span>                                                                             |
| <span data-ttu-id="8ca0e-451">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-451">TLS capable</span></span>       | <span data-ttu-id="8ca0e-452">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-452">Yes</span></span>                                                                             |
| <span data-ttu-id="8ca0e-453">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-453">Object identifier</span></span> | <span data-ttu-id="8ca0e-454">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="8ca0e-454">1.3.132.0.30</span></span>                                                                    |



 

<span data-ttu-id="8ca0e-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP192K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT\_ECC\_CURVE\_SECP192K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-456">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-456">Requirement</span></span> | <span data-ttu-id="8ca0e-457">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-457">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-458">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-458">Name</span></span>              | <span data-ttu-id="8ca0e-459">secP192k1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-459">secP192k1</span></span>                                                                       |
| <span data-ttu-id="8ca0e-460">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-460">Standard</span></span>          | [<span data-ttu-id="8ca0e-461">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="8ca0e-461">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="8ca0e-462">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-462">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-463">192</span><span class="sxs-lookup"><span data-stu-id="8ca0e-463">192</span></span>                                                                             |
| <span data-ttu-id="8ca0e-464">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-464">TLS capable</span></span>       | <span data-ttu-id="8ca0e-465">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-465">Yes</span></span>                                                                             |
| <span data-ttu-id="8ca0e-466">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-466">Object identifier</span></span> | <span data-ttu-id="8ca0e-467">1.3.132.0.31</span><span class="sxs-lookup"><span data-stu-id="8ca0e-467">1.3.132.0.31</span></span>                                                                    |



 

<span data-ttu-id="8ca0e-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP192R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP192R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-469">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-469">Requirement</span></span> | <span data-ttu-id="8ca0e-470">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-470">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-471">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-471">Name</span></span>              | <span data-ttu-id="8ca0e-472">secP192r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-472">secP192r1</span></span>                                                                       |
| <span data-ttu-id="8ca0e-473">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-473">Standard</span></span>          | [<span data-ttu-id="8ca0e-474">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="8ca0e-474">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="8ca0e-475">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-475">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-476">192</span><span class="sxs-lookup"><span data-stu-id="8ca0e-476">192</span></span>                                                                             |
| <span data-ttu-id="8ca0e-477">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-477">TLS capable</span></span>       | <span data-ttu-id="8ca0e-478">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-478">Yes</span></span>                                                                             |
| <span data-ttu-id="8ca0e-479">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-479">Object identifier</span></span> | <span data-ttu-id="8ca0e-480">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-480">1.2.840.10045.3.1.1</span></span>                                                             |



 

<span data-ttu-id="8ca0e-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP224K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT\_ECC\_CURVE\_SECP224K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-482">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-482">Requirement</span></span> | <span data-ttu-id="8ca0e-483">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-483">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-484">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-484">Name</span></span>              | <span data-ttu-id="8ca0e-485">secP224k1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-485">secP224k1</span></span>                                                                       |
| <span data-ttu-id="8ca0e-486">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-486">Standard</span></span>          | [<span data-ttu-id="8ca0e-487">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="8ca0e-487">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="8ca0e-488">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-488">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-489">224</span><span class="sxs-lookup"><span data-stu-id="8ca0e-489">224</span></span>                                                                             |
| <span data-ttu-id="8ca0e-490">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-490">TLS capable</span></span>       | <span data-ttu-id="8ca0e-491">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-491">Yes</span></span>                                                                             |
| <span data-ttu-id="8ca0e-492">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-492">Object identifier</span></span> | <span data-ttu-id="8ca0e-493">1.3.132.0.32</span><span class="sxs-lookup"><span data-stu-id="8ca0e-493">1.3.132.0.32</span></span>                                                                    |



 

<span data-ttu-id="8ca0e-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP224R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT\_ECC\_CURVE\_SECP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-495">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-495">Requirement</span></span> | <span data-ttu-id="8ca0e-496">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-496">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-497">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-497">Name</span></span>              | <span data-ttu-id="8ca0e-498">secP224r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-498">secP224r1</span></span>                                                                       |
| <span data-ttu-id="8ca0e-499">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-499">Standard</span></span>          | [<span data-ttu-id="8ca0e-500">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="8ca0e-500">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="8ca0e-501">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-501">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-502">224</span><span class="sxs-lookup"><span data-stu-id="8ca0e-502">224</span></span>                                                                             |
| <span data-ttu-id="8ca0e-503">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-503">TLS capable</span></span>       | <span data-ttu-id="8ca0e-504">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-504">Yes</span></span>                                                                             |
| <span data-ttu-id="8ca0e-505">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-505">Object identifier</span></span> | <span data-ttu-id="8ca0e-506">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="8ca0e-506">1.3.132.0.33</span></span>                                                                    |



 

<span data-ttu-id="8ca0e-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP256K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT\_ECC\_CURVE\_SECP256K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-508">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-508">Requirement</span></span> | <span data-ttu-id="8ca0e-509">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-509">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-510">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-510">Name</span></span>              | <span data-ttu-id="8ca0e-511">secP256k1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-511">secP256k1</span></span>                                                                       |
| <span data-ttu-id="8ca0e-512">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-512">Standard</span></span>          | [<span data-ttu-id="8ca0e-513">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="8ca0e-513">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="8ca0e-514">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-514">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-515">256</span><span class="sxs-lookup"><span data-stu-id="8ca0e-515">256</span></span>                                                                             |
| <span data-ttu-id="8ca0e-516">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-516">TLS capable</span></span>       | <span data-ttu-id="8ca0e-517">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-517">Yes</span></span>                                                                             |
| <span data-ttu-id="8ca0e-518">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-518">Object identifier</span></span> | <span data-ttu-id="8ca0e-519">1.3.132.0.10</span><span class="sxs-lookup"><span data-stu-id="8ca0e-519">1.3.132.0.10</span></span>                                                                    |



 

<span data-ttu-id="8ca0e-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP256R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT\_ECC\_CURVE\_SECP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-521">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-521">Requirement</span></span> | <span data-ttu-id="8ca0e-522">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-522">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-523">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-523">Name</span></span>              | <span data-ttu-id="8ca0e-524">secP256r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-524">secP256r1</span></span>                                                                       |
| <span data-ttu-id="8ca0e-525">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-525">Standard</span></span>          | [<span data-ttu-id="8ca0e-526">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="8ca0e-526">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="8ca0e-527">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-527">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-528">256</span><span class="sxs-lookup"><span data-stu-id="8ca0e-528">256</span></span>                                                                             |
| <span data-ttu-id="8ca0e-529">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-529">TLS capable</span></span>       | <span data-ttu-id="8ca0e-530">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-530">Yes</span></span>                                                                             |
| <span data-ttu-id="8ca0e-531">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-531">Object identifier</span></span> | <span data-ttu-id="8ca0e-532">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="8ca0e-532">1.2.840.10045.3.1.7</span></span>                                                             |



 

<span data-ttu-id="8ca0e-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP384R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-534">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-534">Requirement</span></span> | <span data-ttu-id="8ca0e-535">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-535">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-536">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-536">Name</span></span>              | <span data-ttu-id="8ca0e-537">secP384r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-537">secP384r1</span></span>                                                                       |
| <span data-ttu-id="8ca0e-538">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-538">Standard</span></span>          | [<span data-ttu-id="8ca0e-539">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="8ca0e-539">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="8ca0e-540">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-540">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-541">384</span><span class="sxs-lookup"><span data-stu-id="8ca0e-541">384</span></span>                                                                             |
| <span data-ttu-id="8ca0e-542">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-542">TLS capable</span></span>       | <span data-ttu-id="8ca0e-543">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-543">Yes</span></span>                                                                             |
| <span data-ttu-id="8ca0e-544">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-544">Object identifier</span></span> | <span data-ttu-id="8ca0e-545">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="8ca0e-545">1.3.132.0.34</span></span>                                                                    |



 

<span data-ttu-id="8ca0e-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP521R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT\_ECC\_CURVE\_SECP521R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-547">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-547">Requirement</span></span> | <span data-ttu-id="8ca0e-548">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-548">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-549">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-549">Name</span></span>              | <span data-ttu-id="8ca0e-550">secP521r1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-550">secP521r1</span></span>                                                                       |
| <span data-ttu-id="8ca0e-551">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-551">Standard</span></span>          | [<span data-ttu-id="8ca0e-552">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="8ca0e-552">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="8ca0e-553">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-553">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-554">521</span><span class="sxs-lookup"><span data-stu-id="8ca0e-554">521</span></span>                                                                             |
| <span data-ttu-id="8ca0e-555">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-555">TLS capable</span></span>       | <span data-ttu-id="8ca0e-556">Yes</span><span class="sxs-lookup"><span data-stu-id="8ca0e-556">Yes</span></span>                                                                             |
| <span data-ttu-id="8ca0e-557">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-557">Object identifier</span></span> | <span data-ttu-id="8ca0e-558">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="8ca0e-558">1.3.132.0.35</span></span>                                                                    |



 

<span data-ttu-id="8ca0e-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT \_ ECC \_ 曲線 \_ WTLS12**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT\_ECC\_CURVE\_WTLS12**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-560">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-560">Requirement</span></span> | <span data-ttu-id="8ca0e-561">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-561">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="8ca0e-562">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-562">Name</span></span>              | <span data-ttu-id="8ca0e-563">wtls12</span><span class="sxs-lookup"><span data-stu-id="8ca0e-563">wtls12</span></span>       |
| <span data-ttu-id="8ca0e-564">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-564">Standard</span></span>          | <span data-ttu-id="8ca0e-565">WTLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-565">WTLS</span></span>         |
| <span data-ttu-id="8ca0e-566">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-566">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-567">224</span><span class="sxs-lookup"><span data-stu-id="8ca0e-567">224</span></span>          |
| <span data-ttu-id="8ca0e-568">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-568">TLS capable</span></span>       | <span data-ttu-id="8ca0e-569">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-569">No</span></span>           |
| <span data-ttu-id="8ca0e-570">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-570">Object identifier</span></span> | <span data-ttu-id="8ca0e-571">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="8ca0e-571">1.3.132.0.33</span></span> |



 

<span data-ttu-id="8ca0e-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT \_ ECC \_ 曲線 \_ WTLS7**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT\_ECC\_CURVE\_WTLS7**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-573">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-573">Requirement</span></span> | <span data-ttu-id="8ca0e-574">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-574">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="8ca0e-575">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-575">Name</span></span>              | <span data-ttu-id="8ca0e-576">wtls7</span><span class="sxs-lookup"><span data-stu-id="8ca0e-576">wtls7</span></span>        |
| <span data-ttu-id="8ca0e-577">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-577">Standard</span></span>          | <span data-ttu-id="8ca0e-578">WTLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-578">WTLS</span></span>         |
| <span data-ttu-id="8ca0e-579">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-579">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-580">160</span><span class="sxs-lookup"><span data-stu-id="8ca0e-580">160</span></span>          |
| <span data-ttu-id="8ca0e-581">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-581">TLS capable</span></span>       | <span data-ttu-id="8ca0e-582">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-582">No</span></span>           |
| <span data-ttu-id="8ca0e-583">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-583">Object identifier</span></span> | <span data-ttu-id="8ca0e-584">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="8ca0e-584">1.3.132.0.30</span></span> |



 

<span data-ttu-id="8ca0e-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ECC \_ 曲線 \_ WTLS9**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT\_ECC\_CURVE\_WTLS9** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-586">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-586">Requirement</span></span> | <span data-ttu-id="8ca0e-587">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-587">Value</span></span> |
|-------------------|---------------|
| <span data-ttu-id="8ca0e-588">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-588">Name</span></span>              | <span data-ttu-id="8ca0e-589">wtls9</span><span class="sxs-lookup"><span data-stu-id="8ca0e-589">wtls9</span></span>         |
| <span data-ttu-id="8ca0e-590">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-590">Standard</span></span>          | <span data-ttu-id="8ca0e-591">WTLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-591">WTLS</span></span>          |
| <span data-ttu-id="8ca0e-592">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-592">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-593">160</span><span class="sxs-lookup"><span data-stu-id="8ca0e-593">160</span></span>           |
| <span data-ttu-id="8ca0e-594">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-594">TLS capable</span></span>       | <span data-ttu-id="8ca0e-595">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-595">No</span></span>            |
| <span data-ttu-id="8ca0e-596">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-596">Object identifier</span></span> | <span data-ttu-id="8ca0e-597">2.23.43.1.4.9</span><span class="sxs-lookup"><span data-stu-id="8ca0e-597">2.23.43.1.4.9</span></span> |



 

<span data-ttu-id="8ca0e-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P192V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT\_ECC\_CURVE\_X962P192V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-599">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-599">Requirement</span></span> | <span data-ttu-id="8ca0e-600">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-600">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="8ca0e-601">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-601">Name</span></span>              | <span data-ttu-id="8ca0e-602">x962P192v1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-602">x962P192v1</span></span>          |
| <span data-ttu-id="8ca0e-603">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-603">Standard</span></span>          | <span data-ttu-id="8ca0e-604">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="8ca0e-604">ANSI X9.62</span></span>          |
| <span data-ttu-id="8ca0e-605">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-605">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-606">192</span><span class="sxs-lookup"><span data-stu-id="8ca0e-606">192</span></span>                 |
| <span data-ttu-id="8ca0e-607">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-607">TLS capable</span></span>       | <span data-ttu-id="8ca0e-608">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-608">No</span></span>                  |
| <span data-ttu-id="8ca0e-609">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-609">Object identifier</span></span> | <span data-ttu-id="8ca0e-610">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-610">1.2.840.10045.3.1.1</span></span> |



 

<span data-ttu-id="8ca0e-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P192V2**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P192V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-612">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-612">Requirement</span></span> | <span data-ttu-id="8ca0e-613">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-613">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="8ca0e-614">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-614">Name</span></span>              | <span data-ttu-id="8ca0e-615">x962P192v2</span><span class="sxs-lookup"><span data-stu-id="8ca0e-615">x962P192v2</span></span>          |
| <span data-ttu-id="8ca0e-616">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-616">Standard</span></span>          | <span data-ttu-id="8ca0e-617">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="8ca0e-617">ANSI X9.62</span></span>          |
| <span data-ttu-id="8ca0e-618">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-618">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-619">192</span><span class="sxs-lookup"><span data-stu-id="8ca0e-619">192</span></span>                 |
| <span data-ttu-id="8ca0e-620">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-620">TLS capable</span></span>       | <span data-ttu-id="8ca0e-621">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-621">No</span></span>                  |
| <span data-ttu-id="8ca0e-622">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-622">Object identifier</span></span> | <span data-ttu-id="8ca0e-623">1.2.840.10045.3.1.2</span><span class="sxs-lookup"><span data-stu-id="8ca0e-623">1.2.840.10045.3.1.2</span></span> |



 

<span data-ttu-id="8ca0e-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P192V3**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT\_ECC\_CURVE\_X962P192V3**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-625">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-625">Requirement</span></span> | <span data-ttu-id="8ca0e-626">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-626">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="8ca0e-627">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-627">Name</span></span>              | <span data-ttu-id="8ca0e-628">x962P192v3</span><span class="sxs-lookup"><span data-stu-id="8ca0e-628">x962P192v3</span></span>          |
| <span data-ttu-id="8ca0e-629">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-629">Standard</span></span>          | <span data-ttu-id="8ca0e-630">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="8ca0e-630">ANSI X9.62</span></span>          |
| <span data-ttu-id="8ca0e-631">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-631">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-632">192</span><span class="sxs-lookup"><span data-stu-id="8ca0e-632">192</span></span>                 |
| <span data-ttu-id="8ca0e-633">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-633">TLS capable</span></span>       | <span data-ttu-id="8ca0e-634">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-634">No</span></span>                  |
| <span data-ttu-id="8ca0e-635">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-635">Object identifier</span></span> | <span data-ttu-id="8ca0e-636">1.2.840.10045.3.1.3</span><span class="sxs-lookup"><span data-stu-id="8ca0e-636">1.2.840.10045.3.1.3</span></span> |



 

<span data-ttu-id="8ca0e-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-638">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-638">Requirement</span></span> | <span data-ttu-id="8ca0e-639">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-639">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="8ca0e-640">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-640">Name</span></span>              | <span data-ttu-id="8ca0e-641">x962P239v1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-641">x962P239v1</span></span>          |
| <span data-ttu-id="8ca0e-642">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-642">Standard</span></span>          | <span data-ttu-id="8ca0e-643">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="8ca0e-643">ANSI X9.62</span></span>          |
| <span data-ttu-id="8ca0e-644">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-644">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-645">239</span><span class="sxs-lookup"><span data-stu-id="8ca0e-645">239</span></span>                 |
| <span data-ttu-id="8ca0e-646">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-646">TLS capable</span></span>       | <span data-ttu-id="8ca0e-647">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-647">No</span></span>                  |
| <span data-ttu-id="8ca0e-648">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-648">Object identifier</span></span> | <span data-ttu-id="8ca0e-649">1.2.840.10045.3.1.4</span><span class="sxs-lookup"><span data-stu-id="8ca0e-649">1.2.840.10045.3.1.4</span></span> |



 

<span data-ttu-id="8ca0e-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V2**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-651">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-651">Requirement</span></span> | <span data-ttu-id="8ca0e-652">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-652">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="8ca0e-653">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-653">Name</span></span>              | <span data-ttu-id="8ca0e-654">x962P239v2</span><span class="sxs-lookup"><span data-stu-id="8ca0e-654">x962P239v2</span></span>          |
| <span data-ttu-id="8ca0e-655">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-655">Standard</span></span>          | <span data-ttu-id="8ca0e-656">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="8ca0e-656">ANSI X9.62</span></span>          |
| <span data-ttu-id="8ca0e-657">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-657">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-658">239</span><span class="sxs-lookup"><span data-stu-id="8ca0e-658">239</span></span>                 |
| <span data-ttu-id="8ca0e-659">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-659">TLS capable</span></span>       | <span data-ttu-id="8ca0e-660">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-660">No</span></span>                  |
| <span data-ttu-id="8ca0e-661">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-661">Object identifier</span></span> | <span data-ttu-id="8ca0e-662">1.2.840.10045.3.1.5</span><span class="sxs-lookup"><span data-stu-id="8ca0e-662">1.2.840.10045.3.1.5</span></span> |



 

<span data-ttu-id="8ca0e-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V3**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V3** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-664">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-664">Requirement</span></span> | <span data-ttu-id="8ca0e-665">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-665">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="8ca0e-666">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-666">Name</span></span>              | <span data-ttu-id="8ca0e-667">x962P239v3</span><span class="sxs-lookup"><span data-stu-id="8ca0e-667">x962P239v3</span></span>          |
| <span data-ttu-id="8ca0e-668">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-668">Standard</span></span>          | <span data-ttu-id="8ca0e-669">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="8ca0e-669">ANSI X9.62</span></span>          |
| <span data-ttu-id="8ca0e-670">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-670">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-671">239</span><span class="sxs-lookup"><span data-stu-id="8ca0e-671">239</span></span>                 |
| <span data-ttu-id="8ca0e-672">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-672">TLS capable</span></span>       | <span data-ttu-id="8ca0e-673">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-673">No</span></span>                  |
| <span data-ttu-id="8ca0e-674">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-674">Object identifier</span></span> | <span data-ttu-id="8ca0e-675">1.2.840.10045.3.1.6</span><span class="sxs-lookup"><span data-stu-id="8ca0e-675">1.2.840.10045.3.1.6</span></span> |



 

<span data-ttu-id="8ca0e-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P256V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="8ca0e-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT\_ECC\_CURVE\_X962P256V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="8ca0e-677">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-677">Requirement</span></span> | <span data-ttu-id="8ca0e-678">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-678">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="8ca0e-679">名稱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-679">Name</span></span>              | <span data-ttu-id="8ca0e-680">x962P256v1</span><span class="sxs-lookup"><span data-stu-id="8ca0e-680">x962P256v1</span></span>          |
| <span data-ttu-id="8ca0e-681">標準</span><span class="sxs-lookup"><span data-stu-id="8ca0e-681">Standard</span></span>          | <span data-ttu-id="8ca0e-682">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="8ca0e-682">ANSI X9.62</span></span>          |
| <span data-ttu-id="8ca0e-683">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="8ca0e-683">Key size (bits)</span></span>   | <span data-ttu-id="8ca0e-684">256</span><span class="sxs-lookup"><span data-stu-id="8ca0e-684">256</span></span>                 |
| <span data-ttu-id="8ca0e-685">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="8ca0e-685">TLS capable</span></span>       | <span data-ttu-id="8ca0e-686">No</span><span class="sxs-lookup"><span data-stu-id="8ca0e-686">No</span></span>                  |
| <span data-ttu-id="8ca0e-687">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="8ca0e-687">Object identifier</span></span> | <span data-ttu-id="8ca0e-688">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="8ca0e-688">1.2.840.10045.3.1.7</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ca0e-689">備註</span><span class="sxs-lookup"><span data-stu-id="8ca0e-689">Remarks</span></span>

<span data-ttu-id="8ca0e-690">若要使用命名曲線，請使用 **BCRYPT \_ ECDSA \_ 演算法** 或 **BCRYPT \_ ECDH \_ 演算法** 來呼叫 [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) ，作為演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ca0e-690">To use a named curve, call [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) using either the **BCRYPT\_ECDSA\_ALGORITHM** or the **BCRYPT\_ECDH\_ALGORITHM** as the algorithm ID.</span></span> <span data-ttu-id="8ca0e-691">然後，呼叫 [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) ，並將 [ **BCRYPT \_ ECC \_ 曲線 \_ 名稱** ] 屬性設定為上述其中一個曲線或任何已在電腦上註冊的命名曲線，如命令所示 `certutil -displayEccCurve` 。</span><span class="sxs-lookup"><span data-stu-id="8ca0e-691">Then, call [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) and set the **BCRYPT\_ECC\_CURVE\_NAME** property to one of the above curves or any named curves registered on the computer as shown by the `certutil -displayEccCurve` command.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca0e-692">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-692">Requirements</span></span>



| <span data-ttu-id="8ca0e-693">需求</span><span class="sxs-lookup"><span data-stu-id="8ca0e-693">Requirement</span></span> | <span data-ttu-id="8ca0e-694">值</span><span class="sxs-lookup"><span data-stu-id="8ca0e-694">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca0e-695">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ca0e-695">Minimum supported client</span></span><br/> | <span data-ttu-id="8ca0e-696">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ca0e-696">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8ca0e-697">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ca0e-697">Minimum supported server</span></span><br/> | <span data-ttu-id="8ca0e-698">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ca0e-698">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8ca0e-699">標頭</span><span class="sxs-lookup"><span data-stu-id="8ca0e-699">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ca0e-700"><dt>Bcrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ca0e-700"><dt>Bcrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ca0e-701">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ca0e-701">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca0e-702">**BCryptOpenAlgorithmProvider**</span><span class="sxs-lookup"><span data-stu-id="8ca0e-702">**BCryptOpenAlgorithmProvider**</span></span>](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[<span data-ttu-id="8ca0e-703">**NCryptCreatePersistedKey**</span><span class="sxs-lookup"><span data-stu-id="8ca0e-703">**NCryptCreatePersistedKey**</span></span>](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




