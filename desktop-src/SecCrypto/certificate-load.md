---
description: 從檔案匯入憑證。
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: ICertificate2：： Load 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9193297ad7eacc1994e4bf3729a87054573b1574
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977390"
---
# <a name="icertificate2load-method"></a><span data-ttu-id="c35c8-103">ICertificate2：： Load 方法</span><span class="sxs-lookup"><span data-stu-id="c35c8-103">ICertificate2::Load method</span></span>

<span data-ttu-id="c35c8-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="c35c8-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c35c8-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="c35c8-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c35c8-106">**Load** 方法會從檔案匯入憑證。</span><span class="sxs-lookup"><span data-stu-id="c35c8-106">The **Load** method imports a certificate from a file.</span></span> <span data-ttu-id="c35c8-107">此方法是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="c35c8-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="c35c8-108">語法</span><span class="sxs-lookup"><span data-stu-id="c35c8-108">Syntax</span></span>


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c35c8-109">參數</span><span class="sxs-lookup"><span data-stu-id="c35c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c35c8-110">*檔案名* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c35c8-110">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c35c8-111">字串，包含包含憑證資料的 .cer 或 .pfx 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c35c8-111">A string that contains the path to a .cer or .pfx file that contains the certificate data.</span></span>

</dd> <dt>

<span data-ttu-id="c35c8-112">*密碼* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c35c8-112">*Password* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c35c8-113">字串，包含 [*私密金鑰*](../secgloss/p-gly.md)檔案的 [*明文*](../secgloss/p-gly.md)密碼。</span><span class="sxs-lookup"><span data-stu-id="c35c8-113">A string that contains the [*plaintext*](../secgloss/p-gly.md) password to the [*private key*](../secgloss/p-gly.md) file.</span></span> <span data-ttu-id="c35c8-114">密碼最多可包含32個 Unicode 字元，包括結束的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="c35c8-114">The password can contain up to 32 Unicode characters, including a terminating null character.</span></span> <span data-ttu-id="c35c8-115">如需保護密碼的相關資訊，請參閱 [處理密碼](../secbp/handling-passwords.md)。</span><span class="sxs-lookup"><span data-stu-id="c35c8-115">For information about protecting the password, see [Handling Passwords](../secbp/handling-passwords.md).</span></span>

</dd> <dt>

<span data-ttu-id="c35c8-116">*KeyStorageFlag* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c35c8-116">*KeyStorageFlag* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c35c8-117">用來定義金鑰儲存旗標之 [**CAPICOM \_ 金鑰 \_ 儲存 \_ 旗**](capicom-key-storage-flag.md) 標列舉的值。</span><span class="sxs-lookup"><span data-stu-id="c35c8-117">A value of the [**CAPICOM\_KEY\_STORAGE\_FLAG**](capicom-key-storage-flag.md) enumeration that defines key storage flags.</span></span> <span data-ttu-id="c35c8-118">預設值是 [CAPICOM \_ 金鑰 \_ 儲存] \_ 預設值。</span><span class="sxs-lookup"><span data-stu-id="c35c8-118">The default is CAPICOM\_KEY\_STORAGE\_DEFAULT.</span></span> <span data-ttu-id="c35c8-119">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="c35c8-119">The following table shows the possible values.</span></span>



| <span data-ttu-id="c35c8-120">值</span><span class="sxs-lookup"><span data-stu-id="c35c8-120">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="c35c8-121">意義</span><span class="sxs-lookup"><span data-stu-id="c35c8-121">Meaning</span></span>                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <span data-ttu-id="c35c8-122"><dt>**CAPICOM \_ 金鑰 \_ 儲存 \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="c35c8-122"><dt>**CAPICOM\_KEY\_STORAGE\_DEFAULT**</dt></span></span> </dl>                       | <span data-ttu-id="c35c8-123">預設金鑰存放區。</span><span class="sxs-lookup"><span data-stu-id="c35c8-123">Default key storage.</span></span><br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <span data-ttu-id="c35c8-124"><dt>**可 \_ 匯出的 CAPICOM 金鑰 \_ 儲存體 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c35c8-124"><dt>**CAPICOM\_KEY\_STORAGE\_EXPORTABLE**</dt></span></span> </dl>              | <span data-ttu-id="c35c8-125">金鑰可以匯出。</span><span class="sxs-lookup"><span data-stu-id="c35c8-125">The key is exportable.</span></span><br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <span data-ttu-id="c35c8-126"><dt>**已 \_ 保護的 CAPICOM 金鑰 \_ 儲存區 \_ 使用者 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c35c8-126"><dt>**CAPICOM\_KEY\_STORAGE\_USER\_PROTECTED**</dt></span></span> </dl> | <span data-ttu-id="c35c8-127">金鑰是由使用者保護。</span><span class="sxs-lookup"><span data-stu-id="c35c8-127">The key is user protected.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="c35c8-128">*KeyLocation* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="c35c8-128">*KeyLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c35c8-129">定義索引鍵位置類型之 [**CAPICOM \_ 金鑰 \_ 位置**](capicom-key-location.md) 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="c35c8-129">A value of the [**CAPICOM\_KEY\_LOCATION**](capicom-key-location.md) enumeration that defines key location types.</span></span> <span data-ttu-id="c35c8-130">預設值是 [CAPICOM \_ 目前 \_ 使用者 \_ 金鑰]。</span><span class="sxs-lookup"><span data-stu-id="c35c8-130">The default value is CAPICOM\_CURRENT\_USER\_KEY.</span></span> <span data-ttu-id="c35c8-131">下表顯示可能的值。</span><span class="sxs-lookup"><span data-stu-id="c35c8-131">The following table shows the possible values.</span></span>



| <span data-ttu-id="c35c8-132">值</span><span class="sxs-lookup"><span data-stu-id="c35c8-132">Value</span></span>                                                                                                                                                                                               | <span data-ttu-id="c35c8-133">意義</span><span class="sxs-lookup"><span data-stu-id="c35c8-133">Meaning</span></span>                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <span data-ttu-id="c35c8-134"><dt>**CAPICOM \_ 目前 \_ 使用者 \_ 金鑰**</dt></span><span class="sxs-lookup"><span data-stu-id="c35c8-134"><dt>**CAPICOM\_CURRENT\_USER\_KEY**</dt></span></span> </dl>    | <span data-ttu-id="c35c8-135">金鑰是使用者金鑰。</span><span class="sxs-lookup"><span data-stu-id="c35c8-135">The key is a user key.</span></span><br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <span data-ttu-id="c35c8-136"><dt>**CAPICOM \_ 本機 \_ 電腦 \_ 金鑰**</dt></span><span class="sxs-lookup"><span data-stu-id="c35c8-136"><dt>**CAPICOM\_LOCAL\_MACHINE\_KEY**</dt></span></span> </dl> | <span data-ttu-id="c35c8-137">金鑰是電腦金鑰。</span><span class="sxs-lookup"><span data-stu-id="c35c8-137">The key is a machine key.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c35c8-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="c35c8-138">Return value</span></span>

<span data-ttu-id="c35c8-139">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c35c8-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c35c8-140">備註</span><span class="sxs-lookup"><span data-stu-id="c35c8-140">Remarks</span></span>

<span data-ttu-id="c35c8-141">\_ \_ \_ 從 web 應用程式編寫腳本時，此方法不允許引發 CAPICOM E。</span><span class="sxs-lookup"><span data-stu-id="c35c8-141">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="c35c8-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="c35c8-142">Requirements</span></span>



| <span data-ttu-id="c35c8-143">需求</span><span class="sxs-lookup"><span data-stu-id="c35c8-143">Requirement</span></span> | <span data-ttu-id="c35c8-144">值</span><span class="sxs-lookup"><span data-stu-id="c35c8-144">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c35c8-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c35c8-145">End of client support</span></span><br/> | <span data-ttu-id="c35c8-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c35c8-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c35c8-147">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c35c8-147">End of server support</span></span><br/> | <span data-ttu-id="c35c8-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c35c8-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c35c8-149">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c35c8-149">Redistributable</span></span><br/>       | <span data-ttu-id="c35c8-150">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c35c8-150">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c35c8-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c35c8-151">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c35c8-152"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c35c8-152"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
