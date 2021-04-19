---
description: 從 DLL 取得函數的位址。
ms.assetid: e425948c-5588-4a4f-994c-4e608af18439
title: _GetProcAddress_ 函數
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetProcAddress_
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 0d717036b92e79056fd3b1bf69f1fd17784db713
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000948"
---
# <a name="_getprocaddress_-function"></a><span data-ttu-id="aa78d-103">\_GetProcAddress \_ 函數</span><span class="sxs-lookup"><span data-stu-id="aa78d-103">\_GetProcAddress\_ function</span></span>

<span data-ttu-id="aa78d-104">\[此函式是在 **GetProcAddress** 函數上的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="aa78d-104">\[This function is a wrapper over the **GetProcAddress** function.</span></span> <span data-ttu-id="aa78d-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="aa78d-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="aa78d-106">應用程式應該直接呼叫 **GetProcAddress** 。\]</span><span class="sxs-lookup"><span data-stu-id="aa78d-106">Applications should call **GetProcAddress** directly.\]</span></span>

<span data-ttu-id="aa78d-107">從 DLL 取得函數的位址。</span><span class="sxs-lookup"><span data-stu-id="aa78d-107">Gets the address of a function from a DLL.</span></span> <span data-ttu-id="aa78d-108">請參閱 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)。</span><span class="sxs-lookup"><span data-stu-id="aa78d-108">See [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

## <a name="syntax"></a><span data-ttu-id="aa78d-109">語法</span><span class="sxs-lookup"><span data-stu-id="aa78d-109">Syntax</span></span>


```C++
FARPROC _GetProcAddress_(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="aa78d-110">參數</span><span class="sxs-lookup"><span data-stu-id="aa78d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa78d-111">*...*</span><span class="sxs-lookup"><span data-stu-id="aa78d-111">*...*</span></span> 
<span data-ttu-id="aa78d-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="aa78d-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="aa78d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa78d-113">Requirements</span></span>



| <span data-ttu-id="aa78d-114">需求</span><span class="sxs-lookup"><span data-stu-id="aa78d-114">Requirement</span></span> | <span data-ttu-id="aa78d-115">值</span><span class="sxs-lookup"><span data-stu-id="aa78d-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa78d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="aa78d-116">DLL</span></span><br/> | <dl> <span data-ttu-id="aa78d-117"><dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa78d-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa78d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aa78d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa78d-119">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="aa78d-119">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 
