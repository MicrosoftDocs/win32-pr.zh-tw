---
title: IDODownload：:P ause 方法
description: 暫停下載。
keywords:
- IDODownload：:P ause 方法
topic_type:
- apiref
api_name:
- IDODownload.Pause
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a7239253238b0d9b7e606329b10f05b3645b7e16
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104092479"
---
# <a name="idodownloadpause-method"></a><span data-ttu-id="4827b-104">IDODownload：:P ause 方法</span><span class="sxs-lookup"><span data-stu-id="4827b-104">IDODownload::Pause method</span></span>

<span data-ttu-id="4827b-105">暫停下載。</span><span class="sxs-lookup"><span data-stu-id="4827b-105">Pauses the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="4827b-106">語法</span><span class="sxs-lookup"><span data-stu-id="4827b-106">Syntax</span></span>

```cpp
HRESULT Pause();
```

## <a name="return-value"></a><span data-ttu-id="4827b-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="4827b-107">Return Value</span></span>

<span data-ttu-id="4827b-108">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="4827b-108">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="4827b-109">否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。</span><span class="sxs-lookup"><span data-stu-id="4827b-109">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="4827b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="4827b-110">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="4827b-111">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="4827b-111">**Minimum supported client**</span></span> | <span data-ttu-id="4827b-112">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4827b-112">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="4827b-113">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="4827b-113">**Minimum supported server**</span></span> | <span data-ttu-id="4827b-114">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4827b-114">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="4827b-115">**標頭**</span><span class="sxs-lookup"><span data-stu-id="4827b-115">**Header**</span></span> | <span data-ttu-id="4827b-116">Do。h</span><span class="sxs-lookup"><span data-stu-id="4827b-116">Do.h</span></span> |
