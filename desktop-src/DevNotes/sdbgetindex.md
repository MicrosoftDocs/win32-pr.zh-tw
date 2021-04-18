---
description: 從指定的資料庫抓取指定之標記和索引鍵類型的索引。
ms.assetid: 5fa44252-ba26-43ed-9de0-5917e4ec797c
title: SdbGetIndex 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetIndex
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c7bcc211e4277a2ffee6a68258d7616cb7aa2a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468201"
---
# <a name="sdbgetindex-function"></a><span data-ttu-id="aeb9c-103">SdbGetIndex 函式</span><span class="sxs-lookup"><span data-stu-id="aeb9c-103">SdbGetIndex function</span></span>

<span data-ttu-id="aeb9c-104">從指定的資料庫抓取指定之標記和索引鍵類型的索引。</span><span class="sxs-lookup"><span data-stu-id="aeb9c-104">Retrieves the index for the specified tag and key type from the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeb9c-105">語法</span><span class="sxs-lookup"><span data-stu-id="aeb9c-105">Syntax</span></span>


```C++
TAGID WINAPI SdbGetIndex(
  _In_      PDB     pdb,
  _In_      TAG     tWhich,
  _In_      TAG     tKey,
  _Out_opt_ LPDWORD lpdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="aeb9c-106">參數</span><span class="sxs-lookup"><span data-stu-id="aeb9c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aeb9c-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aeb9c-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb9c-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="aeb9c-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="aeb9c-109">*tWhich* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aeb9c-109">*tWhich* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb9c-110">標記。</span><span class="sxs-lookup"><span data-stu-id="aeb9c-110">The TAG.</span></span>

</dd> <dt>

<span data-ttu-id="aeb9c-111">*tKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aeb9c-111">*tKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb9c-112">索引鍵類型。</span><span class="sxs-lookup"><span data-stu-id="aeb9c-112">The key type.</span></span>

</dd> <dt>

<span data-ttu-id="aeb9c-113">*lpdwFlags* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="aeb9c-113">*lpdwFlags* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aeb9c-114">此參數可以是0或 **SHIMDB \_ 索引 \_ 唯一索引 \_ 鍵** (0x00000001) 。</span><span class="sxs-lookup"><span data-stu-id="aeb9c-114">This parameter can be 0 or **SHIMDB\_INDEX\_UNIQUE\_KEY** (0x00000001).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aeb9c-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="aeb9c-115">Return value</span></span>

<span data-ttu-id="aeb9c-116">索引的 **TAGID** 或 **TAGID \_ Null**。</span><span class="sxs-lookup"><span data-stu-id="aeb9c-116">The **TAGID** of the index or **TAGID\_NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="aeb9c-117">備註</span><span class="sxs-lookup"><span data-stu-id="aeb9c-117">Remarks</span></span>

<span data-ttu-id="aeb9c-118">產生的索引可用於讀取作業。</span><span class="sxs-lookup"><span data-stu-id="aeb9c-118">The resulting index can be used for read operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeb9c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="aeb9c-119">Requirements</span></span>



| <span data-ttu-id="aeb9c-120">需求</span><span class="sxs-lookup"><span data-stu-id="aeb9c-120">Requirement</span></span> | <span data-ttu-id="aeb9c-121">值</span><span class="sxs-lookup"><span data-stu-id="aeb9c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aeb9c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aeb9c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="aeb9c-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aeb9c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="aeb9c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aeb9c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="aeb9c-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aeb9c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="aeb9c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="aeb9c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aeb9c-127"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aeb9c-127"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




