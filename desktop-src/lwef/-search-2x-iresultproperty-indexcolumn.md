---
title: 'IResultProperty IndexColumn 屬性 (WdsSharedIDL .h) '
description: 索引中的屬性資料行名稱。
ms.assetid: a043be43-49ef-46e0-bfb6-01104288e9ef
keywords:
- IndexColumn 屬性舊版 Windows 環境功能
- IndexColumn 屬性舊版 Windows 環境功能，IResultProperty 介面
- IResultProperty 介面舊版 Windows 環境功能，IndexColumn 屬性
topic_type:
- apiref
api_name:
- IResultProperty.IndexColumn
- IResultProperty.get_IndexColumn
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a4749f9ba1200f1af8ba202056e48f0123e8402
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843376"
---
# <a name="iresultpropertyindexcolumn-property"></a><span data-ttu-id="a59b6-106">IResultProperty：： IndexColumn 屬性</span><span class="sxs-lookup"><span data-stu-id="a59b6-106">IResultProperty::IndexColumn property</span></span>

> [!NOTE]
> <span data-ttu-id="a59b6-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="a59b6-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="a59b6-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="a59b6-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="a59b6-109">索引中的屬性資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="a59b6-109">Properties column name in the index.</span></span>

<span data-ttu-id="a59b6-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="a59b6-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a59b6-111">語法</span><span class="sxs-lookup"><span data-stu-id="a59b6-111">Syntax</span></span>


```C++
HRESULT get_IndexColumn(
  [out, retval] BSTR *column
);
```



## <a name="property-value"></a><span data-ttu-id="a59b6-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="a59b6-112">Property value</span></span>

<span data-ttu-id="a59b6-113">傳回索引中資料行名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="a59b6-113">returns a pointer to the column name in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="a59b6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a59b6-114">Requirements</span></span>



| <span data-ttu-id="a59b6-115">需求</span><span class="sxs-lookup"><span data-stu-id="a59b6-115">Requirement</span></span> | <span data-ttu-id="a59b6-116">值</span><span class="sxs-lookup"><span data-stu-id="a59b6-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="a59b6-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a59b6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a59b6-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a59b6-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="a59b6-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a59b6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a59b6-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a59b6-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a59b6-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a59b6-121">Redistributable</span></span><br/>          | <span data-ttu-id="a59b6-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="a59b6-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="a59b6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a59b6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a59b6-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="a59b6-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





