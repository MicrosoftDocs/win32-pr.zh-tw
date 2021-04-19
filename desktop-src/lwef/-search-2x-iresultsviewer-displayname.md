---
title: 'IResultsViewer DisplayName 屬性 (WdsView .h) '
description: 類型的當地語系化顯示名稱。
ms.assetid: 22503996-e693-47bc-b84f-cc4d3af2cb78
keywords:
- DisplayName 屬性舊版 Windows 環境功能
- DisplayName 屬性舊版 Windows 環境功能，IResultsViewer 介面
- IResultsViewer 介面舊版 Windows 環境功能，DisplayName 屬性
topic_type:
- apiref
api_name:
- IResultsViewer.DisplayName
- IResultsViewer.get_DisplayName
api_location:
- WdsView.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe5ba65729fb238dbed57b71d893a9814c8ac8f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968347"
---
# <a name="iresultsviewerdisplayname-property"></a><span data-ttu-id="db73c-106">IResultsViewer：:D isplayName 屬性</span><span class="sxs-lookup"><span data-stu-id="db73c-106">IResultsViewer::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="db73c-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="db73c-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="db73c-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="db73c-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="db73c-109">類型的當地語系化顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="db73c-109">Localized display name of the type.</span></span>

<span data-ttu-id="db73c-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="db73c-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="db73c-111">語法</span><span class="sxs-lookup"><span data-stu-id="db73c-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="db73c-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="db73c-112">Property value</span></span>

<span data-ttu-id="db73c-113">值的指標，此值會接收類型的當地語系化顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="db73c-113">Pointer to a value that receives the localized display name for the type.</span></span>

## <a name="requirements"></a><span data-ttu-id="db73c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="db73c-114">Requirements</span></span>



| <span data-ttu-id="db73c-115">需求</span><span class="sxs-lookup"><span data-stu-id="db73c-115">Requirement</span></span> | <span data-ttu-id="db73c-116">值</span><span class="sxs-lookup"><span data-stu-id="db73c-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="db73c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="db73c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="db73c-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db73c-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="db73c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="db73c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="db73c-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="db73c-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="db73c-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="db73c-121">Redistributable</span></span><br/>          | <span data-ttu-id="db73c-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="db73c-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                        |
| <span data-ttu-id="db73c-123">標頭</span><span class="sxs-lookup"><span data-stu-id="db73c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="db73c-124"><dt>WdsView。h</dt></span><span class="sxs-lookup"><span data-stu-id="db73c-124"><dt>WdsView.h</dt></span></span> </dl> |



 

 





