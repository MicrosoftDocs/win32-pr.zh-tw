---
description: 在指定的型別內建立指定的子類型。
ms.assetid: afd5c0c6-5779-4a78-83aa-cae36f5de564
title: 'IPStore：： CreateSubtype 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CreateSubtype
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e7f304b2d54bb1ae09673e77f37f95257fa6fd10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977425"
---
# <a name="ipstorecreatesubtype-method"></a><span data-ttu-id="5af9d-103">IPStore：： CreateSubtype 方法</span><span class="sxs-lookup"><span data-stu-id="5af9d-103">IPStore::CreateSubtype method</span></span>

<span data-ttu-id="5af9d-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="5af9d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="5af9d-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="5af9d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="5af9d-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="5af9d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="5af9d-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="5af9d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="5af9d-108">在指定的型別內建立指定的子類型。</span><span class="sxs-lookup"><span data-stu-id="5af9d-108">Creates the specified subtype within the specified type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5af9d-109">語法</span><span class="sxs-lookup"><span data-stu-id="5af9d-109">Syntax</span></span>


```C++
HRESULT CreateSubtype(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET pRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5af9d-110">參數</span><span class="sxs-lookup"><span data-stu-id="5af9d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af9d-111">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5af9d-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5af9d-112">指定提供者存放區。</span><span class="sxs-lookup"><span data-stu-id="5af9d-112">Specifies the provider storage area.</span></span>



| <span data-ttu-id="5af9d-113">值</span><span class="sxs-lookup"><span data-stu-id="5af9d-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="5af9d-114">意義</span><span class="sxs-lookup"><span data-stu-id="5af9d-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="5af9d-115"><dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="5af9d-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="5af9d-116">存放區會保留在登錄的 [目前使用者] 區段中。</span><span class="sxs-lookup"><span data-stu-id="5af9d-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="5af9d-117"><dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="5af9d-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="5af9d-118">存放區會保留在登錄的 [本機電腦] 區段中。</span><span class="sxs-lookup"><span data-stu-id="5af9d-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5af9d-119">*pType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5af9d-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5af9d-120">識別儲存體資料類型之 **GUID** 的指標。</span><span class="sxs-lookup"><span data-stu-id="5af9d-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="5af9d-121">*pSubtype* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5af9d-121">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5af9d-122">**GUID** 的指標，可識別儲存體的資料子類型。</span><span class="sxs-lookup"><span data-stu-id="5af9d-122">A pointer to a **GUID** that identifies the data subtype of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="5af9d-123">*pInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5af9d-123">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5af9d-124">[**PST \_ TYPEINFO**](pst-typeinfo.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5af9d-124">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5af9d-125">*pRules* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5af9d-125">*pRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5af9d-126">[**PST \_ ACCESSRULESET**](pst-accessruleset.md)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5af9d-126">A pointer to a [**PST\_ACCESSRULESET**](pst-accessruleset.md) structure.</span></span>

<span data-ttu-id="5af9d-127">**WINDOWS XP：** 此參數會被忽略。</span><span class="sxs-lookup"><span data-stu-id="5af9d-127">**Windows XP:** This parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5af9d-128">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5af9d-128">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5af9d-129">保護必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="5af9d-129">Reserved; must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5af9d-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="5af9d-130">Return value</span></span>

<span data-ttu-id="5af9d-131">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="5af9d-131">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="5af9d-132">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="5af9d-132">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="5af9d-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="5af9d-133">Requirements</span></span>



| <span data-ttu-id="5af9d-134">需求</span><span class="sxs-lookup"><span data-stu-id="5af9d-134">Requirement</span></span> | <span data-ttu-id="5af9d-135">值</span><span class="sxs-lookup"><span data-stu-id="5af9d-135">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5af9d-136">標頭</span><span class="sxs-lookup"><span data-stu-id="5af9d-136">Header</span></span><br/> | <dl> <span data-ttu-id="5af9d-137"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="5af9d-137"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="5af9d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="5af9d-138">DLL</span></span><br/>    | <dl> <span data-ttu-id="5af9d-139"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5af9d-139"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5af9d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5af9d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af9d-141">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="5af9d-141">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="5af9d-142">**PST \_ ACCESSRULESET**</span><span class="sxs-lookup"><span data-stu-id="5af9d-142">**PST\_ACCESSRULESET**</span></span>](pst-accessruleset.md)
</dt> <dt>

[<span data-ttu-id="5af9d-143">**PST \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="5af9d-143">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
