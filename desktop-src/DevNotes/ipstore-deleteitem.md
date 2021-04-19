---
description: 從受保護的儲存體中刪除指定的專案。
ms.assetid: 1d071245-a563-4fba-9300-c47ca9a9d625
title: 'IPStore：:D eleteItem 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 3a882b9178160e8e82222943501c3317f8f11536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984379"
---
# <a name="ipstoredeleteitem-method"></a><span data-ttu-id="627a5-103">IPStore：:D eleteItem 方法</span><span class="sxs-lookup"><span data-stu-id="627a5-103">IPStore::DeleteItem method</span></span>

<span data-ttu-id="627a5-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="627a5-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="627a5-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="627a5-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="627a5-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="627a5-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="627a5-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="627a5-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="627a5-108">從受保護的儲存體中刪除指定的專案。</span><span class="sxs-lookup"><span data-stu-id="627a5-108">Deletes the specified item from the protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="627a5-109">語法</span><span class="sxs-lookup"><span data-stu-id="627a5-109">Syntax</span></span>


```C++
HRESULT DeleteItem(
  [in]       PST_KEY         Key,
  [in] const GUID            *pItemType,
  [in] const GUID            *pItemSubType,
  [in]       LPCWSTR         szItemName,
  [in]       PPST_PROMPTINFO pPromptInfo,
  [in]       DWORD           dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="627a5-110">參數</span><span class="sxs-lookup"><span data-stu-id="627a5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="627a5-111">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="627a5-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627a5-112">提供者存放區。</span><span class="sxs-lookup"><span data-stu-id="627a5-112">The provider storage area.</span></span>



| <span data-ttu-id="627a5-113">值</span><span class="sxs-lookup"><span data-stu-id="627a5-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="627a5-114">意義</span><span class="sxs-lookup"><span data-stu-id="627a5-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="627a5-115"><dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="627a5-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="627a5-116">存放區會保留在登錄的 [目前使用者] 區段中。</span><span class="sxs-lookup"><span data-stu-id="627a5-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="627a5-117"><dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="627a5-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="627a5-118">存放區會保留在登錄的 [本機電腦] 區段中。</span><span class="sxs-lookup"><span data-stu-id="627a5-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="627a5-119">*pItemType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="627a5-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627a5-120">**GUID** 的指標，識別要刪除之專案的資料類型。</span><span class="sxs-lookup"><span data-stu-id="627a5-120">A pointer to a **GUID** that identifies the data type of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="627a5-121">*pItemSubType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="627a5-121">*pItemSubType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627a5-122">**GUID** ，表示要刪除的專案子類型。</span><span class="sxs-lookup"><span data-stu-id="627a5-122">A **GUID** that indicates the item subtype to delete.</span></span>

</dd> <dt>

<span data-ttu-id="627a5-123">*szItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="627a5-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627a5-124">字串，其中包含要刪除之專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="627a5-124">A string that contains the name of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="627a5-125">*pPromptInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="627a5-125">*pPromptInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627a5-126">[**PST \_ PROMPTINFO**](pst-promptinfo.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="627a5-126">A pointer to a [**PST\_PROMPTINFO**](pst-promptinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="627a5-127">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="627a5-127">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627a5-128">指定刪除操作的使用者介面和安全性行為。</span><span class="sxs-lookup"><span data-stu-id="627a5-128">Specifies user interface and security behaviors for the delete operation.</span></span>



| <span data-ttu-id="627a5-129">值</span><span class="sxs-lookup"><span data-stu-id="627a5-129">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="627a5-130">意義</span><span class="sxs-lookup"><span data-stu-id="627a5-130">Meaning</span></span>                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="PST_NO_UI_MIGRATION"></span><span id="pst_no_ui_migration"></span><dl> <span data-ttu-id="627a5-131"><dt>**PST \_沒有任何 \_ UI \_ 遷移**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="627a5-131"><dt>**PST\_NO\_UI\_MIGRATION**</dt> <dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="627a5-132">除非需要自訂密碼，否則不顯示使用者介面。</span><span class="sxs-lookup"><span data-stu-id="627a5-132">Do not show user interface unless a custom password is required.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="627a5-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="627a5-133">Return value</span></span>

<span data-ttu-id="627a5-134">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="627a5-134">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="627a5-135">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="627a5-135">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="627a5-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="627a5-136">Requirements</span></span>



| <span data-ttu-id="627a5-137">需求</span><span class="sxs-lookup"><span data-stu-id="627a5-137">Requirement</span></span> | <span data-ttu-id="627a5-138">值</span><span class="sxs-lookup"><span data-stu-id="627a5-138">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="627a5-139">標頭</span><span class="sxs-lookup"><span data-stu-id="627a5-139">Header</span></span><br/> | <dl> <span data-ttu-id="627a5-140"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="627a5-140"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="627a5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="627a5-141">DLL</span></span><br/>    | <dl> <span data-ttu-id="627a5-142"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="627a5-142"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="627a5-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="627a5-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="627a5-144">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="627a5-144">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="627a5-145">**PST \_ PROMPTINFO**</span><span class="sxs-lookup"><span data-stu-id="627a5-145">**PST\_PROMPTINFO**</span></span>](pst-promptinfo.md)
</dt> </dl>

 

 
