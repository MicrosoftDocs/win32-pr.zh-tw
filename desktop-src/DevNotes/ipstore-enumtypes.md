---
description: 傳回列舉受保護資料庫中目前註冊之類型的介面。
ms.assetid: 0c0c2ad7-90b0-4fc0-8972-82eb159653be
title: 'IPStore：： EnumTypes 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 73166a9fc1d76ae9f67528636eda567b9fa190a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999083"
---
# <a name="ipstoreenumtypes-method"></a><span data-ttu-id="2fe9e-103">IPStore：： EnumTypes 方法</span><span class="sxs-lookup"><span data-stu-id="2fe9e-103">IPStore::EnumTypes method</span></span>

<span data-ttu-id="2fe9e-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="2fe9e-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="2fe9e-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="2fe9e-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="2fe9e-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="2fe9e-108">傳回列舉受保護資料庫中目前註冊之類型的介面。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-108">Returns an interface for enumerating types that are currently registered in the protected database.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fe9e-109">語法</span><span class="sxs-lookup"><span data-stu-id="2fe9e-109">Syntax</span></span>


```C++
HRESULT EnumTypes(
  [in] PST_KEY          Key,
  [in] DWORD            dwFlags,
  [in] IEnumPStoreTypes **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="2fe9e-110">參數</span><span class="sxs-lookup"><span data-stu-id="2fe9e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fe9e-111">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2fe9e-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fe9e-112">指定類型是否為本機電腦，或僅與建立的使用者相關聯。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="2fe9e-113">值</span><span class="sxs-lookup"><span data-stu-id="2fe9e-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="2fe9e-114">意義</span><span class="sxs-lookup"><span data-stu-id="2fe9e-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="2fe9e-115"><dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="2fe9e-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="2fe9e-116">存放區會保留在登錄的 [目前使用者] 區段中。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="2fe9e-117"><dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="2fe9e-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="2fe9e-118">存放區會保留在登錄的 [本機電腦] 區段中。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2fe9e-119">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2fe9e-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fe9e-120">Reserved：必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-120">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="2fe9e-121">*ppenum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2fe9e-121">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2fe9e-122">用來執行列舉工作之 [**IEnumPStoreTypes**](ienumpstoretypes.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-122">A pointer to an [**IEnumPStoreTypes**](ienumpstoretypes.md) interface that is used to perform the enumeration tasks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fe9e-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="2fe9e-123">Return value</span></span>

<span data-ttu-id="2fe9e-124">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-124">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="2fe9e-125">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="2fe9e-125">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="2fe9e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2fe9e-126">Requirements</span></span>



| <span data-ttu-id="2fe9e-127">需求</span><span class="sxs-lookup"><span data-stu-id="2fe9e-127">Requirement</span></span> | <span data-ttu-id="2fe9e-128">值</span><span class="sxs-lookup"><span data-stu-id="2fe9e-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fe9e-129">標頭</span><span class="sxs-lookup"><span data-stu-id="2fe9e-129">Header</span></span><br/> | <dl> <span data-ttu-id="2fe9e-130"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="2fe9e-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="2fe9e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="2fe9e-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="2fe9e-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fe9e-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2fe9e-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2fe9e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fe9e-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="2fe9e-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
