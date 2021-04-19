---
description: InkEdit 控制項的內容變更時發生。
ms.assetid: 6c65fcca-c84a-414c-a4e5-c5fdffb13e51
title: InkEdit (筆跡) 變更事件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1ad11ef335a397070001f1ae6be785d60fe9cb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994468"
---
# <a name="inkeditchange-event"></a><span data-ttu-id="699b6-103">InkEdit。變更事件</span><span class="sxs-lookup"><span data-stu-id="699b6-103">InkEdit.Change event</span></span>

<span data-ttu-id="699b6-104">[InkEdit](inkedit-control-reference.md)控制項的內容變更時發生。</span><span class="sxs-lookup"><span data-stu-id="699b6-104">Occurs when the content of the [InkEdit](inkedit-control-reference.md) control changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="699b6-105">語法</span><span class="sxs-lookup"><span data-stu-id="699b6-105">Syntax</span></span>


```C++
void Change();
```



## <a name="parameters"></a><span data-ttu-id="699b6-106">參數</span><span class="sxs-lookup"><span data-stu-id="699b6-106">Parameters</span></span>

<span data-ttu-id="699b6-107">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="699b6-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="699b6-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="699b6-108">Return value</span></span>

<span data-ttu-id="699b6-109">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="699b6-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="699b6-110">備註</span><span class="sxs-lookup"><span data-stu-id="699b6-110">Remarks</span></span>

<span data-ttu-id="699b6-111">每當影響 [InkEdit](inkedit-control-reference.md) 控制項內容的任何屬性變更時，就會發生此事件。</span><span class="sxs-lookup"><span data-stu-id="699b6-111">This event occurs whenever any properties that affect the contents of the [InkEdit](inkedit-control-reference.md) control change.</span></span>

<span data-ttu-id="699b6-112">此事件方法是在 **\_ IInkEditEvents** 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="699b6-112">This event method is defined in the **\_IInkEditEvents** interface.</span></span> <span data-ttu-id="699b6-113">**\_ IInkEditEvents** 介面會以 **DISPID \_ IeeChange** 的識別碼來實作為 IDispatch 介面。</span><span class="sxs-lookup"><span data-stu-id="699b6-113">The **\_IInkEditEvents** interface implements the IDispatch interface with an identifier of **DISPID\_IeeChange**.</span></span>

## <a name="requirements"></a><span data-ttu-id="699b6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="699b6-114">Requirements</span></span>



| <span data-ttu-id="699b6-115">需求</span><span class="sxs-lookup"><span data-stu-id="699b6-115">Requirement</span></span> | <span data-ttu-id="699b6-116">值</span><span class="sxs-lookup"><span data-stu-id="699b6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="699b6-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="699b6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="699b6-118">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="699b6-118">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="699b6-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="699b6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="699b6-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="699b6-120">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="699b6-121">標頭</span><span class="sxs-lookup"><span data-stu-id="699b6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="699b6-122"><dt>筆跡 (也需要筆跡 \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="699b6-122"><dt>Inked.h (also requires inked\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="699b6-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="699b6-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="699b6-124"><dt>InkEd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="699b6-124"><dt>InkEd.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="699b6-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="699b6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="699b6-126">InkEdit</span><span class="sxs-lookup"><span data-stu-id="699b6-126">InkEdit</span></span>](inkedit-control-reference.md)
</dt> </dl>

 

 




