---
description: 當 Shell 視窗的註冊撤銷時呼叫。
title: DShellWindowsEvents. WindowRevoked 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRevoked
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 92e8653f-7f41-4e0b-97e5-429fddc51951
ms.openlocfilehash: 7ed78dcaa545b2321b04aff9ff2f4e711f93c992
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843179"
---
# <a name="dshellwindowseventswindowrevoked-method"></a><span data-ttu-id="6151f-103">DShellWindowsEvents. WindowRevoked 方法</span><span class="sxs-lookup"><span data-stu-id="6151f-103">DShellWindowsEvents.WindowRevoked method</span></span>

<span data-ttu-id="6151f-104">當 Shell 視窗的註冊撤銷時呼叫。</span><span class="sxs-lookup"><span data-stu-id="6151f-104">Called when a Shell window's registration is revoked.</span></span>

## <a name="syntax"></a><span data-ttu-id="6151f-105">語法</span><span class="sxs-lookup"><span data-stu-id="6151f-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRevoked(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="6151f-106">參數</span><span class="sxs-lookup"><span data-stu-id="6151f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6151f-107">*lCookie* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6151f-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6151f-108">類型： **整數**</span><span class="sxs-lookup"><span data-stu-id="6151f-108">Type: **Integer**</span></span>

<span data-ttu-id="6151f-109">識別已撤銷之視窗的 cookie。</span><span class="sxs-lookup"><span data-stu-id="6151f-109">The cookie that identifies the window that was revoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6151f-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6151f-110">Return value</span></span>

<span data-ttu-id="6151f-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6151f-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6151f-112">備註</span><span class="sxs-lookup"><span data-stu-id="6151f-112">Remarks</span></span>

<span data-ttu-id="6151f-113">當某個視窗註冊為 Shell 視窗時，會授與一個 cookie。</span><span class="sxs-lookup"><span data-stu-id="6151f-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="6151f-114">如需詳細資訊，請參閱 [**註冊**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)。</span><span class="sxs-lookup"><span data-stu-id="6151f-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="6151f-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6151f-115">Requirements</span></span>



| <span data-ttu-id="6151f-116">需求</span><span class="sxs-lookup"><span data-stu-id="6151f-116">Requirement</span></span> | <span data-ttu-id="6151f-117">值</span><span class="sxs-lookup"><span data-stu-id="6151f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6151f-118">產品</span><span class="sxs-lookup"><span data-stu-id="6151f-118">Product</span></span><br/> | <span data-ttu-id="6151f-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="6151f-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="6151f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6151f-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="6151f-121"><dt>Shdocvw.dll (5.00.2014.0216 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="6151f-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6151f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6151f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6151f-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="6151f-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="6151f-124">**WindowRegistered**</span><span class="sxs-lookup"><span data-stu-id="6151f-124">**WindowRegistered**</span></span>](dshellwindowsevents-windowregistered.md)
</dt> <dt>

[<span data-ttu-id="6151f-125">**撤銷**</span><span class="sxs-lookup"><span data-stu-id="6151f-125">**Revoke**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-revoke)
</dt> </dl>

 

 




