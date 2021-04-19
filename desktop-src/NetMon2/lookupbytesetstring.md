---
description: LookupByteSetString 函式會傳回對應至已加上標籤集合之指定值的字串。
ms.assetid: 295891f9-dc8d-4dbe-aac9-7d0a96993cfa
title: 'LookupByteSetString 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LookupByteSetString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 7a2b5bffbfcb30ed8ec00da42fbc9ad6008fd5ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970201"
---
# <a name="lookupbytesetstring-function"></a><span data-ttu-id="130aa-103">LookupByteSetString 函式</span><span class="sxs-lookup"><span data-stu-id="130aa-103">LookupByteSetString function</span></span>

<span data-ttu-id="130aa-104">**LookupByteSetString** 函式會傳回對應至已加上標籤集合之指定值的字串。</span><span class="sxs-lookup"><span data-stu-id="130aa-104">The **LookupByteSetString** function returns the string corresponding to the specified value of a labeled set.</span></span>

## <a name="syntax"></a><span data-ttu-id="130aa-105">語法</span><span class="sxs-lookup"><span data-stu-id="130aa-105">Syntax</span></span>


```C++
LPBYTE WINAPI LookupByteSetString(
   LPSET lpSet,
   BYTE  Value
);
```



## <a name="parameters"></a><span data-ttu-id="130aa-106">參數</span><span class="sxs-lookup"><span data-stu-id="130aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="130aa-107">*lpSet*</span><span class="sxs-lookup"><span data-stu-id="130aa-107">*lpSet*</span></span> 
</dt> <dd>

<span data-ttu-id="130aa-108">標記集合的指標，您可以從中解壓縮值的標籤。</span><span class="sxs-lookup"><span data-stu-id="130aa-108">Pointer to a labeled set, from which you can extract the value's label.</span></span>

</dd> <dt>

<span data-ttu-id="130aa-109">*值*</span><span class="sxs-lookup"><span data-stu-id="130aa-109">*Value*</span></span> 
</dt> <dd>

<span data-ttu-id="130aa-110">已加上標籤之集合的值。</span><span class="sxs-lookup"><span data-stu-id="130aa-110">Value of a labeled set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="130aa-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="130aa-111">Return value</span></span>

<span data-ttu-id="130aa-112">如果函式成功，則傳回值會是對應于所提供之值的字串。</span><span class="sxs-lookup"><span data-stu-id="130aa-112">If the function is successful, the return value is a string corresponding to the value provided.</span></span>

<span data-ttu-id="130aa-113">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="130aa-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="130aa-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="130aa-114">Requirements</span></span>



| <span data-ttu-id="130aa-115">需求</span><span class="sxs-lookup"><span data-stu-id="130aa-115">Requirement</span></span> | <span data-ttu-id="130aa-116">值</span><span class="sxs-lookup"><span data-stu-id="130aa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="130aa-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="130aa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="130aa-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="130aa-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="130aa-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="130aa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="130aa-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="130aa-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="130aa-121">標頭</span><span class="sxs-lookup"><span data-stu-id="130aa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="130aa-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="130aa-122"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="130aa-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="130aa-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="130aa-124"><dt>剖析器 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="130aa-124"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="130aa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="130aa-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="130aa-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="130aa-126"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




