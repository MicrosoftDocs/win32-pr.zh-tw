---
description: 表示與憑證相關聯的私密金鑰。
ms.assetid: 26ad1d1c-17c5-4191-ac97-b911e62b4119
title: PrivateKey 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e87ca7a5bf12bbaf943bccacaa075a51ae75ed37
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984287"
---
# <a name="privatekey-object"></a><span data-ttu-id="c2561-103">PrivateKey 物件</span><span class="sxs-lookup"><span data-stu-id="c2561-103">PrivateKey object</span></span>

<span data-ttu-id="c2561-104">\[**PrivateKey** 物件可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c2561-104">\[The **PrivateKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c2561-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2. PrivateKey 屬性**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="c2561-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c2561-106">**PrivateKey** 物件代表與憑證相關聯的 [*私密金鑰*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="c2561-106">The **PrivateKey** object represents the [*private key*](../secgloss/p-gly.md) associated with a certificate.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c2561-107">使用時機</span><span class="sxs-lookup"><span data-stu-id="c2561-107">When to use</span></span>

<span data-ttu-id="c2561-108">**PrivateKey** 物件是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="c2561-108">The **PrivateKey** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="c2561-109">取得私密金鑰的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c2561-109">Retrieve information about the private key.</span></span>
-   <span data-ttu-id="c2561-110">開啟私密金鑰容器。</span><span class="sxs-lookup"><span data-stu-id="c2561-110">Open the private key container.</span></span>
-   <span data-ttu-id="c2561-111">刪除私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2561-111">Delete the private key.</span></span>

## <a name="members"></a><span data-ttu-id="c2561-112">成員</span><span class="sxs-lookup"><span data-stu-id="c2561-112">Members</span></span>

<span data-ttu-id="c2561-113">**PrivateKey** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c2561-113">The **PrivateKey** object has these types of members:</span></span>

-   [<span data-ttu-id="c2561-114">方法</span><span class="sxs-lookup"><span data-stu-id="c2561-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="c2561-115">屬性</span><span class="sxs-lookup"><span data-stu-id="c2561-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c2561-116">方法</span><span class="sxs-lookup"><span data-stu-id="c2561-116">Methods</span></span>

<span data-ttu-id="c2561-117">**PrivateKey** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="c2561-117">The **PrivateKey** object has these methods.</span></span>



| <span data-ttu-id="c2561-118">方法</span><span class="sxs-lookup"><span data-stu-id="c2561-118">Method</span></span>                                                  | <span data-ttu-id="c2561-119">描述</span><span class="sxs-lookup"><span data-stu-id="c2561-119">Description</span></span>                                                                                                                                                          |
|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2561-120">**刪除**</span><span class="sxs-lookup"><span data-stu-id="c2561-120">**Delete**</span></span>](privatekey-delete.md)                     | <span data-ttu-id="c2561-121">刪除 **PrivateKey** 物件所參考的私用金鑰容器。</span><span class="sxs-lookup"><span data-stu-id="c2561-121">Deletes the private key container referenced by the **PrivateKey** object.</span></span><br/>                                                                                |
| [<span data-ttu-id="c2561-122">**IsAccessible**</span><span class="sxs-lookup"><span data-stu-id="c2561-122">**IsAccessible**</span></span>](privatekey-isaccessible.md)         | <span data-ttu-id="c2561-123">抓取布林值，指出使用者是否可以存取私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2561-123">Retrieves a Boolean value that indicates whether the private key is accessible by the user.</span></span> <span data-ttu-id="c2561-124">若為 true，則使用者可以存取私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2561-124">If true, the user can access the private key.</span></span><br/>                 |
| [<span data-ttu-id="c2561-125">**IsExportable**</span><span class="sxs-lookup"><span data-stu-id="c2561-125">**IsExportable**</span></span>](privatekey-isexportable.md)         | <span data-ttu-id="c2561-126">抓取布林值，指出是否可以匯出私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2561-126">Retrieves a Boolean value that indicates whether the private key can be exported.</span></span> <span data-ttu-id="c2561-127">若為 true，則可以匯出私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2561-127">If true, the private key can be exported.</span></span><br/>                               |
| [<span data-ttu-id="c2561-128">**IsHardwareDevice**</span><span class="sxs-lookup"><span data-stu-id="c2561-128">**IsHardwareDevice**</span></span>](privatekey-ishardwaredevice.md) | <span data-ttu-id="c2561-129">抓取布林值，指出私密金鑰是否儲存在硬體裝置上。</span><span class="sxs-lookup"><span data-stu-id="c2561-129">Retrieves a Boolean value that indicates whether the private key is stored on a hardware device.</span></span> <span data-ttu-id="c2561-130">若為 true，則會將私密金鑰儲存在硬體裝置上。</span><span class="sxs-lookup"><span data-stu-id="c2561-130">If true, the private key is stored on a hardware device.</span></span><br/> |
| [<span data-ttu-id="c2561-131">**IsMachineKeyset**</span><span class="sxs-lookup"><span data-stu-id="c2561-131">**IsMachineKeyset**</span></span>](privatekey-ismachinekeyset.md)   | <span data-ttu-id="c2561-132">抓取布林值，指出私密金鑰是否為電腦金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2561-132">Retrieves a Boolean value that indicates whether the private key is a machine key.</span></span> <span data-ttu-id="c2561-133">若為 true，則私密金鑰為電腦金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2561-133">If true, the private key is a machine key.</span></span><br/>                             |
| [<span data-ttu-id="c2561-134">**IsProtected**</span><span class="sxs-lookup"><span data-stu-id="c2561-134">**IsProtected**</span></span>](privatekey-isprotected.md)           | <span data-ttu-id="c2561-135">抓取布林值，指出私密金鑰是否受到保護。</span><span class="sxs-lookup"><span data-stu-id="c2561-135">Retrieves a Boolean value that indicates whether the private key is protected.</span></span> <span data-ttu-id="c2561-136">若為 true，則會保護私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="c2561-136">If true, the private key is protected.</span></span><br/>                                     |
| [<span data-ttu-id="c2561-137">**IsRemovable**</span><span class="sxs-lookup"><span data-stu-id="c2561-137">**IsRemovable**</span></span>](privatekey-isremovable.md)           | <span data-ttu-id="c2561-138">抓取布林值，指出私密金鑰是否在可移動裝置上。</span><span class="sxs-lookup"><span data-stu-id="c2561-138">Retrieves a Boolean value that indicates whether the private key is on a removable device.</span></span> <span data-ttu-id="c2561-139">若為 true，則私密金鑰位於卸載式裝置上。</span><span class="sxs-lookup"><span data-stu-id="c2561-139">If true, the private key is on a removable device.</span></span><br/>             |
| [<span data-ttu-id="c2561-140">**打開**</span><span class="sxs-lookup"><span data-stu-id="c2561-140">**Open**</span></span>](privatekey-open.md)                         | <span data-ttu-id="c2561-141">存取現有的金鑰容器。</span><span class="sxs-lookup"><span data-stu-id="c2561-141">Accesses an existing key container.</span></span><br/>                                                                                                                       |



 

### <a name="properties"></a><span data-ttu-id="c2561-142">屬性</span><span class="sxs-lookup"><span data-stu-id="c2561-142">Properties</span></span>

<span data-ttu-id="c2561-143">**PrivateKey** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c2561-143">The **PrivateKey** object has these properties.</span></span>



| <span data-ttu-id="c2561-144">屬性</span><span class="sxs-lookup"><span data-stu-id="c2561-144">Property</span></span>                                                                 | <span data-ttu-id="c2561-145">存取類型</span><span class="sxs-lookup"><span data-stu-id="c2561-145">Access type</span></span>          | <span data-ttu-id="c2561-146">Description</span><span class="sxs-lookup"><span data-stu-id="c2561-146">Description</span></span>                                                                                               |
|:-------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c2561-147">**容器**</span><span class="sxs-lookup"><span data-stu-id="c2561-147">**ContainerName**</span></span>](privatekey-containername.md)<br/>             | <span data-ttu-id="c2561-148">唯讀</span><span class="sxs-lookup"><span data-stu-id="c2561-148">Read-only</span></span><br/> | <span data-ttu-id="c2561-149">抓取包含私密金鑰容器名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="c2561-149">Retrieves a string that contains the private key container name.</span></span> <span data-ttu-id="c2561-150">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="c2561-150">This is the default property.</span></span><br/> |
| [<span data-ttu-id="c2561-151">**KeySpec**</span><span class="sxs-lookup"><span data-stu-id="c2561-151">**KeySpec**</span></span>](privatekey-keyspec.md)<br/>                         | <span data-ttu-id="c2561-152">唯讀</span><span class="sxs-lookup"><span data-stu-id="c2561-152">Read-only</span></span><br/> | <span data-ttu-id="c2561-153">抓取金鑰規格。</span><span class="sxs-lookup"><span data-stu-id="c2561-153">Retrieves the key specification.</span></span><br/>                                                               |
| [<span data-ttu-id="c2561-154">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="c2561-154">**ProviderName**</span></span>](privatekey-providername.md)<br/>               | <span data-ttu-id="c2561-155">唯讀</span><span class="sxs-lookup"><span data-stu-id="c2561-155">Read-only</span></span><br/> | <span data-ttu-id="c2561-156">抓取包含 CSP 名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="c2561-156">Retrieves a string that contains the name of the CSP.</span></span><br/>                                          |
| [<span data-ttu-id="c2561-157">**ProviderType**</span><span class="sxs-lookup"><span data-stu-id="c2561-157">**ProviderType**</span></span>](privatekey-providertype.md)<br/>               | <span data-ttu-id="c2561-158">唯讀</span><span class="sxs-lookup"><span data-stu-id="c2561-158">Read-only</span></span><br/> | <span data-ttu-id="c2561-159">抓取指定提供者類型的列舉值。</span><span class="sxs-lookup"><span data-stu-id="c2561-159">Retrieves an enumeration value that specifies the type of provider.</span></span><br/>                            |
| [<span data-ttu-id="c2561-160">**UniqueContainerName**</span><span class="sxs-lookup"><span data-stu-id="c2561-160">**UniqueContainerName**</span></span>](privatekey-uniquecontainername.md)<br/> | <span data-ttu-id="c2561-161">唯讀</span><span class="sxs-lookup"><span data-stu-id="c2561-161">Read-only</span></span><br/> | <span data-ttu-id="c2561-162">抓取包含唯一私用金鑰容器名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="c2561-162">Retrieves a string that contains the unique private key container name.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="c2561-163">備註</span><span class="sxs-lookup"><span data-stu-id="c2561-163">Remarks</span></span>

<span data-ttu-id="c2561-164">您可以建立 **PrivateKey** 物件，而且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="c2561-164">The **PrivateKey** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="c2561-165">**PrivateKey** 物件的 PROGID 是 CAPICOM。PrivateKey。1。</span><span class="sxs-lookup"><span data-stu-id="c2561-165">The ProgID for the **PrivateKey** object is CAPICOM.PrivateKey.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2561-166">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2561-166">Requirements</span></span>



| <span data-ttu-id="c2561-167">需求</span><span class="sxs-lookup"><span data-stu-id="c2561-167">Requirement</span></span> | <span data-ttu-id="c2561-168">值</span><span class="sxs-lookup"><span data-stu-id="c2561-168">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2561-169">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c2561-169">Redistributable</span></span><br/> | <span data-ttu-id="c2561-170">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c2561-170">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c2561-171">DLL</span><span class="sxs-lookup"><span data-stu-id="c2561-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="c2561-172"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2561-172"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
