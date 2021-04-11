---
title: IMsRdpClientNonScriptable7 DisableDpiCursorScalingForProcess 方法
description: 停用從伺服器收到的滑鼠游標區域調整，以確保正確轉譯資料指標圖形，而不進行修改。
ms.tgt_platform: multiple
keywords:
- DisableDpiCursorScalingForProcess 方法遠端桌面服務
- DisableDpiCursorScalingForProcess 方法遠端桌面服務，IMsRdpClientNonScriptable7 介面
- IMsRdpClientNonScriptable7 介面遠端桌面服務，DisableDpiCursorScalingForProcess 方法
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.DisableDpiCursorScalingForProcess
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: a0de989fb0b1c3c644c73f214d368f2cab2ba5d5
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104317539"
---
# <a name="imsrdpclientnonscriptable7disabledpicursorscalingforprocess-method"></a><span data-ttu-id="84980-106">IMsRdpClientNonScriptable7：:D isableDpiCursorScalingForProcess 方法</span><span class="sxs-lookup"><span data-stu-id="84980-106">IMsRdpClientNonScriptable7::DisableDpiCursorScalingForProcess method</span></span>

<span data-ttu-id="84980-107">停用從伺服器收到的滑鼠游標區域調整，以確保正確轉譯資料指標圖形，而不進行修改。</span><span class="sxs-lookup"><span data-stu-id="84980-107">Disables local scaling of the mouse cursor received from the server, ensuring that the cursor shape is rendered correctly without modification.</span></span>

## <a name="syntax"></a><span data-ttu-id="84980-108">語法</span><span class="sxs-lookup"><span data-stu-id="84980-108">Syntax</span></span>

```C++
HRESULT DisableDpiCursorScalingForProcess();
```

## <a name="parameters"></a><span data-ttu-id="84980-109">參數</span><span class="sxs-lookup"><span data-stu-id="84980-109">Parameters</span></span>

<span data-ttu-id="84980-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="84980-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="84980-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="84980-111">Return value</span></span>

<span data-ttu-id="84980-112">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="84980-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="84980-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="84980-113">Requirements</span></span>

| <span data-ttu-id="84980-114">需求</span><span class="sxs-lookup"><span data-stu-id="84980-114">Requirement</span></span> | <span data-ttu-id="84980-115">值</span><span class="sxs-lookup"><span data-stu-id="84980-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="84980-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84980-116">Minimum supported client</span></span>| <span data-ttu-id="84980-117">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="84980-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="84980-118">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="84980-118">Type library</span></span>            | <span data-ttu-id="84980-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="84980-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="84980-120">DLL</span><span class="sxs-lookup"><span data-stu-id="84980-120">DLL</span></span>                  | <span data-ttu-id="84980-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="84980-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="84980-122">IID</span><span class="sxs-lookup"><span data-stu-id="84980-122">IID</span></span>                      | <span data-ttu-id="84980-123">IID \_ IMsRdpClientNonScriptable7 定義為71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="84980-123">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="84980-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="84980-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84980-125">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="84980-125">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>
