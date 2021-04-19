---
description: 載入程式庫。
ms.assetid: 191fcbd8-4542-4cad-955e-6951f3005fc5
title: _LoadLibrary 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _LoadLibrary
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: ce4502813c1ca2a292486a18f1946f4c605c96cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990131"
---
# <a name="_loadlibrary-function"></a><span data-ttu-id="67084-103">\_LoadLibrary 函式</span><span class="sxs-lookup"><span data-stu-id="67084-103">\_LoadLibrary function</span></span>

<span data-ttu-id="67084-104">\[此函式是 **LoadLibrary** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="67084-104">\[This function is a wrapper over the **LoadLibrary** function.</span></span> <span data-ttu-id="67084-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="67084-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="67084-106">應用程式應該直接呼叫 **LoadLibrary** 。\]</span><span class="sxs-lookup"><span data-stu-id="67084-106">Applications should call **LoadLibrary** directly.\]</span></span>

<span data-ttu-id="67084-107">載入程式庫。</span><span class="sxs-lookup"><span data-stu-id="67084-107">Loads a library.</span></span> <span data-ttu-id="67084-108">請參閱 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)。</span><span class="sxs-lookup"><span data-stu-id="67084-108">See [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

## <a name="syntax"></a><span data-ttu-id="67084-109">語法</span><span class="sxs-lookup"><span data-stu-id="67084-109">Syntax</span></span>


```C++
HMODULE _LoadLibrary(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="67084-110">參數</span><span class="sxs-lookup"><span data-stu-id="67084-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67084-111">*...*</span><span class="sxs-lookup"><span data-stu-id="67084-111">*...*</span></span> 
<span data-ttu-id="67084-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="67084-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="67084-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="67084-113">Requirements</span></span>



| <span data-ttu-id="67084-114">需求</span><span class="sxs-lookup"><span data-stu-id="67084-114">Requirement</span></span> | <span data-ttu-id="67084-115">值</span><span class="sxs-lookup"><span data-stu-id="67084-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67084-116">DLL</span><span class="sxs-lookup"><span data-stu-id="67084-116">DLL</span></span><br/> | <dl> <span data-ttu-id="67084-117"><dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67084-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67084-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="67084-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67084-119">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="67084-119">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
