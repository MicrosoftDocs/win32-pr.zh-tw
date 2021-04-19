---
description: 在離線登錄 hive 中建立指定的登錄機碼。 如果索引鍵已經存在，則函式會將它開啟。
ms.assetid: 40e7468d-e781-4945-9023-580c06088b87
title: 'ORCreateKey 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 9a14198cb6f1912612a092e003a68fd9ff49f867
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991339"
---
# <a name="orcreatekey-function"></a><span data-ttu-id="a48bd-104">ORCreateKey 函式</span><span class="sxs-lookup"><span data-stu-id="a48bd-104">ORCreateKey function</span></span>

<span data-ttu-id="a48bd-105">在離線登錄 hive 中建立指定的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="a48bd-105">Creates the specified registry key in an offline registry hive.</span></span> <span data-ttu-id="a48bd-106">如果索引鍵已經存在，則函式會將它開啟。</span><span class="sxs-lookup"><span data-stu-id="a48bd-106">If the key already exists, the function opens it.</span></span>

## <a name="syntax"></a><span data-ttu-id="a48bd-107">語法</span><span class="sxs-lookup"><span data-stu-id="a48bd-107">Syntax</span></span>


```C++
DWORD ORCreateKey(
  _In_      ORHKEY               Handle,
  _In_      PCWSTR               lpSubKey,
  _In_opt_  PWSTR                lpClass,
  _In_opt_  DWORD                dwOptions,
  _In_opt_  PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Out_     PORHKEY              phkResult,
  _Out_opt_ PDWORD               pdwDisposition
);
```



## <a name="parameters"></a><span data-ttu-id="a48bd-108">參數</span><span class="sxs-lookup"><span data-stu-id="a48bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a48bd-109">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a48bd-109">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a48bd-110">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a48bd-110">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="a48bd-111">*lpSubKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a48bd-111">*lpSubKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a48bd-112">包含此函式開啟或建立之子機碼名稱的 Unicode 字串指標。</span><span class="sxs-lookup"><span data-stu-id="a48bd-112">A pointer to a Unicode string that contains the name of a subkey that this function opens or creates.</span></span> <span data-ttu-id="a48bd-113">*LpSubKey* 參數必須指定 *Handle* 參數所識別之機碼的子機碼;在登錄樹狀目錄中，最多可以有32層級的深度。</span><span class="sxs-lookup"><span data-stu-id="a48bd-113">The *lpSubKey* parameter must specify a subkey of the key identified by the *Handle* parameter; it can be up to 32 levels deep in the registry tree.</span></span> <span data-ttu-id="a48bd-114">如需索引鍵名稱的詳細資訊，請參閱登錄 [結構](../sysinfo/structure-of-the-registry.md)。</span><span class="sxs-lookup"><span data-stu-id="a48bd-114">For more information about key names, see [Structure of the Registry](../sysinfo/structure-of-the-registry.md).</span></span>

<span data-ttu-id="a48bd-115">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a48bd-115">This parameter cannot be **NULL**.</span></span>

<span data-ttu-id="a48bd-116">索引鍵名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="a48bd-116">Key names are not case sensitive.</span></span>

</dd> <dt>

<span data-ttu-id="a48bd-117">*lpClass* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a48bd-117">*lpClass* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a48bd-118">類別 (此索引鍵) 物件類型。</span><span class="sxs-lookup"><span data-stu-id="a48bd-118">The class (object type) of this key.</span></span> <span data-ttu-id="a48bd-119">您可以忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="a48bd-119">This parameter may be ignored.</span></span> <span data-ttu-id="a48bd-120">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a48bd-120">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a48bd-121">*>dwoptions* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a48bd-121">*dwOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a48bd-122">此參數可以是0或下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a48bd-122">This parameter can be 0 or one of the following values.</span></span>



| <span data-ttu-id="a48bd-123">值</span><span class="sxs-lookup"><span data-stu-id="a48bd-123">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="a48bd-124">意義</span><span class="sxs-lookup"><span data-stu-id="a48bd-124">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="REG_OPTION_CREATE_LINK"></span><span id="reg_option_create_link"></span><dl> <span data-ttu-id="a48bd-125"><dt>**REG \_選項 \_ 建立 \_ 連結**</dt> <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="a48bd-125"><dt>**REG\_OPTION\_CREATE\_LINK**</dt> <dt>0x00000002L</dt></span></span> </dl>    | <span data-ttu-id="a48bd-126">索引鍵是符號連結。</span><span class="sxs-lookup"><span data-stu-id="a48bd-126">The key is a symbolic link.</span></span> <span data-ttu-id="a48bd-127">目標路徑會指派給機碼的 L "SymbolicLinkValue" 值。</span><span class="sxs-lookup"><span data-stu-id="a48bd-127">The target path is assigned to the L"SymbolicLinkValue" value of the key.</span></span> <span data-ttu-id="a48bd-128">目標路徑必須是絕對登錄路徑。</span><span class="sxs-lookup"><span data-stu-id="a48bd-128">The target path must be an absolute registry path.</span></span> <span data-ttu-id="a48bd-129">如果設定此選項，則也必須設定 **REG \_ 選項 \_ 非 \_ VOLATILE** 。</span><span class="sxs-lookup"><span data-stu-id="a48bd-129">If this option is set, **REG\_OPTION\_NON\_VOLATILE** must also be set.</span></span> <br/> <span data-ttu-id="a48bd-130">如果 *lpSubKey* 參數指定現有的金鑰，就必須使用 **REG \_ OPTION \_ CREATE \_ LINK** 來建立它。</span><span class="sxs-lookup"><span data-stu-id="a48bd-130">If the *lpSubKey* parameter specifies an existing key, it must have been created with **REG\_OPTION\_CREATE\_LINK**.</span></span><br/> <span data-ttu-id="a48bd-131">只有在應用程式相容性絕對必要時，才應該使用登錄符號連結。</span><span class="sxs-lookup"><span data-stu-id="a48bd-131">Registry symbolic links should be used only when absolutely necessary for application compatibility.</span></span> <br/> |
| <span id="REG_OPTION_NON_VOLATILE"></span><span id="reg_option_non_volatile"></span><dl> <span data-ttu-id="a48bd-132"><dt>**REG \_選項 \_ 非 \_ VOLATILE**</dt> <dt>0x00000000L</dt></span><span class="sxs-lookup"><span data-stu-id="a48bd-132"><dt>**REG\_OPTION\_NON\_VOLATILE**</dt> <dt>0x00000000L</dt></span></span> </dl> | <span data-ttu-id="a48bd-133">金鑰不是 volatile;這是預設值。</span><span class="sxs-lookup"><span data-stu-id="a48bd-133">The key is not volatile; this is the default.</span></span> <span data-ttu-id="a48bd-134">這項資訊會儲存在檔案中，並在系統重新開機時予以保留。</span><span class="sxs-lookup"><span data-stu-id="a48bd-134">The information is stored in a file and is preserved when the system is restarted.</span></span> <span data-ttu-id="a48bd-135">[**ORSaveHive**](orsavehive.md)函式會儲存非 volatile 的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="a48bd-135">The [**ORSaveHive**](orsavehive.md) function saves keys that are not volatile.</span></span><br/>                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

<span data-ttu-id="a48bd-136">*pSecurityDescriptor* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a48bd-136">*pSecurityDescriptor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a48bd-137">[安全 \_ 描述項](/windows/win32/api/winnt/ns-winnt-security_descriptor)結構的指標，其中包含新金鑰的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="a48bd-137">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that contains a security descriptor for the new key.</span></span> <span data-ttu-id="a48bd-138">如果 *pSecurityDescriptor* 為 **Null**，則索引鍵會取得預設安全描述項。</span><span class="sxs-lookup"><span data-stu-id="a48bd-138">If *pSecurityDescriptor* is **NULL**, the key gets a default security descriptor.</span></span> <span data-ttu-id="a48bd-139">金鑰之預設安全描述項中的 Acl 會從其直接父機碼繼承。</span><span class="sxs-lookup"><span data-stu-id="a48bd-139">The ACLs in a default security descriptor for a key are inherited from its direct parent key.</span></span>

</dd> <dt>

<span data-ttu-id="a48bd-140">*phkResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a48bd-140">*phkResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a48bd-141">變數的指標，此變數會接收開啟或建立之索引鍵的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a48bd-141">A pointer to a variable that receives a handle to the opened or created key.</span></span> <span data-ttu-id="a48bd-142">當您完成使用控制碼之後，請使用 [**ORCloseKey**](orclosekey.md) 函數來關閉金鑰。</span><span class="sxs-lookup"><span data-stu-id="a48bd-142">Use the [**ORCloseKey**](orclosekey.md) function to close the key after you have finished using the handle.</span></span>

</dd> <dt>

<span data-ttu-id="a48bd-143">*pdwDisposition* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="a48bd-143">*pdwDisposition* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a48bd-144">變數的指標，此變數會接收下列其中一個配置值。</span><span class="sxs-lookup"><span data-stu-id="a48bd-144">A pointer to a variable that receives one of the following disposition values.</span></span>



| <span data-ttu-id="a48bd-145">值</span><span class="sxs-lookup"><span data-stu-id="a48bd-145">Value</span></span>                                                                                                                                                                                                                                                          | <span data-ttu-id="a48bd-146">意義</span><span class="sxs-lookup"><span data-stu-id="a48bd-146">Meaning</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="REG_CREATED_NEW_KEY"></span><span id="reg_created_new_key"></span><dl> <span data-ttu-id="a48bd-147"><dt>**REG \_已建立 \_ 新的 \_ 金鑰**</dt> <dt>0x00000001L</dt></span><span class="sxs-lookup"><span data-stu-id="a48bd-147"><dt>**REG\_CREATED\_NEW\_KEY**</dt> <dt>0x00000001L</dt></span></span> </dl>             | <span data-ttu-id="a48bd-148">金鑰不存在且已建立。</span><span class="sxs-lookup"><span data-stu-id="a48bd-148">The key did not exist and was created.</span></span><br/>                       |
| <span id="REG_OPENED_EXISTING_KEY"></span><span id="reg_opened_existing_key"></span><dl> <span data-ttu-id="a48bd-149"><dt>**REG \_開啟 \_ 現有的 \_ 金鑰**</dt> <dt>0x00000002L</dt></span><span class="sxs-lookup"><span data-stu-id="a48bd-149"><dt>**REG\_OPENED\_EXISTING\_KEY**</dt> <dt>0x00000002L</dt></span></span> </dl> | <span data-ttu-id="a48bd-150">金鑰已存在，而且只會在未變更的情況下開啟。</span><span class="sxs-lookup"><span data-stu-id="a48bd-150">The key existed and was simply opened without being changed.</span></span><br/> |



 

<span data-ttu-id="a48bd-151">如果 *pdwDisposition* 為 **Null**，則不會傳回任何處置資訊。</span><span class="sxs-lookup"><span data-stu-id="a48bd-151">If *pdwDisposition* is **NULL**, no disposition information is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a48bd-152">傳回值</span><span class="sxs-lookup"><span data-stu-id="a48bd-152">Return value</span></span>

<span data-ttu-id="a48bd-153">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="a48bd-153">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="a48bd-154">如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a48bd-154">If the function fails, the return value is a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="a48bd-155">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="a48bd-155">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="a48bd-156">如果 *>dwoptions* 參數是以 **REG \_ 選項 \_ CREATE \_ LINK** 設定，但 **reg \_ 選項 \_ \_** 為 clear，或是要傳回的控制碼是 hive 的根目錄控制碼，則函式會傳回錯誤 \_ 不正確 \_ 參數。</span><span class="sxs-lookup"><span data-stu-id="a48bd-156">If the *dwOptions* parameter is set with **REG\_OPTION\_CREATE\_LINK** but **REG\_OPTION\_NON\_VOLATILE** is clear, or if the handle to be returned would be a handle to the root key of the hive, the function returns ERROR\_INVALID\_PARAMETER.</span></span>

## <a name="remarks"></a><span data-ttu-id="a48bd-157">備註</span><span class="sxs-lookup"><span data-stu-id="a48bd-157">Remarks</span></span>

<span data-ttu-id="a48bd-158">**ORCreateKey** 函數所建立的索引鍵沒有值。</span><span class="sxs-lookup"><span data-stu-id="a48bd-158">The key that the **ORCreateKey** function creates has no values.</span></span> <span data-ttu-id="a48bd-159">應用程式可以使用 [**ORSetValue**](orsetvalue.md) 函數來設定索引鍵值。</span><span class="sxs-lookup"><span data-stu-id="a48bd-159">An application can use the [**ORSetValue**](orsetvalue.md) function to set key values.</span></span>

<span data-ttu-id="a48bd-160">**ORCreateKey** 函式不能用來在離線登錄 hive 中建立根金鑰。</span><span class="sxs-lookup"><span data-stu-id="a48bd-160">The **ORCreateKey** function cannot be used to create the root key in an offline registry hive.</span></span> <span data-ttu-id="a48bd-161">您可以使用 [**ORCreateHive**](orcreatehive.md) 函式來建立根金鑰，並取得索引鍵的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a48bd-161">Use the [**ORCreateHive**](orcreatehive.md) function to create the root key and obtain a handle to the key.</span></span>

<span data-ttu-id="a48bd-162">離線登錄不支援儲存個別的金鑰。</span><span class="sxs-lookup"><span data-stu-id="a48bd-162">The offline registry does not support saving individual keys.</span></span> <span data-ttu-id="a48bd-163">使用 [**ORSaveHive**](orsavehive.md) 函式，將索引鍵和其子機碼儲存在 hive 中。</span><span class="sxs-lookup"><span data-stu-id="a48bd-163">Use the [**ORSaveHive**](orsavehive.md) function to save a key and its subkeys in a hive.</span></span>

## <a name="requirements"></a><span data-ttu-id="a48bd-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="a48bd-164">Requirements</span></span>



| <span data-ttu-id="a48bd-165">需求</span><span class="sxs-lookup"><span data-stu-id="a48bd-165">Requirement</span></span> | <span data-ttu-id="a48bd-166">值</span><span class="sxs-lookup"><span data-stu-id="a48bd-166">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a48bd-167">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a48bd-167">Redistributable</span></span><br/> | <span data-ttu-id="a48bd-168">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="a48bd-168">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="a48bd-169">標頭</span><span class="sxs-lookup"><span data-stu-id="a48bd-169">Header</span></span><br/>          | <dl> <span data-ttu-id="a48bd-170"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="a48bd-170"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="a48bd-171">DLL</span><span class="sxs-lookup"><span data-stu-id="a48bd-171">DLL</span></span><br/>             | <dl> <span data-ttu-id="a48bd-172"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a48bd-172"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a48bd-173">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a48bd-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a48bd-174">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="a48bd-174">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="a48bd-175">**ORCreateHive**</span><span class="sxs-lookup"><span data-stu-id="a48bd-175">**ORCreateHive**</span></span>](orcreatehive.md)
</dt> <dt>

[<span data-ttu-id="a48bd-176">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="a48bd-176">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="a48bd-177">**ORSaveHive**</span><span class="sxs-lookup"><span data-stu-id="a48bd-177">**ORSaveHive**</span></span>](orsavehive.md)
</dt> <dt>

[<span data-ttu-id="a48bd-178">安全 \_ 描述項</span><span class="sxs-lookup"><span data-stu-id="a48bd-178">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

 
