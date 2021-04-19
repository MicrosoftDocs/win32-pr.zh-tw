---
description: 從受保護的儲存體關閉指定的資料項目。
ms.assetid: 74919354-5e31-4ab5-9326-9f9aae206bd7
title: 'IPStore：： CloseItem 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.CloseItem
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: e5f550df0ffa4dd2f35a91e768d70bb0359b9a4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989595"
---
# <a name="ipstorecloseitem-method"></a><span data-ttu-id="3b427-103">IPStore：： CloseItem 方法</span><span class="sxs-lookup"><span data-stu-id="3b427-103">IPStore::CloseItem method</span></span>

<span data-ttu-id="3b427-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="3b427-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="3b427-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="3b427-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="3b427-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="3b427-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="3b427-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="3b427-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="3b427-108">從受保護的儲存體關閉指定的資料項目。</span><span class="sxs-lookup"><span data-stu-id="3b427-108">Closes a specified data item from protected storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b427-109">語法</span><span class="sxs-lookup"><span data-stu-id="3b427-109">Syntax</span></span>


```C++
HRESULT CloseItem(
  [in]       PST_KEY Key,
  [in] const PSGUID  *pItemType,
  [in] const GUID    *pItemSubtype,
  [in]       LPCWSTR *szItemName,
  [in]       DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3b427-110">參數</span><span class="sxs-lookup"><span data-stu-id="3b427-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b427-111">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b427-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b427-112">指定類型是否為本機電腦，或僅與建立的使用者相關聯。</span><span class="sxs-lookup"><span data-stu-id="3b427-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="3b427-113">值</span><span class="sxs-lookup"><span data-stu-id="3b427-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="3b427-114">意義</span><span class="sxs-lookup"><span data-stu-id="3b427-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="3b427-115"><dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="3b427-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="3b427-116">存放區會保留在登錄的 [目前使用者] 區段中。</span><span class="sxs-lookup"><span data-stu-id="3b427-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="3b427-117"><dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="3b427-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="3b427-118">存放區會保留在登錄的 [本機電腦] 區段中。</span><span class="sxs-lookup"><span data-stu-id="3b427-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="3b427-119">*pItemType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b427-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b427-120">**GUID** 的指標，識別要關閉之專案的資料類型。</span><span class="sxs-lookup"><span data-stu-id="3b427-120">A pointer to a **GUID** that identifies the data type of the item to close.</span></span>

</dd> <dt>

<span data-ttu-id="3b427-121">*pItemSubtype* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b427-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b427-122">**GUID** 的指標，指出要關閉的專案子類型。</span><span class="sxs-lookup"><span data-stu-id="3b427-122">A pointer to a **GUID** that indicates the item subtype to close.</span></span>

</dd> <dt>

<span data-ttu-id="3b427-123">*szItemName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b427-123">*szItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b427-124">字串，其中包含要關閉之專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="3b427-124">A string that contains the name of the item to close.</span></span>

</dd> <dt>

<span data-ttu-id="3b427-125">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b427-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b427-126">Reserved：必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="3b427-126">Reserved: must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b427-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b427-127">Return value</span></span>

<span data-ttu-id="3b427-128">傳回值是 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3b427-128">The return value is an **HRESULT** value.</span></span> <span data-ttu-id="3b427-129">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="3b427-129">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b427-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b427-130">Requirements</span></span>



| <span data-ttu-id="3b427-131">需求</span><span class="sxs-lookup"><span data-stu-id="3b427-131">Requirement</span></span> | <span data-ttu-id="3b427-132">值</span><span class="sxs-lookup"><span data-stu-id="3b427-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b427-133">標頭</span><span class="sxs-lookup"><span data-stu-id="3b427-133">Header</span></span><br/> | <dl> <span data-ttu-id="3b427-134"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b427-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="3b427-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3b427-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="3b427-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b427-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b427-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b427-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b427-138">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="3b427-138">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
