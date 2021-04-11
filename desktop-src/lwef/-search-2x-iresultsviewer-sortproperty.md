---
title: 'IResultsViewer SortProperty 屬性 (WdsView .h) '
description: 這個屬性會設定或傳回用來排序結果的屬性（property）（IndexColumn）。
ms.assetid: 5b117f2e-52cc-43ef-9ebd-d7a800015465
keywords:
- SortProperty 屬性舊版 Windows 環境功能
- SortProperty 屬性舊版 Windows 環境功能，IResultsViewer 介面
- IResultsViewer 介面舊版 Windows 環境功能，SortProperty 屬性
topic_type:
- apiref
api_name:
- IResultsViewer.SortProperty
- IResultsViewer.get_SortProperty
- IResultsViewer.put_SortProperty
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cb75b98f1f0a726ef0d61b5c476df1485ba7189
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843504"
---
# <a name="iresultsviewersortproperty-property"></a><span data-ttu-id="51a8c-106">IResultsViewer：： SortProperty 屬性</span><span class="sxs-lookup"><span data-stu-id="51a8c-106">IResultsViewer::SortProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="51a8c-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="51a8c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="51a8c-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="51a8c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="51a8c-109">這個屬性會設定或傳回用來排序結果的屬性（property）（IndexColumn）。</span><span class="sxs-lookup"><span data-stu-id="51a8c-109">This property will set or return the IndexColumn of the property to sort results by.</span></span>

<span data-ttu-id="51a8c-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="51a8c-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="51a8c-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="51a8c-111">Syntax</span></span>


```C++
HRESULT put_SortProperty(
  [in]          BSTR column
);

HRESULT get_SortProperty(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="51a8c-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="51a8c-112">Property value</span></span>

<span data-ttu-id="51a8c-113">設定 IndexColumn 屬性。</span><span class="sxs-lookup"><span data-stu-id="51a8c-113">Sets the IndexColumn property.</span></span>

## <a name="requirements"></a><span data-ttu-id="51a8c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="51a8c-114">Requirements</span></span>



| <span data-ttu-id="51a8c-115">需求</span><span class="sxs-lookup"><span data-stu-id="51a8c-115">Requirement</span></span> | <span data-ttu-id="51a8c-116">值</span><span class="sxs-lookup"><span data-stu-id="51a8c-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="51a8c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51a8c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="51a8c-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51a8c-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="51a8c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51a8c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="51a8c-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51a8c-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="51a8c-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="51a8c-121">Redistributable</span></span><br/>          | <span data-ttu-id="51a8c-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="51a8c-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="51a8c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="51a8c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="51a8c-124"><dt>WdsView。h</dt></span><span class="sxs-lookup"><span data-stu-id="51a8c-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





