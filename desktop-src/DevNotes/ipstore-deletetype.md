---
description: 從受保護的儲存資料庫中刪除指定的類型。
ms.assetid: 5e3a08eb-e16b-4d9f-82be-241eb3137d17
title: 'IPStore：:D eleteType 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.DeleteType
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 7833dd59a10b0194347e906d5c5a4711585dea14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994163"
---
# <a name="ipstoredeletetype-method"></a><span data-ttu-id="737e3-103">IPStore：:D eleteType 方法</span><span class="sxs-lookup"><span data-stu-id="737e3-103">IPStore::DeleteType method</span></span>

<span data-ttu-id="737e3-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="737e3-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="737e3-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="737e3-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="737e3-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="737e3-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="737e3-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="737e3-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="737e3-108">從受保護的儲存資料庫中刪除指定的類型。</span><span class="sxs-lookup"><span data-stu-id="737e3-108">Deletes a specified type from the protected storage database.</span></span>

## <a name="syntax"></a><span data-ttu-id="737e3-109">語法</span><span class="sxs-lookup"><span data-stu-id="737e3-109">Syntax</span></span>


```C++
HRESULT DeleteType(
  [in]       PST_KEY Key,
  [in] const GUID    *pType,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="737e3-110">參數</span><span class="sxs-lookup"><span data-stu-id="737e3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="737e3-111">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="737e3-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="737e3-112">指定類型是否為本機電腦，或僅與建立的使用者相關聯。</span><span class="sxs-lookup"><span data-stu-id="737e3-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="737e3-113">值</span><span class="sxs-lookup"><span data-stu-id="737e3-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="737e3-114">意義</span><span class="sxs-lookup"><span data-stu-id="737e3-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="737e3-115"><dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="737e3-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="737e3-116">存放區會保留在登錄的 [目前使用者] 區段中。</span><span class="sxs-lookup"><span data-stu-id="737e3-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="737e3-117"><dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="737e3-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="737e3-118">存放區會保留在登錄的 [本機電腦] 區段中。</span><span class="sxs-lookup"><span data-stu-id="737e3-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="737e3-119">*pType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="737e3-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="737e3-120">識別儲存體資料類型之 **GUID** 的指標。</span><span class="sxs-lookup"><span data-stu-id="737e3-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="737e3-121">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="737e3-121">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="737e3-122">Reserved：必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="737e3-122">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="737e3-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="737e3-123">Return value</span></span>

<span data-ttu-id="737e3-124">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="737e3-124">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="737e3-125">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="737e3-125">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="737e3-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="737e3-126">Requirements</span></span>



| <span data-ttu-id="737e3-127">需求</span><span class="sxs-lookup"><span data-stu-id="737e3-127">Requirement</span></span> | <span data-ttu-id="737e3-128">值</span><span class="sxs-lookup"><span data-stu-id="737e3-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="737e3-129">標頭</span><span class="sxs-lookup"><span data-stu-id="737e3-129">Header</span></span><br/> | <dl> <span data-ttu-id="737e3-130"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="737e3-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="737e3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="737e3-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="737e3-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="737e3-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="737e3-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="737e3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="737e3-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="737e3-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
