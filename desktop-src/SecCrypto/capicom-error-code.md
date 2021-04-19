---
description: 定義 CAPICOM 傳回的錯誤碼。
ms.assetid: e72b8290-b482-4629-8b87-5a15677865a6
title: 'CAPICOM_ERROR_CODE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ERROR_CODE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: ccd4963c83f1ad7ce3bc686b7736ce47d699ce30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989854"
---
# <a name="capicom_error_code-enumeration"></a><span data-ttu-id="cb3b3-103">CAPICOM \_ 錯誤碼 \_ 列舉</span><span class="sxs-lookup"><span data-stu-id="cb3b3-103">CAPICOM\_ERROR\_CODE enumeration</span></span>

<span data-ttu-id="cb3b3-104">**Capicom \_ 錯誤碼 \_** 列舉型別會定義由 capicom 傳回的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-104">The **CAPICOM\_ERROR\_CODE** enumeration type defines error codes that are returned by CAPICOM.</span></span>

> [!Note]  
> <span data-ttu-id="cb3b3-105">Visual Basic Scripting Edition 錯誤會傳回大於零的 **Err** 數值。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-105">Visual Basic Scripting Edition errors return an **Err.number** value greater than zero.</span></span> <span data-ttu-id="cb3b3-106">針對這些錯誤，錯誤 **。描述** 值會提供錯誤原因的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-106">For those errors, **Err.Description** values provide information about the cause of the error.</span></span> <span data-ttu-id="cb3b3-107">除了 Visual Basic Scripting Edition 錯誤之外，CAPICOM 錯誤還會傳回由 **capicom \_ 錯誤碼 \_** 定義的程式碼。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-107">In addition to Visual Basic Scripting Edition errors, CAPICOM errors return the codes defined by **CAPICOM\_ERROR\_CODE**.</span></span>

 

## <a name="members"></a><span data-ttu-id="cb3b3-108">成員</span><span class="sxs-lookup"><span data-stu-id="cb3b3-108">Members</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb3b3-109">member</span><span class="sxs-lookup"><span data-stu-id="cb3b3-109">Member</span></span></th>
<th><span data-ttu-id="cb3b3-110">描述</span><span class="sxs-lookup"><span data-stu-id="cb3b3-110">Description</span></span></th>
<th><span data-ttu-id="cb3b3-111">值</span><span class="sxs-lookup"><span data-stu-id="cb3b3-111">Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cb3b3-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-112"><strong>CAPICOM_E_ENCODE_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="cb3b3-113">使用了不正確編碼類型。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-113">An encoding type that is not valid was used.</span></span><br/> <span data-ttu-id="cb3b3-114">下列清單顯示有效的編碼類型：</span><span class="sxs-lookup"><span data-stu-id="cb3b3-114">The following list shows the valid encoding types:</span></span>
<ul>
<li><span data-ttu-id="cb3b3-115">CAPICOM_ENCODE_ANY</span><span class="sxs-lookup"><span data-stu-id="cb3b3-115">CAPICOM_ENCODE_ANY</span></span></li>
<li><span data-ttu-id="cb3b3-116">CAPICOM_ENCODE_BASE64</span><span class="sxs-lookup"><span data-stu-id="cb3b3-116">CAPICOM_ENCODE_BASE64</span></span></li>
<li><span data-ttu-id="cb3b3-117">CAPICOM_ENCODE_BINARY</span><span class="sxs-lookup"><span data-stu-id="cb3b3-117">CAPICOM_ENCODE_BINARY</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="cb3b3-118">0x80880100</span><span class="sxs-lookup"><span data-stu-id="cb3b3-118">0x80880100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-119"><strong>CAPICOM_E_EKU_INVALID_OID</strong></span></span></td>
<td><span data-ttu-id="cb3b3-120">無法設定<a href="eku.md"><strong>EKU</strong></a>物件的<a href="eku-oid.md"><strong>OID</strong></a>屬性，因為<a href="eku-name.md"><strong>Name</strong></a>屬性未設定為 CAPICOM_EKU_OTHER。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-120">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object cannot be set because the <a href="eku-name.md"><strong>Name</strong></a> property is not set to CAPICOM_EKU_OTHER.</span></span><br/> <span data-ttu-id="cb3b3-121">設定<a href="eku-oid.md"><strong>OID</strong></a>屬性之前，請先將 [<a href="eku-name.md"><strong>名稱</strong></a>] 屬性設定為 CAPICOM_EKU_OTHER。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-121">Set the <a href="eku-name.md"><strong>Name</strong></a> property to CAPICOM_EKU_OTHER before setting the <a href="eku-oid.md"><strong>OID</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-122">0x80880200</span><span class="sxs-lookup"><span data-stu-id="cb3b3-122">0x80880200</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-123"><strong>CAPICOM_E_EKU_OID_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-124"><a href="eku.md"><strong>EKU</strong></a>物件的<a href="eku-oid.md"><strong>OID</strong></a>屬性尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-124">The <a href="eku-oid.md"><strong>OID</strong></a> property of the <a href="eku.md"><strong>EKU</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="cb3b3-125">將 [ <a href="eku-name.md"><strong>名稱</strong></a> ] 屬性設定為 [CAPICOM_EKU_OTHER 以外的任何內容，或將 [ <strong>名稱</strong> ] 屬性設定為 [CAPICOM_EKU_OTHER]，並將 [ <a href="eku-oid.md"><strong>OID</strong></a> ] 屬性設定為值。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-125">Either set the <a href="eku-name.md"><strong>Name</strong></a> property to anything other than CAPICOM_EKU_OTHER, or set the <strong>Name</strong> property to CAPICOM_EKU_OTHER and the <a href="eku-oid.md"><strong>OID</strong></a> property to a value.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-126">0x80880201</span><span class="sxs-lookup"><span data-stu-id="cb3b3-126">0x80880201</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-127"><strong>CAPICOM_E_CERTIFICATE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-128"><a href="certificate.md"><strong>憑證</strong></a>物件尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-128">The <a href="certificate.md"><strong>Certificate</strong></a> object has not been initialized.</span></span><br/> <span data-ttu-id="cb3b3-129">通常，當 <a href="certificate.md"><strong>憑證</strong></a> 物件具現化但未與數位憑證相關聯時，就會傳回此錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-129">Usually, this error code is returned when a <a href="certificate.md"><strong>Certificate</strong></a> object is instantiated but not associated with a digital certificate.</span></span> <span data-ttu-id="cb3b3-130">若要建立物件與數位憑證之間的關聯，請將它指派給現有的 <strong>憑證</strong> 物件或呼叫匯 <a href="certificate-import.md"><strong>入</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-130">To associate the object with a digital certificate, either assign it to an existing <strong>Certificate</strong> object or call the <a href="certificate-import.md"><strong>Import</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-131">0x80880210</span><span class="sxs-lookup"><span data-stu-id="cb3b3-131">0x80880210</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRI加值稅E_KEY</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-132"><strong>CAPICOM_E_CERTIFICATE_NO_PRIVATE_KEY</strong></span></span></td>
<td><span data-ttu-id="cb3b3-133"><a href="certificate.md"><strong>憑證</strong></a>物件沒有相關聯的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-133">The <a href="certificate.md"><strong>Certificate</strong></a> object does not have an associated private key.</span></span><br/> <span data-ttu-id="cb3b3-134">嘗試使用簽署人的私密金鑰來簽署資料時，會傳回此錯誤碼，但與<a href="signer.md"><strong>簽署者</strong></a>物件相關聯的<a href="certificate.md"><strong>憑證</strong></a>物件無法用於簽署作業。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-134">This error code is returned when an attempt is made to sign data using the signer's private key, but the <a href="certificate.md"><strong>Certificate</strong></a> object that is associated with the <a href="signer.md"><strong>Signer</strong></a> object cannot be used for the signing operation.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-135">0x80880211</span><span class="sxs-lookup"><span data-stu-id="cb3b3-135">0x80880211</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-136"><strong>CAPICOM_E_CHAIN_NOT_BUILT</strong></span></span></td>
<td><span data-ttu-id="cb3b3-137"><a href="chain.md"><strong>鏈</strong></a>物件尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-137">The <a href="chain.md"><strong>Chain</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="cb3b3-138">若要初始化 <a href="chain.md"><strong>Chain</strong></a> 物件，請呼叫 <a href="chain-build.md"><strong>Build</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-138">To initialize the <a href="chain.md"><strong>Chain</strong></a> object, call the <a href="chain-build.md"><strong>Build</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-139">0x80880220</span><span class="sxs-lookup"><span data-stu-id="cb3b3-139">0x80880220</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-140"><strong>CAPICOM_E_STORE_NOT_OPENED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-141"><a href="store.md"><strong>存放區</strong></a>物件尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-141">The <a href="store.md"><strong>Store</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="cb3b3-142">若要初始化 <a href="store.md"><strong>存放區</strong></a> 物件，請呼叫 <a href="store-open.md"><strong>Open</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-142">To initialize the <a href="store.md"><strong>Store</strong></a> object, call the <a href="store-open.md"><strong>Open</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-143">0x80880230</span><span class="sxs-lookup"><span data-stu-id="cb3b3-143">0x80880230</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-144"><strong>CAPICOM_E_STORE_EMPTY</strong></span></span></td>
<td><span data-ttu-id="cb3b3-145"><a href="store.md"><strong>存放區</strong></a>物件未包含任何<a href="certificate.md"><strong>憑證</strong></a>物件。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-145">The <a href="store.md"><strong>Store</strong></a> object does not contain any <a href="certificate.md"><strong>Certificate</strong></a> objects.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-146">0x80880231</span><span class="sxs-lookup"><span data-stu-id="cb3b3-146">0x80880231</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-147"><strong>CAPICOM_E_STORE_INVALID_OPEN_MODE</strong></span></span></td>
<td><span data-ttu-id="cb3b3-148"><a href="store-open.md"><strong>Store. Open</strong></a>方法的<em>OpenMode</em>參數不包含有效的 CAPICOM_STORE_OPEN_MODE 值。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-148">The <em>OpenMode</em> parameter of the <a href="store-open.md"><strong>Store.Open</strong></a> method does not contain a valid value of CAPICOM_STORE_OPEN_MODE.</span></span><br/> <span data-ttu-id="cb3b3-149">下列清單顯示 CAPICOM_STORE_OPEN_MODE 的有效值：</span><span class="sxs-lookup"><span data-stu-id="cb3b3-149">The following list shows the valid values of CAPICOM_STORE_OPEN_MODE:</span></span>
<ul>
<li><span data-ttu-id="cb3b3-150">CAPICOM_STORE_OPEN_READ_ONLY</span><span class="sxs-lookup"><span data-stu-id="cb3b3-150">CAPICOM_STORE_OPEN_READ_ONLY</span></span></li>
<li><span data-ttu-id="cb3b3-151">CAPICOM_STORE_OPEN_READ_WRITE</span><span class="sxs-lookup"><span data-stu-id="cb3b3-151">CAPICOM_STORE_OPEN_READ_WRITE</span></span></li>
<li><span data-ttu-id="cb3b3-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span><span class="sxs-lookup"><span data-stu-id="cb3b3-152">CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED</span></span></li>
<li><span data-ttu-id="cb3b3-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span><span class="sxs-lookup"><span data-stu-id="cb3b3-153">CAPICOM_STORE_OPEN_EXISTING_ONLY</span></span></li>
<li><span data-ttu-id="cb3b3-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span><span class="sxs-lookup"><span data-stu-id="cb3b3-154">CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="cb3b3-155">0x80880232</span><span class="sxs-lookup"><span data-stu-id="cb3b3-155">0x80880232</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-156"><strong>CAPICOM_E_STORE_INVALID_SAVE_AS_TYPE</strong></span></span></td>
<td><span data-ttu-id="cb3b3-157">傳遞給<a href="store.md"><strong>Store</strong></a>物件之<a href="store-export.md"><strong>Export</strong></a>方法的<em>SaveAs</em>值無效。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-157">The <em>SaveAs</em> value passed to the <a href="store-export.md"><strong>Export</strong></a> method of the <a href="store.md"><strong>Store</strong></a> object was not valid.</span></span> <br/> <span data-ttu-id="cb3b3-158">下列清單顯示有效的 <em>SaveAs</em> 值：</span><span class="sxs-lookup"><span data-stu-id="cb3b3-158">The following list shows the valid <em>SaveAs</em> values:</span></span>
<ul>
<li><span data-ttu-id="cb3b3-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span><span class="sxs-lookup"><span data-stu-id="cb3b3-159">CAPICOM_STORE_SAVE_AS_SERIALIZED</span></span></li>
<li><span data-ttu-id="cb3b3-160">CAPICOM_STORE_SAVE_AS_PKCS7</span><span class="sxs-lookup"><span data-stu-id="cb3b3-160">CAPICOM_STORE_SAVE_AS_PKCS7</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="cb3b3-161">0x80880233</span><span class="sxs-lookup"><span data-stu-id="cb3b3-161">0x80880233</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-162"><strong>CAPICOM_E_ATTRIBUTE_NAME_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-163">尚未初始化<a href="attribute.md"><strong>Attribute</strong></a>物件的<a href="attribute-name.md"><strong>Name</strong></a>屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-163">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="cb3b3-164">設定 [ <a href="attribute-name.md"><strong>名稱</strong></a> ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-164">Set the <a href="attribute-name.md"><strong>Name</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-165">0x80880240</span><span class="sxs-lookup"><span data-stu-id="cb3b3-165">0x80880240</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-166"><strong>CAPICOM_E_ATTRIBUTE_VALUE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-167">尚未初始化<a href="attribute.md"><strong>Attribute</strong></a>物件的<a href="attribute-value.md"><strong>Value</strong></a>屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-167">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="cb3b3-168">設定 <a href="attribute-value.md"><strong>Value</strong></a> 屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-168">Set the <a href="attribute-value.md"><strong>Value</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-169">0x80880241</span><span class="sxs-lookup"><span data-stu-id="cb3b3-169">0x80880241</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-170"><strong>CAPICOM_E_ATTRIBUTE_INVALID_NAME</strong></span></span></td>
<td><span data-ttu-id="cb3b3-171"><a href="attribute.md"><strong>Attribute</strong></a>物件的<a href="attribute-name.md"><strong>Name</strong></a>屬性無效。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-171">The <a href="attribute-name.md"><strong>Name</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="cb3b3-172">下列清單顯示有效的屬性名稱：</span><span class="sxs-lookup"><span data-stu-id="cb3b3-172">The following list shows the valid attribute names:</span></span>
<ul>
<li><span data-ttu-id="cb3b3-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span><span class="sxs-lookup"><span data-stu-id="cb3b3-173">CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME</span></span></li>
<li><span data-ttu-id="cb3b3-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span><span class="sxs-lookup"><span data-stu-id="cb3b3-174">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME</span></span></li>
<li><span data-ttu-id="cb3b3-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cb3b3-175">CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="cb3b3-176">0x80880242</span><span class="sxs-lookup"><span data-stu-id="cb3b3-176">0x80880242</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-177"><strong>CAPICOM_E_ATTRIBUTE_INVALID_VALUE</strong></span></span></td>
<td><span data-ttu-id="cb3b3-178"><a href="attribute.md"><strong>Attribute</strong></a>物件的<a href="attribute-value.md"><strong>Value</strong></a>屬性無效，因為資料類型不符合<strong>名稱</strong>屬性所指定的資料類型。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-178">The <a href="attribute-value.md"><strong>Value</strong></a> property of the <a href="attribute.md"><strong>Attribute</strong></a> object is not valid because the data type does not match the data type indicated by the <strong>Name</strong> property.</span></span> <br/> <span data-ttu-id="cb3b3-179">例如，如果 [ <a href="attribute-value.md"><strong>名稱</strong></a> ] 屬性設定為 [CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME]，則資料類型必須是 [ <strong>日期</strong>]。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-179">For example, if the <a href="attribute-value.md"><strong>Name</strong></a> property is set to CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME, the data type must be <strong>DATE</strong>.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-180">0x80880243</span><span class="sxs-lookup"><span data-stu-id="cb3b3-180">0x80880243</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-181"><strong>CAPICOM_E_SIGNER_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-182"><a href="signer.md"><strong>簽署者</strong></a>物件尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-182">The <a href="signer.md"><strong>Signer</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="cb3b3-183">若要初始化 <a href="signer.md"><strong>簽署者</strong></a> 物件，請設定 <a href="signer-certificate.md"><strong>Certificate</strong></a> 屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-183">To initialize the <a href="signer.md"><strong>Signer</strong></a> object, set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-184">0x80880250</span><span class="sxs-lookup"><span data-stu-id="cb3b3-184">0x80880250</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-185"><strong>CAPICOM_E_SIGNER_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="cb3b3-186">在 <a href="signeddata.md"><strong>SignedData</strong></a> 物件中找不到簽署人。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-186">The signer cannot be found in the <a href="signeddata.md"><strong>SignedData</strong></a> object.</span></span> <br/> <span data-ttu-id="cb3b3-187">通常不會發生這種情況，因為 <a href="signeddata.md"><strong>SignedData</strong></a> 物件是由 CAPICOM 所建立;但是，如果 <strong>SignedData</strong> 物件是由協力廠商產品所建立，則簽署者的憑證可能不會包含在 PKCS #7 結構中。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-187">Usually, this does not happen with a <a href="signeddata.md"><strong>SignedData</strong></a> object that was created by CAPICOM; however, if the <strong>SignedData</strong> object was created by a third-party product, the signer's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-188">0x80880251</span><span class="sxs-lookup"><span data-stu-id="cb3b3-188">0x80880251</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-189"><strong>CAPICOM_E_SIGNER_NO_CHAIN</strong></span></span></td>
<td><span data-ttu-id="cb3b3-190">在<a href="signer.md"><strong>簽署人</strong></a>物件中找不到<a href="chain.md"><strong>鏈</strong></a>物件。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-190">A <a href="chain.md"><strong>Chain</strong></a> object cannot be found in the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-191">0x80880252//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-191">0x80880252 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-192"><strong>CAPICOM_E_SIGNER_INVALID_USAGE</strong></span></span></td>
<td><span data-ttu-id="cb3b3-193">嘗試以不正確方式使用簽署人。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-193">An attempt is made to use the signer in a way that is not valid.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-194">0x80880253 //v2.0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-194">0x80880253 //v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-195"><strong>CAPICOM_E_SIGN_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-196"><a href="signeddata.md"><strong>SignedData</strong></a>物件尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-196">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="cb3b3-197">若要初始化 <a href="signeddata.md"><strong>SignedData</strong></a> 物件，請設定 <a href="signeddata-content.md"><strong>Content</strong></a> 屬性，或呼叫 <a href="signeddata-verify.md"><strong>Verify</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-197">To initialize the <a href="signeddata.md"><strong>SignedData</strong></a> object, set the <a href="signeddata-content.md"><strong>Content</strong></a> property or call the <a href="signeddata-verify.md"><strong>Verify</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-198">0x80880260</span><span class="sxs-lookup"><span data-stu-id="cb3b3-198">0x80880260</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-199"><strong>CAPICOM_E_SIGN_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="cb3b3-200"><a href="signeddata.md"><strong>SignedData</strong></a>物件包含不正確類型。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-200">The <a href="signeddata.md"><strong>SignedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="cb3b3-201">通常，這會在嘗試使用 <a href="signeddata.md"><strong>SignedData</strong></a> 物件驗證封包訊息時發生，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-201">Usually, this happens when an attempt is made to verify an enveloped message with a <a href="signeddata.md"><strong>SignedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-202">0x80880261</span><span class="sxs-lookup"><span data-stu-id="cb3b3-202">0x80880261</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-203"><strong>CAPICOM_E_SIGN_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-204"><a href="signeddata.md"><strong>SignedData</strong></a>物件尚未簽署。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-204">The <a href="signeddata.md"><strong>SignedData</strong></a> object has not been signed.</span></span> <br/> <span data-ttu-id="cb3b3-205">若要簽署 <a href="signeddata.md"><strong>SignedData</strong></a> 物件，請呼叫 <a href="signeddata-sign.md"><strong>sign</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-205">To sign the <a href="signeddata.md"><strong>SignedData</strong></a> object, call the <a href="signeddata-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-206">0x80880262</span><span class="sxs-lookup"><span data-stu-id="cb3b3-206">0x80880262</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-207"><strong>CAPICOM_E_INVALID_ALGORITHM</strong></span></span></td>
<td><span data-ttu-id="cb3b3-208"><a href="algorithm.md"><strong>演算法</strong></a>物件的 [<a href="algorithm-name.md"><strong>名稱</strong></a>] 屬性的演算法值無效。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-208">The algorithm value for the <a href="algorithm-name.md"><strong>Name</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="cb3b3-209">下列清單顯示 <a href="algorithm-name.md"><strong>Name</strong></a> 屬性的有效演算法值：</span><span class="sxs-lookup"><span data-stu-id="cb3b3-209">The following list shows the valid algorithm values for the <a href="algorithm-name.md"><strong>Name</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="cb3b3-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span><span class="sxs-lookup"><span data-stu-id="cb3b3-210">CAPICOM_ENCRYPTION_ALGORITHM_RC2</span></span></li>
<li><span data-ttu-id="cb3b3-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span><span class="sxs-lookup"><span data-stu-id="cb3b3-211">CAPICOM_ENCRYPTION_ALGORITHM_RC4</span></span></li>
<li><span data-ttu-id="cb3b3-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span><span class="sxs-lookup"><span data-stu-id="cb3b3-212">CAPICOM_ENCRYPTION_ALGORITHM_DES</span></span></li>
<li><span data-ttu-id="cb3b3-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span><span class="sxs-lookup"><span data-stu-id="cb3b3-213">CAPICOM_ENCRYPTION_ALGORITHM_3DES</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="cb3b3-214">0x80880270</span><span class="sxs-lookup"><span data-stu-id="cb3b3-214">0x80880270</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-215"><strong>CAPICOM_E_INVALID_KEY_LENGTH</strong></span></span></td>
<td><span data-ttu-id="cb3b3-216"><a href="algorithm.md"><strong>演算法</strong></a>物件之<a href="algorithm-keylength.md"><strong>KeyLength</strong></a>屬性的金鑰長度值無效。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-216">The key length value for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property of the <a href="algorithm.md"><strong>Algorithm</strong></a> object is not valid.</span></span> <br/> <span data-ttu-id="cb3b3-217">下列清單顯示 <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> 屬性的有效金鑰長度值：</span><span class="sxs-lookup"><span data-stu-id="cb3b3-217">The following list shows the valid key length values for the <a href="algorithm-keylength.md"><strong>KeyLength</strong></a> property:</span></span>
<ul>
<li><span data-ttu-id="cb3b3-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span><span class="sxs-lookup"><span data-stu-id="cb3b3-218">CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM</span></span></li>
<li><span data-ttu-id="cb3b3-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span><span class="sxs-lookup"><span data-stu-id="cb3b3-219">CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS</span></span></li>
<li><span data-ttu-id="cb3b3-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span><span class="sxs-lookup"><span data-stu-id="cb3b3-220">CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS</span></span></li>
<li><span data-ttu-id="cb3b3-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span><span class="sxs-lookup"><span data-stu-id="cb3b3-221">CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS</span></span></li>
</ul>
<br/></td>
<td><span data-ttu-id="cb3b3-222">0x80880271</span><span class="sxs-lookup"><span data-stu-id="cb3b3-222">0x80880271</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-223"><strong>CAPICOM_E_ENVELOP_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-224"><a href="envelopeddata.md"><strong>EnvelopedData</strong></a>物件尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-224">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="cb3b3-225">若要初始化 <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> 物件，請設定 <a href="envelopeddata-content.md"><strong>Content</strong></a> 屬性，或呼叫 <a href="envelopeddata-decrypt.md"><strong>解密</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-225">To initialize the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object, either set the <a href="envelopeddata-content.md"><strong>Content</strong></a> property or call the <a href="envelopeddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-226">0x80880280</span><span class="sxs-lookup"><span data-stu-id="cb3b3-226">0x80880280</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-227"><strong>CAPICOM_E_ENVELOP_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="cb3b3-228"><a href="envelopeddata.md"><strong>EnvelopedData</strong></a>物件包含不正確類型。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-228">The <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object contains a type that is not valid.</span></span> <br/> <span data-ttu-id="cb3b3-229">通常，這會在嘗試使用 <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> 物件驗證已簽署的訊息時發生，反之亦然。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-229">Usually, this happens when an attempt is made to verify a signed message with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object or vice versa.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-230">0x80880281</span><span class="sxs-lookup"><span data-stu-id="cb3b3-230">0x80880281</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-231"><strong>CAPICOM_E_ENVELOP_NO_RECIPIENT</strong></span></span></td>
<td><span data-ttu-id="cb3b3-232">呼叫<strong>EnvelopedData</strong>物件的<a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a>方法時，不會在<a href="envelopeddata.md"><strong>EnvelopedData</strong></a>物件中指定任何收件者。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-232">There is no recipient specified in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object when the <a href="envelopeddata-encrypt.md"><strong>Encrypt</strong></a> method of an <strong>EnvelopedData</strong> object is called.</span></span> <br/> <span data-ttu-id="cb3b3-233">若要加入收件者，請呼叫收件者 <a href="recipients-add.md"><strong>。 add</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-233">To add a recipient, call the <a href="recipients-add.md"><strong>Recipients.Add</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-234">0x80880282</span><span class="sxs-lookup"><span data-stu-id="cb3b3-234">0x80880282</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-235"><strong>CAPICOM_E_ENVELOP_RECIPIENT_NOT_FOUND</strong></span></span></td>
<td><span data-ttu-id="cb3b3-236">在 <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> 物件中找不到收件者。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-236">The recipient cannot be found in the <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object.</span></span> <br/> <span data-ttu-id="cb3b3-237">通常不會發生這種情況，因為 <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> 物件是由 CAPICOM 所建立;但是，如果 <strong>EnvelopedData</strong> 物件是由協力廠商產品所建立，則該收件者的憑證可能不會包含在 PKCS #7 結構中。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-237">Usually, this does not happen with an <a href="envelopeddata.md"><strong>EnvelopedData</strong></a> object that was created by CAPICOM; however, if the <strong>EnvelopedData</strong> object was created by a third-party product, the recipient's certificate may not be included in the PKCS #7 structure.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-238">0x80880283</span><span class="sxs-lookup"><span data-stu-id="cb3b3-238">0x80880283</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-239"><strong>CAPICOM_E_ENCRYPT_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-240"><a href="encrypteddata.md"><strong>A</strong></a>物件尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-240">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="cb3b3-241">若要初始化 <a href="encrypteddata.md"><strong>a</strong></a> 物件，請設定 <a href="encrypteddata-content.md"><strong>Content</strong></a> 屬性，或呼叫 <a href="encrypteddata-decrypt.md"><strong>解密</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-241">To initialize the <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, either set the <a href="encrypteddata-content.md"><strong>Content</strong></a> property or call the <a href="encrypteddata-decrypt.md"><strong>Decrypt</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-242">0x80880290</span><span class="sxs-lookup"><span data-stu-id="cb3b3-242">0x80880290</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-243"><strong>CAPICOM_E_ENCRYPT_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="cb3b3-244"><a href="encrypteddata.md"><strong>A</strong></a>物件不是有效的類型。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-244">The <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object is not a valid type.</span></span> <br/> <span data-ttu-id="cb3b3-245">這通常表示資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-245">Usually, this means the data is corrupted.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-246">0x80880291</span><span class="sxs-lookup"><span data-stu-id="cb3b3-246">0x80880291</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-247"><strong>CAPICOM_E_ENCRYPT_NO_SECRET</strong></span></span></td>
<td><span data-ttu-id="cb3b3-248"><a href="encrypteddata.md"><strong>A</strong></a>物件的密碼尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-248">The secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object has not been initialized.</span></span> <br/> <span data-ttu-id="cb3b3-249">若要初始化 <a href="encrypteddata.md"><strong>a</strong></a> 物件的秘密，請呼叫 <a href="encrypteddata-setsecret.md"><strong>>client.setsecret</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-249">To initialize the secret of an <a href="encrypteddata.md"><strong>EncryptedData</strong></a> object, call the <a href="encrypteddata-setsecret.md"><strong>SetSecret</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-250">0x80880292</span><span class="sxs-lookup"><span data-stu-id="cb3b3-250">0x80880292</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-251"><strong>CAPICOM_E_PRI加值稅E_KEY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-251"><strong>CAPICOM_E_PRIVATE_KEY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-252"><a href="privatekey.md"><strong>PrivateKey</strong></a>物件尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-252">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-253">0x80880300//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-253">0x80880300 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-254"><strong>CAPICOM_E_PRI加值稅E_KEY_NOT_EXPORTABLE</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-254"><strong>CAPICOM_E_PRIVATE_KEY_NOT_EXPORTABLE</strong></span></span></td>
<td><span data-ttu-id="cb3b3-255">無法匯出 <a href="privatekey.md"><strong>PrivateKey</strong></a> 物件。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-255">The <a href="privatekey.md"><strong>PrivateKey</strong></a> object cannot be exported.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-256">0x80880301//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-256">0x80880301 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-257"><strong>CAPICOM_E_ENCODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-258"><a href="encodeddata.md"><strong>EncodedData</strong></a>物件尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-258">The <a href="encodeddata.md"><strong>EncodedData</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-259">0x80880320//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-259">0x80880320 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-260"><strong>CAPICOM_E_EXTENSION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-261"><a href="extension.md"><strong>擴充</strong></a>物件尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-261">The <a href="extension.md"><strong>Extension</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-262">0x80880330//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-262">0x80880330 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-263"><strong>CAPICOM_E_PROPERTY_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-264"><a href="extendedproperty.md"><strong>ExtendedProperty</strong></a>物件的<a href="extendedproperty-propid.md"><strong>PropID</strong></a>屬性尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-264">The <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of the <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-265">0x80880340//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-265">0x80880340 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-266"><strong>CAPICOM_E_FIND_INVALID_TYPE</strong></span></span></td>
<td><span data-ttu-id="cb3b3-267">憑證的 <em>FindType</em> 參數 <a href="certificates-find.md"><strong>。 Find</strong></a> 方法不是 <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-267">The <em>FindType</em> parameter of the <a href="certificates-find.md"><strong>Certificates.Find</strong></a> method is not a value of the <a href="capicom-certificate-find-type.md"><strong>CAPICOM_CERTIFICATE_FIND_TYPE</strong></a> enumeration.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-268">0x80880350//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-268">0x80880350 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-269"><strong>CAPICOM_E_FIND_INVALID_PREDEFINED_POLICY</strong></span></span></td>
<td><span data-ttu-id="cb3b3-270">針對尋找作業指定的預先定義原則無效。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-270">The specified predefined policy for the find operation is not valid.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-271">0x80880351//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-271">0x80880351 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-272"><strong>CAPICOM_E_CODE_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-273"><a href="signedcode.md"><strong>SignedCode</strong></a>物件尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-273">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-274">0x80880360//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-274">0x80880360 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-275"><strong>CAPICOM_E_CODE_NOT_SIGNED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-276"><a href="signedcode.md"><strong>SignedCode</strong></a>物件尚未簽署。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-276">The <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been signed.</span></span><br/> <span data-ttu-id="cb3b3-277">若要簽署 <a href="signedcode.md"><strong>SignedCode</strong></a> 物件，請呼叫 <a href="signedcode-sign.md"><strong>sign</strong></a> 方法。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-277">To sign the <a href="signedcode.md"><strong>SignedCode</strong></a> object, call the <a href="signedcode-sign.md"><strong>Sign</strong></a> method.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-278">0x80880361//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-278">0x80880361 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-279"><strong>CAPICOM_E_CODE_DESCRIPTION_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-280"><a href="signedcode.md"><strong>SignedCode</strong></a>物件的<a href="signedcode-description.md"><strong>Description</strong></a>屬性尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-280">The <a href="signedcode-description.md"><strong>Description</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-281">0x80880362//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-281">0x80880362 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-282"><strong>CAPICOM_E_CODE_DESCRIPTION_URL_NOT_INITIALIZED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-283"><a href="signedcode.md"><strong>SignedCode</strong></a>物件的<a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a>屬性尚未初始化。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-283">The <a href="signedcode-descriptionurl.md"><strong>DescriptionURL</strong></a> property of the <a href="signedcode.md"><strong>SignedCode</strong></a> object has not been initialized.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-284">0x80880363//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-284">0x80880363 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-285"><strong>CAPICOM_E_CODE_INVALID_TIMESTAMP_URL</strong></span></span></td>
<td><span data-ttu-id="cb3b3-286"><a href="signedcode-timestamp.md"><strong>SignedCode</strong></a>的<em>URL</em>參數無效。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-286">The <em>URL</em> parameter of the <a href="signedcode-timestamp.md"><strong>SignedCode.Timestamp</strong></a> method is not valid.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-287">0x80880364//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-287">0x80880364 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-288"><strong>CAPICOM_E_HASH_NO_DATA</strong></span></span></td>
<td><span data-ttu-id="cb3b3-289"><a href="hasheddata.md"><strong>HashedData</strong></a>物件不包含任何資料。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-289">The <a href="hasheddata.md"><strong>HashedData</strong></a> object does not contain any data.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-290">0x80880370//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-290">0x80880370 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-291"><strong>CAPICOM_E_INVALID_CONVERT_TYPE</strong></span></span></td>
<td><span data-ttu-id="cb3b3-292">轉換類型無效。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-292">The convert type is not valid.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-293">0x80880380//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-293">0x80880380 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-294"><strong>CAPICOM_E_NOT_SUPPORTED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-295">目前的平臺不支援要求的操作。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-295">The requested operation is not supported in the current platform.</span></span> <br/></td>
<td><span data-ttu-id="cb3b3-296">0x80880900</span><span class="sxs-lookup"><span data-stu-id="cb3b3-296">0x80880900</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-297"><strong>CAPICOM_E_UI_DISABLED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-297"><strong>CAPICOM_E_UI_DISABLED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-298">簽署時，尚未設定<a href="signer.md"><strong>簽署者</strong></a>物件的<a href="signer-certificate.md"><strong>Certificate</strong></a>屬性，但使用者憑證的提示已停用。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-298">When signing, the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object has not been set, but the prompt for the user certificate has been disabled.</span></span> <br/> <span data-ttu-id="cb3b3-299">設定<a href="settings.md"><strong>[設定] 物件的</strong></a>[ <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> ] 屬性，或設定 [<a href="signer.md"><strong>簽署者</strong></a>] 物件的 [<a href="signer-certificate.md"><strong>憑證</strong></a>] 屬性，即可啟用提示。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-299">Either enable the prompt by setting the <a href="settings-enablepromptforcertificateui.md"><strong>EnablePromptForCertificateUI</strong></a> property of the <a href="settings.md"><strong>Settings</strong></a> object, or set the <a href="signer-certificate.md"><strong>Certificate</strong></a> property of the <a href="signer.md"><strong>Signer</strong></a> object.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-300">0x80880901</span><span class="sxs-lookup"><span data-stu-id="cb3b3-300">0x80880901</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-301"><strong>CAPICOM_E_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-301"><strong>CAPICOM_E_CANCELLED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-302">使用者已取消作業。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-302">The operation has been canceled by the user.</span></span> <br/> <span data-ttu-id="cb3b3-303">當系統提示使用者執行特定作業（例如存取私密金鑰），而使用者取消作業時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-303">This happens when the user is prompted for permission to carry out a certain operation, such as accessing the private key, and the user cancels the operation.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-304">0x80880902</span><span class="sxs-lookup"><span data-stu-id="cb3b3-304">0x80880902</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-305"><strong>CAPICOM_E_NOT_ALLOWED</strong></span></span></td>
<td><span data-ttu-id="cb3b3-306">不允許嘗試的操作。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-306">The attempted operation is not allowed.</span></span><br/> <span data-ttu-id="cb3b3-307">例如，如果物件附加至憑證，就不允許變更<a href="extendedproperty.md"><strong>ExtendedProperty</strong></a>物件的<a href="extendedproperty-propid.md"><strong>PropID</strong></a>屬性。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-307">For example, changing the <a href="extendedproperty-propid.md"><strong>PropID</strong></a> property of an <a href="extendedproperty.md"><strong>ExtendedProperty</strong></a> object is not allowed if the object is attached to a certificate.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-308">0x80880903//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-308">0x80880903 // v2.0</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-309"><strong>CAPICOM_E_OUT_OF_RESOURCE</strong></span></span></td>
<td><span data-ttu-id="cb3b3-310">CAPICOM 的資源已用盡。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-310">CAPICOM has run out of a resource.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-311">0x80880904//v2。0</span><span class="sxs-lookup"><span data-stu-id="cb3b3-311">0x80880904 // v2.0</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cb3b3-312"><strong>CAPICOM_E_INTERNAL</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-312"><strong>CAPICOM_E_INTERNAL</strong></span></span></td>
<td><span data-ttu-id="cb3b3-313">發生內部錯誤。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-313">An internal error has occurred.</span></span> <br/> <span data-ttu-id="cb3b3-314">請洽詢 Microsoft 技術支援人員以取得協助。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-314">Contact Microsoft Technical Support for assistance.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-315">0x80880911</span><span class="sxs-lookup"><span data-stu-id="cb3b3-315">0x80880911</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cb3b3-316"><strong>CAPICOM_E_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="cb3b3-316"><strong>CAPICOM_E_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="cb3b3-317">發生未知的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-317">An unknown error has occurred.</span></span> <br/> <span data-ttu-id="cb3b3-318">盡可能收集最多的資訊，並洽詢您的廠商。</span><span class="sxs-lookup"><span data-stu-id="cb3b3-318">Collect as much information as possible, and contact your vendor.</span></span><br/></td>
<td><span data-ttu-id="cb3b3-319">0x80880999</span><span class="sxs-lookup"><span data-stu-id="cb3b3-319">0x80880999</span></span></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="cb3b3-320">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb3b3-320">Requirements</span></span>



| <span data-ttu-id="cb3b3-321">需求</span><span class="sxs-lookup"><span data-stu-id="cb3b3-321">Requirement</span></span> | <span data-ttu-id="cb3b3-322">值</span><span class="sxs-lookup"><span data-stu-id="cb3b3-322">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cb3b3-323">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="cb3b3-323">Redistributable</span></span><br/> | <span data-ttu-id="cb3b3-324">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="cb3b3-324">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="cb3b3-325">標頭</span><span class="sxs-lookup"><span data-stu-id="cb3b3-325">Header</span></span><br/>          | <dl> <span data-ttu-id="cb3b3-326"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="cb3b3-326"><dt>Capicom.h</dt></span></span> </dl> |



 

 




