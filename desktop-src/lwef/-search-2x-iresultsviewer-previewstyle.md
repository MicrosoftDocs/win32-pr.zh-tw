---
title: 'IResultsViewer PreviewStyle 屬性 (WdsView .h) '
description: 控制預覽窗格的顯示模式。
ms.assetid: 750664ea-506a-4219-ade5-1c7f1ffbd0d7
keywords:
- PreviewStyle 屬性舊版 Windows 環境功能
- PreviewStyle 屬性舊版 Windows 環境功能，IResultsViewer 介面
- IResultsViewer 介面舊版 Windows 環境功能，PreviewStyle 屬性
topic_type:
- apiref
api_name:
- IResultsViewer.PreviewStyle
- IResultsViewer.get_PreviewStyle
- IResultsViewer.put_PreviewStyle
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9eb3cb2cfd94d5cf1e93080259257bb27fa4f086
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965063"
---
# <a name="iresultsviewerpreviewstyle-property"></a><span data-ttu-id="7e457-106">IResultsViewer：:P reviewStyle 屬性</span><span class="sxs-lookup"><span data-stu-id="7e457-106">IResultsViewer::PreviewStyle property</span></span>

> [!NOTE]
> <span data-ttu-id="7e457-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="7e457-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7e457-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="7e457-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="7e457-109">控制預覽窗格的顯示模式。</span><span class="sxs-lookup"><span data-stu-id="7e457-109">Controls the preview pane's display mode.</span></span>

<span data-ttu-id="7e457-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="7e457-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e457-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e457-111">Syntax</span></span>


```C++
HRESULT put_PreviewStyle(
  [in]          PreviewDisplayStyle style
);

HRESULT get_PreviewStyle(
  [out, retval] PreviewDisplayStyle *style
);
```



## <a name="property-value"></a><span data-ttu-id="7e457-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="7e457-112">Property value</span></span>

<span data-ttu-id="7e457-113">設定預覽窗格的目前樣式屬性。</span><span class="sxs-lookup"><span data-stu-id="7e457-113">Sets the current style property for the preview pane.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e457-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e457-114">Requirements</span></span>



| <span data-ttu-id="7e457-115">需求</span><span class="sxs-lookup"><span data-stu-id="7e457-115">Requirement</span></span> | <span data-ttu-id="7e457-116">值</span><span class="sxs-lookup"><span data-stu-id="7e457-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7e457-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e457-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7e457-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e457-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7e457-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e457-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7e457-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e457-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="7e457-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7e457-121">Redistributable</span></span><br/>          | <span data-ttu-id="7e457-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="7e457-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="7e457-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7e457-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e457-124"><dt>WdsView。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e457-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





