---
description: 在 Windows 10 1607 版和更新版本中啟用的橢圓曲線。
title: Windows 10 1607 版和更新版本中的 TLS 橢圓曲線
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 813a7c117f5f1e3fc1c6484fc57d1c9f14cf9567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194193"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a><span data-ttu-id="6657c-103">Windows 10 1607 版和更新版本中的 TLS 橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="6657c-103">TLS Elliptic Curves in Windows 10 version 1607 and later</span></span>

<span data-ttu-id="6657c-104">針對 Windows 10 （1607和更新版本），下列的橢圓曲線預設會啟用，並依預設使用 Microsoft Schannel 提供者：</span><span class="sxs-lookup"><span data-stu-id="6657c-104">For Windows 10, versions 1607 and later, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="6657c-105">橢圓曲線字串</span><span class="sxs-lookup"><span data-stu-id="6657c-105">Elliptic curve string</span></span> | <span data-ttu-id="6657c-106">可在 FIPS 模式中使用</span><span class="sxs-lookup"><span data-stu-id="6657c-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="6657c-107">curve25519</span><span class="sxs-lookup"><span data-stu-id="6657c-107">curve25519</span></span> | <span data-ttu-id="6657c-108">No</span><span class="sxs-lookup"><span data-stu-id="6657c-108">No</span></span> |
| <span data-ttu-id="6657c-109">NistP256</span><span class="sxs-lookup"><span data-stu-id="6657c-109">NistP256</span></span> | <span data-ttu-id="6657c-110">Yes</span><span class="sxs-lookup"><span data-stu-id="6657c-110">Yes</span></span> |
| <span data-ttu-id="6657c-111">NistP384</span><span class="sxs-lookup"><span data-stu-id="6657c-111">NistP384</span></span> | <span data-ttu-id="6657c-112">Yes</span><span class="sxs-lookup"><span data-stu-id="6657c-112">Yes</span></span> |


<span data-ttu-id="6657c-113">Microsoft Schannel 提供者支援下列橢圓曲線，但預設不會啟用：</span><span class="sxs-lookup"><span data-stu-id="6657c-113">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="6657c-114">橢圓曲線字串</span><span class="sxs-lookup"><span data-stu-id="6657c-114">Elliptic curve string</span></span> | <span data-ttu-id="6657c-115">可在 FIPS 模式中使用</span><span class="sxs-lookup"><span data-stu-id="6657c-115">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="6657c-116">brainpoolP256r1</span><span class="sxs-lookup"><span data-stu-id="6657c-116">brainpoolP256r1</span></span> | <span data-ttu-id="6657c-117">No</span><span class="sxs-lookup"><span data-stu-id="6657c-117">No</span></span> |
| <span data-ttu-id="6657c-118">brainpoolP384r1</span><span class="sxs-lookup"><span data-stu-id="6657c-118">brainpoolP384r1</span></span> | <span data-ttu-id="6657c-119">No</span><span class="sxs-lookup"><span data-stu-id="6657c-119">No</span></span> |
| <span data-ttu-id="6657c-120">brainpoolP512r1</span><span class="sxs-lookup"><span data-stu-id="6657c-120">brainpoolP512r1</span></span> | <span data-ttu-id="6657c-121">No</span><span class="sxs-lookup"><span data-stu-id="6657c-121">No</span></span> |
| <span data-ttu-id="6657c-122">nistP192</span><span class="sxs-lookup"><span data-stu-id="6657c-122">nistP192</span></span> | <span data-ttu-id="6657c-123">No</span><span class="sxs-lookup"><span data-stu-id="6657c-123">No</span></span> |
| <span data-ttu-id="6657c-124">nistP224</span><span class="sxs-lookup"><span data-stu-id="6657c-124">nistP224</span></span> | <span data-ttu-id="6657c-125">No</span><span class="sxs-lookup"><span data-stu-id="6657c-125">No</span></span> |
| <span data-ttu-id="6657c-126">nistP521</span><span class="sxs-lookup"><span data-stu-id="6657c-126">nistP521</span></span> | <span data-ttu-id="6657c-127">Yes</span><span class="sxs-lookup"><span data-stu-id="6657c-127">Yes</span></span> |
| <span data-ttu-id="6657c-128">secP160k1</span><span class="sxs-lookup"><span data-stu-id="6657c-128">secP160k1</span></span> | <span data-ttu-id="6657c-129">No</span><span class="sxs-lookup"><span data-stu-id="6657c-129">No</span></span> |
| <span data-ttu-id="6657c-130">secP160r1</span><span class="sxs-lookup"><span data-stu-id="6657c-130">secP160r1</span></span> | <span data-ttu-id="6657c-131">No</span><span class="sxs-lookup"><span data-stu-id="6657c-131">No</span></span> |
| <span data-ttu-id="6657c-132">secP160r2</span><span class="sxs-lookup"><span data-stu-id="6657c-132">secP160r2</span></span> | <span data-ttu-id="6657c-133">No</span><span class="sxs-lookup"><span data-stu-id="6657c-133">No</span></span> |
| <span data-ttu-id="6657c-134">secP192k1</span><span class="sxs-lookup"><span data-stu-id="6657c-134">secP192k1</span></span> | <span data-ttu-id="6657c-135">No</span><span class="sxs-lookup"><span data-stu-id="6657c-135">No</span></span> |
| <span data-ttu-id="6657c-136">secP192r1</span><span class="sxs-lookup"><span data-stu-id="6657c-136">secP192r1</span></span> | <span data-ttu-id="6657c-137">No</span><span class="sxs-lookup"><span data-stu-id="6657c-137">No</span></span> |
| <span data-ttu-id="6657c-138">secP224k1</span><span class="sxs-lookup"><span data-stu-id="6657c-138">secP224k1</span></span> | <span data-ttu-id="6657c-139">No</span><span class="sxs-lookup"><span data-stu-id="6657c-139">No</span></span> |
| <span data-ttu-id="6657c-140">secP224r1</span><span class="sxs-lookup"><span data-stu-id="6657c-140">secP224r1</span></span> | <span data-ttu-id="6657c-141">No</span><span class="sxs-lookup"><span data-stu-id="6657c-141">No</span></span> |
| <span data-ttu-id="6657c-142">secP256k1</span><span class="sxs-lookup"><span data-stu-id="6657c-142">secP256k1</span></span> | <span data-ttu-id="6657c-143">No</span><span class="sxs-lookup"><span data-stu-id="6657c-143">No</span></span> |
| <span data-ttu-id="6657c-144">secP256r1</span><span class="sxs-lookup"><span data-stu-id="6657c-144">secP256r1</span></span> | <span data-ttu-id="6657c-145">No</span><span class="sxs-lookup"><span data-stu-id="6657c-145">No</span></span> |
| <span data-ttu-id="6657c-146">secP384r1</span><span class="sxs-lookup"><span data-stu-id="6657c-146">secP384r1</span></span> | <span data-ttu-id="6657c-147">No</span><span class="sxs-lookup"><span data-stu-id="6657c-147">No</span></span> |
| <span data-ttu-id="6657c-148">secP521r1</span><span class="sxs-lookup"><span data-stu-id="6657c-148">secP521r1</span></span> | <span data-ttu-id="6657c-149">No</span><span class="sxs-lookup"><span data-stu-id="6657c-149">No</span></span> |



## <a name="enabling-elliptic-curves"></a><span data-ttu-id="6657c-150">啟用橢圓曲線</span><span class="sxs-lookup"><span data-stu-id="6657c-150">Enabling Elliptic Curves</span></span>

<span data-ttu-id="6657c-151">若要新增橢圓曲線，可以部署群組原則或使用 TLS Cmdlet：</span><span class="sxs-lookup"><span data-stu-id="6657c-151">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="6657c-152">若要使用群組原則，請在 [電腦設定] 下 [設定 ECC 曲線順序](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) > 系統管理範本 > 網路 > SSL 設定] 設定，以及您想要啟用之所有橢圓曲線的優先順序清單。</span><span class="sxs-lookup"><span data-stu-id="6657c-152">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="6657c-153">若要使用 PowerShell，請參閱 [tls](/powershell/module/tls) Cmdlet 以取得 tls Cmdlet 語法和描述的完整清單。</span><span class="sxs-lookup"><span data-stu-id="6657c-153">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="6657c-154">在 Windows 10 之前，會使用橢圓曲線附加加密套件字串來決定曲線的優先順序。</span><span class="sxs-lookup"><span data-stu-id="6657c-154">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="6657c-155">Windows 10 支援橢圓曲線優先順序順序設定，因此不需要橢圓曲線尾碼，而是在提供時由新的橢圓曲線優先順序順序覆寫，以允許組織使用群組原則，以相同的加密套件來設定不同版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="6657c-155">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="6657c-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6657c-156">See Also</span></span>

[<span data-ttu-id="6657c-157">設定 TLS ECC 曲線順序</span><span class="sxs-lookup"><span data-stu-id="6657c-157">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="6657c-158">管理 TLS ECC 順序</span><span class="sxs-lookup"><span data-stu-id="6657c-158">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="6657c-159">使用群組原則管理 Windows ECC 曲線</span><span class="sxs-lookup"><span data-stu-id="6657c-159">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="6657c-160">TLS Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6657c-160">TLS cmdlets</span></span>](/powershell/module/tls)
