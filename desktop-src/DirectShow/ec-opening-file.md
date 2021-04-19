---
description: 圖形正在開啟檔案，或已完成檔案的開啟。
ms.assetid: 352867e1-025f-4adb-be32-f7941c0ec8cf
title: 'EC_OPENING_FILE (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf275a2f9b64f9a30c8049b5207622270edc5098
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995461"
---
# <a name="ec_opening_file"></a><span data-ttu-id="b8f7a-103">EC \_ 開啟 \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="b8f7a-103">EC\_OPENING\_FILE</span></span>

<span data-ttu-id="b8f7a-104">圖形正在開啟檔案，或已完成檔案的開啟。</span><span class="sxs-lookup"><span data-stu-id="b8f7a-104">The graph is opening a file, or has finished opening a file.</span></span>

## <a name="parameters"></a><span data-ttu-id="b8f7a-105">參數</span><span class="sxs-lookup"><span data-stu-id="b8f7a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8f7a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b8f7a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b8f7a-107">如果圖形正在開始開啟檔案，則 **為 TRUE** ; 如果圖形不再開啟檔案，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="b8f7a-107">**TRUE** if the graph is starting to open a file, or **FALSE** if the graph is no longer opening the file.</span></span>

</dd> <dt>

<span data-ttu-id="b8f7a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b8f7a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b8f7a-109">零個。</span><span class="sxs-lookup"><span data-stu-id="b8f7a-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b8f7a-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="b8f7a-110">Default Action</span></span>

<span data-ttu-id="b8f7a-111">無。</span><span class="sxs-lookup"><span data-stu-id="b8f7a-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8f7a-112">備註</span><span class="sxs-lookup"><span data-stu-id="b8f7a-112">Remarks</span></span>

<span data-ttu-id="b8f7a-113">如果篩選準則花了很長的時間來開啟檔案，則篩選準則可以傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="b8f7a-113">A filter can send this event if it spends significant time opening a file.</span></span> <span data-ttu-id="b8f7a-114"> (例如，檔案可能位於網路上。 ) 應用程式可以使用此事件來調整其使用者介面。</span><span class="sxs-lookup"><span data-stu-id="b8f7a-114">(For example, the file might be located on a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8f7a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8f7a-115">Requirements</span></span>



| <span data-ttu-id="b8f7a-116">需求</span><span class="sxs-lookup"><span data-stu-id="b8f7a-116">Requirement</span></span> | <span data-ttu-id="b8f7a-117">值</span><span class="sxs-lookup"><span data-stu-id="b8f7a-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8f7a-118">標頭</span><span class="sxs-lookup"><span data-stu-id="b8f7a-118">Header</span></span><br/> | <dl> <span data-ttu-id="b8f7a-119"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="b8f7a-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8f7a-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8f7a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8f7a-121">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="b8f7a-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b8f7a-122">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="b8f7a-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




