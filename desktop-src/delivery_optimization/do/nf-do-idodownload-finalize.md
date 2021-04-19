---
title: IDODownload：： Finalize 方法
description: 完成下載。
keywords:
- IDODownload：： Finalize 方法
topic_type:
- apiref
api_name:
- IDODownload.Finalize
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 6befc9a7e64fb0963d45257d68d6bb8d2ba7a2cb
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "107001273"
---
# <a name="idodownloadfinalize-method"></a><span data-ttu-id="d6590-104">IDODownload：： Finalize 方法</span><span class="sxs-lookup"><span data-stu-id="d6590-104">IDODownload::Finalize method</span></span>

<span data-ttu-id="d6590-105">完成下載。</span><span class="sxs-lookup"><span data-stu-id="d6590-105">Finalizes the download.</span></span> <span data-ttu-id="d6590-106">完成之後，就無法藉由呼叫 **Start** 來繼續進行下載。</span><span class="sxs-lookup"><span data-stu-id="d6590-106">Once finalized, a download cannot be resumed by calling **Start**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6590-107">語法</span><span class="sxs-lookup"><span data-stu-id="d6590-107">Syntax</span></span>

```cpp
HRESULT Finalize();
```

## <a name="return-value"></a><span data-ttu-id="d6590-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="d6590-108">Return Value</span></span>

<span data-ttu-id="d6590-109">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="d6590-109">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="d6590-110">否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。</span><span class="sxs-lookup"><span data-stu-id="d6590-110">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="d6590-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d6590-111">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d6590-112">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="d6590-112">**Minimum supported client**</span></span> | <span data-ttu-id="d6590-113">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6590-113">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d6590-114">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="d6590-114">**Minimum supported server**</span></span> | <span data-ttu-id="d6590-115">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d6590-115">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d6590-116">**標頭**</span><span class="sxs-lookup"><span data-stu-id="d6590-116">**Header**</span></span> | <span data-ttu-id="d6590-117">Do。h</span><span class="sxs-lookup"><span data-stu-id="d6590-117">Do.h</span></span> |
