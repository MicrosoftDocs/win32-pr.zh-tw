---
description: 取得電腦名稱。
ms.assetid: 8b6fd61a-dd5a-46b8-920e-cc8a848732b6
title: _GetComputerName 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetComputerName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: a8fc124e9a5b036e1be83e49e504d2a4d42ea27a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990056"
---
# <a name="_getcomputername-function"></a><span data-ttu-id="d5c6d-103">\_GetComputerName 函式</span><span class="sxs-lookup"><span data-stu-id="d5c6d-103">\_GetComputerName function</span></span>

<span data-ttu-id="d5c6d-104">\[此函式是 **GetComputerName** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="d5c6d-104">\[This function is a wrapper over the **GetComputerName** function.</span></span> <span data-ttu-id="d5c6d-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="d5c6d-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="d5c6d-106">應用程式應該直接呼叫 **GetComputerName** 。\]</span><span class="sxs-lookup"><span data-stu-id="d5c6d-106">Applications should call **GetComputerName** directly.\]</span></span>

<span data-ttu-id="d5c6d-107">取得電腦名稱。</span><span class="sxs-lookup"><span data-stu-id="d5c6d-107">Gets the computer name.</span></span> <span data-ttu-id="d5c6d-108">請參閱 [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea)。</span><span class="sxs-lookup"><span data-stu-id="d5c6d-108">See [**GetComputerName**](/windows/win32/api/winbase/nf-winbase-getcomputernamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5c6d-109">語法</span><span class="sxs-lookup"><span data-stu-id="d5c6d-109">Syntax</span></span>


```C++
BOOL _GetComputerName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="d5c6d-110">參數</span><span class="sxs-lookup"><span data-stu-id="d5c6d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5c6d-111">*...*</span><span class="sxs-lookup"><span data-stu-id="d5c6d-111">*...*</span></span> 
<span data-ttu-id="d5c6d-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d5c6d-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d5c6d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5c6d-113">Requirements</span></span>



| <span data-ttu-id="d5c6d-114">需求</span><span class="sxs-lookup"><span data-stu-id="d5c6d-114">Requirement</span></span> | <span data-ttu-id="d5c6d-115">值</span><span class="sxs-lookup"><span data-stu-id="d5c6d-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5c6d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d5c6d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="d5c6d-117"><dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5c6d-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5c6d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5c6d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5c6d-119">**GetComputerName**</span><span class="sxs-lookup"><span data-stu-id="d5c6d-119">**GetComputerName**</span></span>](/windows/win32/api/winbase/nf-winbase-getcomputernamea)
</dt> </dl>

 

 
