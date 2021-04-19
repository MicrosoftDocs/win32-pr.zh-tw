---
description: 取得使用者名稱。
ms.assetid: 1373fc9d-ab1c-49b9-8b82-de2e99c4821c
title: _GetUserName 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetUserName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: f61be4596c5076dd7763ed171124888382f3ef6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993256"
---
# <a name="_getusername-function"></a><span data-ttu-id="126ee-103">\_GetUserName 函式</span><span class="sxs-lookup"><span data-stu-id="126ee-103">\_GetUserName function</span></span>

<span data-ttu-id="126ee-104">\[此函式是 **GetUserName** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="126ee-104">\[This function is a wrapper over the **GetUserName** function.</span></span> <span data-ttu-id="126ee-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="126ee-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="126ee-106">應用程式應該直接呼叫 **GetUserName** 。\]</span><span class="sxs-lookup"><span data-stu-id="126ee-106">Applications should call **GetUserName** directly.\]</span></span>

<span data-ttu-id="126ee-107">取得使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="126ee-107">Gets the user name.</span></span> <span data-ttu-id="126ee-108">請參閱 [**GetUserName**](/windows/win32/api/winbase/nf-winbase-getusernamea)。</span><span class="sxs-lookup"><span data-stu-id="126ee-108">See [**GetUserName**](/windows/win32/api/winbase/nf-winbase-getusernamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="126ee-109">語法</span><span class="sxs-lookup"><span data-stu-id="126ee-109">Syntax</span></span>


```C++
BOOL _GetUserName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="126ee-110">參數</span><span class="sxs-lookup"><span data-stu-id="126ee-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="126ee-111">*...*</span><span class="sxs-lookup"><span data-stu-id="126ee-111">*...*</span></span> 
<span data-ttu-id="126ee-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="126ee-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="126ee-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="126ee-113">Requirements</span></span>



| <span data-ttu-id="126ee-114">需求</span><span class="sxs-lookup"><span data-stu-id="126ee-114">Requirement</span></span> | <span data-ttu-id="126ee-115">值</span><span class="sxs-lookup"><span data-stu-id="126ee-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="126ee-116">DLL</span><span class="sxs-lookup"><span data-stu-id="126ee-116">DLL</span></span><br/> | <dl> <span data-ttu-id="126ee-117"><dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="126ee-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="126ee-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="126ee-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="126ee-119">**GetUserName**</span><span class="sxs-lookup"><span data-stu-id="126ee-119">**GetUserName**</span></span>](/windows/win32/api/winbase/nf-winbase-getusernamea)
</dt> </dl>

 

 
