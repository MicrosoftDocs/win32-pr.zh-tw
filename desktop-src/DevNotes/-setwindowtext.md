---
description: 變更指定之視窗標題列 (的文字（如果有一個) ）。
ms.assetid: 0da53972-8f2e-4ca5-92f8-97eb88514e35
title: _SetWindowText 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetWindowText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 8832f8ee08877edae695a858874c3a2f87a2c286
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999686"
---
# <a name="_setwindowtext-function"></a><span data-ttu-id="0ed0c-103">\_SetWindowText 函式</span><span class="sxs-lookup"><span data-stu-id="0ed0c-103">\_SetWindowText function</span></span>

<span data-ttu-id="0ed0c-104">\[此函式是 **SetWindowText** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="0ed0c-104">\[This function is a wrapper over the **SetWindowText** function.</span></span> <span data-ttu-id="0ed0c-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="0ed0c-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="0ed0c-106">應用程式應該直接呼叫 **SetWindowText** 。\]</span><span class="sxs-lookup"><span data-stu-id="0ed0c-106">Applications should call **SetWindowText** directly.\]</span></span>

<span data-ttu-id="0ed0c-107">變更指定之視窗標題列 (的文字（如果有一個) ）。</span><span class="sxs-lookup"><span data-stu-id="0ed0c-107">Changes the text of the specified window's title bar (if it has one).</span></span> <span data-ttu-id="0ed0c-108">請參閱 [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)。</span><span class="sxs-lookup"><span data-stu-id="0ed0c-108">See [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed0c-109">語法</span><span class="sxs-lookup"><span data-stu-id="0ed0c-109">Syntax</span></span>


```C++
BOOL _SetWindowText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="0ed0c-110">參數</span><span class="sxs-lookup"><span data-stu-id="0ed0c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ed0c-111">*...*</span><span class="sxs-lookup"><span data-stu-id="0ed0c-111">*...*</span></span> 
<span data-ttu-id="0ed0c-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0ed0c-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0ed0c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ed0c-113">Requirements</span></span>



| <span data-ttu-id="0ed0c-114">需求</span><span class="sxs-lookup"><span data-stu-id="0ed0c-114">Requirement</span></span> | <span data-ttu-id="0ed0c-115">值</span><span class="sxs-lookup"><span data-stu-id="0ed0c-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed0c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="0ed0c-116">DLL</span></span><br/> | <dl> <span data-ttu-id="0ed0c-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ed0c-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ed0c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ed0c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed0c-119">**SetWindowText**</span><span class="sxs-lookup"><span data-stu-id="0ed0c-119">**SetWindowText**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowtexta)
</dt> </dl>

 

 
