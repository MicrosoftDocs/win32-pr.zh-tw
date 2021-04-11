---
title: MsimtfIsWindowFiltered 函式
description: MsimtfIsWindowFiltered 函式會測試指定的視窗是否由 AIMM (Active Input Method Manager) 篩選。
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- MsimtfIsWindowFiltered 函式文字服務架構
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ad9bd9fb61c546ec3e2f1d96d5fc9cf932613a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105396"
---
# <a name="msimtfiswindowfiltered-function"></a><span data-ttu-id="56f28-104">MsimtfIsWindowFiltered 函式</span><span class="sxs-lookup"><span data-stu-id="56f28-104">MsimtfIsWindowFiltered function</span></span>

<span data-ttu-id="56f28-105">**MsimtfIsWindowFiltered** 函式會測試指定的視窗是否由 AIMM (Active Input Method Manager) 篩選。</span><span class="sxs-lookup"><span data-stu-id="56f28-105">The **MsimtfIsWindowFiltered** function tests if the given window is filtered by AIMM (Active Input Method Manager).</span></span>

## <a name="syntax"></a><span data-ttu-id="56f28-106">語法</span><span class="sxs-lookup"><span data-stu-id="56f28-106">Syntax</span></span>


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="56f28-107">參數</span><span class="sxs-lookup"><span data-stu-id="56f28-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56f28-108">*hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="56f28-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56f28-109">要測試的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="56f28-109">A window handle to be tested.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56f28-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="56f28-110">Return value</span></span>



| <span data-ttu-id="56f28-111">傳回碼</span><span class="sxs-lookup"><span data-stu-id="56f28-111">Return code</span></span>                                                                          | <span data-ttu-id="56f28-112">Description</span><span class="sxs-lookup"><span data-stu-id="56f28-112">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="56f28-113"><dt>**真**</dt></span><span class="sxs-lookup"><span data-stu-id="56f28-113"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="56f28-114">如果使用 Active Input Method Manager 篩選此視窗。</span><span class="sxs-lookup"><span data-stu-id="56f28-114">If this window is filtered by Active Input Method Manager.</span></span><br/>     |
| <dl> <span data-ttu-id="56f28-115"><dt>**假**</dt></span><span class="sxs-lookup"><span data-stu-id="56f28-115"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="56f28-116">如果這個視窗不是由作用中的輸入方法管理員進行篩選。</span><span class="sxs-lookup"><span data-stu-id="56f28-116">If this window is not filtered by Active Input Method Manager.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="56f28-117">備註</span><span class="sxs-lookup"><span data-stu-id="56f28-117">Remarks</span></span>

<span data-ttu-id="56f28-118">您可以使用 IActiveIMMApp：： FilterClientWindows 來篩選視窗。</span><span class="sxs-lookup"><span data-stu-id="56f28-118">A window can be filtered by IActiveIMMApp::FilterClientWindows.</span></span>

## <a name="requirements"></a><span data-ttu-id="56f28-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="56f28-119">Requirements</span></span>



| <span data-ttu-id="56f28-120">需求</span><span class="sxs-lookup"><span data-stu-id="56f28-120">Requirement</span></span> | <span data-ttu-id="56f28-121">值</span><span class="sxs-lookup"><span data-stu-id="56f28-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="56f28-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56f28-122">Minimum supported client</span></span><br/> | <span data-ttu-id="56f28-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56f28-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="56f28-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56f28-124">Minimum supported server</span></span><br/> | <span data-ttu-id="56f28-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56f28-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="56f28-126">DLL</span><span class="sxs-lookup"><span data-stu-id="56f28-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56f28-127"><dt>Msimtf.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56f28-127"><dt>Msimtf.dll</dt></span></span> </dl> |



 

 





