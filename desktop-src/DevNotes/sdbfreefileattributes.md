---
description: 釋出指定的檔案屬性資料。
ms.assetid: c1a4dcf8-614f-49a5-a923-8d7d610e6406
title: SdbFreeFileAttributes 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFreeFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6f28812fbbec83dd1a41c8a21cb4c9544dbefea5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688520"
---
# <a name="sdbfreefileattributes-function"></a><span data-ttu-id="5a05e-103">SdbFreeFileAttributes 函式</span><span class="sxs-lookup"><span data-stu-id="5a05e-103">SdbFreeFileAttributes function</span></span>

<span data-ttu-id="5a05e-104">釋出指定的檔案屬性資料。</span><span class="sxs-lookup"><span data-stu-id="5a05e-104">Frees the specified file attribute data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a05e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5a05e-105">Syntax</span></span>


```C++
BOOL WINAPI SdbFreeFileAttributes(
  _In_ PATTRINFO pFileAttributes
);
```



## <a name="parameters"></a><span data-ttu-id="5a05e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5a05e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a05e-107">*pFileAttributes* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5a05e-107">*pFileAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a05e-108">[**SdbGetFileAttributes**](sdbgetfileattributes.md)函數所傳回的 [**ATTRINFO**](attrinfo.md)結構。</span><span class="sxs-lookup"><span data-stu-id="5a05e-108">An [**ATTRINFO**](attrinfo.md) structure returned by the [**SdbGetFileAttributes**](sdbgetfileattributes.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a05e-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a05e-109">Return value</span></span>

<span data-ttu-id="5a05e-110">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="5a05e-110">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a05e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a05e-111">Requirements</span></span>



| <span data-ttu-id="5a05e-112">需求</span><span class="sxs-lookup"><span data-stu-id="5a05e-112">Requirement</span></span> | <span data-ttu-id="5a05e-113">值</span><span class="sxs-lookup"><span data-stu-id="5a05e-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a05e-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a05e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="5a05e-115">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a05e-115">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5a05e-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a05e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="5a05e-117">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a05e-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="5a05e-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5a05e-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a05e-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a05e-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a05e-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a05e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a05e-121">**SdbGetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="5a05e-121">**SdbGetFileAttributes**</span></span>](sdbgetfileattributes.md)
</dt> </dl>

 

 




