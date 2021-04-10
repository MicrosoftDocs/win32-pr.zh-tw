---
description: 從字串建立索引鍵。
ms.assetid: 107138b9-96f0-4144-a4bc-7115b6deab60
title: SdbMakeIndexKeyFromString 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbMakeIndexKeyFromString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 691e691f14692775f0c681a7efa3ce91f756be1d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936027"
---
# <a name="sdbmakeindexkeyfromstring-function"></a><span data-ttu-id="0223c-103">SdbMakeIndexKeyFromString 函式</span><span class="sxs-lookup"><span data-stu-id="0223c-103">SdbMakeIndexKeyFromString function</span></span>

<span data-ttu-id="0223c-104">從字串建立索引鍵。</span><span class="sxs-lookup"><span data-stu-id="0223c-104">Creates a key from a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="0223c-105">語法</span><span class="sxs-lookup"><span data-stu-id="0223c-105">Syntax</span></span>


```C++
ULONGLONG WINAPI SdbMakeIndexKeyFromString(
  _In_ LPCTSTR pwszKey
);
```



## <a name="parameters"></a><span data-ttu-id="0223c-106">參數</span><span class="sxs-lookup"><span data-stu-id="0223c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0223c-107">*pwszKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0223c-107">*pwszKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0223c-108">字串。</span><span class="sxs-lookup"><span data-stu-id="0223c-108">The string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0223c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0223c-109">Return value</span></span>

<span data-ttu-id="0223c-110">如果發生錯誤，函式會傳回索引鍵或0。</span><span class="sxs-lookup"><span data-stu-id="0223c-110">The function returns the key or 0 if there is an error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0223c-111">備註</span><span class="sxs-lookup"><span data-stu-id="0223c-111">Remarks</span></span>

<span data-ttu-id="0223c-112">標準索引鍵是字串的前八個字元，轉換成大寫，然後轉換成 **ULONGLONG** 值。</span><span class="sxs-lookup"><span data-stu-id="0223c-112">The standard index key is the first eight characters of the string, converted to upper case, then cast to a **ULONGLONG** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0223c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0223c-113">Requirements</span></span>



| <span data-ttu-id="0223c-114">需求</span><span class="sxs-lookup"><span data-stu-id="0223c-114">Requirement</span></span> | <span data-ttu-id="0223c-115">值</span><span class="sxs-lookup"><span data-stu-id="0223c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0223c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0223c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0223c-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0223c-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0223c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0223c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0223c-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0223c-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0223c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="0223c-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0223c-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0223c-121"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




