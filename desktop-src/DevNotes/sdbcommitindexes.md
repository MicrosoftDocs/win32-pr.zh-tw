---
description: 將新建立的索引認可至指定的資料庫。
ms.assetid: 92f05e5f-599a-4870-8175-61b83c943514
title: SdbCommitIndexes 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCommitIndexes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 0709a913dc78cefdf405a0a3bd29030801941c37
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110281"
---
# <a name="sdbcommitindexes-function"></a><span data-ttu-id="73612-103">SdbCommitIndexes 函式</span><span class="sxs-lookup"><span data-stu-id="73612-103">SdbCommitIndexes function</span></span>

<span data-ttu-id="73612-104">將新建立的索引認可至指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="73612-104">Commits newly created indexes to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="73612-105">語法</span><span class="sxs-lookup"><span data-stu-id="73612-105">Syntax</span></span>


```C++
BOOL WINAPI SdbCommitIndexes(
  _Inout_ PDB pdb
);
```



## <a name="parameters"></a><span data-ttu-id="73612-106">參數</span><span class="sxs-lookup"><span data-stu-id="73612-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73612-107">*pdb* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="73612-107">*pdb* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="73612-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="73612-108">A handle to the shim database.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73612-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="73612-109">Return value</span></span>

<span data-ttu-id="73612-110">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="73612-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="73612-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="73612-111">Requirements</span></span>



| <span data-ttu-id="73612-112">需求</span><span class="sxs-lookup"><span data-stu-id="73612-112">Requirement</span></span> | <span data-ttu-id="73612-113">值</span><span class="sxs-lookup"><span data-stu-id="73612-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73612-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73612-114">Minimum supported client</span></span><br/> | <span data-ttu-id="73612-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73612-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="73612-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73612-116">Minimum supported server</span></span><br/> | <span data-ttu-id="73612-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="73612-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="73612-118">DLL</span><span class="sxs-lookup"><span data-stu-id="73612-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73612-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73612-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73612-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73612-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73612-121">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="73612-121">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="73612-122">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="73612-122">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> <dt>

[<span data-ttu-id="73612-123">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="73612-123">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




