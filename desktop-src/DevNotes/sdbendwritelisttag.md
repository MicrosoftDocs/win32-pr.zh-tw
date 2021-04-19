---
description: 結束指定清單的寫入作業。
ms.assetid: 318aa5dc-b562-47f8-8cd6-daa97f28c0f0
title: SdbEndWriteListTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbEndWriteListTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: f5f203e3b643fcae174eae3634b5d337a0d7276a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971120"
---
# <a name="sdbendwritelisttag-function"></a><span data-ttu-id="82342-103">SdbEndWriteListTag 函式</span><span class="sxs-lookup"><span data-stu-id="82342-103">SdbEndWriteListTag function</span></span>

<span data-ttu-id="82342-104">結束指定清單的寫入作業。</span><span class="sxs-lookup"><span data-stu-id="82342-104">Ends the write operations for the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="82342-105">語法</span><span class="sxs-lookup"><span data-stu-id="82342-105">Syntax</span></span>


```C++
BOOL WINAPI SdbEndWriteListTag(
  _Inout_ PDB   pdb,
  _In_    TAGID tiList
);
```



## <a name="parameters"></a><span data-ttu-id="82342-106">參數</span><span class="sxs-lookup"><span data-stu-id="82342-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82342-107">*pdb* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="82342-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="82342-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="82342-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="82342-109">*tiList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="82342-109">*tiList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82342-110">清單的 [**TAGID**](tagid.md)</span><span class="sxs-lookup"><span data-stu-id="82342-110">The [**TAGID**](tagid.md) of the list</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82342-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="82342-111">Return value</span></span>

<span data-ttu-id="82342-112">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="82342-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="82342-113">備註</span><span class="sxs-lookup"><span data-stu-id="82342-113">Remarks</span></span>

<span data-ttu-id="82342-114">寫入所有清單專案之後，請呼叫此函式;它會標示清單的結尾。</span><span class="sxs-lookup"><span data-stu-id="82342-114">Call this function after writing all list entries; it will mark the end of the list.</span></span>

## <a name="requirements"></a><span data-ttu-id="82342-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="82342-115">Requirements</span></span>



| <span data-ttu-id="82342-116">需求</span><span class="sxs-lookup"><span data-stu-id="82342-116">Requirement</span></span> | <span data-ttu-id="82342-117">值</span><span class="sxs-lookup"><span data-stu-id="82342-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82342-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82342-118">Minimum supported client</span></span><br/> | <span data-ttu-id="82342-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82342-119">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="82342-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82342-120">Minimum supported server</span></span><br/> | <span data-ttu-id="82342-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82342-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="82342-122">DLL</span><span class="sxs-lookup"><span data-stu-id="82342-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82342-123"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82342-123"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82342-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82342-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82342-125">**SdbBeginWriteListTag**</span><span class="sxs-lookup"><span data-stu-id="82342-125">**SdbBeginWriteListTag**</span></span>](sdbbeginwritelisttag.md)
</dt> <dt>

[<span data-ttu-id="82342-126">**SdbCloseDatabase**</span><span class="sxs-lookup"><span data-stu-id="82342-126">**SdbCloseDatabase**</span></span>](sdbclosedatabase.md)
</dt> <dt>

[<span data-ttu-id="82342-127">**SdbCloseDatabaseWrite**</span><span class="sxs-lookup"><span data-stu-id="82342-127">**SdbCloseDatabaseWrite**</span></span>](sdbclosedatabasewrite.md)
</dt> </dl>

 

 




