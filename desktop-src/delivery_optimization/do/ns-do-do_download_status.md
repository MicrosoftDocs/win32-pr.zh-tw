---
title: DO_DOWNLOAD_STATUS 結構
description: 用來取得特定下載的狀態。
keywords:
- DO_DOWNLOAD_STATUS 結構
topic_type:
- apiref
api_name:
- DO_DOWNLOAD_STATUS
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 5e113bb4866ef1033886dbb1579d21aa296d0e5e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106968077"
---
# <a name="do_download_status-structure"></a><span data-ttu-id="ff6f6-104">DO_DOWNLOAD_STATUS 結構</span><span class="sxs-lookup"><span data-stu-id="ff6f6-104">DO_DOWNLOAD_STATUS structure</span></span>

<span data-ttu-id="ff6f6-105">**DO_DOWNLOAD_STATUS** 結構是用來取得特定下載的狀態。</span><span class="sxs-lookup"><span data-stu-id="ff6f6-105">The **DO_DOWNLOAD_STATUS** structure is used to obtain the status of a specific download.</span></span> <span data-ttu-id="ff6f6-106">它是透過呼叫 **IDODownload：： GetStatus** 函數來取得。</span><span class="sxs-lookup"><span data-stu-id="ff6f6-106">It is obtained by calling the **IDODownload::GetStatus** function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff6f6-107">語法</span><span class="sxs-lookup"><span data-stu-id="ff6f6-107">Syntax</span></span>
```cpp
typedef struct _DO_DOWNLOAD_STATUS
{
  UINT64 BytesTotal;
  UINT64 BytesTransferred;
  DODownloadState State;
  HRESULT Error;
  HRESULT ExtendedError;
} DO_DOWNLOAD_STATUS;
```

## <a name="members"></a><span data-ttu-id="ff6f6-108">成員</span><span class="sxs-lookup"><span data-stu-id="ff6f6-108">Members</span></span>

`BytesTotal`

<span data-ttu-id="ff6f6-109">要下載的總位元組數。</span><span class="sxs-lookup"><span data-stu-id="ff6f6-109">The total number of bytes to download.</span></span>

`BytesTransferred`

<span data-ttu-id="ff6f6-110">已下載的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="ff6f6-110">The number of bytes that have already been downloaded.</span></span>

`State`

<span data-ttu-id="ff6f6-111">**DODownloadState** 列舉所定義的目前下載狀態。</span><span class="sxs-lookup"><span data-stu-id="ff6f6-111">The current download state as defined by the **DODownloadState** enumeration.</span></span>

`Error`

<span data-ttu-id="ff6f6-112">如果 () 存在與目前下載相關聯的錯誤資訊，則為錯誤資訊。</span><span class="sxs-lookup"><span data-stu-id="ff6f6-112">The error information (if it exists) that is associated with the current download.</span></span>

`ExtendedError`

<span data-ttu-id="ff6f6-113">擴充的錯誤資訊 (如果存在於與目前下載相關聯的) 。</span><span class="sxs-lookup"><span data-stu-id="ff6f6-113">The extended error information (if it exists) that is associated with the current download.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff6f6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff6f6-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ff6f6-115">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="ff6f6-115">**Minimum supported client**</span></span> | <span data-ttu-id="ff6f6-116">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff6f6-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="ff6f6-117">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="ff6f6-117">**Minimum supported server**</span></span> | <span data-ttu-id="ff6f6-118">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff6f6-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="ff6f6-119">**標頭**</span><span class="sxs-lookup"><span data-stu-id="ff6f6-119">**Header**</span></span> | <span data-ttu-id="ff6f6-120">Do。h</span><span class="sxs-lookup"><span data-stu-id="ff6f6-120">Do.h</span></span> |
