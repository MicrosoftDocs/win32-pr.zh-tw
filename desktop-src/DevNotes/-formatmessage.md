---
description: 格式化訊息字串。
ms.assetid: e5513b0d-5f93-4bcd-a011-eb4a6fab91e1
title: _FormatMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _FormatMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: 27cbcfb0d69d0b4dec72834bfc8f69a9f97048ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998821"
---
# <a name="_formatmessage-function"></a><span data-ttu-id="a28d3-103">\_FormatMessage 函式</span><span class="sxs-lookup"><span data-stu-id="a28d3-103">\_FormatMessage function</span></span>

<span data-ttu-id="a28d3-104">\[此函式是 **FormatMessage** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="a28d3-104">\[This function is a wrapper over the **FormatMessage** function.</span></span> <span data-ttu-id="a28d3-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="a28d3-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="a28d3-106">應用程式應該直接呼叫 **FormatMessage** 。\]</span><span class="sxs-lookup"><span data-stu-id="a28d3-106">Applications should call **FormatMessage** directly.\]</span></span>

<span data-ttu-id="a28d3-107">格式化訊息字串。</span><span class="sxs-lookup"><span data-stu-id="a28d3-107">Formats a message string.</span></span> <span data-ttu-id="a28d3-108">請參閱 [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)。</span><span class="sxs-lookup"><span data-stu-id="a28d3-108">See [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage).</span></span>

## <a name="syntax"></a><span data-ttu-id="a28d3-109">語法</span><span class="sxs-lookup"><span data-stu-id="a28d3-109">Syntax</span></span>


```C++
DWORD _FormatMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="a28d3-110">參數</span><span class="sxs-lookup"><span data-stu-id="a28d3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a28d3-111">*...*</span><span class="sxs-lookup"><span data-stu-id="a28d3-111">*...*</span></span> 
<span data-ttu-id="a28d3-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a28d3-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a28d3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a28d3-113">Requirements</span></span>



| <span data-ttu-id="a28d3-114">需求</span><span class="sxs-lookup"><span data-stu-id="a28d3-114">Requirement</span></span> | <span data-ttu-id="a28d3-115">值</span><span class="sxs-lookup"><span data-stu-id="a28d3-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a28d3-116">DLL</span><span class="sxs-lookup"><span data-stu-id="a28d3-116">DLL</span></span><br/> | <dl> <span data-ttu-id="a28d3-117"><dt>Msmdun80.dll;</dt><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a28d3-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a28d3-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a28d3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a28d3-119">**FormatMessage**</span><span class="sxs-lookup"><span data-stu-id="a28d3-119">**FormatMessage**</span></span>](/windows/win32/api/winbase/nf-winbase-formatmessage)
</dt> </dl>

 

 
