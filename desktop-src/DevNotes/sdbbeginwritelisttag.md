---
description: 建立寫入作業的新清單標記。
ms.assetid: 3a52e2f2-9648-45fb-b487-ccfe5ed24f7f
title: SdbBeginWriteListTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbBeginWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a9dcf6bdd3798b18e08b796eb268f93dc4ec6bbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689051"
---
# <a name="sdbbeginwritelisttag-function"></a><span data-ttu-id="450ce-103">SdbBeginWriteListTag 函式</span><span class="sxs-lookup"><span data-stu-id="450ce-103">SdbBeginWriteListTag function</span></span>

<span data-ttu-id="450ce-104">建立寫入作業的新清單標記。</span><span class="sxs-lookup"><span data-stu-id="450ce-104">Creates a new list TAG for write operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="450ce-105">語法</span><span class="sxs-lookup"><span data-stu-id="450ce-105">Syntax</span></span>


```C++
TAGID WINAPI SdbBeginWriteListTag(
  _In_ PDB pdb,
  _In_ TAG tTag
);
```



## <a name="parameters"></a><span data-ttu-id="450ce-106">參數</span><span class="sxs-lookup"><span data-stu-id="450ce-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="450ce-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="450ce-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="450ce-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="450ce-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="450ce-109">*tTag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="450ce-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="450ce-110">新專案的標記。</span><span class="sxs-lookup"><span data-stu-id="450ce-110">The TAG for the new entry.</span></span> <span data-ttu-id="450ce-111">這個值必須是類型 **標記 \_ 類型 \_ 清單**。</span><span class="sxs-lookup"><span data-stu-id="450ce-111">This value must be of type **TAG\_TYPE\_LIST**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="450ce-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="450ce-112">Return value</span></span>

<span data-ttu-id="450ce-113">函數會在成功時傳回新清單的 [**TAGID**](tagid.md) ，或在失敗時傳回 **TAGID \_ Null** 。</span><span class="sxs-lookup"><span data-stu-id="450ce-113">The function returns the [**TAGID**](tagid.md) of the new list on success or **TAGID\_NULL** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="450ce-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="450ce-114">Requirements</span></span>



| <span data-ttu-id="450ce-115">需求</span><span class="sxs-lookup"><span data-stu-id="450ce-115">Requirement</span></span> | <span data-ttu-id="450ce-116">值</span><span class="sxs-lookup"><span data-stu-id="450ce-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="450ce-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="450ce-117">Minimum supported client</span></span><br/> | <span data-ttu-id="450ce-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="450ce-118">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="450ce-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="450ce-119">Minimum supported server</span></span><br/> | <span data-ttu-id="450ce-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="450ce-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="450ce-121">DLL</span><span class="sxs-lookup"><span data-stu-id="450ce-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="450ce-122"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="450ce-122"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="450ce-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="450ce-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="450ce-124">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="450ce-124">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="450ce-125">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="450ce-125">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> <dt>

[<span data-ttu-id="450ce-126">**SdbEndWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="450ce-126">**SdbEndWriteListTag**</span></span>](sdbendwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="450ce-127">**標記**</span><span class="sxs-lookup"><span data-stu-id="450ce-127">**TAG**</span></span>](tag.md)
</dt> <dt>

[<span data-ttu-id="450ce-128">標記類型</span><span class="sxs-lookup"><span data-stu-id="450ce-128">TAG Types</span></span>](tag-types.md)
</dt> <dt>

[<span data-ttu-id="450ce-129">**TAGID**</span><span class="sxs-lookup"><span data-stu-id="450ce-129">**TAGID**</span></span>](tagid.md)
</dt> </dl>

 

 




