---
title: 'IResultProperty 提示屬性 (WdsSharedIDL .h) '
description: 用來協助資料抓取的特殊值。
ms.assetid: fa888c5e-898e-4f48-b87e-2d0d078fd1fe
keywords:
- 提示屬性舊版 Windows 環境功能
- 提示屬性舊版 Windows 環境功能，IResultProperty 介面
- IResultProperty 介面舊版 Windows 環境功能，提示屬性
topic_type:
- apiref
api_name:
- IResultProperty.Hint
- IResultProperty.get_Hint
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3edfed528ab6a6833cced99c113c33e7e2f859d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966500"
---
# <a name="iresultpropertyhint-property"></a><span data-ttu-id="6420b-106">IResultProperty：：提示屬性</span><span class="sxs-lookup"><span data-stu-id="6420b-106">IResultProperty::Hint property</span></span>

> [!NOTE]
> <span data-ttu-id="6420b-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="6420b-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6420b-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="6420b-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="6420b-109">用來協助資料抓取的特殊值。</span><span class="sxs-lookup"><span data-stu-id="6420b-109">Special value used to aid data retrieval.</span></span>

<span data-ttu-id="6420b-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6420b-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6420b-111">語法</span><span class="sxs-lookup"><span data-stu-id="6420b-111">Syntax</span></span>


```C++
HRESULT get_Hint(
  [out, retval] ling *hint
);
```



## <a name="property-value"></a><span data-ttu-id="6420b-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="6420b-112">Property value</span></span>

<span data-ttu-id="6420b-113">傳回提示的指標。</span><span class="sxs-lookup"><span data-stu-id="6420b-113">returns a pointer to the hint.</span></span>

## <a name="requirements"></a><span data-ttu-id="6420b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6420b-114">Requirements</span></span>



| <span data-ttu-id="6420b-115">需求</span><span class="sxs-lookup"><span data-stu-id="6420b-115">Requirement</span></span> | <span data-ttu-id="6420b-116">值</span><span class="sxs-lookup"><span data-stu-id="6420b-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6420b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6420b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6420b-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6420b-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6420b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6420b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6420b-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6420b-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6420b-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6420b-121">Redistributable</span></span><br/>          | <span data-ttu-id="6420b-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="6420b-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="6420b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6420b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6420b-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="6420b-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





