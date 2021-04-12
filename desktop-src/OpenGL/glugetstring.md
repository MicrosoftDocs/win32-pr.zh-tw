---
title: 'gluGetString 函式 (X.glu 隊) '
description: GluGetString 函式會取得描述 X.GLU 隊版本號碼或支援之 X.GLU 隊延伸模組呼叫的字串。
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- gluGetString 函式 OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384461"
---
# <a name="glugetstring-function"></a><span data-ttu-id="07f0f-104">gluGetString 函式</span><span class="sxs-lookup"><span data-stu-id="07f0f-104">gluGetString function</span></span>

<span data-ttu-id="07f0f-105">**GluGetString** 函式會取得描述 x.glu 隊版本號碼或支援之 x.glu 隊延伸模組呼叫的字串。</span><span class="sxs-lookup"><span data-stu-id="07f0f-105">The **gluGetString** function gets a string that describes the GLU version number or supported GLU extension calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="07f0f-106">語法</span><span class="sxs-lookup"><span data-stu-id="07f0f-106">Syntax</span></span>


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="07f0f-107">參數</span><span class="sxs-lookup"><span data-stu-id="07f0f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07f0f-108">*name*</span><span class="sxs-lookup"><span data-stu-id="07f0f-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="07f0f-109">X.GLU 隊 (X.GLU 隊版本的版本號碼 \_) 或可用的廠商專屬延伸模組呼叫 (X.glu 隊 \_ 延伸模組) 。</span><span class="sxs-lookup"><span data-stu-id="07f0f-109">Either the version number of GLU (GLU\_VERSION) or available vendor-specific extension calls (GLU\_EXTENSIONS).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07f0f-110">備註</span><span class="sxs-lookup"><span data-stu-id="07f0f-110">Remarks</span></span>

<span data-ttu-id="07f0f-111">**GluGetString** 函式會傳回靜態、以 null 終止之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="07f0f-111">The **gluGetString** function returns a pointer to a static, null-terminated string.</span></span> <span data-ttu-id="07f0f-112">當 *name* 為 x.glu 隊 \_ 版本時，傳回的字串是代表 x.glu 隊版本號碼的值。</span><span class="sxs-lookup"><span data-stu-id="07f0f-112">When *name* is GLU\_VERSION, the returned string is a value that represents the version number of GLU.</span></span> <span data-ttu-id="07f0f-113">版本號碼的格式如下所示：</span><span class="sxs-lookup"><span data-stu-id="07f0f-113">The format of the version number is as follows:</span></span>

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

<span data-ttu-id="07f0f-114">版本號碼的格式為「主要 \_ 號碼. 次要 \_ 號碼」或「主要號碼號碼。 \_ \_ 發行號碼」 \_ 。</span><span class="sxs-lookup"><span data-stu-id="07f0f-114">The version number has the form "major\_number.minor\_number" or "major\_number.minor\_number.release\_number".</span></span> <span data-ttu-id="07f0f-115">廠商專屬的資訊是選擇性的，且格式和內容取決於執行。</span><span class="sxs-lookup"><span data-stu-id="07f0f-115">The vendor-specific information is optional, and the format and contents depend on the implementation.</span></span>

<span data-ttu-id="07f0f-116">當 *name* 為 x.glu 隊 \_ EXTENSIONS 時，傳回的字串會包含以空格分隔的支援 x.glu 隊延伸模組名稱清單。</span><span class="sxs-lookup"><span data-stu-id="07f0f-116">When *name* is GLU\_EXTENSIONS, the returned string contains a list of names of supported GLU extensions that are separated by spaces.</span></span> <span data-ttu-id="07f0f-117">傳回之名稱清單的格式如下所示：</span><span class="sxs-lookup"><span data-stu-id="07f0f-117">The format of the returned list of names is as follows:</span></span>

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

<span data-ttu-id="07f0f-118">延伸模組名稱不能包含任何空格。</span><span class="sxs-lookup"><span data-stu-id="07f0f-118">The extension names cannot contain any spaces.</span></span>

<span data-ttu-id="07f0f-119">**GluGetString** 函數適用于 x.glu 隊1.1 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="07f0f-119">The **gluGetString** function is valid for GLU version 1.1 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="07f0f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="07f0f-120">Requirements</span></span>



| <span data-ttu-id="07f0f-121">需求</span><span class="sxs-lookup"><span data-stu-id="07f0f-121">Requirement</span></span> | <span data-ttu-id="07f0f-122">值</span><span class="sxs-lookup"><span data-stu-id="07f0f-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="07f0f-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07f0f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="07f0f-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07f0f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="07f0f-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07f0f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="07f0f-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07f0f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="07f0f-127">標頭</span><span class="sxs-lookup"><span data-stu-id="07f0f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="07f0f-128"><dt>X.glu 隊。h</dt></span><span class="sxs-lookup"><span data-stu-id="07f0f-128"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="07f0f-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="07f0f-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="07f0f-130"><dt>Glu32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="07f0f-130"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="07f0f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="07f0f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07f0f-132"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07f0f-132"><dt>Glu32.dll</dt></span></span> </dl> |



 

 





