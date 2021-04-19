---
description: 開啟指定的憑證存放區。
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Store. Open 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ef4ffe89a4b726ecfa33fb95d213d809cae2487b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998783"
---
# <a name="storeopen-method"></a><span data-ttu-id="003d2-103">Store. Open 方法</span><span class="sxs-lookup"><span data-stu-id="003d2-103">Store.Open method</span></span>

<span data-ttu-id="003d2-104">\[**Open** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="003d2-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="003d2-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="003d2-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="003d2-106">**Open** 方法會開啟指定的 [*憑證存放區*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="003d2-106">The **Open** method opens a specified [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="003d2-107">根據預設，會以 \_ \_ 唯讀方式開啟 capicom 目前的使用者 \_ 存放區位置和 capicom \_ MY \_ store 存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-107">By default, the CAPICOM\_CURRENT\_USER\_STORE location and CAPICOM\_MY\_STORE store are opened as read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="003d2-108">語法</span><span class="sxs-lookup"><span data-stu-id="003d2-108">Syntax</span></span>


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a><span data-ttu-id="003d2-109">參數</span><span class="sxs-lookup"><span data-stu-id="003d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="003d2-110">*StoreLocation* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="003d2-110">*StoreLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="003d2-111">[CAPICOM \_ 存放區 \_ 位置](capicom-store-location.md)列舉的值，指出要開啟之存放區的位置。</span><span class="sxs-lookup"><span data-stu-id="003d2-111">A value of the [CAPICOM\_STORE\_LOCATION](capicom-store-location.md) enumeration that indicates the location of the store to be opened.</span></span> <span data-ttu-id="003d2-112">預設值是 [CAPICOM \_ 目前 \_ 使用者 \_ 存放區]。</span><span class="sxs-lookup"><span data-stu-id="003d2-112">The default value is CAPICOM\_CURRENT\_USER\_STORE.</span></span> <span data-ttu-id="003d2-113">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="003d2-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="003d2-114">值</span><span class="sxs-lookup"><span data-stu-id="003d2-114">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="003d2-115">意義</span><span class="sxs-lookup"><span data-stu-id="003d2-115">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <span data-ttu-id="003d2-116"><dt>**CAPICOM \_ ACTIVE \_ DIRECTORY \_ 使用者 \_ 存放區**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-116"><dt>**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="003d2-117">存放區是 Active Directory 存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-117">The store is an Active Directory store.</span></span> <span data-ttu-id="003d2-118">如果 Active Directory 存放區開啟為讀取/寫入，則不會產生任何錯誤，但不會保存存放區的任何變更。</span><span class="sxs-lookup"><span data-stu-id="003d2-118">No error will be generated if an Active Directory store is opened as read/write, but any changes to the store will not be persisted.</span></span> <span data-ttu-id="003d2-119">憑證無法在 Active Directory 存放區中新增或移除。</span><span class="sxs-lookup"><span data-stu-id="003d2-119">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <span data-ttu-id="003d2-120"><dt>**CAPICOM \_ 目前的 \_ 使用者 \_ 存放區**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-120"><dt>**CAPICOM\_CURRENT\_USER\_STORE**</dt></span></span> </dl>                             | <span data-ttu-id="003d2-121">存放區是目前的使用者存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-121">The store is a current user store.</span></span> <span data-ttu-id="003d2-122">目前的使用者存放區可能是「讀取/寫入」存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-122">A current user store may be a read/write store.</span></span> <span data-ttu-id="003d2-123">如果是，就會保存存放區內容中的變更。</span><span class="sxs-lookup"><span data-stu-id="003d2-123">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <span data-ttu-id="003d2-124"><dt>**CAPICOM \_ 本機 \_ 電腦 \_ 存放區**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-124"><dt>**CAPICOM\_LOCAL\_MACHINE\_STORE**</dt></span></span> </dl>                          | <span data-ttu-id="003d2-125">存放區是本機電腦存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-125">The store is a local computer store.</span></span> <span data-ttu-id="003d2-126">只有當使用者擁有讀取/寫入權限時，本機電腦存放區才可以是讀取/寫入存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-126">Local computer stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="003d2-127">如果使用者具有讀取/寫入權限，且存放區已開啟讀取/寫入，則會保存存放區內容中的變更。</span><span class="sxs-lookup"><span data-stu-id="003d2-127">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <span data-ttu-id="003d2-128"><dt>**CAPICOM \_ 記憶體 \_ 存放區**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-128"><dt>**CAPICOM\_MEMORY\_STORE**</dt></span></span> </dl>                                                | <span data-ttu-id="003d2-129">存放區是記憶體存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-129">The store is a memory store.</span></span> <span data-ttu-id="003d2-130">存放區內容中的任何變更都不會保存。</span><span class="sxs-lookup"><span data-stu-id="003d2-130">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <span data-ttu-id="003d2-131"><dt>**CAPICOM \_ 智慧 \_ 卡 \_ 使用者 \_ 存放區**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-131"><dt>**CAPICOM\_SMART\_CARD\_USER\_STORE**</dt></span></span> </dl>                   | <span data-ttu-id="003d2-132">存放區是一組目前的智慧卡。</span><span class="sxs-lookup"><span data-stu-id="003d2-132">The store is the group of present smart cards.</span></span> <span data-ttu-id="003d2-133">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="003d2-133">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="003d2-134">*StoreName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="003d2-134">*StoreName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="003d2-135">字串，包含要開啟之系統憑證存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="003d2-135">A string that contains the name of the system certificate store to be opened.</span></span> <span data-ttu-id="003d2-136">預設值是 [CAPICOM \_ 我的 \_ 存放區]。</span><span class="sxs-lookup"><span data-stu-id="003d2-136">The default value is CAPICOM\_MY\_STORE.</span></span> <span data-ttu-id="003d2-137">如果從 web 腳本開啟存放區， \\ 名稱中不允許使用反斜線 () 字元。</span><span class="sxs-lookup"><span data-stu-id="003d2-137">If the store is opened from a web script, the backslash (\\) character is not allowed in the name.</span></span> <span data-ttu-id="003d2-138">除了系統所定義的存放區之外，還可以開啟使用者定義存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-138">In addition to stores defined by the system, user-defined stores can be opened.</span></span>

<span data-ttu-id="003d2-139">這個參數可以是使用者定義的存放區，也可以是下列其中一個系統憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-139">This parameter can be a user-defined store or one of the following system certificate stores.</span></span>



| <span data-ttu-id="003d2-140">值</span><span class="sxs-lookup"><span data-stu-id="003d2-140">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="003d2-141">意義</span><span class="sxs-lookup"><span data-stu-id="003d2-141">Meaning</span></span>                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <span data-ttu-id="003d2-142"><dt>**CAPICOM \_ CA \_ 存放區**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-142"><dt>**CAPICOM\_CA\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="003d2-143">CA 存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-143">CA store.</span></span> <span data-ttu-id="003d2-144">此存放區是用來儲存中繼 CA 憑證。</span><span class="sxs-lookup"><span data-stu-id="003d2-144">This store is used to store intermediate CA certificates.</span></span><br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <span data-ttu-id="003d2-145"><dt>**CAPICOM \_ 我的 \_ 存放區**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-145"><dt>**CAPICOM\_MY\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="003d2-146">我的存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-146">My store.</span></span> <span data-ttu-id="003d2-147">此存放區會用於使用者的個人憑證。</span><span class="sxs-lookup"><span data-stu-id="003d2-147">This store is used for a user's personal certificates.</span></span><br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <span data-ttu-id="003d2-148"><dt>**CAPICOM \_ 其他 \_ 存放區**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-148"><dt>**CAPICOM\_OTHER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="003d2-149">AddressBook 存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-149">AddressBook store.</span></span> <span data-ttu-id="003d2-150">此存放區是用來保留其他人的憑證。</span><span class="sxs-lookup"><span data-stu-id="003d2-150">This store is used to keep the certificates of others.</span></span><br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <span data-ttu-id="003d2-151"><dt>**CAPICOM \_ 根 \_ 存放區**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-151"><dt>**CAPICOM\_ROOT\_STORE**</dt></span></span> </dl>    | <span data-ttu-id="003d2-152">根存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-152">Root store.</span></span> <span data-ttu-id="003d2-153">此存放區是用來儲存根 CA 和自我簽署的受信任憑證。</span><span class="sxs-lookup"><span data-stu-id="003d2-153">This store is used to store the root CA and self-signed, trusted certificates.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="003d2-154">*OpenMode* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="003d2-154">*OpenMode* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="003d2-155">表示存放區開啟模式之 [CAPICOM \_ 存放區 \_ 開啟 \_ 模式](capicom-store-open-mode.md) 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="003d2-155">A value of the [CAPICOM\_STORE\_OPEN\_MODE](capicom-store-open-mode.md) enumeration that indicates the open mode of the store.</span></span> <span data-ttu-id="003d2-156">預設值是 [CAPICOM \_ 存放區 \_ 開啟 \_ 唯讀] \_ 。</span><span class="sxs-lookup"><span data-stu-id="003d2-156">The default value is CAPICOM\_STORE\_OPEN\_READ\_ONLY.</span></span> <span data-ttu-id="003d2-157">如果從 web 腳本開啟存放區，則會強制將這個值強制設 \_ 為 \_ 僅限開放式儲存區 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="003d2-157">If the store is opened from a web script, this value is forced to CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY.</span></span> <span data-ttu-id="003d2-158">此參數可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="003d2-158">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="003d2-159">值</span><span class="sxs-lookup"><span data-stu-id="003d2-159">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="003d2-160">意義</span><span class="sxs-lookup"><span data-stu-id="003d2-160">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <span data-ttu-id="003d2-161"><dt>**允許的 CAPICOM \_ 存放區 \_ 開啟 \_ 上限 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-161"><dt>**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</dt></span></span> </dl> | <span data-ttu-id="003d2-162">如果使用者具有讀取/寫入權限，請以讀取/寫入模式開啟存放區。否則，請在唯讀模式中開啟存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-162">Open the store in read/write mode if the user has read/write permissions; otherwise, open the store in read-only mode.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <span data-ttu-id="003d2-163"><dt>**CAPICOM \_ 存放區 \_ 開啟 \_ 唯讀 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-163"><dt>**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</dt></span></span> </dl>                   | <span data-ttu-id="003d2-164">在唯讀模式開啟存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-164">Open the store in read-only mode.</span></span><br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <span data-ttu-id="003d2-165"><dt>**CAPICOM \_ 存放區 \_ 開啟 \_ 讀 \_ 寫**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-165"><dt>**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</dt></span></span> </dl>                | <span data-ttu-id="003d2-166">以讀取/寫入模式開啟存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-166">Open the store in read/write mode.</span></span><br/>                                                                                     |



 

<span data-ttu-id="003d2-167">下列旗標可以使用邏輯 **OR** 運算，與上表中的值結合。</span><span class="sxs-lookup"><span data-stu-id="003d2-167">The following flags can be combined with the values in the previous table by using a logical-**OR** operation.</span></span>



| <span data-ttu-id="003d2-168">值</span><span class="sxs-lookup"><span data-stu-id="003d2-168">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="003d2-169">意義</span><span class="sxs-lookup"><span data-stu-id="003d2-169">Meaning</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <span data-ttu-id="003d2-170"><dt>**CAPICOM \_ 存放 \_ 區 \_ 僅開啟現有 \_ 的**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-170"><dt>**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</dt></span></span> </dl>          | <span data-ttu-id="003d2-171">僅開啟現有的商店;請勿建立新的存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-171">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="003d2-172">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="003d2-172">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <span data-ttu-id="003d2-173"><dt>**開啟的 CAPICOM \_ 存放區 \_ \_ 包含 \_ 封存**</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-173"><dt>**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</dt></span></span> </dl> | <span data-ttu-id="003d2-174">使用存放區時，請包含封存的憑證。</span><span class="sxs-lookup"><span data-stu-id="003d2-174">Include archived certificates when using the store.</span></span> <span data-ttu-id="003d2-175">在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="003d2-175">Introduced in CAPICOM 2.0.</span></span><br/>   |



 

<span data-ttu-id="003d2-176">某些位置中的存放區只能在唯讀模式中開啟。</span><span class="sxs-lookup"><span data-stu-id="003d2-176">Stores in some locations can be opened only in read-only mode.</span></span> <span data-ttu-id="003d2-177">這些包含在 CAPICOM \_ 本機 \_ 電腦 \_ 存放區中，使用者沒有寫入權限的所有存放區。</span><span class="sxs-lookup"><span data-stu-id="003d2-177">These include all stores in CAPICOM\_LOCAL\_MACHINE\_STORE for which the user does not have write permissions.</span></span> <span data-ttu-id="003d2-178">如果沒有適當的存取權和許可權，嘗試以讀取/寫入存放區的形式開啟存放區，將會導致 **open** 方法失敗。</span><span class="sxs-lookup"><span data-stu-id="003d2-178">Attempts to open a store as a read/write store without proper access and permissions will result in the failure of the **Open** method.</span></span> <span data-ttu-id="003d2-179">Active Directory 存放區可以開啟為讀取/寫入存放區，而不會導致 **Open** 方法失敗，但將不會保存存放區的變更。</span><span class="sxs-lookup"><span data-stu-id="003d2-179">Active Directory stores can be opened as a read/write store without failure of the **Open** method, but changes to the store will not be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="003d2-180">傳回值</span><span class="sxs-lookup"><span data-stu-id="003d2-180">Return value</span></span>

<span data-ttu-id="003d2-181">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="003d2-181">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="003d2-182">備註</span><span class="sxs-lookup"><span data-stu-id="003d2-182">Remarks</span></span>

<span data-ttu-id="003d2-183">如果在智慧卡存放區上呼叫這個方法，可能會叫用額外的智慧卡使用者介面。</span><span class="sxs-lookup"><span data-stu-id="003d2-183">If this method is called on a SmartCard store, additional SmartCard user interfaces may be invoked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="003d2-184">從 web 腳本呼叫這個方法時，腳本必須存取本機電腦上的數位憑證。</span><span class="sxs-lookup"><span data-stu-id="003d2-184">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="003d2-185">如果您允許腳本存取您的數位憑證，執行腳本的網站也可以存取儲存在憑證中的任何個人資訊。</span><span class="sxs-lookup"><span data-stu-id="003d2-185">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="003d2-186">第一次從特定網域呼叫這個方法時，會產生一個對話方塊，使用者必須在此對話方塊中指出是否允許存取憑證。</span><span class="sxs-lookup"><span data-stu-id="003d2-186">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span> <span data-ttu-id="003d2-187">從 web 腳本開啟的存放區會自動強制將 CAPICOM \_ 存放區設為 \_ 開放式 \_ 現有的旗標 \_ 。</span><span class="sxs-lookup"><span data-stu-id="003d2-187">Stores opened from a web script automatically force the CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY flag.</span></span>

 

<span data-ttu-id="003d2-188">如果 *StoreLocation* 為 **CAPICOM \_ 智慧 \_ 卡 \_ 使用者 \_ 存放區**，則會忽略 *StoreName* 。</span><span class="sxs-lookup"><span data-stu-id="003d2-188">If *StoreLocation* is **CAPICOM\_SMART\_CARD\_USER\_STORE**, *StoreName* is ignored.</span></span> <span data-ttu-id="003d2-189">在此情況下，CAPICOM 會讀取所有包含智慧卡之可用讀取器的憑證。</span><span class="sxs-lookup"><span data-stu-id="003d2-189">In this case, CAPICOM reads all certificates from all available readers that contain a smart card.</span></span>

## <a name="requirements"></a><span data-ttu-id="003d2-190">規格需求</span><span class="sxs-lookup"><span data-stu-id="003d2-190">Requirements</span></span>



| <span data-ttu-id="003d2-191">需求</span><span class="sxs-lookup"><span data-stu-id="003d2-191">Requirement</span></span> | <span data-ttu-id="003d2-192">值</span><span class="sxs-lookup"><span data-stu-id="003d2-192">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="003d2-193">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="003d2-193">Redistributable</span></span><br/> | <span data-ttu-id="003d2-194">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="003d2-194">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="003d2-195">DLL</span><span class="sxs-lookup"><span data-stu-id="003d2-195">DLL</span></span><br/>             | <dl> <span data-ttu-id="003d2-196"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="003d2-196"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="003d2-197">另請參閱</span><span class="sxs-lookup"><span data-stu-id="003d2-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="003d2-198">**市集**</span><span class="sxs-lookup"><span data-stu-id="003d2-198">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="003d2-199">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="003d2-199">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="003d2-200">**關閉**</span><span class="sxs-lookup"><span data-stu-id="003d2-200">**Close**</span></span>](store-close.md)
</dt> </dl>

 

 
