---
title: DO_DOWNLOAD_RANGE_INFO 結構
description: 識別要從檔案下載的位元組範圍陣列。
keywords:
- DO_DOWNLOAD_RANGE_INFO 結構
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE_INFO
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 01628ea29895012f60552e696b7f68854f426f8d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104374015"
---
# <a name="do_download_range_info-structure"></a><span data-ttu-id="8adbe-104">DO_DOWNLOAD_RANGE_INFO 結構</span><span class="sxs-lookup"><span data-stu-id="8adbe-104">DO_DOWNLOAD_RANGE_INFO structure</span></span>

<span data-ttu-id="8adbe-105">**DO_DOWNLOAD_RANGE_INFO** 結構會識別要從檔案下載的位元組範圍陣列。</span><span class="sxs-lookup"><span data-stu-id="8adbe-105">The **DO_DOWNLOAD_RANGE_INFO** structure identifies an array of ranges of bytes to download from a file.</span></span> <span data-ttu-id="8adbe-106">它通常會以選擇性引數形式傳遞至 **IDODownload：： Start** 函式。</span><span class="sxs-lookup"><span data-stu-id="8adbe-106">It is typically passed as an optional argument to the **IDODownload::Start** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="8adbe-107">語法</span><span class="sxs-lookup"><span data-stu-id="8adbe-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGES_INFO
{
  UINT RangeCount;
  [size_is(RangeCount)] DO_DOWNLOAD_RANGE Ranges[];
} DO_DOWNLOAD_RANGES_INFO;
```

## <a name="members"></a><span data-ttu-id="8adbe-108">成員</span><span class="sxs-lookup"><span data-stu-id="8adbe-108">Members</span></span>

`RangeCount`

<span data-ttu-id="8adbe-109">範圍中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="8adbe-109">Number of elements in Ranges.</span></span>

`Ranges`

<span data-ttu-id="8adbe-110">一或多個 **DO_DOWNLOAD_RANGE** 結構的陣列，指定要下載的範圍。</span><span class="sxs-lookup"><span data-stu-id="8adbe-110">Array of one or more **DO_DOWNLOAD_RANGE** structures that specify the ranges to download.</span></span>

## <a name="requirements"></a><span data-ttu-id="8adbe-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="8adbe-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="8adbe-112">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="8adbe-112">**Minimum supported client**</span></span> | <span data-ttu-id="8adbe-113">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8adbe-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="8adbe-114">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="8adbe-114">**Minimum supported server**</span></span> | <span data-ttu-id="8adbe-115">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8adbe-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="8adbe-116">**標頭**</span><span class="sxs-lookup"><span data-stu-id="8adbe-116">**Header**</span></span> | <span data-ttu-id="8adbe-117">Do。h</span><span class="sxs-lookup"><span data-stu-id="8adbe-117">Do.h</span></span> |
