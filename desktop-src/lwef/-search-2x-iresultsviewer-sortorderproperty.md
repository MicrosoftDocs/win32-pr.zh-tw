---
title: IResultsViewer SortOrderProperty 屬性 (WdsView.h)
description: 這個屬性會設定或傳回排序結果所依據的資料行順序。
ms.assetid: ea05f4df-4caf-404f-8890-a109ca88555c
keywords:
- SortOrderProperty 屬性舊版 Windows 環境功能
- SortOrderProperty 屬性舊版 Windows 環境功能，IResultsViewer 介面
- IResultsViewer 介面舊版 Windows 環境功能，SortOrderProperty 屬性
topic_type:
- apiref
api_name:
- IResultsViewer.SortOrderProperty
- IResultsViewer.get_SortOrderProperty
- IResultsViewer.put_SortOrderProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa36dba99afbee58b480e17f241cb32f75cd5dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "107001294"
---
# <a name="iresultsviewersortorderproperty-property"></a><span data-ttu-id="10afc-106">IResultsViewer：： SortOrderProperty 屬性</span><span class="sxs-lookup"><span data-stu-id="10afc-106">IResultsViewer::SortOrderProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="10afc-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="10afc-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="10afc-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="10afc-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="10afc-109">這個屬性會設定或傳回排序結果所依據的資料行順序。</span><span class="sxs-lookup"><span data-stu-id="10afc-109">This property will set or return the order of columns to sort results by.</span></span>

<span data-ttu-id="10afc-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="10afc-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="10afc-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="10afc-111">Syntax</span></span>


```C++
HRESULT put_SortOrderProperty(
  [in]          ColumnSortOrder order
);

HRESULT get_SortOrderProperty(
  [out, retval] ColumnSortOrder *order
);
```



## <a name="property-value"></a><span data-ttu-id="10afc-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="10afc-112">Property value</span></span>

<span data-ttu-id="10afc-113">設定 [**ColumnSortOrder**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) 屬性。</span><span class="sxs-lookup"><span data-stu-id="10afc-113">Sets the [**ColumnSortOrder**](/windows/win32/api/mmcobj/ne-mmcobj-_columnsortorder) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="10afc-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="10afc-114">Requirements</span></span>



| <span data-ttu-id="10afc-115">需求</span><span class="sxs-lookup"><span data-stu-id="10afc-115">Requirement</span></span> | <span data-ttu-id="10afc-116">值</span><span class="sxs-lookup"><span data-stu-id="10afc-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="10afc-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10afc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="10afc-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10afc-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="10afc-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10afc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="10afc-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10afc-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="10afc-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="10afc-121">Redistributable</span></span><br/>          | <span data-ttu-id="10afc-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="10afc-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="10afc-123">標頭</span><span class="sxs-lookup"><span data-stu-id="10afc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="10afc-124"><dt>WdsView。h</dt></span><span class="sxs-lookup"><span data-stu-id="10afc-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





