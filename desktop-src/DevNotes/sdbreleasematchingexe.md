---
description: 釋放 SdbGetMatchingExe 函式所使用的資源。
ms.assetid: 4a784f72-2108-4d5e-86e1-1960ac921c8f
title: SdbReleaseMatchingExe 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbReleaseMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: c98d9a79e8942f4bd3ea4c41119825d862de1418
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025875"
---
# <a name="sdbreleasematchingexe-function"></a><span data-ttu-id="90a46-103">SdbReleaseMatchingExe 函式</span><span class="sxs-lookup"><span data-stu-id="90a46-103">SdbReleaseMatchingExe function</span></span>

<span data-ttu-id="90a46-104">釋放 [**SdbGetMatchingExe**](sdbgetmatchingexe.md) 函式所使用的資源。</span><span class="sxs-lookup"><span data-stu-id="90a46-104">Releases resources used by the [**SdbGetMatchingExe**](sdbgetmatchingexe.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="90a46-105">語法</span><span class="sxs-lookup"><span data-stu-id="90a46-105">Syntax</span></span>


```C++
void WINAPI SdbReleaseMatchingExe(
  _In_ HSDB   hSDB,
  _In_ TAGREF trExe
);
```



## <a name="parameters"></a><span data-ttu-id="90a46-106">參數</span><span class="sxs-lookup"><span data-stu-id="90a46-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90a46-107">*hSDB* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90a46-107">*hSDB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90a46-108">[**SdbInitDatabase**](sdbinitdatabase.md)函式所傳回之填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="90a46-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="90a46-109">*trExe* \[在\]</span><span class="sxs-lookup"><span data-stu-id="90a46-109">*trExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="90a46-110">[**SdbGetMatchingExe**](sdbgetmatchingexe.md)傳回的 [**TAGREF**](tagref.md) 。</span><span class="sxs-lookup"><span data-stu-id="90a46-110">The [**TAGREF**](tagref.md) returned by [**SdbGetMatchingExe**](sdbgetmatchingexe.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90a46-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="90a46-111">Return value</span></span>

<span data-ttu-id="90a46-112">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="90a46-112">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="90a46-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="90a46-113">Requirements</span></span>



| <span data-ttu-id="90a46-114">需求</span><span class="sxs-lookup"><span data-stu-id="90a46-114">Requirement</span></span> | <span data-ttu-id="90a46-115">值</span><span class="sxs-lookup"><span data-stu-id="90a46-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90a46-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="90a46-116">Minimum supported client</span></span><br/> | <span data-ttu-id="90a46-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90a46-117">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="90a46-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="90a46-118">Minimum supported server</span></span><br/> | <span data-ttu-id="90a46-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="90a46-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="90a46-120">DLL</span><span class="sxs-lookup"><span data-stu-id="90a46-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="90a46-121"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="90a46-121"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90a46-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="90a46-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90a46-123">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="90a46-123">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> <dt>

[<span data-ttu-id="90a46-124">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="90a46-124">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> </dl>

 

 




