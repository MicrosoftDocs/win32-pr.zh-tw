---
description: 當視窗註冊為 Shell 視窗時呼叫。
title: DShellWindowsEvents. WindowRegistered 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents.WindowRegistered
api_type:
- COM
api_location:
- Shdocvw.dll
ms.assetid: 7faf758a-daa0-47f5-9f95-61fe3d8286ea
ms.openlocfilehash: b12ed98c6b2a11e5886ed9e76d324a1a6842cda8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974905"
---
# <a name="dshellwindowseventswindowregistered-method"></a><span data-ttu-id="baede-103">DShellWindowsEvents. WindowRegistered 方法</span><span class="sxs-lookup"><span data-stu-id="baede-103">DShellWindowsEvents.WindowRegistered method</span></span>

<span data-ttu-id="baede-104">當視窗註冊為 Shell 視窗時呼叫。</span><span class="sxs-lookup"><span data-stu-id="baede-104">Called when a window is registered as a Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="baede-105">語法</span><span class="sxs-lookup"><span data-stu-id="baede-105">Syntax</span></span>


```JScript
DShellWindowsEvents.WindowRegistered(
  lCookie
)
```



## <a name="parameters"></a><span data-ttu-id="baede-106">參數</span><span class="sxs-lookup"><span data-stu-id="baede-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baede-107">*lCookie* \[在\]</span><span class="sxs-lookup"><span data-stu-id="baede-107">*lCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="baede-108">類型： **整數**</span><span class="sxs-lookup"><span data-stu-id="baede-108">Type: **Integer**</span></span>

<span data-ttu-id="baede-109">識別已註冊之視窗的 cookie。</span><span class="sxs-lookup"><span data-stu-id="baede-109">The cookie that identifies the window that was registered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baede-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="baede-110">Return value</span></span>

<span data-ttu-id="baede-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="baede-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="baede-112">備註</span><span class="sxs-lookup"><span data-stu-id="baede-112">Remarks</span></span>

<span data-ttu-id="baede-113">當某個視窗註冊為 Shell 視窗時，會授與一個 cookie。</span><span class="sxs-lookup"><span data-stu-id="baede-113">A window is granted a cookie when it is registered as a Shell window.</span></span> <span data-ttu-id="baede-114">如需詳細資訊，請參閱 [**註冊**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)。</span><span class="sxs-lookup"><span data-stu-id="baede-114">For more information, see [**Register**](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register).</span></span>

## <a name="requirements"></a><span data-ttu-id="baede-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="baede-115">Requirements</span></span>



| <span data-ttu-id="baede-116">需求</span><span class="sxs-lookup"><span data-stu-id="baede-116">Requirement</span></span> | <span data-ttu-id="baede-117">值</span><span class="sxs-lookup"><span data-stu-id="baede-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baede-118">產品</span><span class="sxs-lookup"><span data-stu-id="baede-118">Product</span></span><br/> | <span data-ttu-id="baede-119">Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="baede-119">Internet Explorer 5</span></span><br/>                                                                                           |
| <span data-ttu-id="baede-120">DLL</span><span class="sxs-lookup"><span data-stu-id="baede-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="baede-121"><dt>Shdocvw.dll (5.00.2014.0216 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="baede-121"><dt>Shdocvw.dll (version 5.00.2014.0216 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baede-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="baede-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baede-123">**DShellWindowsEvents**</span><span class="sxs-lookup"><span data-stu-id="baede-123">**DShellWindowsEvents**</span></span>](dshellwindowsevents.md)
</dt> <dt>

[<span data-ttu-id="baede-124">**WindowRevoked**</span><span class="sxs-lookup"><span data-stu-id="baede-124">**WindowRevoked**</span></span>](dshellwindowsevents-windowrevoked.md)
</dt> <dt>

[<span data-ttu-id="baede-125">**註冊**</span><span class="sxs-lookup"><span data-stu-id="baede-125">**Register**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-register)
</dt> <dt>

[<span data-ttu-id="baede-126">**RegisterPending**</span><span class="sxs-lookup"><span data-stu-id="baede-126">**RegisterPending**</span></span>](/windows/desktop/api/Exdisp/nf-exdisp-ishellwindows-registerpending)
</dt> </dl>

 

 




