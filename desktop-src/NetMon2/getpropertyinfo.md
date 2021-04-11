---
description: GetPropertyInfo 函式會傳回指定之通訊協定的屬性資訊指標。
ms.assetid: f65166ba-1d94-4d65-b9d7-edb84ada0826
title: 'GetPropertyInfo 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyInfo
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 007332a85f170f865604526199681cad6d68cdcb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847735"
---
# <a name="getpropertyinfo-function"></a><span data-ttu-id="cbc67-103">GetPropertyInfo 函式</span><span class="sxs-lookup"><span data-stu-id="cbc67-103">GetPropertyInfo function</span></span>

<span data-ttu-id="cbc67-104">**GetPropertyInfo** 函式會傳回指定之通訊協定的屬性資訊指標。</span><span class="sxs-lookup"><span data-stu-id="cbc67-104">The **GetPropertyInfo** function returns a pointer to the property information of a given protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc67-105">語法</span><span class="sxs-lookup"><span data-stu-id="cbc67-105">Syntax</span></span>


```C++
LPPROPERTYINFO WINAPI GetPropertyInfo(
  _In_ HPROPERTY hProperty
);
```



## <a name="parameters"></a><span data-ttu-id="cbc67-106">參數</span><span class="sxs-lookup"><span data-stu-id="cbc67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cbc67-107">*hProperty* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cbc67-107">*hProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cbc67-108">屬性的控制碼。</span><span class="sxs-lookup"><span data-stu-id="cbc67-108">Handle to a property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cbc67-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="cbc67-109">Return value</span></span>

<span data-ttu-id="cbc67-110">如果函式成功，則傳回值為屬性的指標。</span><span class="sxs-lookup"><span data-stu-id="cbc67-110">If the function is successful, the return value is a pointer to the property.</span></span>

<span data-ttu-id="cbc67-111">如果函式不成功，則傳回值為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="cbc67-111">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="cbc67-112">備註</span><span class="sxs-lookup"><span data-stu-id="cbc67-112">Remarks</span></span>

<span data-ttu-id="cbc67-113">[*專家*](e.md) 和 [*剖析*](p.md) 器可以呼叫 **GetPropertyInfo** 函數。</span><span class="sxs-lookup"><span data-stu-id="cbc67-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetPropertyInfo** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbc67-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cbc67-114">Requirements</span></span>



| <span data-ttu-id="cbc67-115">需求</span><span class="sxs-lookup"><span data-stu-id="cbc67-115">Requirement</span></span> | <span data-ttu-id="cbc67-116">值</span><span class="sxs-lookup"><span data-stu-id="cbc67-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc67-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cbc67-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cbc67-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbc67-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="cbc67-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cbc67-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cbc67-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cbc67-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cbc67-121">標頭</span><span class="sxs-lookup"><span data-stu-id="cbc67-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cbc67-122"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="cbc67-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="cbc67-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="cbc67-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="cbc67-124"><dt>Nmapi .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cbc67-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="cbc67-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cbc67-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cbc67-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cbc67-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




