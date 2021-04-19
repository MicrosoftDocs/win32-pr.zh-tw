---
description: 傳回用來列舉受保護儲存資料庫中專案的子類型介面指標。
ms.assetid: 940c321d-ec14-43fd-841b-cf581796bc87
title: 'IPStore：： EnumItems 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.EnumItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 9b44ee41a7daa4a75a19ca0f7045d69f5b380c9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998763"
---
# <a name="ipstoreenumitems-method"></a><span data-ttu-id="6c58c-103">IPStore：： EnumItems 方法</span><span class="sxs-lookup"><span data-stu-id="6c58c-103">IPStore::EnumItems method</span></span>

<span data-ttu-id="6c58c-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="6c58c-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="6c58c-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="6c58c-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="6c58c-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="6c58c-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="6c58c-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="6c58c-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="6c58c-108">傳回用來列舉受保護儲存資料庫中專案的子類型介面指標。</span><span class="sxs-lookup"><span data-stu-id="6c58c-108">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c58c-109">語法</span><span class="sxs-lookup"><span data-stu-id="6c58c-109">Syntax</span></span>


```C++
HRESULT EnumItems(
  [in]       PST_KEY          Key,
  [in] const PSGUID           *pItemType,
  [in] const GUID             *pItemSubtype,
  [in]       DWORD            dwFlags,
  [in]       IEnumPStoreItems **ppenum
);
```



## <a name="parameters"></a><span data-ttu-id="6c58c-110">參數</span><span class="sxs-lookup"><span data-stu-id="6c58c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c58c-111">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c58c-111">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c58c-112">指定類型是否為本機電腦，或僅與建立的使用者相關聯。</span><span class="sxs-lookup"><span data-stu-id="6c58c-112">Specifies whether the type is local to the computer or associated only with the creating user.</span></span>



| <span data-ttu-id="6c58c-113">值</span><span class="sxs-lookup"><span data-stu-id="6c58c-113">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="6c58c-114">意義</span><span class="sxs-lookup"><span data-stu-id="6c58c-114">Meaning</span></span>                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="PST_KEY_CURRENT_USER"></span><span id="pst_key_current_user"></span><dl> <span data-ttu-id="6c58c-115"><dt>**PST \_金鑰 \_ 目前 \_ 使用者**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="6c58c-115"><dt>**PST\_KEY\_CURRENT\_USER**</dt> <dt>0x00000000</dt></span></span> </dl>    | <span data-ttu-id="6c58c-116">存放區會保留在登錄的 [目前使用者] 區段中。</span><span class="sxs-lookup"><span data-stu-id="6c58c-116">The storage is maintained in the current user section of the registry.</span></span><br/>  |
| <span id="PST_KEY_LOCAL_MACHINE"></span><span id="pst_key_local_machine"></span><dl> <span data-ttu-id="6c58c-117"><dt>**PST \_\_ \_ 機碼本機電腦**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="6c58c-117"><dt>**PST\_KEY\_LOCAL\_MACHINE**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="6c58c-118">存放區會保留在登錄的 [本機電腦] 區段中。</span><span class="sxs-lookup"><span data-stu-id="6c58c-118">The storage is maintained in the local machine section of the registry.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6c58c-119">*pItemType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c58c-119">*pItemType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c58c-120">**GUID** 的指標，識別要列舉之專案的資料類型。</span><span class="sxs-lookup"><span data-stu-id="6c58c-120">A pointer to a **GUID** that identifies the data type of the item to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="6c58c-121">*pItemSubtype* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c58c-121">*pItemSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c58c-122">**GUID** 的指標，識別要列舉之專案的資料子型別。</span><span class="sxs-lookup"><span data-stu-id="6c58c-122">A pointer to a **GUID** that identifies the data subtype of the item to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="6c58c-123">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c58c-123">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c58c-124">Reserved：必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="6c58c-124">Reserved: Must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6c58c-125">*ppenum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c58c-125">*ppenum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c58c-126">指向 [**IEnumPStoreItems**](ienumpstoreitems.md) 介面指標的指標。</span><span class="sxs-lookup"><span data-stu-id="6c58c-126">A pointer to a pointer to an [**IEnumPStoreItems**](ienumpstoreitems.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c58c-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c58c-127">Return value</span></span>

<span data-ttu-id="6c58c-128">傳回值是 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="6c58c-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="6c58c-129">值為 **PST \_ E \_ OK** 表示函式已成功。</span><span class="sxs-lookup"><span data-stu-id="6c58c-129">A value of **PST\_E\_OK** indicates the function was successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c58c-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c58c-130">Requirements</span></span>



| <span data-ttu-id="6c58c-131">需求</span><span class="sxs-lookup"><span data-stu-id="6c58c-131">Requirement</span></span> | <span data-ttu-id="6c58c-132">值</span><span class="sxs-lookup"><span data-stu-id="6c58c-132">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c58c-133">標頭</span><span class="sxs-lookup"><span data-stu-id="6c58c-133">Header</span></span><br/> | <dl> <span data-ttu-id="6c58c-134"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c58c-134"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="6c58c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6c58c-135">DLL</span></span><br/>    | <dl> <span data-ttu-id="6c58c-136"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c58c-136"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c58c-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c58c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c58c-138">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="6c58c-138">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
