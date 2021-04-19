---
description: 從指定之視窗的標題列抓取文字。
ms.assetid: c14151f9-222f-40a2-837e-7f9a728efc82
title: _GetWindowText 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 61c84c8a5f00ad97b8a76ef4139b20b74f1be085
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977634"
---
# <a name="_getwindowtext-function"></a><span data-ttu-id="eb637-103">\_GetWindowText 函式</span><span class="sxs-lookup"><span data-stu-id="eb637-103">\_GetWindowText function</span></span>

<span data-ttu-id="eb637-104">\[此函式是 **GetWindowText** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="eb637-104">\[This function is a wrapper over the **GetWindowText** function.</span></span> <span data-ttu-id="eb637-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="eb637-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="eb637-106">應用程式應該直接呼叫 **GetWindowText** 。\]</span><span class="sxs-lookup"><span data-stu-id="eb637-106">Applications should call **GetWindowText** directly.\]</span></span>

<span data-ttu-id="eb637-107">從指定之視窗的標題列抓取文字。</span><span class="sxs-lookup"><span data-stu-id="eb637-107">Retrieves the text from the specified window's title bar.</span></span> <span data-ttu-id="eb637-108">請參閱 [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)。</span><span class="sxs-lookup"><span data-stu-id="eb637-108">See [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb637-109">語法</span><span class="sxs-lookup"><span data-stu-id="eb637-109">Syntax</span></span>


```C++
int _GetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="eb637-110">參數</span><span class="sxs-lookup"><span data-stu-id="eb637-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb637-111">*...*</span><span class="sxs-lookup"><span data-stu-id="eb637-111">*...*</span></span> 
<span data-ttu-id="eb637-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="eb637-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="eb637-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb637-113">Requirements</span></span>



| <span data-ttu-id="eb637-114">需求</span><span class="sxs-lookup"><span data-stu-id="eb637-114">Requirement</span></span> | <span data-ttu-id="eb637-115">值</span><span class="sxs-lookup"><span data-stu-id="eb637-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb637-116">DLL</span><span class="sxs-lookup"><span data-stu-id="eb637-116">DLL</span></span><br/> | <dl> <span data-ttu-id="eb637-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb637-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb637-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb637-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb637-119">**GetWindowText**</span><span class="sxs-lookup"><span data-stu-id="eb637-119">**GetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> </dl>

 

 
