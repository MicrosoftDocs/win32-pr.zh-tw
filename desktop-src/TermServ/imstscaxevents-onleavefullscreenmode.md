---
title: IMsTscAxEvents OnLeaveFullScreenMode 方法
description: 當用戶端離開全螢幕模式時呼叫。 例如，當使用者按下全螢幕模式快速鍵組合 (CTRL + ALT + BREAK) 時，就會呼叫此事件。
ms.assetid: 95c5d427-b6e2-4a42-9816-b130ab533ac0
ms.tgt_platform: multiple
keywords:
- OnLeaveFullScreenMode 方法遠端桌面服務
- OnLeaveFullScreenMode 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnLeaveFullScreenMode 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLeaveFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4ee414f2dceba35a17ff86bce03c83d75aab48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025239"
---
# <a name="imstscaxeventsonleavefullscreenmode-method"></a><span data-ttu-id="a9737-107">IMsTscAxEvents：： OnLeaveFullScreenMode 方法</span><span class="sxs-lookup"><span data-stu-id="a9737-107">IMsTscAxEvents::OnLeaveFullScreenMode method</span></span>

<span data-ttu-id="a9737-108">當用戶端離開全螢幕模式時呼叫。</span><span class="sxs-lookup"><span data-stu-id="a9737-108">Called when the client leaves full-screen mode.</span></span> <span data-ttu-id="a9737-109">例如，當使用者按下全螢幕模式 [快速鍵](terminal-services-shortcut-keys.md) 組合 (CTRL + ALT + BREAK) 時，就會呼叫此事件。</span><span class="sxs-lookup"><span data-stu-id="a9737-109">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

## <a name="syntax"></a><span data-ttu-id="a9737-110">語法</span><span class="sxs-lookup"><span data-stu-id="a9737-110">Syntax</span></span>


```C++
void OnLeaveFullScreenMode();
```



## <a name="parameters"></a><span data-ttu-id="a9737-111">參數</span><span class="sxs-lookup"><span data-stu-id="a9737-111">Parameters</span></span>

<span data-ttu-id="a9737-112">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a9737-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9737-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9737-113">Return value</span></span>

<span data-ttu-id="a9737-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a9737-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9737-115">備註</span><span class="sxs-lookup"><span data-stu-id="a9737-115">Remarks</span></span>

<span data-ttu-id="a9737-116">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="a9737-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9737-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9737-117">Requirements</span></span>



| <span data-ttu-id="a9737-118">需求</span><span class="sxs-lookup"><span data-stu-id="a9737-118">Requirement</span></span> | <span data-ttu-id="a9737-119">值</span><span class="sxs-lookup"><span data-stu-id="a9737-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9737-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9737-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a9737-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9737-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a9737-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9737-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a9737-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9737-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a9737-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a9737-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="a9737-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9737-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a9737-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a9737-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9737-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9737-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a9737-128">IID</span><span class="sxs-lookup"><span data-stu-id="a9737-128">IID</span></span><br/>                      | <span data-ttu-id="a9737-129">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="a9737-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a9737-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9737-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9737-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="a9737-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





