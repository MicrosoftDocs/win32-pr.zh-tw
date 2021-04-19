---
description: 抓取與類型相關聯的資訊。
ms.assetid: 27a283a5-8924-4a2f-8f58-e673a424e28a
title: 'IPStore：： GetTypeInfo 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.GetTypeInfo
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: c533c30268bf8b8e879e937359471da8cd7af8b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981384"
---
# <a name="ipstoregettypeinfo-method"></a><span data-ttu-id="4ecc2-103">IPStore：： GetTypeInfo 方法</span><span class="sxs-lookup"><span data-stu-id="4ecc2-103">IPStore::GetTypeInfo method</span></span>

<span data-ttu-id="4ecc2-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="4ecc2-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="4ecc2-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="4ecc2-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="4ecc2-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="4ecc2-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="4ecc2-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="4ecc2-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="4ecc2-108">抓取與類型相關聯的資訊。</span><span class="sxs-lookup"><span data-stu-id="4ecc2-108">Retrieves information associated with a type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ecc2-109">語法</span><span class="sxs-lookup"><span data-stu-id="4ecc2-109">Syntax</span></span>


```C++
HRESULT GetTypeInfo(
  [in]       PST_KEY       Key,
  [in] const GUID          *pType,
  [in]       PPST_TYPEINFO **ppInfo,
  [in]       DWORD         dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4ecc2-110">參數</span><span class="sxs-lookup"><span data-stu-id="4ecc2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ecc2-111">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ecc2-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ecc2-112">指定類型是否為本機電腦，或僅與建立的使用者相關聯。</span><span class="sxs-lookup"><span data-stu-id="4ecc2-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="4ecc2-113">值</span><span class="sxs-lookup"><span data-stu-id="4ecc2-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="4ecc2-114">意義</span><span class="sxs-lookup"><span data-stu-id="4ecc2-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="4ecc2-115"><dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="4ecc2-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="4ecc2-116">存放區會保留在登錄的 [目前使用者] 區段中。</span><span class="sxs-lookup"><span data-stu-id="4ecc2-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="4ecc2-117"><dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4ecc2-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="4ecc2-118">存放區會保留在登錄的 [本機電腦] 區段中。</span><span class="sxs-lookup"><span data-stu-id="4ecc2-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4ecc2-119">*pType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ecc2-119">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ecc2-120">識別儲存體資料類型之 **GUID** 的指標。</span><span class="sxs-lookup"><span data-stu-id="4ecc2-120">A pointer to a **GUID** that identifies the data type of the storage.</span></span>

</dd> <dt>

<span data-ttu-id="4ecc2-121">*ppInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ecc2-121">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ecc2-122">包含資料類型名稱之 [**PST \_ TYPEINFO**](pst-typeinfo.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4ecc2-122">A pointer to a [**PST\_TYPEINFO**](pst-typeinfo.md) structure that contains the name of the data type.</span></span>

</dd> <dt>

<span data-ttu-id="4ecc2-123">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4ecc2-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ecc2-124">Reserved：必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="4ecc2-124">Reserved: Must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ecc2-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="4ecc2-125">Return value</span></span>

<span data-ttu-id="4ecc2-126">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4ecc2-126">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="4ecc2-127">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="4ecc2-127">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ecc2-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="4ecc2-128">Requirements</span></span>



| <span data-ttu-id="4ecc2-129">需求</span><span class="sxs-lookup"><span data-stu-id="4ecc2-129">Requirement</span></span> | <span data-ttu-id="4ecc2-130">值</span><span class="sxs-lookup"><span data-stu-id="4ecc2-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ecc2-131">標頭</span><span class="sxs-lookup"><span data-stu-id="4ecc2-131">Header</span></span><br/> | <dl> <span data-ttu-id="4ecc2-132"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="4ecc2-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="4ecc2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4ecc2-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="4ecc2-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ecc2-134"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ecc2-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4ecc2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ecc2-136">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="4ecc2-136">**IPStore**</span></span>](ipstore.md)
</dt> <dt>

[<span data-ttu-id="4ecc2-137">**PST \_ TYPEINFO**</span><span class="sxs-lookup"><span data-stu-id="4ecc2-137">**PST\_TYPEINFO**</span></span>](pst-typeinfo.md)
</dt> </dl>

 

 
