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
# <a name="cng-named-elliptic-curves"></a><span data-ttu-id="2f3c0-103">CNG 命名橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="2f3c0-103">CNG Named Elliptic Curves</span></span>

<span data-ttu-id="2f3c0-104">從 Windows 10 開始，CNG 提供下列命名橢圓曲線的支援 (ANSI X x9.62、X 9.63、FIPS 186-2) 。</span><span class="sxs-lookup"><span data-stu-id="2f3c0-104">Beginning in Windows 10, CNG provides support for the following named elliptic curves (ANSI X9.62, X9.63, FIPS 186-2).</span></span>

<dl> <span data-ttu-id="2f3c0-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT \_ ECC \_ 曲線 \_ 25519**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-105"><dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT\_ECC\_CURVE\_25519**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-106">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-106">Requirement</span></span> | <span data-ttu-id="2f3c0-107">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-107">Value</span></span> |
|-------------------|-------------------------------------------------------------|
| <span data-ttu-id="2f3c0-108">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-108">Name</span></span>              | <span data-ttu-id="2f3c0-109">curve25519</span><span class="sxs-lookup"><span data-stu-id="2f3c0-109">curve25519</span></span>                                                  |
| <span data-ttu-id="2f3c0-110">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-110">Standard</span></span>          | [<span data-ttu-id="2f3c0-111">曲線25519</span><span class="sxs-lookup"><span data-stu-id="2f3c0-111">Curve 25519</span></span>](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| <span data-ttu-id="2f3c0-112">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-112">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-113">255</span><span class="sxs-lookup"><span data-stu-id="2f3c0-113">255</span></span>                                                         |
| <span data-ttu-id="2f3c0-114">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-114">TLS capable</span></span>       |                                                             |
| <span data-ttu-id="2f3c0-115">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-115">Object identifier</span></span> | <span data-ttu-id="2f3c0-116">無</span><span class="sxs-lookup"><span data-stu-id="2f3c0-116">None</span></span>                                                        |



 

<span data-ttu-id="2f3c0-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-117"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-118">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-118">Requirement</span></span> | <span data-ttu-id="2f3c0-119">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-119">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-120">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-120">Name</span></span>              | <span data-ttu-id="2f3c0-121">brainpoolP160r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-121">brainpoolP160r1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-122">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-122">Standard</span></span>          | [<span data-ttu-id="2f3c0-123">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-123">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-124">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-124">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-125">160</span><span class="sxs-lookup"><span data-stu-id="2f3c0-125">160</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-126">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-126">TLS capable</span></span>       | <span data-ttu-id="2f3c0-127">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-127">No</span></span>                                                                                                                |
| <span data-ttu-id="2f3c0-128">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-128">Object identifier</span></span> | <span data-ttu-id="2f3c0-129">1.3.36.3.3.2.8.1.1.1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-129">1.3.36.3.3.2.8.1.1.1</span></span>                                                                                              |



 

<span data-ttu-id="2f3c0-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ BRAINPOOLP160T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-130"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP160T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-131">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-131">Requirement</span></span> | <span data-ttu-id="2f3c0-132">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-133">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-133">Name</span></span>              | <span data-ttu-id="2f3c0-134">brainpoolP160t1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-134">brainpoolP160t1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-135">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-135">Standard</span></span>          | [<span data-ttu-id="2f3c0-136">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-136">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-137">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-137">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-138">160</span><span class="sxs-lookup"><span data-stu-id="2f3c0-138">160</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-139">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-139">TLS capable</span></span>       | <span data-ttu-id="2f3c0-140">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-140">No</span></span>                                                                                                                |
| <span data-ttu-id="2f3c0-141">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-141">Object identifier</span></span> | <span data-ttu-id="2f3c0-142">1.3.36.3.3.2.8.1.1.2</span><span class="sxs-lookup"><span data-stu-id="2f3c0-142">1.3.36.3.3.2.8.1.1.2</span></span>                                                                                              |



 

<span data-ttu-id="2f3c0-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP192R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-143"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-144">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-144">Requirement</span></span> | <span data-ttu-id="2f3c0-145">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-145">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-146">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-146">Name</span></span>              | <span data-ttu-id="2f3c0-147">brainpoolP192r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-147">brainpoolP192r1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-148">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-148">Standard</span></span>          | [<span data-ttu-id="2f3c0-149">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-149">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-150">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-150">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-151">192</span><span class="sxs-lookup"><span data-stu-id="2f3c0-151">192</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-152">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-152">TLS capable</span></span>       | <span data-ttu-id="2f3c0-153">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-153">No</span></span>                                                                                                                |
| <span data-ttu-id="2f3c0-154">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-154">Object identifier</span></span> | <span data-ttu-id="2f3c0-155">1.3.36.3.3.2.8.1.1.3</span><span class="sxs-lookup"><span data-stu-id="2f3c0-155">1.3.36.3.3.2.8.1.1.3</span></span>                                                                                              |



 

<span data-ttu-id="2f3c0-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP192T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-156"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP192T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-157">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-157">Requirement</span></span> | <span data-ttu-id="2f3c0-158">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-158">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-159">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-159">Name</span></span>              | <span data-ttu-id="2f3c0-160">brainpoolP192t1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-160">brainpoolP192t1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-161">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-161">Standard</span></span>          | [<span data-ttu-id="2f3c0-162">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-162">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-163">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-163">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-164">192</span><span class="sxs-lookup"><span data-stu-id="2f3c0-164">192</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-165">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-165">TLS capable</span></span>       | <span data-ttu-id="2f3c0-166">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-166">No</span></span>                                                                                                                |
| <span data-ttu-id="2f3c0-167">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-167">Object identifier</span></span> | <span data-ttu-id="2f3c0-168">1.3.36.3.3.2.8.1.1.4</span><span class="sxs-lookup"><span data-stu-id="2f3c0-168">1.3.36.3.3.2.8.1.1.4</span></span>                                                                                              |



 

<span data-ttu-id="2f3c0-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP224R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-169"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-170">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-170">Requirement</span></span> | <span data-ttu-id="2f3c0-171">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-171">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-172">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-172">Name</span></span>              | <span data-ttu-id="2f3c0-173">brainpoolP224r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-173">brainpoolP224r1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-174">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-174">Standard</span></span>          | [<span data-ttu-id="2f3c0-175">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-175">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-176">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-176">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-177">224</span><span class="sxs-lookup"><span data-stu-id="2f3c0-177">224</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-178">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-178">TLS capable</span></span>       | <span data-ttu-id="2f3c0-179">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-179">No</span></span>                                                                                                                |
| <span data-ttu-id="2f3c0-180">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-180">Object identifier</span></span> | <span data-ttu-id="2f3c0-181">1.3.36.3.3.2.8.1.1.5</span><span class="sxs-lookup"><span data-stu-id="2f3c0-181">1.3.36.3.3.2.8.1.1.5</span></span>                                                                                              |



 

<span data-ttu-id="2f3c0-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP224T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-182"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP224T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-183">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-183">Requirement</span></span> | <span data-ttu-id="2f3c0-184">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-184">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-185">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-185">Name</span></span>              | <span data-ttu-id="2f3c0-186">brainpoolP224t1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-186">brainpoolP224t1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-187">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-187">Standard</span></span>          | [<span data-ttu-id="2f3c0-188">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-188">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-189">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-189">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-190">224</span><span class="sxs-lookup"><span data-stu-id="2f3c0-190">224</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-191">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-191">TLS capable</span></span>       | <span data-ttu-id="2f3c0-192">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-192">No</span></span>                                                                                                                |
| <span data-ttu-id="2f3c0-193">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-193">Object identifier</span></span> | <span data-ttu-id="2f3c0-194">1.3.36.3.3.2.8.1.1.6</span><span class="sxs-lookup"><span data-stu-id="2f3c0-194">1.3.36.3.3.2.8.1.1.6</span></span>                                                                                              |



 

<span data-ttu-id="2f3c0-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP256R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-195"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-196">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-196">Requirement</span></span> | <span data-ttu-id="2f3c0-197">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-197">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-198">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-198">Name</span></span>              | <span data-ttu-id="2f3c0-199">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-199">brainpoolP256r1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-200">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-200">Standard</span></span>          | [<span data-ttu-id="2f3c0-201">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-201">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-202">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-202">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-203">256</span><span class="sxs-lookup"><span data-stu-id="2f3c0-203">256</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-204">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-204">TLS capable</span></span>       | <span data-ttu-id="2f3c0-205">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-205">Yes</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-206">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-206">Object identifier</span></span> | <span data-ttu-id="2f3c0-207">1.3.36.3.3.2.8.1.1.7</span><span class="sxs-lookup"><span data-stu-id="2f3c0-207">1.3.36.3.3.2.8.1.1.7</span></span>                                                                                              |



 

<span data-ttu-id="2f3c0-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP256T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-208"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP256T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-209">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-209">Requirement</span></span> | <span data-ttu-id="2f3c0-210">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-210">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-211">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-211">Name</span></span>              | <span data-ttu-id="2f3c0-212">brainpoolP256t1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-212">brainpoolP256t1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-213">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-213">Standard</span></span>          | [<span data-ttu-id="2f3c0-214">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-214">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-215">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-215">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-216">256</span><span class="sxs-lookup"><span data-stu-id="2f3c0-216">256</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-217">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-217">TLS capable</span></span>       | <span data-ttu-id="2f3c0-218">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-218">No</span></span>                                                                                                                |
| <span data-ttu-id="2f3c0-219">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-219">Object identifier</span></span> | <span data-ttu-id="2f3c0-220">1.3.36.3.3.2.8.1.1.8</span><span class="sxs-lookup"><span data-stu-id="2f3c0-220">1.3.36.3.3.2.8.1.1.8</span></span>                                                                                              |



 

<span data-ttu-id="2f3c0-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP320R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-221"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP320R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-222">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-222">Requirement</span></span> | <span data-ttu-id="2f3c0-223">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-223">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-224">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-224">Name</span></span>              | <span data-ttu-id="2f3c0-225">brainpoolP320r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-225">brainpoolP320r1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-226">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-226">Standard</span></span>          | [<span data-ttu-id="2f3c0-227">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-227">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-228">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-228">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-229">320</span><span class="sxs-lookup"><span data-stu-id="2f3c0-229">320</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-230">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-230">TLS capable</span></span>       | <span data-ttu-id="2f3c0-231">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-231">No</span></span>                                                                                                                |
| <span data-ttu-id="2f3c0-232">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-232">Object identifier</span></span> | <span data-ttu-id="2f3c0-233">1.3.36.3.3.2.8.1.1.9</span><span class="sxs-lookup"><span data-stu-id="2f3c0-233">1.3.36.3.3.2.8.1.1.9</span></span>                                                                                              |



 

<span data-ttu-id="2f3c0-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP32 0T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-234"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP32 0T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-235">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-235">Requirement</span></span> | <span data-ttu-id="2f3c0-236">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-236">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-237">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-237">Name</span></span>              | <span data-ttu-id="2f3c0-238">brainpoolP320t1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-238">brainpoolP320t1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-239">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-239">Standard</span></span>          | [<span data-ttu-id="2f3c0-240">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-240">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-241">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-241">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-242">320</span><span class="sxs-lookup"><span data-stu-id="2f3c0-242">320</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-243">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-243">TLS capable</span></span>       | <span data-ttu-id="2f3c0-244">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-244">No</span></span>                                                                                                                |
| <span data-ttu-id="2f3c0-245">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-245">Object identifier</span></span> | <span data-ttu-id="2f3c0-246">1.3.36.3.3.2.8.1.1.10</span><span class="sxs-lookup"><span data-stu-id="2f3c0-246">1.3.36.3.3.2.8.1.1.10</span></span>                                                                                             |



 

<span data-ttu-id="2f3c0-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ BRAINPOOLP384R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-247"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-248">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-248">Requirement</span></span> | <span data-ttu-id="2f3c0-249">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-249">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-250">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-250">Name</span></span>              | <span data-ttu-id="2f3c0-251">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-251">brainpoolP384r1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-252">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-252">Standard</span></span>          | [<span data-ttu-id="2f3c0-253">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-253">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-254">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-254">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-255">384</span><span class="sxs-lookup"><span data-stu-id="2f3c0-255">384</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-256">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-256">TLS capable</span></span>       | <span data-ttu-id="2f3c0-257">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-257">Yes</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-258">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-258">Object identifier</span></span> | <span data-ttu-id="2f3c0-259">1.3.36.3.3.2.8.1.1.11</span><span class="sxs-lookup"><span data-stu-id="2f3c0-259">1.3.36.3.3.2.8.1.1.11</span></span>                                                                                             |



 

<span data-ttu-id="2f3c0-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP384T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-260"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP384T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-261">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-261">Requirement</span></span> | <span data-ttu-id="2f3c0-262">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-262">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-263">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-263">Name</span></span>              | <span data-ttu-id="2f3c0-264">brainpoolP384t1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-264">brainpoolP384t1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-265">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-265">Standard</span></span>          | [<span data-ttu-id="2f3c0-266">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-266">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-267">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-267">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-268">384</span><span class="sxs-lookup"><span data-stu-id="2f3c0-268">384</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-269">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-269">TLS capable</span></span>       | <span data-ttu-id="2f3c0-270">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-270">No</span></span>                                                                                                                |
| <span data-ttu-id="2f3c0-271">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-271">Object identifier</span></span> | <span data-ttu-id="2f3c0-272">1.3.36.3.3.2.8.1.1.12</span><span class="sxs-lookup"><span data-stu-id="2f3c0-272">1.3.36.3.3.2.8.1.1.12</span></span>                                                                                             |



 

<span data-ttu-id="2f3c0-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP512R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-273"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-274">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-274">Requirement</span></span> | <span data-ttu-id="2f3c0-275">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-275">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-276">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-276">Name</span></span>              | <span data-ttu-id="2f3c0-277">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-277">brainpoolP512r1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-278">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-278">Standard</span></span>          | [<span data-ttu-id="2f3c0-279">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-279">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-280">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-280">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-281">512</span><span class="sxs-lookup"><span data-stu-id="2f3c0-281">512</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-282">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-282">TLS capable</span></span>       | <span data-ttu-id="2f3c0-283">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-283">Yes</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-284">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-284">Object identifier</span></span> | <span data-ttu-id="2f3c0-285">1.3.36.3.3.2.8.1.1.13</span><span class="sxs-lookup"><span data-stu-id="2f3c0-285">1.3.36.3.3.2.8.1.1.13</span></span>                                                                                             |



 

<span data-ttu-id="2f3c0-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP512T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-286"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT\_ECC\_CURVE\_BRAINPOOLP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-287">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-287">Requirement</span></span> | <span data-ttu-id="2f3c0-288">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-288">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-289">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-289">Name</span></span>              | <span data-ttu-id="2f3c0-290">brainpoolP512t1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-290">brainpoolP512t1</span></span>                                                                                                   |
| <span data-ttu-id="2f3c0-291">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-291">Standard</span></span>          | [<span data-ttu-id="2f3c0-292">ECC Brainpool 標準曲線和曲線產生</span><span class="sxs-lookup"><span data-stu-id="2f3c0-292">ECC Brainpool Standard Curves and Curve Generation</span></span>](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| <span data-ttu-id="2f3c0-293">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-293">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-294">512</span><span class="sxs-lookup"><span data-stu-id="2f3c0-294">512</span></span>                                                                                                               |
| <span data-ttu-id="2f3c0-295">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-295">TLS capable</span></span>       | <span data-ttu-id="2f3c0-296">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-296">No</span></span>                                                                                                                |
| <span data-ttu-id="2f3c0-297">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-297">Object identifier</span></span> | <span data-ttu-id="2f3c0-298">1.3.36.3.3.2.8.1.1.14</span><span class="sxs-lookup"><span data-stu-id="2f3c0-298">1.3.36.3.3.2.8.1.1.14</span></span>                                                                                             |



 

<span data-ttu-id="2f3c0-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ECC \_ 曲線 \_ EC192WAPI**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-299"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT\_ECC\_CURVE\_EC192WAPI** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-300">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-300">Requirement</span></span> | <span data-ttu-id="2f3c0-301">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-301">Value</span></span> |
|-------------------|----------------------------------------------------------------|
| <span data-ttu-id="2f3c0-302">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-302">Name</span></span>              | <span data-ttu-id="2f3c0-303">ec192wapi</span><span class="sxs-lookup"><span data-stu-id="2f3c0-303">ec192wapi</span></span>                                                      |
| <span data-ttu-id="2f3c0-304">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-304">Standard</span></span>          | <span data-ttu-id="2f3c0-305">國際區域網路的中文標準 (GB 15629.11-2003) </span><span class="sxs-lookup"><span data-stu-id="2f3c0-305">Chinese National Standard for Wireless LANs (GB 15629.11-2003)</span></span> |
| <span data-ttu-id="2f3c0-306">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-306">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-307">192</span><span class="sxs-lookup"><span data-stu-id="2f3c0-307">192</span></span>                                                            |
| <span data-ttu-id="2f3c0-308">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-308">TLS capable</span></span>       | <span data-ttu-id="2f3c0-309">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-309">No</span></span>                                                             |
| <span data-ttu-id="2f3c0-310">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-310">Object identifier</span></span> | <span data-ttu-id="2f3c0-311">1.2.156.11235.1.1.2.1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-311">1.2.156.11235.1.1.2.1</span></span>                                          |



 

<span data-ttu-id="2f3c0-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP192**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-312"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT\_ECC\_CURVE\_NISTP192**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-313">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-313">Requirement</span></span> | <span data-ttu-id="2f3c0-314">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-314">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-315">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-315">Name</span></span>              | <span data-ttu-id="2f3c0-316">nistP192</span><span class="sxs-lookup"><span data-stu-id="2f3c0-316">nistP192</span></span>                                                                                                                     |
| <span data-ttu-id="2f3c0-317">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-317">Standard</span></span>          | [<span data-ttu-id="2f3c0-318">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="2f3c0-318">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="2f3c0-319">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-319">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-320">192</span><span class="sxs-lookup"><span data-stu-id="2f3c0-320">192</span></span>                                                                                                                          |
| <span data-ttu-id="2f3c0-321">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-321">TLS capable</span></span>       | <span data-ttu-id="2f3c0-322">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-322">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="2f3c0-323">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-323">Object identifier</span></span> | <span data-ttu-id="2f3c0-324">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-324">1.2.840.10045.3.1.1</span></span>                                                                                                          |



 

<span data-ttu-id="2f3c0-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ECC \_ 曲線 \_ NISTP224**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-325"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT\_ECC\_CURVE\_NISTP224** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-326">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-326">Requirement</span></span> | <span data-ttu-id="2f3c0-327">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-327">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-328">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-328">Name</span></span>              | <span data-ttu-id="2f3c0-329">nistP224</span><span class="sxs-lookup"><span data-stu-id="2f3c0-329">nistP224</span></span>                                                                                                                     |
| <span data-ttu-id="2f3c0-330">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-330">Standard</span></span>          | [<span data-ttu-id="2f3c0-331">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="2f3c0-331">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="2f3c0-332">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-332">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-333">224</span><span class="sxs-lookup"><span data-stu-id="2f3c0-333">224</span></span>                                                                                                                          |
| <span data-ttu-id="2f3c0-334">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-334">TLS capable</span></span>       | <span data-ttu-id="2f3c0-335">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-335">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="2f3c0-336">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-336">Object identifier</span></span> | <span data-ttu-id="2f3c0-337">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="2f3c0-337">1.3.132.0.33</span></span>                                                                                                                 |



 

<span data-ttu-id="2f3c0-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP256**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-338"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT\_ECC\_CURVE\_NISTP256**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-339">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-339">Requirement</span></span> | <span data-ttu-id="2f3c0-340">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-340">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-341">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-341">Name</span></span>              | <span data-ttu-id="2f3c0-342">nistP256</span><span class="sxs-lookup"><span data-stu-id="2f3c0-342">nistP256</span></span>                                                                                                                     |
| <span data-ttu-id="2f3c0-343">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-343">Standard</span></span>          | [<span data-ttu-id="2f3c0-344">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="2f3c0-344">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="2f3c0-345">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-345">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-346">256</span><span class="sxs-lookup"><span data-stu-id="2f3c0-346">256</span></span>                                                                                                                          |
| <span data-ttu-id="2f3c0-347">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-347">TLS capable</span></span>       | <span data-ttu-id="2f3c0-348">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-348">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="2f3c0-349">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-349">Object identifier</span></span> | <span data-ttu-id="2f3c0-350">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="2f3c0-350">1.2.840.10045.3.1.7</span></span>                                                                                                          |



 

<span data-ttu-id="2f3c0-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ECC \_ 曲線 \_ NISTP384**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-351"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT\_ECC\_CURVE\_NISTP384** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-352">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-352">Requirement</span></span> | <span data-ttu-id="2f3c0-353">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-353">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-354">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-354">Name</span></span>              | <span data-ttu-id="2f3c0-355">nistP384</span><span class="sxs-lookup"><span data-stu-id="2f3c0-355">nistP384</span></span>                                                                                                                     |
| <span data-ttu-id="2f3c0-356">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-356">Standard</span></span>          | [<span data-ttu-id="2f3c0-357">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="2f3c0-357">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="2f3c0-358">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-358">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-359">384</span><span class="sxs-lookup"><span data-stu-id="2f3c0-359">384</span></span>                                                                                                                          |
| <span data-ttu-id="2f3c0-360">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-360">TLS capable</span></span>       | <span data-ttu-id="2f3c0-361">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-361">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="2f3c0-362">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-362">Object identifier</span></span> | <span data-ttu-id="2f3c0-363">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="2f3c0-363">1.3.132.0.34</span></span>                                                                                                                 |



 

<span data-ttu-id="2f3c0-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP521**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-364"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT\_ECC\_CURVE\_NISTP521**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-365">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-365">Requirement</span></span> | <span data-ttu-id="2f3c0-366">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-366">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-367">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-367">Name</span></span>              | <span data-ttu-id="2f3c0-368">nistP521</span><span class="sxs-lookup"><span data-stu-id="2f3c0-368">nistP521</span></span>                                                                                                                     |
| <span data-ttu-id="2f3c0-369">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-369">Standard</span></span>          | [<span data-ttu-id="2f3c0-370">聯邦政府使用的建議橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="2f3c0-370">Recommended Elliptic Curves for Federal Government Use</span></span>](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| <span data-ttu-id="2f3c0-371">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-371">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-372">521</span><span class="sxs-lookup"><span data-stu-id="2f3c0-372">521</span></span>                                                                                                                          |
| <span data-ttu-id="2f3c0-373">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-373">TLS capable</span></span>       | <span data-ttu-id="2f3c0-374">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-374">Yes</span></span>                                                                                                                          |
| <span data-ttu-id="2f3c0-375">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-375">Object identifier</span></span> | <span data-ttu-id="2f3c0-376">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="2f3c0-376">1.3.132.0.35</span></span>                                                                                                                 |



 

<span data-ttu-id="2f3c0-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ NUMSP256T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-377"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP256T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-378">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-378">Requirement</span></span> | <span data-ttu-id="2f3c0-379">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-379">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-380">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-380">Name</span></span>              | <span data-ttu-id="2f3c0-381">numsP256t1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-381">numsP256t1</span></span>                                                                                                                              |
| <span data-ttu-id="2f3c0-382">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-382">Standard</span></span>          | [<span data-ttu-id="2f3c0-383">MSR ECCLib 中的曲線選取和支援曲線參數規格</span><span class="sxs-lookup"><span data-stu-id="2f3c0-383">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="2f3c0-384">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-384">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-385">256</span><span class="sxs-lookup"><span data-stu-id="2f3c0-385">256</span></span>                                                                                                                                     |
| <span data-ttu-id="2f3c0-386">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-386">TLS capable</span></span>       | <span data-ttu-id="2f3c0-387">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-387">No</span></span>                                                                                                                                      |
| <span data-ttu-id="2f3c0-388">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-388">Object identifier</span></span> | <span data-ttu-id="2f3c0-389">無</span><span class="sxs-lookup"><span data-stu-id="2f3c0-389">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="2f3c0-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ NUMSP384T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-390"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT\_ECC\_CURVE\_NUMSP384T1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-391">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-391">Requirement</span></span> | <span data-ttu-id="2f3c0-392">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-392">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-393">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-393">Name</span></span>              | <span data-ttu-id="2f3c0-394">numsP384t1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-394">numsP384t1</span></span>                                                                                                                              |
| <span data-ttu-id="2f3c0-395">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-395">Standard</span></span>          | [<span data-ttu-id="2f3c0-396">MSR ECCLib 中的曲線選取和支援曲線參數規格</span><span class="sxs-lookup"><span data-stu-id="2f3c0-396">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="2f3c0-397">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-397">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-398">384</span><span class="sxs-lookup"><span data-stu-id="2f3c0-398">384</span></span>                                                                                                                                     |
| <span data-ttu-id="2f3c0-399">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-399">TLS capable</span></span>       | <span data-ttu-id="2f3c0-400">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-400">No</span></span>                                                                                                                                      |
| <span data-ttu-id="2f3c0-401">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-401">Object identifier</span></span> | <span data-ttu-id="2f3c0-402">無</span><span class="sxs-lookup"><span data-stu-id="2f3c0-402">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="2f3c0-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ NUMSP512T1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-403"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT\_ECC\_CURVE\_NUMSP512T1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-404">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-404">Requirement</span></span> | <span data-ttu-id="2f3c0-405">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-405">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-406">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-406">Name</span></span>              | <span data-ttu-id="2f3c0-407">numsP512t1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-407">numsP512t1</span></span>                                                                                                                              |
| <span data-ttu-id="2f3c0-408">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-408">Standard</span></span>          | [<span data-ttu-id="2f3c0-409">MSR ECCLib 中的曲線選取和支援曲線參數規格</span><span class="sxs-lookup"><span data-stu-id="2f3c0-409">Specification of Curve Selection and Supported Curve Parameters in MSR ECCLib</span></span>](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| <span data-ttu-id="2f3c0-410">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-410">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-411">512</span><span class="sxs-lookup"><span data-stu-id="2f3c0-411">512</span></span>                                                                                                                                     |
| <span data-ttu-id="2f3c0-412">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-412">TLS capable</span></span>       | <span data-ttu-id="2f3c0-413">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-413">No</span></span>                                                                                                                                      |
| <span data-ttu-id="2f3c0-414">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-414">Object identifier</span></span> | <span data-ttu-id="2f3c0-415">無</span><span class="sxs-lookup"><span data-stu-id="2f3c0-415">None</span></span>                                                                                                                                    |



 

<span data-ttu-id="2f3c0-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-416"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160K1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-417">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-417">Requirement</span></span> | <span data-ttu-id="2f3c0-418">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-418">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-419">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-419">Name</span></span>              | <span data-ttu-id="2f3c0-420">secP160k1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-420">secP160k1</span></span>                                                                       |
| <span data-ttu-id="2f3c0-421">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-421">Standard</span></span>          | [<span data-ttu-id="2f3c0-422">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="2f3c0-422">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2f3c0-423">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-423">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-424">160</span><span class="sxs-lookup"><span data-stu-id="2f3c0-424">160</span></span>                                                                             |
| <span data-ttu-id="2f3c0-425">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-425">TLS capable</span></span>       | <span data-ttu-id="2f3c0-426">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-426">Yes</span></span>                                                                             |
| <span data-ttu-id="2f3c0-427">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-427">Object identifier</span></span> | <span data-ttu-id="2f3c0-428">1.3.132.0.9</span><span class="sxs-lookup"><span data-stu-id="2f3c0-428">1.3.132.0.9</span></span>                                                                     |



 

<span data-ttu-id="2f3c0-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-429"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-430">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-430">Requirement</span></span> | <span data-ttu-id="2f3c0-431">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-431">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-432">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-432">Name</span></span>              | <span data-ttu-id="2f3c0-433">secP160r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-433">secP160r1</span></span>                                                                       |
| <span data-ttu-id="2f3c0-434">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-434">Standard</span></span>          | [<span data-ttu-id="2f3c0-435">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="2f3c0-435">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2f3c0-436">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-436">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-437">160</span><span class="sxs-lookup"><span data-stu-id="2f3c0-437">160</span></span>                                                                             |
| <span data-ttu-id="2f3c0-438">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-438">TLS capable</span></span>       | <span data-ttu-id="2f3c0-439">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-439">Yes</span></span>                                                                             |
| <span data-ttu-id="2f3c0-440">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-440">Object identifier</span></span> | <span data-ttu-id="2f3c0-441">1.3.132.0.8</span><span class="sxs-lookup"><span data-stu-id="2f3c0-441">1.3.132.0.8</span></span>                                                                     |



 

<span data-ttu-id="2f3c0-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-442"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP160R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-443">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-443">Requirement</span></span> | <span data-ttu-id="2f3c0-444">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-444">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-445">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-445">Name</span></span>              | <span data-ttu-id="2f3c0-446">secP160r2</span><span class="sxs-lookup"><span data-stu-id="2f3c0-446">secP160r2</span></span>                                                                       |
| <span data-ttu-id="2f3c0-447">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-447">Standard</span></span>          | [<span data-ttu-id="2f3c0-448">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="2f3c0-448">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2f3c0-449">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-449">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-450">160</span><span class="sxs-lookup"><span data-stu-id="2f3c0-450">160</span></span>                                                                             |
| <span data-ttu-id="2f3c0-451">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-451">TLS capable</span></span>       | <span data-ttu-id="2f3c0-452">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-452">Yes</span></span>                                                                             |
| <span data-ttu-id="2f3c0-453">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-453">Object identifier</span></span> | <span data-ttu-id="2f3c0-454">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="2f3c0-454">1.3.132.0.30</span></span>                                                                    |



 

<span data-ttu-id="2f3c0-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP192K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-455"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT\_ECC\_CURVE\_SECP192K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-456">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-456">Requirement</span></span> | <span data-ttu-id="2f3c0-457">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-457">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-458">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-458">Name</span></span>              | <span data-ttu-id="2f3c0-459">secP192k1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-459">secP192k1</span></span>                                                                       |
| <span data-ttu-id="2f3c0-460">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-460">Standard</span></span>          | [<span data-ttu-id="2f3c0-461">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="2f3c0-461">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2f3c0-462">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-462">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-463">192</span><span class="sxs-lookup"><span data-stu-id="2f3c0-463">192</span></span>                                                                             |
| <span data-ttu-id="2f3c0-464">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-464">TLS capable</span></span>       | <span data-ttu-id="2f3c0-465">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-465">Yes</span></span>                                                                             |
| <span data-ttu-id="2f3c0-466">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-466">Object identifier</span></span> | <span data-ttu-id="2f3c0-467">1.3.132.0.31</span><span class="sxs-lookup"><span data-stu-id="2f3c0-467">1.3.132.0.31</span></span>                                                                    |



 

<span data-ttu-id="2f3c0-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP192R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-468"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP192R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-469">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-469">Requirement</span></span> | <span data-ttu-id="2f3c0-470">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-470">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-471">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-471">Name</span></span>              | <span data-ttu-id="2f3c0-472">secP192r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-472">secP192r1</span></span>                                                                       |
| <span data-ttu-id="2f3c0-473">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-473">Standard</span></span>          | [<span data-ttu-id="2f3c0-474">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="2f3c0-474">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2f3c0-475">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-475">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-476">192</span><span class="sxs-lookup"><span data-stu-id="2f3c0-476">192</span></span>                                                                             |
| <span data-ttu-id="2f3c0-477">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-477">TLS capable</span></span>       | <span data-ttu-id="2f3c0-478">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-478">Yes</span></span>                                                                             |
| <span data-ttu-id="2f3c0-479">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-479">Object identifier</span></span> | <span data-ttu-id="2f3c0-480">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-480">1.2.840.10045.3.1.1</span></span>                                                             |



 

<span data-ttu-id="2f3c0-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP224K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-481"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT\_ECC\_CURVE\_SECP224K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-482">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-482">Requirement</span></span> | <span data-ttu-id="2f3c0-483">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-483">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-484">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-484">Name</span></span>              | <span data-ttu-id="2f3c0-485">secP224k1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-485">secP224k1</span></span>                                                                       |
| <span data-ttu-id="2f3c0-486">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-486">Standard</span></span>          | [<span data-ttu-id="2f3c0-487">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="2f3c0-487">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2f3c0-488">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-488">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-489">224</span><span class="sxs-lookup"><span data-stu-id="2f3c0-489">224</span></span>                                                                             |
| <span data-ttu-id="2f3c0-490">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-490">TLS capable</span></span>       | <span data-ttu-id="2f3c0-491">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-491">Yes</span></span>                                                                             |
| <span data-ttu-id="2f3c0-492">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-492">Object identifier</span></span> | <span data-ttu-id="2f3c0-493">1.3.132.0.32</span><span class="sxs-lookup"><span data-stu-id="2f3c0-493">1.3.132.0.32</span></span>                                                                    |



 

<span data-ttu-id="2f3c0-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP224R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-494"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT\_ECC\_CURVE\_SECP224R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-495">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-495">Requirement</span></span> | <span data-ttu-id="2f3c0-496">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-496">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-497">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-497">Name</span></span>              | <span data-ttu-id="2f3c0-498">secP224r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-498">secP224r1</span></span>                                                                       |
| <span data-ttu-id="2f3c0-499">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-499">Standard</span></span>          | [<span data-ttu-id="2f3c0-500">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="2f3c0-500">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2f3c0-501">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-501">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-502">224</span><span class="sxs-lookup"><span data-stu-id="2f3c0-502">224</span></span>                                                                             |
| <span data-ttu-id="2f3c0-503">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-503">TLS capable</span></span>       | <span data-ttu-id="2f3c0-504">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-504">Yes</span></span>                                                                             |
| <span data-ttu-id="2f3c0-505">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-505">Object identifier</span></span> | <span data-ttu-id="2f3c0-506">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="2f3c0-506">1.3.132.0.33</span></span>                                                                    |



 

<span data-ttu-id="2f3c0-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP256K1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-507"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT\_ECC\_CURVE\_SECP256K1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-508">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-508">Requirement</span></span> | <span data-ttu-id="2f3c0-509">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-509">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-510">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-510">Name</span></span>              | <span data-ttu-id="2f3c0-511">secP256k1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-511">secP256k1</span></span>                                                                       |
| <span data-ttu-id="2f3c0-512">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-512">Standard</span></span>          | [<span data-ttu-id="2f3c0-513">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="2f3c0-513">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2f3c0-514">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-514">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-515">256</span><span class="sxs-lookup"><span data-stu-id="2f3c0-515">256</span></span>                                                                             |
| <span data-ttu-id="2f3c0-516">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-516">TLS capable</span></span>       | <span data-ttu-id="2f3c0-517">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-517">Yes</span></span>                                                                             |
| <span data-ttu-id="2f3c0-518">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-518">Object identifier</span></span> | <span data-ttu-id="2f3c0-519">1.3.132.0.10</span><span class="sxs-lookup"><span data-stu-id="2f3c0-519">1.3.132.0.10</span></span>                                                                    |



 

<span data-ttu-id="2f3c0-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP256R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-520"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT\_ECC\_CURVE\_SECP256R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-521">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-521">Requirement</span></span> | <span data-ttu-id="2f3c0-522">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-522">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-523">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-523">Name</span></span>              | <span data-ttu-id="2f3c0-524">secP256r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-524">secP256r1</span></span>                                                                       |
| <span data-ttu-id="2f3c0-525">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-525">Standard</span></span>          | [<span data-ttu-id="2f3c0-526">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="2f3c0-526">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2f3c0-527">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-527">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-528">256</span><span class="sxs-lookup"><span data-stu-id="2f3c0-528">256</span></span>                                                                             |
| <span data-ttu-id="2f3c0-529">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-529">TLS capable</span></span>       | <span data-ttu-id="2f3c0-530">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-530">Yes</span></span>                                                                             |
| <span data-ttu-id="2f3c0-531">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-531">Object identifier</span></span> | <span data-ttu-id="2f3c0-532">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="2f3c0-532">1.2.840.10045.3.1.7</span></span>                                                             |



 

<span data-ttu-id="2f3c0-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP384R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-533"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT\_ECC\_CURVE\_SECP384R1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-534">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-534">Requirement</span></span> | <span data-ttu-id="2f3c0-535">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-535">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-536">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-536">Name</span></span>              | <span data-ttu-id="2f3c0-537">secP384r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-537">secP384r1</span></span>                                                                       |
| <span data-ttu-id="2f3c0-538">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-538">Standard</span></span>          | [<span data-ttu-id="2f3c0-539">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="2f3c0-539">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2f3c0-540">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-540">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-541">384</span><span class="sxs-lookup"><span data-stu-id="2f3c0-541">384</span></span>                                                                             |
| <span data-ttu-id="2f3c0-542">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-542">TLS capable</span></span>       | <span data-ttu-id="2f3c0-543">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-543">Yes</span></span>                                                                             |
| <span data-ttu-id="2f3c0-544">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-544">Object identifier</span></span> | <span data-ttu-id="2f3c0-545">1.3.132.0.34</span><span class="sxs-lookup"><span data-stu-id="2f3c0-545">1.3.132.0.34</span></span>                                                                    |



 

<span data-ttu-id="2f3c0-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP521R1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-546"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT\_ECC\_CURVE\_SECP521R1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-547">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-547">Requirement</span></span> | <span data-ttu-id="2f3c0-548">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-548">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-549">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-549">Name</span></span>              | <span data-ttu-id="2f3c0-550">secP521r1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-550">secP521r1</span></span>                                                                       |
| <span data-ttu-id="2f3c0-551">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-551">Standard</span></span>          | [<span data-ttu-id="2f3c0-552">建議的橢圓曲線網域參數</span><span class="sxs-lookup"><span data-stu-id="2f3c0-552">Recommended Elliptic Curve Domain Parameters</span></span>](https://www.secg.org/sec2-v2.pdf) |
| <span data-ttu-id="2f3c0-553">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-553">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-554">521</span><span class="sxs-lookup"><span data-stu-id="2f3c0-554">521</span></span>                                                                             |
| <span data-ttu-id="2f3c0-555">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-555">TLS capable</span></span>       | <span data-ttu-id="2f3c0-556">Yes</span><span class="sxs-lookup"><span data-stu-id="2f3c0-556">Yes</span></span>                                                                             |
| <span data-ttu-id="2f3c0-557">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-557">Object identifier</span></span> | <span data-ttu-id="2f3c0-558">1.3.132.0.35</span><span class="sxs-lookup"><span data-stu-id="2f3c0-558">1.3.132.0.35</span></span>                                                                    |



 

<span data-ttu-id="2f3c0-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT \_ ECC \_ 曲線 \_ WTLS12**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-559"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT\_ECC\_CURVE\_WTLS12**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-560">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-560">Requirement</span></span> | <span data-ttu-id="2f3c0-561">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-561">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="2f3c0-562">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-562">Name</span></span>              | <span data-ttu-id="2f3c0-563">wtls12</span><span class="sxs-lookup"><span data-stu-id="2f3c0-563">wtls12</span></span>       |
| <span data-ttu-id="2f3c0-564">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-564">Standard</span></span>          | <span data-ttu-id="2f3c0-565">WTLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-565">WTLS</span></span>         |
| <span data-ttu-id="2f3c0-566">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-566">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-567">224</span><span class="sxs-lookup"><span data-stu-id="2f3c0-567">224</span></span>          |
| <span data-ttu-id="2f3c0-568">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-568">TLS capable</span></span>       | <span data-ttu-id="2f3c0-569">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-569">No</span></span>           |
| <span data-ttu-id="2f3c0-570">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-570">Object identifier</span></span> | <span data-ttu-id="2f3c0-571">1.3.132.0.33</span><span class="sxs-lookup"><span data-stu-id="2f3c0-571">1.3.132.0.33</span></span> |



 

<span data-ttu-id="2f3c0-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT \_ ECC \_ 曲線 \_ WTLS7**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-572"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT\_ECC\_CURVE\_WTLS7**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-573">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-573">Requirement</span></span> | <span data-ttu-id="2f3c0-574">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-574">Value</span></span> |
|-------------------|--------------|
| <span data-ttu-id="2f3c0-575">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-575">Name</span></span>              | <span data-ttu-id="2f3c0-576">wtls7</span><span class="sxs-lookup"><span data-stu-id="2f3c0-576">wtls7</span></span>        |
| <span data-ttu-id="2f3c0-577">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-577">Standard</span></span>          | <span data-ttu-id="2f3c0-578">WTLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-578">WTLS</span></span>         |
| <span data-ttu-id="2f3c0-579">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-579">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-580">160</span><span class="sxs-lookup"><span data-stu-id="2f3c0-580">160</span></span>          |
| <span data-ttu-id="2f3c0-581">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-581">TLS capable</span></span>       | <span data-ttu-id="2f3c0-582">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-582">No</span></span>           |
| <span data-ttu-id="2f3c0-583">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-583">Object identifier</span></span> | <span data-ttu-id="2f3c0-584">1.3.132.0.30</span><span class="sxs-lookup"><span data-stu-id="2f3c0-584">1.3.132.0.30</span></span> |



 

<span data-ttu-id="2f3c0-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ECC \_ 曲線 \_ WTLS9**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-585"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT\_ECC\_CURVE\_WTLS9** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-586">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-586">Requirement</span></span> | <span data-ttu-id="2f3c0-587">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-587">Value</span></span> |
|-------------------|---------------|
| <span data-ttu-id="2f3c0-588">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-588">Name</span></span>              | <span data-ttu-id="2f3c0-589">wtls9</span><span class="sxs-lookup"><span data-stu-id="2f3c0-589">wtls9</span></span>         |
| <span data-ttu-id="2f3c0-590">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-590">Standard</span></span>          | <span data-ttu-id="2f3c0-591">WTLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-591">WTLS</span></span>          |
| <span data-ttu-id="2f3c0-592">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-592">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-593">160</span><span class="sxs-lookup"><span data-stu-id="2f3c0-593">160</span></span>           |
| <span data-ttu-id="2f3c0-594">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-594">TLS capable</span></span>       | <span data-ttu-id="2f3c0-595">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-595">No</span></span>            |
| <span data-ttu-id="2f3c0-596">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-596">Object identifier</span></span> | <span data-ttu-id="2f3c0-597">2.23.43.1.4.9</span><span class="sxs-lookup"><span data-stu-id="2f3c0-597">2.23.43.1.4.9</span></span> |



 

<span data-ttu-id="2f3c0-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P192V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-598"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT\_ECC\_CURVE\_X962P192V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-599">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-599">Requirement</span></span> | <span data-ttu-id="2f3c0-600">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-600">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2f3c0-601">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-601">Name</span></span>              | <span data-ttu-id="2f3c0-602">x962P192v1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-602">x962P192v1</span></span>          |
| <span data-ttu-id="2f3c0-603">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-603">Standard</span></span>          | <span data-ttu-id="2f3c0-604">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="2f3c0-604">ANSI X9.62</span></span>          |
| <span data-ttu-id="2f3c0-605">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-605">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-606">192</span><span class="sxs-lookup"><span data-stu-id="2f3c0-606">192</span></span>                 |
| <span data-ttu-id="2f3c0-607">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-607">TLS capable</span></span>       | <span data-ttu-id="2f3c0-608">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-608">No</span></span>                  |
| <span data-ttu-id="2f3c0-609">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-609">Object identifier</span></span> | <span data-ttu-id="2f3c0-610">1.2.840.10045.3.1.1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-610">1.2.840.10045.3.1.1</span></span> |



 

<span data-ttu-id="2f3c0-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P192V2**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-611"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P192V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-612">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-612">Requirement</span></span> | <span data-ttu-id="2f3c0-613">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-613">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2f3c0-614">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-614">Name</span></span>              | <span data-ttu-id="2f3c0-615">x962P192v2</span><span class="sxs-lookup"><span data-stu-id="2f3c0-615">x962P192v2</span></span>          |
| <span data-ttu-id="2f3c0-616">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-616">Standard</span></span>          | <span data-ttu-id="2f3c0-617">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="2f3c0-617">ANSI X9.62</span></span>          |
| <span data-ttu-id="2f3c0-618">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-618">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-619">192</span><span class="sxs-lookup"><span data-stu-id="2f3c0-619">192</span></span>                 |
| <span data-ttu-id="2f3c0-620">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-620">TLS capable</span></span>       | <span data-ttu-id="2f3c0-621">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-621">No</span></span>                  |
| <span data-ttu-id="2f3c0-622">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-622">Object identifier</span></span> | <span data-ttu-id="2f3c0-623">1.2.840.10045.3.1.2</span><span class="sxs-lookup"><span data-stu-id="2f3c0-623">1.2.840.10045.3.1.2</span></span> |



 

<span data-ttu-id="2f3c0-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P192V3**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-624"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT\_ECC\_CURVE\_X962P192V3**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-625">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-625">Requirement</span></span> | <span data-ttu-id="2f3c0-626">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-626">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2f3c0-627">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-627">Name</span></span>              | <span data-ttu-id="2f3c0-628">x962P192v3</span><span class="sxs-lookup"><span data-stu-id="2f3c0-628">x962P192v3</span></span>          |
| <span data-ttu-id="2f3c0-629">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-629">Standard</span></span>          | <span data-ttu-id="2f3c0-630">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="2f3c0-630">ANSI X9.62</span></span>          |
| <span data-ttu-id="2f3c0-631">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-631">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-632">192</span><span class="sxs-lookup"><span data-stu-id="2f3c0-632">192</span></span>                 |
| <span data-ttu-id="2f3c0-633">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-633">TLS capable</span></span>       | <span data-ttu-id="2f3c0-634">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-634">No</span></span>                  |
| <span data-ttu-id="2f3c0-635">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-635">Object identifier</span></span> | <span data-ttu-id="2f3c0-636">1.2.840.10045.3.1.3</span><span class="sxs-lookup"><span data-stu-id="2f3c0-636">1.2.840.10045.3.1.3</span></span> |



 

<span data-ttu-id="2f3c0-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-637"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V1** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-638">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-638">Requirement</span></span> | <span data-ttu-id="2f3c0-639">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-639">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2f3c0-640">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-640">Name</span></span>              | <span data-ttu-id="2f3c0-641">x962P239v1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-641">x962P239v1</span></span>          |
| <span data-ttu-id="2f3c0-642">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-642">Standard</span></span>          | <span data-ttu-id="2f3c0-643">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="2f3c0-643">ANSI X9.62</span></span>          |
| <span data-ttu-id="2f3c0-644">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-644">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-645">239</span><span class="sxs-lookup"><span data-stu-id="2f3c0-645">239</span></span>                 |
| <span data-ttu-id="2f3c0-646">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-646">TLS capable</span></span>       | <span data-ttu-id="2f3c0-647">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-647">No</span></span>                  |
| <span data-ttu-id="2f3c0-648">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-648">Object identifier</span></span> | <span data-ttu-id="2f3c0-649">1.2.840.10045.3.1.4</span><span class="sxs-lookup"><span data-stu-id="2f3c0-649">1.2.840.10045.3.1.4</span></span> |



 

<span data-ttu-id="2f3c0-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V2**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-650"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V2** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-651">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-651">Requirement</span></span> | <span data-ttu-id="2f3c0-652">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-652">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2f3c0-653">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-653">Name</span></span>              | <span data-ttu-id="2f3c0-654">x962P239v2</span><span class="sxs-lookup"><span data-stu-id="2f3c0-654">x962P239v2</span></span>          |
| <span data-ttu-id="2f3c0-655">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-655">Standard</span></span>          | <span data-ttu-id="2f3c0-656">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="2f3c0-656">ANSI X9.62</span></span>          |
| <span data-ttu-id="2f3c0-657">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-657">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-658">239</span><span class="sxs-lookup"><span data-stu-id="2f3c0-658">239</span></span>                 |
| <span data-ttu-id="2f3c0-659">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-659">TLS capable</span></span>       | <span data-ttu-id="2f3c0-660">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-660">No</span></span>                  |
| <span data-ttu-id="2f3c0-661">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-661">Object identifier</span></span> | <span data-ttu-id="2f3c0-662">1.2.840.10045.3.1.5</span><span class="sxs-lookup"><span data-stu-id="2f3c0-662">1.2.840.10045.3.1.5</span></span> |



 

<span data-ttu-id="2f3c0-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V3**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-663"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT\_ECC\_CURVE\_X962P239V3** </dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-664">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-664">Requirement</span></span> | <span data-ttu-id="2f3c0-665">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-665">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2f3c0-666">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-666">Name</span></span>              | <span data-ttu-id="2f3c0-667">x962P239v3</span><span class="sxs-lookup"><span data-stu-id="2f3c0-667">x962P239v3</span></span>          |
| <span data-ttu-id="2f3c0-668">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-668">Standard</span></span>          | <span data-ttu-id="2f3c0-669">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="2f3c0-669">ANSI X9.62</span></span>          |
| <span data-ttu-id="2f3c0-670">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-670">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-671">239</span><span class="sxs-lookup"><span data-stu-id="2f3c0-671">239</span></span>                 |
| <span data-ttu-id="2f3c0-672">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-672">TLS capable</span></span>       | <span data-ttu-id="2f3c0-673">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-673">No</span></span>                  |
| <span data-ttu-id="2f3c0-674">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-674">Object identifier</span></span> | <span data-ttu-id="2f3c0-675">1.2.840.10045.3.1.6</span><span class="sxs-lookup"><span data-stu-id="2f3c0-675">1.2.840.10045.3.1.6</span></span> |



 

<span data-ttu-id="2f3c0-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P256V1**</dt> </span><span class="sxs-lookup"><span data-stu-id="2f3c0-676"></dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT\_ECC\_CURVE\_X962P256V1**</dt> </span></span><dd> <dl> <dt> 

| <span data-ttu-id="2f3c0-677">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-677">Requirement</span></span> | <span data-ttu-id="2f3c0-678">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-678">Value</span></span> |
|-------------------|---------------------|
| <span data-ttu-id="2f3c0-679">名稱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-679">Name</span></span>              | <span data-ttu-id="2f3c0-680">x962P256v1</span><span class="sxs-lookup"><span data-stu-id="2f3c0-680">x962P256v1</span></span>          |
| <span data-ttu-id="2f3c0-681">標準</span><span class="sxs-lookup"><span data-stu-id="2f3c0-681">Standard</span></span>          | <span data-ttu-id="2f3c0-682">ANSI X X9.62</span><span class="sxs-lookup"><span data-stu-id="2f3c0-682">ANSI X9.62</span></span>          |
| <span data-ttu-id="2f3c0-683">金鑰大小 (位元)</span><span class="sxs-lookup"><span data-stu-id="2f3c0-683">Key size (bits)</span></span>   | <span data-ttu-id="2f3c0-684">256</span><span class="sxs-lookup"><span data-stu-id="2f3c0-684">256</span></span>                 |
| <span data-ttu-id="2f3c0-685">支援 TLS</span><span class="sxs-lookup"><span data-stu-id="2f3c0-685">TLS capable</span></span>       | <span data-ttu-id="2f3c0-686">No</span><span class="sxs-lookup"><span data-stu-id="2f3c0-686">No</span></span>                  |
| <span data-ttu-id="2f3c0-687">物件識別碼</span><span class="sxs-lookup"><span data-stu-id="2f3c0-687">Object identifier</span></span> | <span data-ttu-id="2f3c0-688">1.2.840.10045.3.1.7</span><span class="sxs-lookup"><span data-stu-id="2f3c0-688">1.2.840.10045.3.1.7</span></span> |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f3c0-689">備註</span><span class="sxs-lookup"><span data-stu-id="2f3c0-689">Remarks</span></span>

<span data-ttu-id="2f3c0-690">若要使用命名曲線，請使用 **BCRYPT \_ ECDSA \_ 演算法** 或 **BCRYPT \_ ECDH \_ 演算法** 來呼叫 [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) ，作為演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f3c0-690">To use a named curve, call [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) using either the **BCRYPT\_ECDSA\_ALGORITHM** or the **BCRYPT\_ECDH\_ALGORITHM** as the algorithm ID.</span></span> <span data-ttu-id="2f3c0-691">然後，呼叫 [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) ，並將 [ **BCRYPT \_ ECC \_ 曲線 \_ 名稱** ] 屬性設定為上述其中一個曲線或任何已在電腦上註冊的命名曲線，如命令所示 `certutil -displayEccCurve` 。</span><span class="sxs-lookup"><span data-stu-id="2f3c0-691">Then, call [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) and set the **BCRYPT\_ECC\_CURVE\_NAME** property to one of the above curves or any named curves registered on the computer as shown by the `certutil -displayEccCurve` command.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f3c0-692">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-692">Requirements</span></span>



| <span data-ttu-id="2f3c0-693">需求</span><span class="sxs-lookup"><span data-stu-id="2f3c0-693">Requirement</span></span> | <span data-ttu-id="2f3c0-694">值</span><span class="sxs-lookup"><span data-stu-id="2f3c0-694">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2f3c0-695">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f3c0-695">Minimum supported client</span></span><br/> | <span data-ttu-id="2f3c0-696">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f3c0-696">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2f3c0-697">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f3c0-697">Minimum supported server</span></span><br/> | <span data-ttu-id="2f3c0-698">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f3c0-698">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2f3c0-699">標頭</span><span class="sxs-lookup"><span data-stu-id="2f3c0-699">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f3c0-700"><dt>Bcrypt。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f3c0-700"><dt>Bcrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f3c0-701">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f3c0-701">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f3c0-702">**BCryptOpenAlgorithmProvider**</span><span class="sxs-lookup"><span data-stu-id="2f3c0-702">**BCryptOpenAlgorithmProvider**</span></span>](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[<span data-ttu-id="2f3c0-703">**NCryptCreatePersistedKey**</span><span class="sxs-lookup"><span data-stu-id="2f3c0-703">**NCryptCreatePersistedKey**</span></span>](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




