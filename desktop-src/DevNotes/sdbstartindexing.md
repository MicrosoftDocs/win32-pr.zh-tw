---
description: 啟用指定之資料庫的索引建立和修改。
ms.assetid: f780034e-6963-423c-8ffa-9fbe98dca7e1
title: SdbStartIndexing 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbStartIndexing
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: e3324b4cb0d42ca33ee7c3234a1acc099adcb743
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110428"
---
# <a name="sdbstartindexing-function"></a><span data-ttu-id="13a10-103">SdbStartIndexing 函式</span><span class="sxs-lookup"><span data-stu-id="13a10-103">SdbStartIndexing function</span></span>

<span data-ttu-id="13a10-104">啟用指定之資料庫的索引建立和修改。</span><span class="sxs-lookup"><span data-stu-id="13a10-104">Enables index creation and modification for the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="13a10-105">語法</span><span class="sxs-lookup"><span data-stu-id="13a10-105">Syntax</span></span>


```C++
BOOL WINAPI SdbStartIndexing(
  _In_ PDB     pdb,
  _In_ INDEXID iiWhich
);
```



## <a name="parameters"></a><span data-ttu-id="13a10-106">參數</span><span class="sxs-lookup"><span data-stu-id="13a10-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13a10-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13a10-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13a10-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="13a10-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="13a10-109">*iiWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13a10-109">*iiWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13a10-110">索引識別碼。</span><span class="sxs-lookup"><span data-stu-id="13a10-110">The index identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13a10-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="13a10-111">Return value</span></span>

<span data-ttu-id="13a10-112">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="13a10-112">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="13a10-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="13a10-113">Requirements</span></span>



| <span data-ttu-id="13a10-114">需求</span><span class="sxs-lookup"><span data-stu-id="13a10-114">Requirement</span></span> | <span data-ttu-id="13a10-115">值</span><span class="sxs-lookup"><span data-stu-id="13a10-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13a10-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13a10-116">Minimum supported client</span></span><br/> | <span data-ttu-id="13a10-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13a10-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="13a10-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13a10-118">Minimum supported server</span></span><br/> | <span data-ttu-id="13a10-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13a10-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="13a10-120">DLL</span><span class="sxs-lookup"><span data-stu-id="13a10-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13a10-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13a10-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13a10-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13a10-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13a10-123">**SdbCommitIndexes**</span><span class="sxs-lookup"><span data-stu-id="13a10-123">**SdbCommitIndexes**</span></span>](sdbcommitindexes.md)
</dt> <dt>

[<span data-ttu-id="13a10-124">**SdbDeclareIndex**</span><span class="sxs-lookup"><span data-stu-id="13a10-124">**SdbDeclareIndex**</span></span>](sdbdeclareindex.md)
</dt> <dt>

[<span data-ttu-id="13a10-125">**SdbStopIndexing**</span><span class="sxs-lookup"><span data-stu-id="13a10-125">**SdbStopIndexing**</span></span>](sdbstopindexing.md)
</dt> </dl>

 

 




