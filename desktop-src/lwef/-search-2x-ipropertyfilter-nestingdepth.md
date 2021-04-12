---
title: 'IPropertyFilter NestingDepth 屬性 (WdsSharedIDL .h) '
description: 篩選一組嵌套括弧內的深度。
ms.assetid: a52992b3-d232-46a5-907c-8df6bd5ad6fc
keywords:
- NestingDepth 屬性舊版 Windows 環境功能
- NestingDepth 屬性舊版 Windows 環境功能，IPropertyFilter 介面
- IPropertyFilter 介面舊版 Windows 環境功能，NestingDepth 屬性
topic_type:
- apiref
api_name:
- IPropertyFilter.NestingDepth
- IPropertyFilter.get_NestingDepth
- IPropertyFilter.put_NestingDepth
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a2bda4e12bb68b501fa42003ac145113dade3ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384605"
---
# <a name="ipropertyfilternestingdepth-property"></a><span data-ttu-id="49dfb-106">IPropertyFilter：： NestingDepth 屬性</span><span class="sxs-lookup"><span data-stu-id="49dfb-106">IPropertyFilter::NestingDepth property</span></span>

> [!NOTE]
> <span data-ttu-id="49dfb-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="49dfb-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="49dfb-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="49dfb-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="49dfb-109">篩選一組嵌套括弧內的深度。</span><span class="sxs-lookup"><span data-stu-id="49dfb-109">Filters depth within a nested set of parentheses.</span></span>

<span data-ttu-id="49dfb-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="49dfb-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="49dfb-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="49dfb-111">Syntax</span></span>


```C++
HRESULT put_NestingDepth(
  [in]          long depth
);

HRESULT get_NestingDepth(
  [out, retval] long *depth
);
```



## <a name="property-value"></a><span data-ttu-id="49dfb-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="49dfb-112">Property value</span></span>

<span data-ttu-id="49dfb-113">設定表示嵌套括弧深度的數位。</span><span class="sxs-lookup"><span data-stu-id="49dfb-113">Sets the number indicating the depth of nested parentheses.</span></span>

## <a name="requirements"></a><span data-ttu-id="49dfb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="49dfb-114">Requirements</span></span>



| <span data-ttu-id="49dfb-115">需求</span><span class="sxs-lookup"><span data-stu-id="49dfb-115">Requirement</span></span> | <span data-ttu-id="49dfb-116">值</span><span class="sxs-lookup"><span data-stu-id="49dfb-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="49dfb-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49dfb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="49dfb-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49dfb-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="49dfb-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49dfb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="49dfb-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49dfb-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="49dfb-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="49dfb-121">Redistributable</span></span><br/>          | <span data-ttu-id="49dfb-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="49dfb-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="49dfb-123">標頭</span><span class="sxs-lookup"><span data-stu-id="49dfb-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="49dfb-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="49dfb-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





