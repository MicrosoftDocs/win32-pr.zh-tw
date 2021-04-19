---
description: ReadBlobFromFile 函式會讀取檔案中的 BLOB。
ms.assetid: c3d4a892-160b-48e9-8881-0ada3ebd49b0
title: 'ReadBlobFromFile 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadBlobFromFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 66d1f28bd43747adaaecf7fad156d80095a71b5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997213"
---
# <a name="readblobfromfile-function"></a><span data-ttu-id="d78d4-103">ReadBlobFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="d78d4-103">ReadBlobFromFile function</span></span>

<span data-ttu-id="d78d4-104">**ReadBlobFromFile** 函式會讀取檔案中的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="d78d4-104">The **ReadBlobFromFile** function reads a BLOB in a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d78d4-105">語法</span><span class="sxs-lookup"><span data-stu-id="d78d4-105">Syntax</span></span>


```C++
DWORD ReadBlobFromFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="d78d4-106">參數</span><span class="sxs-lookup"><span data-stu-id="d78d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d78d4-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d78d4-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d78d4-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d78d4-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="d78d4-109">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d78d4-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d78d4-110">包含 BLOB 的檔案名之指標。</span><span class="sxs-lookup"><span data-stu-id="d78d4-110">Pointer to the name of the file that contains the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d78d4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d78d4-111">Return value</span></span>

<span data-ttu-id="d78d4-112">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="d78d4-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d78d4-113">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="d78d4-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="d78d4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d78d4-114">Requirements</span></span>



| <span data-ttu-id="d78d4-115">需求</span><span class="sxs-lookup"><span data-stu-id="d78d4-115">Requirement</span></span> | <span data-ttu-id="d78d4-116">值</span><span class="sxs-lookup"><span data-stu-id="d78d4-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d78d4-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d78d4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d78d4-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d78d4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d78d4-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d78d4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d78d4-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d78d4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d78d4-121">標頭</span><span class="sxs-lookup"><span data-stu-id="d78d4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d78d4-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="d78d4-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="d78d4-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="d78d4-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d78d4-124"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d78d4-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="d78d4-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d78d4-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d78d4-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d78d4-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




