---
title: DVD-R 方法
description: Back 方法會將顯示從子功能表傳回至其父功能表。
ms.assetid: 4b6c3562-6484-4ef0-8c5c-c24d88e02096
keywords:
- back 方法 Windows Media Player
- back 方法 Windows Media Player、DVD 類別
- DVD 類別 Windows Media Player、back 方法
topic_type:
- apiref
api_name:
- DVD.back
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e656051d02ec5efc74aa7595d2ca6cb20e648f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384666"
---
# <a name="dvdback-method"></a><span data-ttu-id="d09e7-106">DVD-R 方法</span><span class="sxs-lookup"><span data-stu-id="d09e7-106">DVD.back method</span></span>

<span data-ttu-id="d09e7-107">Back 方法會將顯示從子功能表 **傳回** 至其父功能表。</span><span class="sxs-lookup"><span data-stu-id="d09e7-107">The **back** method returns the display from a submenu to its parent menu.</span></span>

## <a name="syntax"></a><span data-ttu-id="d09e7-108">語法</span><span class="sxs-lookup"><span data-stu-id="d09e7-108">Syntax</span></span>


```JScript
DVD.back()
```



## <a name="parameters"></a><span data-ttu-id="d09e7-109">參數</span><span class="sxs-lookup"><span data-stu-id="d09e7-109">Parameters</span></span>

<span data-ttu-id="d09e7-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d09e7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d09e7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d09e7-111">Return value</span></span>

<span data-ttu-id="d09e7-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d09e7-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d09e7-113">備註</span><span class="sxs-lookup"><span data-stu-id="d09e7-113">Remarks</span></span>

<span data-ttu-id="d09e7-114">每個 DVD 的撰寫方式不同。</span><span class="sxs-lookup"><span data-stu-id="d09e7-114">Every DVD is authored differently.</span></span> <span data-ttu-id="d09e7-115">某些 Dvd 的編寫是為了讓 **back** 方法可從根功能表取得，但叫用時，它不會執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="d09e7-115">Some DVDs are authored so that the **back** method is available from the root menu, but when invoked, it will do nothing.</span></span>

<span data-ttu-id="d09e7-116">**Windows Media Player 10** 行動裝置版：這個方法一律會成功，但不會執行預定的作業。</span><span class="sxs-lookup"><span data-stu-id="d09e7-116">**Windows Media Player 10 Mobile:** This method always succeeds, but does not perform the intended operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="d09e7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d09e7-117">Requirements</span></span>



| <span data-ttu-id="d09e7-118">需求</span><span class="sxs-lookup"><span data-stu-id="d09e7-118">Requirement</span></span> | <span data-ttu-id="d09e7-119">值</span><span class="sxs-lookup"><span data-stu-id="d09e7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d09e7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d09e7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d09e7-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d09e7-121">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d09e7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d09e7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d09e7-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d09e7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d09e7-124">版本</span><span class="sxs-lookup"><span data-stu-id="d09e7-124">Version</span></span><br/>                  | <span data-ttu-id="d09e7-125">適用于 Windows XP 或更新版本的 Windows Media Player。</span><span class="sxs-lookup"><span data-stu-id="d09e7-125">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="d09e7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d09e7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d09e7-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d09e7-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d09e7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d09e7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d09e7-129">**DVD 物件**</span><span class="sxs-lookup"><span data-stu-id="d09e7-129">**DVD Object**</span></span>](dvd-object.md)
</dt> </dl>

 

 





