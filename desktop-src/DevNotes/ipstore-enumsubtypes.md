---
description: 傳回介面，以列舉受保護資料庫中目前註冊之類型的子類型。
ms.assetid: 07cc43ce-2191-4b20-b23d-d96d15aa8dea
title: 'IPStore：： EnumSubtypes 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumSubtypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f0e5aafbfdadebfa96254b3bd5997ec8d07cfb64
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990726"
---
# <a name="ipstoreenumsubtypes-method"></a><span data-ttu-id="74dee-103">IPStore：： EnumSubtypes 方法</span><span class="sxs-lookup"><span data-stu-id="74dee-103">IPStore::EnumSubtypes method</span></span>

<span data-ttu-id="74dee-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="74dee-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="74dee-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="74dee-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="74dee-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="74dee-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="74dee-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="74dee-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="74dee-108">傳回介面，以列舉受保護資料庫中目前註冊之類型的子類型。</span><span class="sxs-lookup"><span data-stu-id="74dee-108">Returns an interface for enumerating subtypes of the types currently registered in the protected database.</span></span>

## <a name="syntax"></a><span data-ttu-id="74dee-109">語法</span><span class="sxs-lookup"><span data-stu-id="74dee-109">Syntax</span></span>


```C++
HRESULT EnumSubtypes(
  [in]       PST_KEY          Key,
  [in] const GUID             *pType,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreTypes **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="74dee-110">參數</span><span class="sxs-lookup"><span data-stu-id="74dee-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74dee-111">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74dee-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74dee-112">指定類型是否為本機電腦，或僅與建立的使用者相關聯。</span><span class="sxs-lookup"><span data-stu-id="74dee-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="74dee-113">值</span><span class="sxs-lookup"><span data-stu-id="74dee-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="74dee-114">意義</span><span class="sxs-lookup"><span data-stu-id="74dee-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="74dee-115"><dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="74dee-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="74dee-116">存放區會保留在登錄的 [目前使用者] 區段中。</span><span class="sxs-lookup"><span data-stu-id="74dee-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="74dee-117"><dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="74dee-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="74dee-118">存放區會保留在登錄的 [本機電腦] 區段中。</span><span class="sxs-lookup"><span data-stu-id="74dee-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="74dee-119">*pType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74dee-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74dee-120">識別儲存體資料類型之 GUID 的指標。</span><span class="sxs-lookup"><span data-stu-id="74dee-120">A pointer to a GUID that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="74dee-121">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74dee-121">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74dee-122">Reserved：必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="74dee-122">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="74dee-123">*ppenum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="74dee-123">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74dee-124">[**IEnumPStoreTypes**](ienumpstoretypes.md)介面的指標，用來列舉子類型。</span><span class="sxs-lookup"><span data-stu-id="74dee-124">A pointer to an [**IEnumPStoreTypes**](ienumpstoretypes.md) interface that is used to enumerate the subtypes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74dee-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="74dee-125">Return value</span></span>

<span data-ttu-id="74dee-126">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="74dee-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="74dee-127">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="74dee-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="74dee-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="74dee-128">Requirements</span></span>



| <span data-ttu-id="74dee-129">需求</span><span class="sxs-lookup"><span data-stu-id="74dee-129">Requirement</span></span> | <span data-ttu-id="74dee-130">值</span><span class="sxs-lookup"><span data-stu-id="74dee-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74dee-131">標頭</span><span class="sxs-lookup"><span data-stu-id="74dee-131">Header</span></span><br/> | <dl> <span data-ttu-id="74dee-132"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="74dee-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="74dee-133">DLL</span><span class="sxs-lookup"><span data-stu-id="74dee-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="74dee-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74dee-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74dee-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74dee-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74dee-136">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="74dee-136">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
