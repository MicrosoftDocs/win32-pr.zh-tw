---
title: 'IResultsViewer FilterType 屬性 (WdsView .h) '
description: 這個屬性會設定或傳回用來篩選結果的 preceived 類型名稱。
ms.assetid: 025955eb-3e44-4e26-8b5f-ae92eb4c8300
keywords:
- FilterType 屬性舊版 Windows 環境功能
- FilterType 屬性舊版 Windows 環境功能，IResultsViewer 介面
- IResultsViewer 介面舊版 Windows 環境功能，FilterType 屬性
topic_type:
- apiref
api_name:
- IResultsViewer.FilterType
- IResultsViewer.get_FilterType
- IResultsViewer.put_FilterType
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890d0ceadddb9f3b46ee8b45f109a389472be218
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966956"
---
# <a name="iresultsviewerfiltertype-property"></a><span data-ttu-id="bdf27-106">IResultsViewer：： FilterType 屬性</span><span class="sxs-lookup"><span data-stu-id="bdf27-106">IResultsViewer::FilterType property</span></span>

> [!NOTE]
> <span data-ttu-id="bdf27-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="bdf27-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="bdf27-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="bdf27-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="bdf27-109">這個屬性會設定或傳回用來篩選結果的 preceived 類型名稱。</span><span class="sxs-lookup"><span data-stu-id="bdf27-109">This property will set or return the name of the preceived type to filter results by.</span></span>

<span data-ttu-id="bdf27-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="bdf27-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdf27-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdf27-111">Syntax</span></span>


```C++
HRESULT put_FilterType(
  [in]          BSTR name
);

HRESULT get_FilterType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="bdf27-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="bdf27-112">Property value</span></span>

<span data-ttu-id="bdf27-113">設定用來篩選結果的認知型別。</span><span class="sxs-lookup"><span data-stu-id="bdf27-113">Sets the perceived type used to filter results.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdf27-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bdf27-114">Requirements</span></span>



| <span data-ttu-id="bdf27-115">需求</span><span class="sxs-lookup"><span data-stu-id="bdf27-115">Requirement</span></span> | <span data-ttu-id="bdf27-116">值</span><span class="sxs-lookup"><span data-stu-id="bdf27-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bdf27-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bdf27-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf27-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdf27-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bdf27-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bdf27-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf27-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bdf27-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="bdf27-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="bdf27-121">Redistributable</span></span><br/>          | <span data-ttu-id="bdf27-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="bdf27-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="bdf27-123">標頭</span><span class="sxs-lookup"><span data-stu-id="bdf27-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdf27-124"><dt>WdsView。h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf27-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





