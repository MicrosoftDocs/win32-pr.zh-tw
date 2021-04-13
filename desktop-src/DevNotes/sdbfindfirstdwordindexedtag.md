---
description: 在指定的索引中尋找符合指定準則的第一個 DWORD 記錄。
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: SdbFindFirstDWORDIndexedTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510365"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a><span data-ttu-id="66999-103">SdbFindFirstDWORDIndexedTag 函式</span><span class="sxs-lookup"><span data-stu-id="66999-103">SdbFindFirstDWORDIndexedTag function</span></span>

<span data-ttu-id="66999-104">在指定的索引中尋找符合指定準則的第一個 **DWORD** 記錄。</span><span class="sxs-lookup"><span data-stu-id="66999-104">Finds the first **DWORD** record in the specified index that meets the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="66999-105">語法</span><span class="sxs-lookup"><span data-stu-id="66999-105">Syntax</span></span>


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
);
```



## <a name="parameters"></a><span data-ttu-id="66999-106">參數</span><span class="sxs-lookup"><span data-stu-id="66999-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66999-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66999-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66999-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="66999-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="66999-109">*tWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66999-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66999-110">索引類型。</span><span class="sxs-lookup"><span data-stu-id="66999-110">The index type.</span></span> <span data-ttu-id="66999-111">如需值清單，請參閱 [**標記**](tag.md) 。</span><span class="sxs-lookup"><span data-stu-id="66999-111">See [**TAG**](tag.md) for a list of values.</span></span>

</dd> <dt>

<span data-ttu-id="66999-112">*tKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66999-112">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66999-113">索引鍵類型。</span><span class="sxs-lookup"><span data-stu-id="66999-113">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="66999-114">*dwName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66999-114">*dwName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66999-115">要尋找的資料名稱。</span><span class="sxs-lookup"><span data-stu-id="66999-115">The name of the data to be found.</span></span> <span data-ttu-id="66999-116">此值將會轉換為索引鍵。</span><span class="sxs-lookup"><span data-stu-id="66999-116">This value will be converted into a key.</span></span>

</dd> <dt>

<span data-ttu-id="66999-117">*pFindInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="66999-117">*pFindInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="66999-118">接收記錄的 [**尋找 \_ 資訊**](find-info.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="66999-118">A [**FIND\_INFO**](find-info.md) structure that receives the record.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66999-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="66999-119">Return value</span></span>

<span data-ttu-id="66999-120">第一個相符項的 **TAGID** ，如果找不到相符的標記，則 **\_ 為 Null** 。</span><span class="sxs-lookup"><span data-stu-id="66999-120">The **TAGID** of the first match or **TAG\_NULL** if no match is found.</span></span>

## <a name="requirements"></a><span data-ttu-id="66999-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="66999-121">Requirements</span></span>



| <span data-ttu-id="66999-122">需求</span><span class="sxs-lookup"><span data-stu-id="66999-122">Requirement</span></span> | <span data-ttu-id="66999-123">值</span><span class="sxs-lookup"><span data-stu-id="66999-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66999-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66999-124">Minimum supported client</span></span><br/> | <span data-ttu-id="66999-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66999-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="66999-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66999-126">Minimum supported server</span></span><br/> | <span data-ttu-id="66999-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66999-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="66999-128">DLL</span><span class="sxs-lookup"><span data-stu-id="66999-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66999-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66999-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66999-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66999-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66999-131">**SdbFindFirstTag**</span><span class="sxs-lookup"><span data-stu-id="66999-131">**SdbFindFirstTag**</span></span>](sdbfindfirsttag.md)
</dt> </dl>

 

 




