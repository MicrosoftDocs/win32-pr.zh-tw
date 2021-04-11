---
description: 將指定檔案中的二進位資料寫入至指定的資料庫。
ms.assetid: 960633a8-5cec-462b-b7dc-72eb3e4fd0a2
title: SdbWriteBinaryTagFromFile 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbWriteBinaryTagFromFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 75b45a935fd9630afcefe8f7d30338a6ad6b10a3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936188"
---
# <a name="sdbwritebinarytagfromfile-function"></a><span data-ttu-id="4488e-103">SdbWriteBinaryTagFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="4488e-103">SdbWriteBinaryTagFromFile function</span></span>

<span data-ttu-id="4488e-104">將指定檔案中的二進位資料寫入至指定的資料庫。</span><span class="sxs-lookup"><span data-stu-id="4488e-104">Writes binary data from the specified file to the specified database.</span></span>

## <a name="syntax"></a><span data-ttu-id="4488e-105">語法</span><span class="sxs-lookup"><span data-stu-id="4488e-105">Syntax</span></span>


```C++
BOOL WINAPI SdbWriteBinaryTagFromFile(
  _In_ PDB     pdb,
  _In_ TAG     tTag,
  _In_ LPCWSTR pwszPath
);
```



## <a name="parameters"></a><span data-ttu-id="4488e-106">參數</span><span class="sxs-lookup"><span data-stu-id="4488e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4488e-107">*pdb* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4488e-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4488e-108">填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4488e-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="4488e-109">*tTag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4488e-109">*tTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4488e-110">專案的標記。</span><span class="sxs-lookup"><span data-stu-id="4488e-110">The TAG for the entry.</span></span> <span data-ttu-id="4488e-111">這個標記必須是 **標記 \_ 類型 \_ BINARY** 類型。</span><span class="sxs-lookup"><span data-stu-id="4488e-111">This TAG must be of type **TAG\_TYPE\_BINARY**.</span></span>

</dd> <dt>

<span data-ttu-id="4488e-112">*pwszPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4488e-112">*pwszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4488e-113">包含資料之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="4488e-113">The path to the file that contains the data.</span></span> <span data-ttu-id="4488e-114">此參數不可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4488e-114">This parameter cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4488e-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="4488e-115">Return value</span></span>

<span data-ttu-id="4488e-116">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="4488e-116">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="4488e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="4488e-117">Requirements</span></span>



| <span data-ttu-id="4488e-118">需求</span><span class="sxs-lookup"><span data-stu-id="4488e-118">Requirement</span></span> | <span data-ttu-id="4488e-119">值</span><span class="sxs-lookup"><span data-stu-id="4488e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4488e-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4488e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4488e-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4488e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="4488e-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4488e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4488e-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4488e-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="4488e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4488e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4488e-125"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4488e-125"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4488e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4488e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4488e-127">**SdbWriteBinaryTag**</span><span class="sxs-lookup"><span data-stu-id="4488e-127">**SdbWriteBinaryTag**</span></span>](sdbwritebinarytag.md)
</dt> </dl>

 

 




