---
description: 從受保護的儲存體讀取指定的資料項目。
ms.assetid: e565a0ea-5d8e-4706-a176-2305a95f0d67
title: 'IPStore：： ReadItem 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 0464ef06bc7c2842d0c8f9ff76e8174f05338919
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990774"
---
# <a name="ipstorereaditem-method"></a><span data-ttu-id="66e5d-103">IPStore：： ReadItem 方法</span><span class="sxs-lookup"><span data-stu-id="66e5d-103">IPStore::ReadItem method</span></span>

<span data-ttu-id="66e5d-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="66e5d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="66e5d-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="66e5d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="66e5d-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="66e5d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="66e5d-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="66e5d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="66e5d-108">從受保護的儲存體讀取指定的資料項目。</span><span class="sxs-lookup"><span data-stu-id="66e5d-108">Reads the specified data item from protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="66e5d-109">語法</span><span class="sxs-lookup"><span data-stu-id="66e5d-109">Syntax</span></span>


```C++
HRESULT ReadItem(
  [in]       PST_KEY        Key,
  [in] const PSGUID         *pItemType,
  [in] const GUID           *pItemSubtype,
  [in]       LPCWSTR        *szItemName,
  [in]       DWORD          cbData,
  [in]       BYTE_RPC_FAR   *pbData,
  [in]       PPST_PROMPTIFO pPromptInfo,
  [in]       DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="66e5d-110">參數</span><span class="sxs-lookup"><span data-stu-id="66e5d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66e5d-111">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e5d-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e5d-112">提供者存放區。</span><span class="sxs-lookup"><span data-stu-id="66e5d-112">The provider storage area.</span></span>



| <span data-ttu-id="66e5d-113">值</span><span class="sxs-lookup"><span data-stu-id="66e5d-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="66e5d-114">意義</span><span class="sxs-lookup"><span data-stu-id="66e5d-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="66e5d-115"><dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="66e5d-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="66e5d-116">存放區會保留在登錄的 [目前使用者] 區段中。</span><span class="sxs-lookup"><span data-stu-id="66e5d-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="66e5d-117"><dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="66e5d-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="66e5d-118">存放區會保留在登錄的 [本機電腦] 區段中。</span><span class="sxs-lookup"><span data-stu-id="66e5d-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="66e5d-119">*pItemType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e5d-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e5d-120">GUID 的指標，識別要讀取之專案的資料類型。</span><span class="sxs-lookup"><span data-stu-id="66e5d-120">A pointer to a GUID that identifies the data type of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="66e5d-121">*pItemSubtype* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e5d-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e5d-122">GUID 的指標，識別要讀取之專案的資料子類型。</span><span class="sxs-lookup"><span data-stu-id="66e5d-122">A pointer to a GUID that identifies the data subtype of the item to read.</span></span>

</dd> <dt>

<span data-ttu-id="66e5d-123">*szItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e5d-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e5d-124">字串的指標，其中包含指派給預存資料項目的名稱。</span><span class="sxs-lookup"><span data-stu-id="66e5d-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="66e5d-125">*cbData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e5d-125">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e5d-126">**DWORD** ，指出包含儲存資料項目的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="66e5d-126">A **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="66e5d-127">*>pbdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e5d-127">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e5d-128">包含儲存資料項目之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="66e5d-128">A pointer to a buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="66e5d-129">*pPromptInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e5d-129">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e5d-130">[**PST \_ PROMPTINFO**](pst-promptinfo.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="66e5d-130">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="66e5d-131">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66e5d-131">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66e5d-132">指定讀取操作的使用者介面和安全性行為。</span><span class="sxs-lookup"><span data-stu-id="66e5d-132">Specifies user interface and security behaviors for the read operation.</span></span>

<span data-ttu-id="66e5d-133">旗標值可以與邏輯 OR 合併。</span><span class="sxs-lookup"><span data-stu-id="66e5d-133">The flag values can be combined with a logical OR.</span></span>



| <span data-ttu-id="66e5d-134">值</span><span class="sxs-lookup"><span data-stu-id="66e5d-134">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="66e5d-135">意義</span><span class="sxs-lookup"><span data-stu-id="66e5d-135">Meaning</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="66e5d-136"><dt>**PST \_不受限制的 \_ ITEMDATA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="66e5d-136"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="66e5d-137">指定資料流程並非安全的。</span><span class="sxs-lookup"><span data-stu-id="66e5d-137">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="66e5d-138">依預設，專案呼叫是安全的。</span><span class="sxs-lookup"><span data-stu-id="66e5d-138">By default, item calls are secure.</span></span><br/>                                                                                                                                             |
| <span id="PST_PROMPT_QUERY"></span><span id="pst_prompt_query"></span><dl> <span data-ttu-id="66e5d-139"><dt>**PST \_提示 \_ 查詢**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="66e5d-139"><dt>**PST\_PROMPT\_QUERY**</dt> <dt>0x00000008</dt></span></span> </dl>                            | <span data-ttu-id="66e5d-140">指定在成功時傳回確認。</span><span class="sxs-lookup"><span data-stu-id="66e5d-140">Specifies that the confirmation be returned upon success.</span></span> <span data-ttu-id="66e5d-141">如果已啟用使用者介面，則會傳回 **PST \_ E \_ OK** 的成功。</span><span class="sxs-lookup"><span data-stu-id="66e5d-141">If the user interface is enabled, a success of **PST\_E\_OK** is returned.</span></span> <span data-ttu-id="66e5d-142">如果未啟用使用者介面，則會傳回有 **PST \_ E \_ 專案 \_** 的值。</span><span class="sxs-lookup"><span data-stu-id="66e5d-142">If the user interface is not enabled, a value of **PST\_E\_ITEM\_EXISTS** is returned.</span></span><br/> |
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="66e5d-143"><dt>**PST \_沒有任何 \_ UI \_ 遷移**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="66e5d-143"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl>                  | <span data-ttu-id="66e5d-144">除非需要自訂密碼，否則不顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="66e5d-144">Do not show user interface unless a custom password is required.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66e5d-145">傳回值</span><span class="sxs-lookup"><span data-stu-id="66e5d-145">Return value</span></span>

<span data-ttu-id="66e5d-146">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="66e5d-146">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="66e5d-147">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="66e5d-147">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="66e5d-148">備註</span><span class="sxs-lookup"><span data-stu-id="66e5d-148">Remarks</span></span>

<span data-ttu-id="66e5d-149">如果 **ReadItem** 順利完成，應用程式會負責使用 [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) 函數釋放傳回的資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="66e5d-149">If **ReadItem** completes successfully, the application is responsible for freeing the returned data buffer using the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="66e5d-150">規格需求</span><span class="sxs-lookup"><span data-stu-id="66e5d-150">Requirements</span></span>



| <span data-ttu-id="66e5d-151">需求</span><span class="sxs-lookup"><span data-stu-id="66e5d-151">Requirement</span></span> | <span data-ttu-id="66e5d-152">值</span><span class="sxs-lookup"><span data-stu-id="66e5d-152">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66e5d-153">標頭</span><span class="sxs-lookup"><span data-stu-id="66e5d-153">Header</span></span><br/> | <dl> <span data-ttu-id="66e5d-154"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="66e5d-154"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="66e5d-155">DLL</span><span class="sxs-lookup"><span data-stu-id="66e5d-155">DLL</span></span><br/>    | <dl> <span data-ttu-id="66e5d-156"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66e5d-156"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e5d-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66e5d-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e5d-158">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="66e5d-158">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="66e5d-159">**PST \_ PROMPTINFO**</span><span class="sxs-lookup"><span data-stu-id="66e5d-159">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
