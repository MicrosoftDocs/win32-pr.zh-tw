---
description: 將資料項目寫入受保護的儲存體。
ms.assetid: d940470c-b881-4e05-8e52-f804eac11e45
title: 'IPStore：： WriteItem 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.WriteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: b11436ca5a884b7d45c853433c3203b219e0527c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990957"
---
# <a name="ipstorewriteitem-method"></a><span data-ttu-id="47f5e-103">IPStore：： WriteItem 方法</span><span class="sxs-lookup"><span data-stu-id="47f5e-103">IPStore::WriteItem method</span></span>

<span data-ttu-id="47f5e-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="47f5e-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="47f5e-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="47f5e-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="47f5e-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="47f5e-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="47f5e-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="47f5e-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="47f5e-108">將資料項目寫入受保護的儲存體。</span><span class="sxs-lookup"><span data-stu-id="47f5e-108">Writes a data item to protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="47f5e-109">語法</span><span class="sxs-lookup"><span data-stu-id="47f5e-109">Syntax</span></span>


```C++
HRESULT WriteItem(
  [in]        PST_KEY        Key,
  [in]  const GUID           *pItemType,
  [in]  const GUID           *pItemSubtype,
  [in]        LPCWSTR        *szItemName,
  [out]       DWORD          *cbData,
  [out]       BYTE           ppbData,
  [in]        PPST_PROMPTIFO pProomptInfo,
  [in]        DWORD          dwDefaultConfirmationStyle,
  [in]        DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="47f5e-110">參數</span><span class="sxs-lookup"><span data-stu-id="47f5e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47f5e-111">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47f5e-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f5e-112">提供者存放區。</span><span class="sxs-lookup"><span data-stu-id="47f5e-112">The provider storage area.</span></span>



| <span data-ttu-id="47f5e-113">值</span><span class="sxs-lookup"><span data-stu-id="47f5e-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="47f5e-114">意義</span><span class="sxs-lookup"><span data-stu-id="47f5e-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="47f5e-115"><dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="47f5e-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="47f5e-116">存放區會保留在登錄的 [目前使用者] 區段中。</span><span class="sxs-lookup"><span data-stu-id="47f5e-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="47f5e-117"><dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="47f5e-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="47f5e-118">存放區會保留在登錄的 [本機電腦] 區段中。</span><span class="sxs-lookup"><span data-stu-id="47f5e-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="47f5e-119">*pItemType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47f5e-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f5e-120">**GUID** 的指標，識別所寫入之資料項目的資料類型。</span><span class="sxs-lookup"><span data-stu-id="47f5e-120">A pointer to a **GUID** that identifies the data type of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="47f5e-121">*pItemSubtype* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47f5e-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f5e-122">**GUID** 的指標，識別所寫入之資料項目的資料子類型。</span><span class="sxs-lookup"><span data-stu-id="47f5e-122">A pointer to a **GUID** that identifies the data subtype of the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="47f5e-123">*szItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47f5e-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f5e-124">字串的指標，其中包含指派給預存資料項目的名稱。</span><span class="sxs-lookup"><span data-stu-id="47f5e-124">A pointer to a string that contains the name assigned to the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="47f5e-125">*cbData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="47f5e-125">*cbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47f5e-126">**DWORD** 的指標，指出包含儲存資料項目的緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="47f5e-126">A pointer to a **DWORD** that indicates the size of the buffer that contains the stored data item.</span></span>

</dd> <dt>

<span data-ttu-id="47f5e-127">*ppbData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="47f5e-127">*ppbData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47f5e-128">包含正在寫入之資料項目的緩衝區指標。</span><span class="sxs-lookup"><span data-stu-id="47f5e-128">A pointer to a buffer that contains the data item being written.</span></span>

</dd> <dt>

<span data-ttu-id="47f5e-129">*pProomptInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47f5e-129">*pProomptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f5e-130">[**PST \_ PROMPTINFO**](pst-promptinfo.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="47f5e-130">Pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="47f5e-131">*dwDefaultConfirmationStyle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47f5e-131">*dwDefaultConfirmationStyle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f5e-132">預設確認樣式。</span><span class="sxs-lookup"><span data-stu-id="47f5e-132">The default confirmation style.</span></span>



| <span data-ttu-id="47f5e-133">值</span><span class="sxs-lookup"><span data-stu-id="47f5e-133">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="47f5e-134">意義</span><span class="sxs-lookup"><span data-stu-id="47f5e-134">Meaning</span></span>                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="PST_CF_DEFAULT"></span><span id="pst_cf_default"></span><dl> <span data-ttu-id="47f5e-135"><dt>**PST \_CF \_ 預設**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="47f5e-135"><dt>**PST\_CF\_DEFAULT**</dt> <dt>0x00000000</dt></span></span> </dl> | <span data-ttu-id="47f5e-136">允許使用者選擇確認樣式。</span><span class="sxs-lookup"><span data-stu-id="47f5e-136">Allows the user to choose the confirmation style.</span></span> <br/> |
| <span id="PST_CF_NONE"></span><span id="pst_cf_none"></span><dl> <span data-ttu-id="47f5e-137"><dt>**PST \_CF \_ 無**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="47f5e-137"><dt>**PST\_CF\_NONE**</dt> <dt>0x00000001</dt></span></span> </dl>          | <span data-ttu-id="47f5e-138">強制建立無訊息專案。</span><span class="sxs-lookup"><span data-stu-id="47f5e-138">Forces silent item creation.</span></span> <br/>                      |



 

</dd> <dt>

<span data-ttu-id="47f5e-139">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47f5e-139">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47f5e-140">寫入操作的使用者介面和安全性行為。</span><span class="sxs-lookup"><span data-stu-id="47f5e-140">The user interface and security behaviors for the write operation.</span></span>



| <span data-ttu-id="47f5e-141">值</span><span class="sxs-lookup"><span data-stu-id="47f5e-141">Value</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="47f5e-142">意義</span><span class="sxs-lookup"><span data-stu-id="47f5e-142">Meaning</span></span>                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="PST_NO_OVERWRITE"></span><span id="pst_no_overwrite"></span><dl> <span data-ttu-id="47f5e-143"><dt>**PST \_無 \_ 覆寫**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="47f5e-143"><dt>**PST\_NO\_OVERWRITE**</dt> <dt>0x00000002</dt></span></span> </dl>                            | <span data-ttu-id="47f5e-144">指定要在受保護的儲存體中建立專案。</span><span class="sxs-lookup"><span data-stu-id="47f5e-144">Specifies that the item be created in protected storage.</span></span> <span data-ttu-id="47f5e-145">不允許覆寫現有的專案。</span><span class="sxs-lookup"><span data-stu-id="47f5e-145">Overwriting of an existing item is disallowed.</span></span><br/> |
| <span id="PST_UNRESTRICTED_ITEMDATA"></span><span id="pst_unrestricted_itemdata"></span><dl> <span data-ttu-id="47f5e-146"><dt>**PST \_不受限制的 \_ ITEMDATA**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="47f5e-146"><dt>**PST\_UNRESTRICTED\_ITEMDATA**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="47f5e-147">指定資料流程並非安全的。</span><span class="sxs-lookup"><span data-stu-id="47f5e-147">Specifies that the data stream is nonsecure.</span></span> <span data-ttu-id="47f5e-148">依預設，專案呼叫是安全的。</span><span class="sxs-lookup"><span data-stu-id="47f5e-148">By default, item calls are secure.</span></span><br/>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47f5e-149">傳回值</span><span class="sxs-lookup"><span data-stu-id="47f5e-149">Return value</span></span>

<span data-ttu-id="47f5e-150">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="47f5e-150">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="47f5e-151">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="47f5e-151">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="47f5e-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="47f5e-152">Requirements</span></span>



| <span data-ttu-id="47f5e-153">需求</span><span class="sxs-lookup"><span data-stu-id="47f5e-153">Requirement</span></span> | <span data-ttu-id="47f5e-154">值</span><span class="sxs-lookup"><span data-stu-id="47f5e-154">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47f5e-155">標頭</span><span class="sxs-lookup"><span data-stu-id="47f5e-155">Header</span></span><br/> | <dl> <span data-ttu-id="47f5e-156"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="47f5e-156"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="47f5e-157">DLL</span><span class="sxs-lookup"><span data-stu-id="47f5e-157">DLL</span></span><br/>    | <dl> <span data-ttu-id="47f5e-158"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47f5e-158"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47f5e-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47f5e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47f5e-160">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="47f5e-160">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="47f5e-161">**PST \_ PROMPTINFO**</span><span class="sxs-lookup"><span data-stu-id="47f5e-161">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
