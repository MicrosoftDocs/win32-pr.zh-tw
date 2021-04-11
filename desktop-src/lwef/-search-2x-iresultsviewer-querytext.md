---
title: 'IResultsViewer >querytext 屬性 (WdsView .h) '
description: 取得或設定目前的查詢文字。
ms.assetid: 3d6b31fa-3f17-45de-a91a-f24a6b076099
keywords:
- '>querytext 屬性舊版 Windows 環境功能'
- '>querytext 屬性舊版 Windows 環境功能，IResultsViewer 介面'
- IResultsViewer 介面舊版 Windows 環境功能，>querytext 屬性
topic_type:
- apiref
api_name:
- IResultsViewer.QueryText
- IResultsViewer.get_QueryText
- IResultsViewer.put_QueryText
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98450114ad64ec0209b14041b8f2516dc6884b8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105780"
---
# <a name="iresultsviewerquerytext-property"></a><span data-ttu-id="e1792-106">IResultsViewer：： >querytext 屬性</span><span class="sxs-lookup"><span data-stu-id="e1792-106">IResultsViewer::QueryText property</span></span>

> [!NOTE]
> <span data-ttu-id="e1792-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="e1792-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="e1792-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="e1792-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="e1792-109">取得或設定目前的查詢文字。</span><span class="sxs-lookup"><span data-stu-id="e1792-109">Gets or sets the current query text.</span></span>

<span data-ttu-id="e1792-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e1792-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1792-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1792-111">Syntax</span></span>


```C++
HRESULT put_QueryText(
  [in]          BSTR query
);

HRESULT get_QueryText(
  [out, retval] BSTR *query
);
```



## <a name="property-value"></a><span data-ttu-id="e1792-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="e1792-112">Property value</span></span>

<span data-ttu-id="e1792-113">設定目前的查詢文字。</span><span class="sxs-lookup"><span data-stu-id="e1792-113">Sets the current query text.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1792-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1792-114">Requirements</span></span>



| <span data-ttu-id="e1792-115">需求</span><span class="sxs-lookup"><span data-stu-id="e1792-115">Requirement</span></span> | <span data-ttu-id="e1792-116">值</span><span class="sxs-lookup"><span data-stu-id="e1792-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e1792-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1792-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e1792-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1792-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e1792-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1792-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e1792-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1792-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="e1792-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e1792-121">Redistributable</span></span><br/>          | <span data-ttu-id="e1792-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="e1792-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="e1792-123">標頭</span><span class="sxs-lookup"><span data-stu-id="e1792-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1792-124"><dt>WdsView。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1792-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





