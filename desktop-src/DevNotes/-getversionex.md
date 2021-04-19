---
description: 取得作業系統版本的相關資訊。
ms.assetid: 1af2c320-6e0b-4692-858b-a2c921ed7ce7
title: _GetVersionEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _GetVersionEx
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: dd4b33bee4a5f1c2a72ef7494176fe2979b4a7cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993982"
---
# <a name="_getversionex-function"></a><span data-ttu-id="bd507-103">\_GetVersionEx 函數</span><span class="sxs-lookup"><span data-stu-id="bd507-103">\_GetVersionEx function</span></span>

<span data-ttu-id="bd507-104">\[此函式是透過 **GetVersionEx** 函式的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="bd507-104">\[This function is a wrapper over the **GetVersionEx** function.</span></span> <span data-ttu-id="bd507-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="bd507-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="bd507-106">應用程式應該直接呼叫 **GetVersionEx** 。\]</span><span class="sxs-lookup"><span data-stu-id="bd507-106">Applications should call **GetVersionEx** directly.\]</span></span>

<span data-ttu-id="bd507-107">取得作業系統版本的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bd507-107">Gets information about the operating system version.</span></span> <span data-ttu-id="bd507-108">請參閱 [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)。</span><span class="sxs-lookup"><span data-stu-id="bd507-108">See [**GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="bd507-109">語法</span><span class="sxs-lookup"><span data-stu-id="bd507-109">Syntax</span></span>


```C++
BOOL _GetVersionEx(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="bd507-110">參數</span><span class="sxs-lookup"><span data-stu-id="bd507-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd507-111">*...*</span><span class="sxs-lookup"><span data-stu-id="bd507-111">*...*</span></span> 
<span data-ttu-id="bd507-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bd507-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="bd507-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd507-113">Requirements</span></span>



| <span data-ttu-id="bd507-114">需求</span><span class="sxs-lookup"><span data-stu-id="bd507-114">Requirement</span></span> | <span data-ttu-id="bd507-115">值</span><span class="sxs-lookup"><span data-stu-id="bd507-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd507-116">DLL</span><span class="sxs-lookup"><span data-stu-id="bd507-116">DLL</span></span><br/> | <dl> <span data-ttu-id="bd507-117"><dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd507-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd507-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd507-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd507-119">**GetVersionEx**</span><span class="sxs-lookup"><span data-stu-id="bd507-119">**GetVersionEx**</span></span>](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa)
</dt> </dl>

 

 
