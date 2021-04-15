---
description: 停用指定資料庫的索引建立和修改。
ms.assetid: d079eae2-574e-4ac1-a0f9-11796e56a790
title: SdbStopIndexing 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStopIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 3c9c6b34c265d611b57a3e73bb0c8fb1822fe752
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510493"
---
# <a name="sdbstopindexing-function"></a><span data-ttu-id="1d2b9-103">SdbStopIndexing 函式</span><span class="sxs-lookup"><span data-stu-id="1d2b9-103">SdbStopIndexing function</span></span>

<span data-ttu-id="1d2b9-104">停用指定資料庫的索引建立和修改。</span><span class="sxs-lookup"><span data-stu-id="1d2b9-104">Disables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d2b9-105">語法</span><span class="sxs-lookup"><span data-stu-id="1d2b9-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStopIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="1d2b9-106">參數</span><span class="sxs-lookup"><span data-stu-id="1d2b9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d2b9-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d2b9-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2b9-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1d2b9-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="1d2b9-109">*iiWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d2b9-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d2b9-110">索引識別碼。</span><span class="sxs-lookup"><span data-stu-id="1d2b9-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d2b9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d2b9-111">Return value</span></span>

<span data-ttu-id="1d2b9-112">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="1d2b9-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d2b9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d2b9-113">Requirements</span></span>



| <span data-ttu-id="1d2b9-114">需求</span><span class="sxs-lookup"><span data-stu-id="1d2b9-114">Requirement</span></span> | <span data-ttu-id="1d2b9-115">值</span><span class="sxs-lookup"><span data-stu-id="1d2b9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d2b9-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d2b9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1d2b9-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d2b9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1d2b9-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d2b9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1d2b9-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d2b9-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1d2b9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1d2b9-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d2b9-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d2b9-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d2b9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d2b9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d2b9-123">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="1d2b9-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="1d2b9-124">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="1d2b9-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="1d2b9-125">**SdbStartIndexing**</span><span class="sxs-lookup"><span data-stu-id="1d2b9-125">**SdbStartIndexing**</span></span>](sdbstartindexing.md)
</dt> </dl>

 

 




