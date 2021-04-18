---
description: 發生于 InkEdit 控制項中目前的文字選取範圍已變更或插入點移動時。
ms.assetid: 14ddffe7-bdfe-4a35-82c7-b3401b5b720c
title: 'InkEdit. SelChange 事件 (筆跡 .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b51ef4edbf7d7fb02be17dc416c0a777a9519a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989475"
---
# <a name="inkeditselchange-event"></a><span data-ttu-id="208ae-103">InkEdit. SelChange 事件</span><span class="sxs-lookup"><span data-stu-id="208ae-103">InkEdit.SelChange event</span></span>

<span data-ttu-id="208ae-104">發生于 [InkEdit](inkedit-control-reference.md) 控制項中目前的文字選取範圍已變更或插入點移動時。</span><span class="sxs-lookup"><span data-stu-id="208ae-104">Occurs when the current selection of text in the [InkEdit](inkedit-control-reference.md) control has changed or the insertion point has moved.</span></span>

## <a name="syntax"></a><span data-ttu-id="208ae-105">語法</span><span class="sxs-lookup"><span data-stu-id="208ae-105">Syntax</span></span>


```C++
void SelChange();
```



## <a name="parameters"></a><span data-ttu-id="208ae-106">參數</span><span class="sxs-lookup"><span data-stu-id="208ae-106">Parameters</span></span>

<span data-ttu-id="208ae-107">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="208ae-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="208ae-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="208ae-108">Return value</span></span>

<span data-ttu-id="208ae-109">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="208ae-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="208ae-110">備註</span><span class="sxs-lookup"><span data-stu-id="208ae-110">Remarks</span></span>

<span data-ttu-id="208ae-111">您可以使用 **SelChange** 事件來檢查提供目前選取專案相關資訊的各種屬性 (例如 [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) ，以便您可以在工具列中更新按鈕，例如。</span><span class="sxs-lookup"><span data-stu-id="208ae-111">You can use the **SelChange** event to check the various properties that give information about the current selection (such as [**SelBold**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selbold)) so you can update buttons in a toolbar, for example.</span></span>

## <a name="requirements"></a><span data-ttu-id="208ae-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="208ae-112">Requirements</span></span>



| <span data-ttu-id="208ae-113">需求</span><span class="sxs-lookup"><span data-stu-id="208ae-113">Requirement</span></span> | <span data-ttu-id="208ae-114">值</span><span class="sxs-lookup"><span data-stu-id="208ae-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="208ae-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="208ae-115">Minimum supported client</span></span><br/> | <span data-ttu-id="208ae-116">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="208ae-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="208ae-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="208ae-117">Minimum supported server</span></span><br/> | <span data-ttu-id="208ae-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="208ae-118">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="208ae-119">標頭</span><span class="sxs-lookup"><span data-stu-id="208ae-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="208ae-120"><dt>筆跡 (也需要筆跡 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="208ae-120"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="208ae-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="208ae-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="208ae-122"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="208ae-122"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="208ae-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="208ae-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="208ae-124">InkEdit</span><span class="sxs-lookup"><span data-stu-id="208ae-124">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




