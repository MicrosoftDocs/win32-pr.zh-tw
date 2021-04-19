---
description: 從檔案將憑證匯入到存放區。
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Store Load 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 32261a6fd8c5cf4382832d8286d63ce5d44fb542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999747"
---
# <a name="storeload-method"></a><span data-ttu-id="a28ad-103">Store Load 方法</span><span class="sxs-lookup"><span data-stu-id="a28ad-103">Store.Load method</span></span>

<span data-ttu-id="a28ad-104">\[**Load** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="a28ad-104">\[The **Load** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a28ad-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="a28ad-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a28ad-106">**Load** 方法會從檔案將憑證匯入到存放區。</span><span class="sxs-lookup"><span data-stu-id="a28ad-106">The **Load** method imports certificates from a file into the store.</span></span>

## <a name="syntax"></a><span data-ttu-id="a28ad-107">語法</span><span class="sxs-lookup"><span data-stu-id="a28ad-107">Syntax</span></span>


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a28ad-108">參數</span><span class="sxs-lookup"><span data-stu-id="a28ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a28ad-109">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a28ad-109">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a28ad-110">字串，其中包含 .cer、. .sst、.spc、. p7s 或 .pfx 檔案的路徑，或任何 Authenticode 簽署的檔案。</span><span class="sxs-lookup"><span data-stu-id="a28ad-110">The string that contains the path to a .cer, .sst, .spc, .p7s, or .pfx file, or any Authenticode signed file.</span></span>

</dd> <dt>

<span data-ttu-id="a28ad-111">*密碼* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a28ad-111">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a28ad-112">字串，其中包含檔案的純文字密碼。</span><span class="sxs-lookup"><span data-stu-id="a28ad-112">The string that contains the plaintext password to the file.</span></span> <span data-ttu-id="a28ad-113">密碼最多可使用32個 Unicode 字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="a28ad-113">Up to 32 Unicode characters, including a terminating null character, can be used for the password.</span></span> <span data-ttu-id="a28ad-114">如需保護密碼的相關資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。</span><span class="sxs-lookup"><span data-stu-id="a28ad-114">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="a28ad-115">*KeyStorageFlag* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a28ad-115">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a28ad-116">用來定義金鑰儲存旗標之 [**CAPICOM \_ 金鑰 \_ 儲存 \_ 旗**](capicom-key-storage-flag.md) 標列舉的值。</span><span class="sxs-lookup"><span data-stu-id="a28ad-116">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="a28ad-117">預設值是 [CAPICOM \_ 金鑰 \_ 儲存] \_ 預設值。</span><span class="sxs-lookup"><span data-stu-id="a28ad-117">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="a28ad-118">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a28ad-118">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a28ad-119">值</span><span class="sxs-lookup"><span data-stu-id="a28ad-119">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="a28ad-120">意義</span><span class="sxs-lookup"><span data-stu-id="a28ad-120">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="a28ad-121"><dt>**CAPICOM \_ 金鑰 \_ 儲存 \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="a28ad-121"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="a28ad-122">預設金鑰存放區。</span><span class="sxs-lookup"><span data-stu-id="a28ad-122">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="a28ad-123"><dt>**可 \_ 匯出的 CAPICOM 金鑰 \_ 儲存體 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a28ad-123"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="a28ad-124">金鑰可以匯出。</span><span class="sxs-lookup"><span data-stu-id="a28ad-124">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="a28ad-125"><dt>**已 \_ 保護的 CAPICOM 金鑰 \_ 儲存區 \_ 使用者 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a28ad-125"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="a28ad-126">金鑰是由使用者保護。</span><span class="sxs-lookup"><span data-stu-id="a28ad-126">The key is user protected.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a28ad-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="a28ad-127">Return value</span></span>

<span data-ttu-id="a28ad-128">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a28ad-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a28ad-129">備註</span><span class="sxs-lookup"><span data-stu-id="a28ad-129">Remarks</span></span>

<span data-ttu-id="a28ad-130">如果在記憶體存放區上呼叫 **Load** 方法，則在刪除記憶體存放區時，將會刪除任何建立的金鑰容器。</span><span class="sxs-lookup"><span data-stu-id="a28ad-130">If the **Load** method is called on a memory store, any key containers that are created will be deleted when the memory store is deleted.</span></span> <span data-ttu-id="a28ad-131">例如，如果 .pfx 檔案載入至記憶體存放區，並在稍後新增至系統存放區 (例如，從記憶體存放區) 的「我的存放區」，則「我的存放區」中的憑證將不會包含金鑰。</span><span class="sxs-lookup"><span data-stu-id="a28ad-131">For example, if a .pfx file is loaded into a memory store and later added to a system store (such as the My store) from the memory store, the certificate in the My store will not contain a key.</span></span> <span data-ttu-id="a28ad-132">在此情況下，.pfx 檔案應該直接載入 My 存放區中。</span><span class="sxs-lookup"><span data-stu-id="a28ad-132">In this case, the .pfx file should be loaded directly into the My store.</span></span>

<span data-ttu-id="a28ad-133">\_ \_ \_ 從 web 應用程式編寫腳本時，此方法不允許引發 CAPICOM E。</span><span class="sxs-lookup"><span data-stu-id="a28ad-133">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

<span data-ttu-id="a28ad-134">如果密碼無法解密私密金鑰檔案，則應該查詢預設 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 。</span><span class="sxs-lookup"><span data-stu-id="a28ad-134">If the password fails to decrypt the private key file, then the default [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) should be queried.</span></span> <span data-ttu-id="a28ad-135">如果預設 CSP 是 Microsoft 基礎密碼編譯提供者，且解密作業失敗，則應該使用 Microsoft 強式密碼編譯提供者或 Microsoft 增強型密碼編譯提供者（視何者而定），再次嘗試進行解密操作。</span><span class="sxs-lookup"><span data-stu-id="a28ad-135">If the default CSP is the Microsoft Base Cryptographic Provider and the decrypt operation fails, then the decrypt operation should be tried again with the Microsoft Strong Cryptographic Provider or Microsoft Enhanced Cryptographic Provider, whichever is available.</span></span>

<span data-ttu-id="a28ad-136">如果要載入到存放區中的憑證與已經存在的憑證相同， **Load** 方法將會從存放區刪除現有的憑證，然後再新增憑證。</span><span class="sxs-lookup"><span data-stu-id="a28ad-136">If the certificate being loaded into the store is the same as one that is already there, the **Load** method will delete the existing certificate from the store and then add the new certificate.</span></span> <span data-ttu-id="a28ad-137">新憑證將繼承現有憑證的屬性。</span><span class="sxs-lookup"><span data-stu-id="a28ad-137">The new certificate will inherit properties from the existing certificate.</span></span> <span data-ttu-id="a28ad-138">新的私密金鑰容器會取代現有的私密金鑰容器。</span><span class="sxs-lookup"><span data-stu-id="a28ad-138">The existing private key container is replaced by the new private key container.</span></span>

## <a name="requirements"></a><span data-ttu-id="a28ad-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="a28ad-139">Requirements</span></span>



| <span data-ttu-id="a28ad-140">需求</span><span class="sxs-lookup"><span data-stu-id="a28ad-140">Requirement</span></span> | <span data-ttu-id="a28ad-141">值</span><span class="sxs-lookup"><span data-stu-id="a28ad-141">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a28ad-142">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a28ad-142">Redistributable</span></span><br/> | <span data-ttu-id="a28ad-143">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a28ad-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a28ad-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a28ad-144">DLL</span></span><br/>             | <dl> <span data-ttu-id="a28ad-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a28ad-145"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a28ad-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a28ad-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a28ad-147">**市集**</span><span class="sxs-lookup"><span data-stu-id="a28ad-147">**Store**</span></span>](store.md)
</dt> </dl>

 

 
