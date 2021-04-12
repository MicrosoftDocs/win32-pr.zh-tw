---
title: IDOManager：： CreateDownload 方法
description: 建立新的下載。
keywords:
- IDOManager：： CreateDownload 方法
topic_type:
- apiref
api_name:
- IDOManager.CreateDownload
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: b79bf0a1c5602fafea113585dfe6e8ca5b01057c
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104374019"
---
# <a name="idomanagercreatedownload-method"></a><span data-ttu-id="4d5c4-104">IDOManager：： CreateDownload 方法</span><span class="sxs-lookup"><span data-stu-id="4d5c4-104">IDOManager::CreateDownload method</span></span>

<span data-ttu-id="4d5c4-105">建立新的下載。</span><span class="sxs-lookup"><span data-stu-id="4d5c4-105">Creates a new download.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d5c4-106">語法</span><span class="sxs-lookup"><span data-stu-id="4d5c4-106">Syntax</span></span>

```cpp
HRESULT CreateDownload(
  IDODownload **download
);
```

## <a name="parameters"></a><span data-ttu-id="4d5c4-107">參數</span><span class="sxs-lookup"><span data-stu-id="4d5c4-107">Parameters</span></span>

`download`

<span data-ttu-id="4d5c4-108">**IDODownload** 介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="4d5c4-108">The address of an **IDODownload** interface pointer.</span></span>

## <a name="return-value"></a><span data-ttu-id="4d5c4-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d5c4-109">Return Value</span></span>

<span data-ttu-id="4d5c4-110">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="4d5c4-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="4d5c4-111">否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。</span><span class="sxs-lookup"><span data-stu-id="4d5c4-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="4d5c4-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d5c4-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4d5c4-113">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="4d5c4-113">**Minimum supported client**</span></span> | <span data-ttu-id="4d5c4-114">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d5c4-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="4d5c4-115">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="4d5c4-115">**Minimum supported server**</span></span> | <span data-ttu-id="4d5c4-116">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d5c4-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="4d5c4-117">**標頭**</span><span class="sxs-lookup"><span data-stu-id="4d5c4-117">**Header**</span></span> | <span data-ttu-id="4d5c4-118">Do。h</span><span class="sxs-lookup"><span data-stu-id="4d5c4-118">Do.h</span></span> |
