---
title: ResultsDisplayStyle 列舉
description: 由 IResultsViewer ResultsStyle 用來設定或決定結果的顯示方式。
ms.assetid: 24b474f2-1aca-4556-ba9a-3b8139e80bf0
keywords:
- ResultsDisplayStyle 列舉舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- ResultsDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26d564e0a7bb8a10b44e2957f26aa20a07afa535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980174"
---
# <a name="resultsdisplaystyle-enumeration"></a><span data-ttu-id="66eb2-104">ResultsDisplayStyle 列舉</span><span class="sxs-lookup"><span data-stu-id="66eb2-104">ResultsDisplayStyle enumeration</span></span>

> [!NOTE]
> <span data-ttu-id="66eb2-105">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="66eb2-105">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="66eb2-106">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="66eb2-106">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="66eb2-107">由 [**IResultsViewer：： ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) 用來設定或決定結果的顯示方式。</span><span class="sxs-lookup"><span data-stu-id="66eb2-107">Used by [**IResultsViewer::ResultsStyle**](-search-2x-iresultsviewer-resultsstyle.md) to set or determine how results are displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="66eb2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="66eb2-108">Syntax</span></span>


```C++
typedef enum ResultsDisplayStyleEnum { 
  SmallIconResults  = 0,
  LargeIconResults  = 1
} ResultsDisplayStyle;
```



## <a name="constants"></a><span data-ttu-id="66eb2-109">常數</span><span class="sxs-lookup"><span data-stu-id="66eb2-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="66eb2-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**</span><span class="sxs-lookup"><span data-stu-id="66eb2-110"><span id="SmallIconResults"></span><span id="smalliconresults"></span><span id="SMALLICONRESULTS"></span>**SmallIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="66eb2-111">表示以小圖示顯示結果。</span><span class="sxs-lookup"><span data-stu-id="66eb2-111">Indicates Results are displayed as small icons.</span></span>

</dd> <dt>

<span data-ttu-id="66eb2-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**</span><span class="sxs-lookup"><span data-stu-id="66eb2-112"><span id="LargeIconResults"></span><span id="largeiconresults"></span><span id="LARGEICONRESULTS"></span>**LargeIconResults**</span></span>
</dt> <dd>

<span data-ttu-id="66eb2-113">指出結果會顯示為大型圖示。</span><span class="sxs-lookup"><span data-stu-id="66eb2-113">Indicates Results are displayed as large icons.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="66eb2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="66eb2-114">Requirements</span></span>



| <span data-ttu-id="66eb2-115">需求</span><span class="sxs-lookup"><span data-stu-id="66eb2-115">Requirement</span></span> | <span data-ttu-id="66eb2-116">值</span><span class="sxs-lookup"><span data-stu-id="66eb2-116">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="66eb2-117">Idl</span><span class="sxs-lookup"><span data-stu-id="66eb2-117">IDL</span></span><br/> | <dl> <span data-ttu-id="66eb2-118"><dt>WdsView .idl</dt></span><span class="sxs-lookup"><span data-stu-id="66eb2-118"><dt>WdsView.idl</dt></span></span> </dl> |



 

 





