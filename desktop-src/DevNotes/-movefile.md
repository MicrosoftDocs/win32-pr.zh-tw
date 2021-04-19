---
description: 移動現有的檔案或目錄，包括其子系。
ms.assetid: 1c533b02-6674-4390-bc49-6420403778a8
title: _MoveFile 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _MoveFile
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 44c57d562feff62e21c4c769bfc9d6a650f4984c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993469"
---
# <a name="_movefile-function"></a><span data-ttu-id="42ead-103">\_MoveFile 函式</span><span class="sxs-lookup"><span data-stu-id="42ead-103">\_MoveFile function</span></span>

<span data-ttu-id="42ead-104">\[此函式是 **MoveFile** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="42ead-104">\[This function is a wrapper over the **MoveFile** function.</span></span> <span data-ttu-id="42ead-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="42ead-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="42ead-106">應用程式應該直接呼叫 **MoveFile** 。\]</span><span class="sxs-lookup"><span data-stu-id="42ead-106">Applications should call **MoveFile** directly.\]</span></span>

<span data-ttu-id="42ead-107">移動現有的檔案或目錄，包括其子系。</span><span class="sxs-lookup"><span data-stu-id="42ead-107">Moves an existing file or directory, including its children.</span></span> <span data-ttu-id="42ead-108">請參閱 [ **MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)</span><span class="sxs-lookup"><span data-stu-id="42ead-108">See [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)</span></span>

## <a name="syntax"></a><span data-ttu-id="42ead-109">語法</span><span class="sxs-lookup"><span data-stu-id="42ead-109">Syntax</span></span>


```C++
BOOL _MoveFile(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="42ead-110">參數</span><span class="sxs-lookup"><span data-stu-id="42ead-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42ead-111">*...*</span><span class="sxs-lookup"><span data-stu-id="42ead-111">*...*</span></span> 
<span data-ttu-id="42ead-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="42ead-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="42ead-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="42ead-113">Requirements</span></span>



| <span data-ttu-id="42ead-114">需求</span><span class="sxs-lookup"><span data-stu-id="42ead-114">Requirement</span></span> | <span data-ttu-id="42ead-115">值</span><span class="sxs-lookup"><span data-stu-id="42ead-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42ead-116">DLL</span><span class="sxs-lookup"><span data-stu-id="42ead-116">DLL</span></span><br/> | <dl> <span data-ttu-id="42ead-117"><dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42ead-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42ead-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42ead-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42ead-119">**MoveFile**</span><span class="sxs-lookup"><span data-stu-id="42ead-119">**MoveFile**</span></span>](/windows/win32/api/winbase/nf-winbase-movefile)
</dt> </dl>

 

 
