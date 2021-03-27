---
description: 接收 IShellWindows 視窗註冊事件。
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: 'DShellWindowsEvents 物件 (Exdisp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974880"
---
# <a name="dshellwindowsevents-object"></a><span data-ttu-id="11f65-103">DShellWindowsEvents 物件</span><span class="sxs-lookup"><span data-stu-id="11f65-103">DShellWindowsEvents object</span></span>

<span data-ttu-id="11f65-104">接收 [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) 視窗註冊事件。</span><span class="sxs-lookup"><span data-stu-id="11f65-104">Receives [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) window registration events.</span></span>

## <a name="members"></a><span data-ttu-id="11f65-105">成員</span><span class="sxs-lookup"><span data-stu-id="11f65-105">Members</span></span>

<span data-ttu-id="11f65-106">**DShellWindowsEvents** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="11f65-106">The **DShellWindowsEvents** object has these types of members:</span></span>

-   [<span data-ttu-id="11f65-107">方法</span><span class="sxs-lookup"><span data-stu-id="11f65-107">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="11f65-108">方法</span><span class="sxs-lookup"><span data-stu-id="11f65-108">Methods</span></span>

<span data-ttu-id="11f65-109">**DShellWindowsEvents** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="11f65-109">The **DShellWindowsEvents** object has these methods.</span></span>



| <span data-ttu-id="11f65-110">方法</span><span class="sxs-lookup"><span data-stu-id="11f65-110">Method</span></span>                                                           | <span data-ttu-id="11f65-111">描述</span><span class="sxs-lookup"><span data-stu-id="11f65-111">Description</span></span>                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="11f65-112">**WindowRegistered**</span><span class="sxs-lookup"><span data-stu-id="11f65-112">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md) | <span data-ttu-id="11f65-113">當視窗註冊為 Shell 視窗時呼叫。</span><span class="sxs-lookup"><span data-stu-id="11f65-113">Called when a window is registered as a Shell window.</span></span> <br/> |
| [<span data-ttu-id="11f65-114">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="11f65-114">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)       | <span data-ttu-id="11f65-115">當 Shell 視窗的註冊撤銷時呼叫。</span><span class="sxs-lookup"><span data-stu-id="11f65-115">Called when a Shell window's registration is revoked.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="11f65-116">備註</span><span class="sxs-lookup"><span data-stu-id="11f65-116">Remarks</span></span>

<span data-ttu-id="11f65-117">使用 **DShellWindowsEvents** 來監視如何註冊或撤銷 Shell 視窗。</span><span class="sxs-lookup"><span data-stu-id="11f65-117">Use **DShellWindowsEvents** to monitor when a Shell window is registered or revoked.</span></span> <span data-ttu-id="11f65-118">如需詳細資訊，請參閱 [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows)。</span><span class="sxs-lookup"><span data-stu-id="11f65-118">For more information, see [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).</span></span>

## <a name="requirements"></a><span data-ttu-id="11f65-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="11f65-119">Requirements</span></span>



| <span data-ttu-id="11f65-120">需求</span><span class="sxs-lookup"><span data-stu-id="11f65-120">Requirement</span></span> | <span data-ttu-id="11f65-121">值</span><span class="sxs-lookup"><span data-stu-id="11f65-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11f65-122">產品</span><span class="sxs-lookup"><span data-stu-id="11f65-122">Product</span></span><br/> | <span data-ttu-id="11f65-123">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="11f65-123">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="11f65-124">標頭</span><span class="sxs-lookup"><span data-stu-id="11f65-124">Header</span></span><br/>  | <dl> <span data-ttu-id="11f65-125"><dt>Exdisp。h</dt></span><span class="sxs-lookup"><span data-stu-id="11f65-125"><dt>Exdisp.h</dt></span></span> </dl>                                      |
| <span data-ttu-id="11f65-126">DLL</span><span class="sxs-lookup"><span data-stu-id="11f65-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="11f65-127"><dt>Shdocvw.dll (5.00.2014.0216 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="11f65-127"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |
| <span data-ttu-id="11f65-128">IID</span><span class="sxs-lookup"><span data-stu-id="11f65-128">IID</span></span><br/>     | <span data-ttu-id="11f65-129">IID \_ IShellWindows</span><span class="sxs-lookup"><span data-stu-id="11f65-129">IID\_IShellWindows</span></span><br/>                                                                                            |



## <a name="see-also"></a><span data-ttu-id="11f65-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11f65-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11f65-131">**ShellWindows**</span><span class="sxs-lookup"><span data-stu-id="11f65-131">**ShellWindows**</span></span>](shellwindows.md)
</dt> </dl>

 

 




