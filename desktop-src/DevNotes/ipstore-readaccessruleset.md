---
description: 讀取指定類型的存取規則。
ms.assetid: fd569e7f-ca5c-4571-bbaa-c669e8780a97
title: 'IPStore：： ReadAccessRuleSet 方法 (Pstore .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore.ReadAccessRuleSet
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: f69c206bde67c2ddf9ed87ba0c50633ab9c15bc3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993206"
---
# <a name="ipstorereadaccessruleset-method"></a><span data-ttu-id="205df-103">IPStore：： ReadAccessRuleSet 方法</span><span class="sxs-lookup"><span data-stu-id="205df-103">IPStore::ReadAccessRuleSet method</span></span>

<span data-ttu-id="205df-104">\[受保護的存放裝置 (Pstore) 可用於 Windows Server 2003 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="205df-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="205df-105">它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀操作，但在後續版本中可能無法使用。</span><span class="sxs-lookup"><span data-stu-id="205df-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="205df-106">Pstore 會使用較舊的資料保護執行。</span><span class="sxs-lookup"><span data-stu-id="205df-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="205df-107">強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]</span><span class="sxs-lookup"><span data-stu-id="205df-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="205df-108">\[這個方法尚未實作。\]</span><span class="sxs-lookup"><span data-stu-id="205df-108">\[This method is not implemented.\]</span></span>

<span data-ttu-id="205df-109">讀取指定類型的存取規則。</span><span class="sxs-lookup"><span data-stu-id="205df-109">Reads the access rules for a given type.</span></span>

## <a name="syntax"></a><span data-ttu-id="205df-110">語法</span><span class="sxs-lookup"><span data-stu-id="205df-110">Syntax</span></span>


```C++
HRESULT ReadAccessRuleSet(
  [in]       PST_KEY            Key,
  [in] const GUID               *pType,
  [in] const GUID               *pSubtype,
  [in]       PPST_TYPEINFO      pInfo,
  [in]       PPST_ACCESSRULESET **ppRules,
  [in]       DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="205df-111">參數</span><span class="sxs-lookup"><span data-stu-id="205df-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="205df-112">*金鑰* \[在\]</span><span class="sxs-lookup"><span data-stu-id="205df-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205df-113">保留的。</span><span class="sxs-lookup"><span data-stu-id="205df-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="205df-114">*pType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="205df-114">*pType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205df-115">保留的。</span><span class="sxs-lookup"><span data-stu-id="205df-115">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="205df-116">*pSubtype* \[在\]</span><span class="sxs-lookup"><span data-stu-id="205df-116">*pSubtype* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205df-117">保留的。</span><span class="sxs-lookup"><span data-stu-id="205df-117">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="205df-118">*pInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="205df-118">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205df-119">保留的。</span><span class="sxs-lookup"><span data-stu-id="205df-119">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="205df-120">*ppRules* \[在\]</span><span class="sxs-lookup"><span data-stu-id="205df-120">*ppRules* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205df-121">保留的。</span><span class="sxs-lookup"><span data-stu-id="205df-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="205df-122">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="205df-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="205df-123">保留的。</span><span class="sxs-lookup"><span data-stu-id="205df-123">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="205df-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="205df-124">Return value</span></span>

<span data-ttu-id="205df-125">呼叫這個方法一律會失敗。</span><span class="sxs-lookup"><span data-stu-id="205df-125">Calls to this method will always fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="205df-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="205df-126">Requirements</span></span>



| <span data-ttu-id="205df-127">需求</span><span class="sxs-lookup"><span data-stu-id="205df-127">Requirement</span></span> | <span data-ttu-id="205df-128">值</span><span class="sxs-lookup"><span data-stu-id="205df-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="205df-129">標頭</span><span class="sxs-lookup"><span data-stu-id="205df-129">Header</span></span><br/> | <dl> <span data-ttu-id="205df-130"><dt>Pstore。h</dt></span><span class="sxs-lookup"><span data-stu-id="205df-130"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="205df-131">DLL</span><span class="sxs-lookup"><span data-stu-id="205df-131">DLL</span></span><br/>    | <dl> <span data-ttu-id="205df-132"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="205df-132"><dt>Pstorec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="205df-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="205df-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="205df-134">**IPStore**</span><span class="sxs-lookup"><span data-stu-id="205df-134">**IPStore**</span></span>](ipstore.md)
</dt> </dl>

 

 
