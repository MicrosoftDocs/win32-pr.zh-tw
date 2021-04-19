---
description: DestroyBlob 函式會釋放與 BLOB 相關聯的所有記憶體，然後損毀 BLOB。
ms.assetid: 46cde0b7-1b59-426e-b19b-3c73af3d461a
title: 'DestroyBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e90630981c16f38d601d4e06d04f9326174ef721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990434"
---
# <a name="destroyblob-function"></a><span data-ttu-id="bd5d4-103">DestroyBlob 函式</span><span class="sxs-lookup"><span data-stu-id="bd5d4-103">DestroyBlob function</span></span>

<span data-ttu-id="bd5d4-104">**DestroyBlob** 函式會釋放與 blob 相關聯的所有記憶體，然後損毀 blob。</span><span class="sxs-lookup"><span data-stu-id="bd5d4-104">The **DestroyBlob** function frees all memory associated with the BLOB and then destroys the BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd5d4-105">語法</span><span class="sxs-lookup"><span data-stu-id="bd5d4-105">Syntax</span></span>


```C++
DWORD DestroyBlob(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="bd5d4-106">參數</span><span class="sxs-lookup"><span data-stu-id="bd5d4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd5d4-107">*hBlob* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd5d4-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd5d4-108">終結之 BLOB 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="bd5d4-108">Handle to the to the BLOB that is destroyed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd5d4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd5d4-109">Return value</span></span>

<span data-ttu-id="bd5d4-110">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="bd5d4-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="bd5d4-111">如果函式不成功，則傳回值為描述錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="bd5d4-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd5d4-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd5d4-112">Requirements</span></span>



| <span data-ttu-id="bd5d4-113">需求</span><span class="sxs-lookup"><span data-stu-id="bd5d4-113">Requirement</span></span> | <span data-ttu-id="bd5d4-114">值</span><span class="sxs-lookup"><span data-stu-id="bd5d4-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd5d4-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd5d4-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bd5d4-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd5d4-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bd5d4-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd5d4-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bd5d4-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd5d4-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd5d4-119">標頭</span><span class="sxs-lookup"><span data-stu-id="bd5d4-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd5d4-120"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="bd5d4-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="bd5d4-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="bd5d4-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="bd5d4-122"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd5d4-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="bd5d4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="bd5d4-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd5d4-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd5d4-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd5d4-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd5d4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5d4-126">CreateBlob</span><span class="sxs-lookup"><span data-stu-id="bd5d4-126">CreateBlob</span></span>](createblob.md)
</dt> </dl>

 

 




