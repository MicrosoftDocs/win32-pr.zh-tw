---
description: 建立 SignedData 或 SignedCode 物件的簽署者。
ms.assetid: fca6489c-56cf-472f-ac0f-73ba531fa212
title: 簽署者物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 974341eb996f2b5d3701757a5352ef56e2837390
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999678"
---
# <a name="signer-object"></a><span data-ttu-id="60812-103">簽署者物件</span><span class="sxs-lookup"><span data-stu-id="60812-103">Signer object</span></span>

<span data-ttu-id="60812-104">\[**簽署者** 物件可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="60812-104">\[The **Signer** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="60812-105">相反地，請使用 [**CmsSigner 類別**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="60812-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="60812-106">**簽署者** 物件會建立 [**SignedData**](signeddata.md)或 [**SignedCode**](signedcode.md)物件的簽署者。</span><span class="sxs-lookup"><span data-stu-id="60812-106">The **Signer** object establishes the signer of a [**SignedData**](signeddata.md) or [**SignedCode**](signedcode.md) object.</span></span> <span data-ttu-id="60812-107">**簽署者** 物件的 [**憑證**](certificate.md)必須具有可用來簽署資料的可用私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="60812-107">The [**Certificate**](certificate.md) of the **Signer** object must have an available private key that can be used to sign data.</span></span>

## <a name="members"></a><span data-ttu-id="60812-108">成員</span><span class="sxs-lookup"><span data-stu-id="60812-108">Members</span></span>

<span data-ttu-id="60812-109">**簽署者** 物件有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="60812-109">The **Signer** object has these types of members:</span></span>

-   [<span data-ttu-id="60812-110">方法</span><span class="sxs-lookup"><span data-stu-id="60812-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="60812-111">屬性</span><span class="sxs-lookup"><span data-stu-id="60812-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="60812-112">方法</span><span class="sxs-lookup"><span data-stu-id="60812-112">Methods</span></span>

<span data-ttu-id="60812-113">**簽署者** 物件具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="60812-113">The **Signer** object has these methods.</span></span>



| <span data-ttu-id="60812-114">方法</span><span class="sxs-lookup"><span data-stu-id="60812-114">Method</span></span>                      | <span data-ttu-id="60812-115">描述</span><span class="sxs-lookup"><span data-stu-id="60812-115">Description</span></span>                                                       |
|:----------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="60812-116">**載入**</span><span class="sxs-lookup"><span data-stu-id="60812-116">**Load**</span></span>](signer-load.md) | <span data-ttu-id="60812-117">從指定的 PFX 檔案載入簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="60812-117">Loads a signing certificate from a specified PFX file.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="60812-118">屬性</span><span class="sxs-lookup"><span data-stu-id="60812-118">Properties</span></span>

<span data-ttu-id="60812-119">**簽署者** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="60812-119">The **Signer** object has these properties.</span></span>



| <span data-ttu-id="60812-120">屬性</span><span class="sxs-lookup"><span data-stu-id="60812-120">Property</span></span>                                                                     | <span data-ttu-id="60812-121">存取類型</span><span class="sxs-lookup"><span data-stu-id="60812-121">Access type</span></span>           | <span data-ttu-id="60812-122">Description</span><span class="sxs-lookup"><span data-stu-id="60812-122">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60812-123">**AuthenticatedAttributes**</span><span class="sxs-lookup"><span data-stu-id="60812-123">**AuthenticatedAttributes**</span></span>](signer-authenticatedattributes.md)<br/> | <span data-ttu-id="60812-124">唯讀</span><span class="sxs-lookup"><span data-stu-id="60812-124">Read-only</span></span><br/>  | <span data-ttu-id="60812-125">已驗證之屬性的集合。</span><span class="sxs-lookup"><span data-stu-id="60812-125">The collection of authenticated attributes.</span></span><br/>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="60812-126">**憑證**</span><span class="sxs-lookup"><span data-stu-id="60812-126">**Certificate**</span></span>](signer-certificate.md)<br/>                         | <span data-ttu-id="60812-127">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="60812-127">Read/write</span></span><br/> | <span data-ttu-id="60812-128">代表資料簽署者之憑證的 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="60812-128">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span><br/> <span data-ttu-id="60812-129">當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="60812-129">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span><br/> <span data-ttu-id="60812-130">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="60812-130">This is the default property.</span></span><br/> |
| [<span data-ttu-id="60812-131">**鏈**</span><span class="sxs-lookup"><span data-stu-id="60812-131">**Chain**</span></span>](signer-chain.md)<br/>                                     | <span data-ttu-id="60812-132">唯讀</span><span class="sxs-lookup"><span data-stu-id="60812-132">Read-only</span></span><br/>  | <span data-ttu-id="60812-133">簽署者的鏈。</span><span class="sxs-lookup"><span data-stu-id="60812-133">The chain of the signer.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="60812-134">**選項**</span><span class="sxs-lookup"><span data-stu-id="60812-134">**Options**</span></span>](signer-options.md)<br/>                                 | <span data-ttu-id="60812-135">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="60812-135">Read/write</span></span><br/> | <span data-ttu-id="60812-136">設定或抓取簽署者的憑證選項。</span><span class="sxs-lookup"><span data-stu-id="60812-136">Sets or retrieves the signer's certificate option.</span></span><br/>                                                                                                                                                                                                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="60812-137">備註</span><span class="sxs-lookup"><span data-stu-id="60812-137">Remarks</span></span>

<span data-ttu-id="60812-138">您可以建立 **簽署者** 物件，而且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="60812-138">The **Signer** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="60812-139">**簽署者** 物件的 PROGID 是 CAPICOM。簽署者。2。</span><span class="sxs-lookup"><span data-stu-id="60812-139">The ProgID for the **Signer** object is CAPICOM.Signer.2.</span></span>

<span data-ttu-id="60812-140">**CAPICOM 1。*x*：** **簽署者** 物件的 ProgID 為 CAPICOM。簽署者1。</span><span class="sxs-lookup"><span data-stu-id="60812-140">**CAPICOM 1.*x*:** The ProgID for the **Signer** object is CAPICOM.Signer.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="60812-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="60812-141">Requirements</span></span>



| <span data-ttu-id="60812-142">需求</span><span class="sxs-lookup"><span data-stu-id="60812-142">Requirement</span></span> | <span data-ttu-id="60812-143">值</span><span class="sxs-lookup"><span data-stu-id="60812-143">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60812-144">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="60812-144">Redistributable</span></span><br/> | <span data-ttu-id="60812-145">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="60812-145">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="60812-146">DLL</span><span class="sxs-lookup"><span data-stu-id="60812-146">DLL</span></span><br/>             | <dl> <span data-ttu-id="60812-147"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60812-147"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60812-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60812-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60812-149">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="60812-149">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
