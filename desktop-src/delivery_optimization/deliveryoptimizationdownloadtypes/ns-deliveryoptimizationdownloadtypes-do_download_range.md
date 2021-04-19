---
title: DO_DOWNLOAD_RANGE 結構
description: 識別要從檔案下載的單一位元組範圍。
keywords:
- DO_DOWNLOAD_RANGE 結構
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_RANGE
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0f328565c80350a05cbfb23f178ea3580586f326
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106968079"
---
# <a name="do_download_range-structure"></a><span data-ttu-id="cd514-104">DO_DOWNLOAD_RANGE 結構</span><span class="sxs-lookup"><span data-stu-id="cd514-104">DO_DOWNLOAD_RANGE structure</span></span>

<span data-ttu-id="cd514-105">**DO_DOWNLOAD_RANGE** 結構會識別要從檔案下載的單一位元組範圍。</span><span class="sxs-lookup"><span data-stu-id="cd514-105">The **DO_DOWNLOAD_RANGE** structure identifies a single range of bytes to download from a file.</span></span> <span data-ttu-id="cd514-106">**DO_DOWNLOAD_RANGE** 結構包含在 **DO_DOWNLOAD_RANGES_INFO** 結構內，以提供要下載的範圍陣列。</span><span class="sxs-lookup"><span data-stu-id="cd514-106">The **DO_DOWNLOAD_RANGE** structure is included within **DO_DOWNLOAD_RANGES_INFO** structure to provide an array of ranges to download.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd514-107">語法</span><span class="sxs-lookup"><span data-stu-id="cd514-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_RANGE
{
  UINT64 Offset;
  UINT64 Length;
} DO_DOWNLOAD_RANGE;
```

## <a name="members"></a><span data-ttu-id="cd514-108">成員</span><span class="sxs-lookup"><span data-stu-id="cd514-108">Members</span></span>

`Offset`

<span data-ttu-id="cd514-109">從檔案下載的位元組範圍開頭以零為基底的位移。</span><span class="sxs-lookup"><span data-stu-id="cd514-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

`Length`

<span data-ttu-id="cd514-110">範圍的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="cd514-110">The length of the range, in bytes.</span></span> <span data-ttu-id="cd514-111">請勿指定零位元組長度。</span><span class="sxs-lookup"><span data-stu-id="cd514-111">Do not specify a zero-byte length.</span></span> <span data-ttu-id="cd514-112">若要指出範圍延伸至檔案結尾，請指定 **DO_LENGTH_TO_EOF**。</span><span class="sxs-lookup"><span data-stu-id="cd514-112">To indicate that the range extends to the end of the file, specify **DO_LENGTH_TO_EOF**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd514-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd514-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cd514-114">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="cd514-114">**Minimum supported client**</span></span> | <span data-ttu-id="cd514-115">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd514-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="cd514-116">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="cd514-116">**Minimum supported server**</span></span> | <span data-ttu-id="cd514-117">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd514-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="cd514-118">**標頭**</span><span class="sxs-lookup"><span data-stu-id="cd514-118">**Header**</span></span> | <span data-ttu-id="cd514-119">DeliveryOptimizationDownloadTypes。h</span><span class="sxs-lookup"><span data-stu-id="cd514-119">DeliveryOptimizationDownloadTypes.h</span></span> |
