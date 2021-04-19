---
description: WriteBlobToFile 函式會將 BLOB 寫入檔案。
ms.assetid: 0793dced-82c2-4553-90b2-acf594c6749e
title: 'WriteBlobToFile 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WriteBlobToFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5fbf17b76631da6dbff9ef2077776106505a37b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975806"
---
# <a name="writeblobtofile-function"></a><span data-ttu-id="72f9e-103">WriteBlobToFile 函式</span><span class="sxs-lookup"><span data-stu-id="72f9e-103">WriteBlobToFile function</span></span>

<span data-ttu-id="72f9e-104">**WriteBlobToFile** 函式會將 BLOB 寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="72f9e-104">The **WriteBlobToFile** function writes a BLOB to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="72f9e-105">語法</span><span class="sxs-lookup"><span data-stu-id="72f9e-105">Syntax</span></span>


```C++
DWORD WriteBlobToFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="72f9e-106">參數</span><span class="sxs-lookup"><span data-stu-id="72f9e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72f9e-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72f9e-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f9e-108">BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="72f9e-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="72f9e-109">*pFileName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="72f9e-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72f9e-110">檔案名稱的指標，BLOB 會儲存在此檔案中。</span><span class="sxs-lookup"><span data-stu-id="72f9e-110">Pointer to the name of the file, in which the BLOB is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72f9e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="72f9e-111">Return value</span></span>

<span data-ttu-id="72f9e-112">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="72f9e-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="72f9e-113">如果函式不成功，則傳回值會是指出錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="72f9e-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="72f9e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="72f9e-114">Requirements</span></span>



| <span data-ttu-id="72f9e-115">需求</span><span class="sxs-lookup"><span data-stu-id="72f9e-115">Requirement</span></span> | <span data-ttu-id="72f9e-116">值</span><span class="sxs-lookup"><span data-stu-id="72f9e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="72f9e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72f9e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="72f9e-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72f9e-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="72f9e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72f9e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="72f9e-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72f9e-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="72f9e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="72f9e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="72f9e-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="72f9e-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="72f9e-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="72f9e-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="72f9e-124"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="72f9e-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="72f9e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="72f9e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72f9e-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72f9e-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




