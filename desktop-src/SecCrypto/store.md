---
description: 提供屬性和方法，可讓您用來選擇、管理及使用憑證存放區和這些存放區中的憑證。
ms.assetid: de4eecf7-c03b-4733-ac29-d5b26b873dba
title: 存放區物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4e8a14fcecf0ded2e4e1a56e2b98e4ac4838b776
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984134"
---
# <a name="store-object"></a><span data-ttu-id="283cc-103">存放區物件</span><span class="sxs-lookup"><span data-stu-id="283cc-103">Store object</span></span>

<span data-ttu-id="283cc-104">\[**Store** 物件可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="283cc-104">\[The **Store** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="283cc-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="283cc-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="283cc-106">Store 物件提供屬性和方法，您可以使用這些屬性和方法來選擇、管理及使用這些 **存放** 區中的 [*憑證存放區*](../secgloss/c-gly.md) 和憑證。</span><span class="sxs-lookup"><span data-stu-id="283cc-106">The **Store** object provides properties and methods that you can use to choose, manage, and use [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="283cc-107">CAPICOM 可以使用目前的使用者、本機電腦、記憶體和 Active Directory 存放區。</span><span class="sxs-lookup"><span data-stu-id="283cc-107">CAPICOM can use Current-User, Local-Machine, memory, and Active Directory stores.</span></span> <span data-ttu-id="283cc-108">此外，存放區支援以智慧卡為基礎的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="283cc-108">Also, stores support smart card–based certificate stores.</span></span> <span data-ttu-id="283cc-109">開發人員應該注意，如果嘗試操作的使用者沒有許可權，某些存放區的某些方法可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="283cc-109">Developers should be aware that some methods may fail with some stores if operations are attempted for which the user does not have rights.</span></span>

## <a name="members"></a><span data-ttu-id="283cc-110">成員</span><span class="sxs-lookup"><span data-stu-id="283cc-110">Members</span></span>

<span data-ttu-id="283cc-111">**Store** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="283cc-111">The **Store** object has these types of members:</span></span>

-   [<span data-ttu-id="283cc-112">方法</span><span class="sxs-lookup"><span data-stu-id="283cc-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="283cc-113">屬性</span><span class="sxs-lookup"><span data-stu-id="283cc-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="283cc-114">方法</span><span class="sxs-lookup"><span data-stu-id="283cc-114">Methods</span></span>

<span data-ttu-id="283cc-115">**Store** 物件具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="283cc-115">The **Store** object has these methods.</span></span>



| <span data-ttu-id="283cc-116">方法</span><span class="sxs-lookup"><span data-stu-id="283cc-116">Method</span></span>                         | <span data-ttu-id="283cc-117">描述</span><span class="sxs-lookup"><span data-stu-id="283cc-117">Description</span></span>                                                                                                                                                                                                      |
|:-------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="283cc-118">**添加**</span><span class="sxs-lookup"><span data-stu-id="283cc-118">**Add**</span></span>](store-add.md)       | <span data-ttu-id="283cc-119">將 [**憑證**](certificate.md) 物件新增至開啟的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="283cc-119">Adds a [**Certificate**](certificate.md) object to the open certificate store.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="283cc-120">**關閉**</span><span class="sxs-lookup"><span data-stu-id="283cc-120">**Close**</span></span>](store-close.md)   | <span data-ttu-id="283cc-121">關閉開啟的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="283cc-121">Closes an open certificate store.</span></span><br/> <span data-ttu-id="283cc-122">**CAPICOM 2.0.0.3 和更早版本：** 不支援 [**Close**](store-close.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="283cc-122">**CAPICOM 2.0.0.3 and earlier:** The [**Close**](store-close.md) method is not supported.</span></span><br/>                                                               |
| [<span data-ttu-id="283cc-123">**刪除**</span><span class="sxs-lookup"><span data-stu-id="283cc-123">**Delete**</span></span>](store-delete.md) | <span data-ttu-id="283cc-124">刪除目前 [**存放區**](certificate.md) 物件所代表的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="283cc-124">Deletes the certificate store represented by the current [**Store**](certificate.md) object.</span></span><br/> <span data-ttu-id="283cc-125">**CAPICOM 2.0.0.3 和更早版本：** 不支援 [**Delete**](store-delete.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="283cc-125">**CAPICOM 2.0.0.3 and earlier:** The [**Delete**](store-delete.md) method is not supported.</span></span><br/> |
| [<span data-ttu-id="283cc-126">**出口**</span><span class="sxs-lookup"><span data-stu-id="283cc-126">**Export**</span></span>](store-export.md) | <span data-ttu-id="283cc-127">匯出編碼 [*BLOB*](../secgloss/b-gly.md)的存放區。</span><span class="sxs-lookup"><span data-stu-id="283cc-127">Exports the store of an encoded [*BLOB*](../secgloss/b-gly.md).</span></span><br/>                                                                                                       |
| [<span data-ttu-id="283cc-128">**匯入**</span><span class="sxs-lookup"><span data-stu-id="283cc-128">**Import**</span></span>](store-import.md) | <span data-ttu-id="283cc-129">匯入先前匯出的存放區。</span><span class="sxs-lookup"><span data-stu-id="283cc-129">Imports a previously exported store.</span></span><br/>                                                                                                                                                                  |
| [<span data-ttu-id="283cc-130">**載入**</span><span class="sxs-lookup"><span data-stu-id="283cc-130">**Load**</span></span>](store-load.md)     | <span data-ttu-id="283cc-131">從檔案將 [**憑證**](certificate.md) 物件匯入存放區。</span><span class="sxs-lookup"><span data-stu-id="283cc-131">Imports [**Certificate**](certificate.md) objects from a file into the store.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="283cc-132">**打開**</span><span class="sxs-lookup"><span data-stu-id="283cc-132">**Open**</span></span>](store-open.md)     | <span data-ttu-id="283cc-133">開啟憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="283cc-133">Opens a certificate store.</span></span><br/>                                                                                                                                                                            |
| [<span data-ttu-id="283cc-134">**移除**</span><span class="sxs-lookup"><span data-stu-id="283cc-134">**Remove**</span></span>](store-remove.md) | <span data-ttu-id="283cc-135">從開啟的存放區中移除 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="283cc-135">Removes a [**Certificate**](certificate.md) object from an open store.</span></span><br/>                                                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="283cc-136">屬性</span><span class="sxs-lookup"><span data-stu-id="283cc-136">Properties</span></span>

<span data-ttu-id="283cc-137">**Store** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="283cc-137">The **Store** object has these properties.</span></span>



| <span data-ttu-id="283cc-138">屬性</span><span class="sxs-lookup"><span data-stu-id="283cc-138">Property</span></span>                                              | <span data-ttu-id="283cc-139">存取類型</span><span class="sxs-lookup"><span data-stu-id="283cc-139">Access type</span></span>          | <span data-ttu-id="283cc-140">Description</span><span class="sxs-lookup"><span data-stu-id="283cc-140">Description</span></span>                                                                                                                                                                                           |
|:------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="283cc-141">**憑證**</span><span class="sxs-lookup"><span data-stu-id="283cc-141">**Certificates**</span></span>](store-certificates.md)<br/> | <span data-ttu-id="283cc-142">唯讀</span><span class="sxs-lookup"><span data-stu-id="283cc-142">Read-only</span></span><br/> | <span data-ttu-id="283cc-143">抓取存放區的 [**憑證**](certificates.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="283cc-143">Retrieves the [**Certificates**](certificates.md) collection of the store.</span></span> <span data-ttu-id="283cc-144">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="283cc-144">This is the default property.</span></span><br/>                                                                                  |
| [<span data-ttu-id="283cc-145">**Location**</span><span class="sxs-lookup"><span data-stu-id="283cc-145">**Location**</span></span>](store-location.md)<br/>         | <span data-ttu-id="283cc-146">唯讀</span><span class="sxs-lookup"><span data-stu-id="283cc-146">Read-only</span></span><br/> | <span data-ttu-id="283cc-147">抓取此物件所代表之憑證存放區的位置。</span><span class="sxs-lookup"><span data-stu-id="283cc-147">Retrieves the location of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="283cc-148">**CAPICOM 2.0.0.3 和更早版本：** 不支援 [**Location**](store-location.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="283cc-148">**CAPICOM 2.0.0.3 and earlier:** The [**Location**](store-location.md) property is not supported.</span></span><br/> |
| [<span data-ttu-id="283cc-149">**Name**</span><span class="sxs-lookup"><span data-stu-id="283cc-149">**Name**</span></span>](store-name.md)<br/>                 | <span data-ttu-id="283cc-150">唯讀</span><span class="sxs-lookup"><span data-stu-id="283cc-150">Read-only</span></span><br/> | <span data-ttu-id="283cc-151">抓取此物件所代表的憑證存放區名稱。</span><span class="sxs-lookup"><span data-stu-id="283cc-151">Retrieves the name of the certificate store that this object represents.</span></span><br/> <span data-ttu-id="283cc-152">**CAPICOM 2.0.0.3 和更早版本：** 不支援 [**Name**](store-name.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="283cc-152">**CAPICOM 2.0.0.3 and earlier:** The [**Name**](store-name.md) property is not supported.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="283cc-153">備註</span><span class="sxs-lookup"><span data-stu-id="283cc-153">Remarks</span></span>

<span data-ttu-id="283cc-154">您可以建立 **存放區** 物件，而且可以安全地進行腳本處理。</span><span class="sxs-lookup"><span data-stu-id="283cc-154">The **Store** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="283cc-155">**存放區** 物件的 PROGID 是 CAPICOM。存放區。2。</span><span class="sxs-lookup"><span data-stu-id="283cc-155">The ProgID for the **Store** object is CAPICOM.Store.2.</span></span>

<span data-ttu-id="283cc-156">**CAPICOM 1。*x*：** **存放區** 物件的 ProgID 是 CAPICOM。Store. 1。</span><span class="sxs-lookup"><span data-stu-id="283cc-156">**CAPICOM 1.*x*:** The ProgID for the **Store** object is CAPICOM.Store.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="283cc-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="283cc-157">Requirements</span></span>



| <span data-ttu-id="283cc-158">需求</span><span class="sxs-lookup"><span data-stu-id="283cc-158">Requirement</span></span> | <span data-ttu-id="283cc-159">值</span><span class="sxs-lookup"><span data-stu-id="283cc-159">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="283cc-160">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="283cc-160">Redistributable</span></span><br/> | <span data-ttu-id="283cc-161">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="283cc-161">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="283cc-162">DLL</span><span class="sxs-lookup"><span data-stu-id="283cc-162">DLL</span></span><br/>             | <dl> <span data-ttu-id="283cc-163"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="283cc-163"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="283cc-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="283cc-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="283cc-165">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="283cc-165">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
