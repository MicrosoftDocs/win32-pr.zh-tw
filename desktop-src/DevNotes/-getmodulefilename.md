---
description: 取得模組路徑。
ms.assetid: ff632357-8d4a-4de4-a69a-0be9e380639d
title: _GetModuleFileName 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetModuleFileName
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 5bf18e8baac62de6474f4ce1e48a0ae115ced778
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983181"
---
# <a name="_getmodulefilename-function"></a><span data-ttu-id="0b91c-103">\_GetModuleFileName 函式</span><span class="sxs-lookup"><span data-stu-id="0b91c-103">\_GetModuleFileName function</span></span>

<span data-ttu-id="0b91c-104">\[此函式是 **GetModuleFileName** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="0b91c-104">\[This function is a wrapper over the **GetModuleFileName** function.</span></span> <span data-ttu-id="0b91c-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="0b91c-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="0b91c-106">應用程式應該直接呼叫 **GetModuleFileName** 。\]</span><span class="sxs-lookup"><span data-stu-id="0b91c-106">Applications should call **GetModuleFileName** directly.\]</span></span>

<span data-ttu-id="0b91c-107">取得模組路徑。</span><span class="sxs-lookup"><span data-stu-id="0b91c-107">Gets the module path.</span></span> <span data-ttu-id="0b91c-108">請參閱 [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)。</span><span class="sxs-lookup"><span data-stu-id="0b91c-108">See [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea).</span></span>

## <a name="syntax"></a><span data-ttu-id="0b91c-109">語法</span><span class="sxs-lookup"><span data-stu-id="0b91c-109">Syntax</span></span>


```C++
DWORD _GetModuleFileName(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="0b91c-110">參數</span><span class="sxs-lookup"><span data-stu-id="0b91c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b91c-111">*...*</span><span class="sxs-lookup"><span data-stu-id="0b91c-111">*...*</span></span> 
<span data-ttu-id="0b91c-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0b91c-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0b91c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b91c-113">Requirements</span></span>



| <span data-ttu-id="0b91c-114">需求</span><span class="sxs-lookup"><span data-stu-id="0b91c-114">Requirement</span></span> | <span data-ttu-id="0b91c-115">值</span><span class="sxs-lookup"><span data-stu-id="0b91c-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b91c-116">DLL</span><span class="sxs-lookup"><span data-stu-id="0b91c-116">DLL</span></span><br/> | <dl> <span data-ttu-id="0b91c-117"><dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b91c-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b91c-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b91c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b91c-119">**GetModuleFileName**</span><span class="sxs-lookup"><span data-stu-id="0b91c-119">**GetModuleFileName**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> </dl>

 

 
