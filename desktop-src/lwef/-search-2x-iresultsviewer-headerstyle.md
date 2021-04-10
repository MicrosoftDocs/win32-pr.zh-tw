---
title: 'IResultsViewer HeaderStyle 屬性 (WdsView .h) '
description: 顯示在視圖中的標頭樣式。
ms.assetid: 092a2ff2-eb88-4347-a81c-6a8005971ca9
keywords:
- HeaderStyle 屬性舊版 Windows 環境功能
- HeaderStyle 屬性舊版 Windows 環境功能，IResultsViewer 介面
- IResultsViewer 介面舊版 Windows 環境功能，HeaderStyle 屬性
topic_type:
- apiref
api_name:
- IResultsViewer.HeaderStyle
- IResultsViewer.get_HeaderStyle
- IResultsViewer.put_HeaderStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc4d0ad56e1303914af712e2a9b6fa0fd416785
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685931"
---
# <a name="iresultsviewerheaderstyle-property"></a><span data-ttu-id="76d82-106">IResultsViewer：： HeaderStyle 屬性</span><span class="sxs-lookup"><span data-stu-id="76d82-106">IResultsViewer::HeaderStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="76d82-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="76d82-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="76d82-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="76d82-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="76d82-109">顯示在視圖中的標頭樣式。</span><span class="sxs-lookup"><span data-stu-id="76d82-109">The style of header displayed in the view.</span></span>

<span data-ttu-id="76d82-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="76d82-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="76d82-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="76d82-111">Syntax</span></span>


```C++
HRESULT put_HeaderStyle(
  [in]          HeaderDisplayStyle style
);

HRESULT get_HeaderStyle(
  [out, retval] HeaderDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="76d82-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="76d82-112">Property value</span></span>

<span data-ttu-id="76d82-113">設定顯示的標頭樣式。</span><span class="sxs-lookup"><span data-stu-id="76d82-113">Sets the style of the header displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="76d82-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="76d82-114">Requirements</span></span>



| <span data-ttu-id="76d82-115">需求</span><span class="sxs-lookup"><span data-stu-id="76d82-115">Requirement</span></span> | <span data-ttu-id="76d82-116">值</span><span class="sxs-lookup"><span data-stu-id="76d82-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76d82-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76d82-117">Minimum supported client</span></span><br/> | <span data-ttu-id="76d82-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76d82-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="76d82-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76d82-119">Minimum supported server</span></span><br/> | <span data-ttu-id="76d82-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76d82-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="76d82-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="76d82-121">Redistributable</span></span><br/>          | <span data-ttu-id="76d82-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="76d82-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="76d82-123">標頭</span><span class="sxs-lookup"><span data-stu-id="76d82-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="76d82-124"><dt>WdsView。h</dt></span><span class="sxs-lookup"><span data-stu-id="76d82-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





