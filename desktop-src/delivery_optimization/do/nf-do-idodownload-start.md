---
title: IDODownload：： Start 方法
description: 啟動或繼續進行下載。
keywords:
- IDODownload：： Start 方法
topic_type:
- apiref
api_name:
- IDODownload.Start
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d05b0660008ae65350c6331428f641bc2126c18
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106976417"
---
# <a name="idodownloadstart-method"></a><span data-ttu-id="cb262-104">IDODownload：： Start 方法</span><span class="sxs-lookup"><span data-stu-id="cb262-104">IDODownload::Start method</span></span>

<span data-ttu-id="cb262-105">啟動或繼續下載，將選擇性範圍傳遞為 [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="cb262-105">Starts or resumes a download, passing optional ranges as a pointer to [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb262-106">語法</span><span class="sxs-lookup"><span data-stu-id="cb262-106">Syntax</span></span>

```cpp
HRESULT Start(
  DO_DOWNLOAD_RANGES_INFO *ranges
);
```

## <a name="parameters"></a><span data-ttu-id="cb262-107">參數</span><span class="sxs-lookup"><span data-stu-id="cb262-107">Parameters</span></span>

`ranges`

<span data-ttu-id="cb262-108">選擇性。</span><span class="sxs-lookup"><span data-stu-id="cb262-108">Optional.</span></span> <span data-ttu-id="cb262-109">[**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md)結構的指標， (只下載檔案) 的特定範圍。</span><span class="sxs-lookup"><span data-stu-id="cb262-109">A pointer to a [**DO_DOWNLOAD_RANGES_INFO**](ns-do-do_download_range_info.md) structure (to download only specific ranges of the file).</span></span> <span data-ttu-id="cb262-110">傳遞 `nullptr` 以下載整個檔案。</span><span class="sxs-lookup"><span data-stu-id="cb262-110">Pass `nullptr` to download the entire file.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb262-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cb262-111">Return Value</span></span>

<span data-ttu-id="cb262-112">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="cb262-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="cb262-113">否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。</span><span class="sxs-lookup"><span data-stu-id="cb262-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="cb262-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cb262-114">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cb262-115">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="cb262-115">**Minimum supported client**</span></span> | <span data-ttu-id="cb262-116">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb262-116">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="cb262-117">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="cb262-117">**Minimum supported server**</span></span> | <span data-ttu-id="cb262-118">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cb262-118">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="cb262-119">**標頭**</span><span class="sxs-lookup"><span data-stu-id="cb262-119">**Header**</span></span> | <span data-ttu-id="cb262-120">Do。h</span><span class="sxs-lookup"><span data-stu-id="cb262-120">Do.h</span></span> |
