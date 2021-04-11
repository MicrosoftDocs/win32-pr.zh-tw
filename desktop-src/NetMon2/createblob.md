---
description: CreateBlob 函式會建立空的 BLOB。
ms.assetid: fa31855b-af85-4ab5-b434-e54111731d8f
title: 'CreateBlob 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: f2abb32afd68dd321a520c1d56c217e801fa9101
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693232"
---
# <a name="createblob-function"></a><span data-ttu-id="9d83a-103">CreateBlob 函式</span><span class="sxs-lookup"><span data-stu-id="9d83a-103">CreateBlob function</span></span>

<span data-ttu-id="9d83a-104">**CreateBlob** 函式會建立空的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="9d83a-104">The **CreateBlob** function creates an empty BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d83a-105">語法</span><span class="sxs-lookup"><span data-stu-id="9d83a-105">Syntax</span></span>


```C++
DWORD CreateBlob(
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="9d83a-106">參數</span><span class="sxs-lookup"><span data-stu-id="9d83a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d83a-107">*phBlob* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9d83a-107">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d83a-108">傳回新 BLOB 指標的變數指標。</span><span class="sxs-lookup"><span data-stu-id="9d83a-108">Pointer to the variable where the pointer to the new BLOB is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d83a-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d83a-109">Return value</span></span>

<span data-ttu-id="9d83a-110">如果函式成功，則傳回值為 NMERR \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="9d83a-110">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="9d83a-111">如果函式不成功，則傳回值為描述錯誤的 NMERR 值。</span><span class="sxs-lookup"><span data-stu-id="9d83a-111">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d83a-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d83a-112">Requirements</span></span>



| <span data-ttu-id="9d83a-113">需求</span><span class="sxs-lookup"><span data-stu-id="9d83a-113">Requirement</span></span> | <span data-ttu-id="9d83a-114">值</span><span class="sxs-lookup"><span data-stu-id="9d83a-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d83a-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d83a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9d83a-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d83a-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="9d83a-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d83a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9d83a-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d83a-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d83a-119">標頭</span><span class="sxs-lookup"><span data-stu-id="9d83a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d83a-120"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="9d83a-120"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="9d83a-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="9d83a-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="9d83a-122"><dt>Npptools .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d83a-122"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="9d83a-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9d83a-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d83a-124"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d83a-124"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d83a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d83a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d83a-126">DestroyBlob</span><span class="sxs-lookup"><span data-stu-id="9d83a-126">DestroyBlob</span></span>](destroyblob.md)
</dt> </dl>

 

 




