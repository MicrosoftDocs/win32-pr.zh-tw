---
title: 'IPropertyFilter UID 屬性 (WdsSharedIDL .h) '
description: 要篩選之屬性的 UID。
ms.assetid: a9dfb34c-a161-4d5f-8d01-695b2f9346e6
keywords:
- UID 屬性舊版 Windows 環境功能
- UID 屬性舊版 Windows 環境功能，IPropertyFilter 介面
- IPropertyFilter 介面舊版 Windows 環境功能，UID 屬性
topic_type:
- apiref
api_name:
- IPropertyFilter.UID
- IPropertyFilter.get_UID
- IPropertyFilter.put_UID
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529f3f9142345705b9e14cabd2a46200d62fe2ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317336"
---
# <a name="ipropertyfilteruid-property"></a><span data-ttu-id="d3f66-106">IPropertyFilter：： UID 屬性</span><span class="sxs-lookup"><span data-stu-id="d3f66-106">IPropertyFilter::UID property</span></span>

> [!NOTE]
> <span data-ttu-id="d3f66-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="d3f66-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="d3f66-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="d3f66-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="d3f66-109">要篩選之屬性的 UID。</span><span class="sxs-lookup"><span data-stu-id="d3f66-109">UID for the property to filter by.</span></span>

<span data-ttu-id="d3f66-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d3f66-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f66-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3f66-111">Syntax</span></span>


```C++
HRESULT put_UID(
  [in]          long uid
);

HRESULT get_UID(
  [out, retval] long *uid
);
```



## <a name="property-value"></a><span data-ttu-id="d3f66-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="d3f66-112">Property value</span></span>

<span data-ttu-id="d3f66-113">設定 UID 屬性。</span><span class="sxs-lookup"><span data-stu-id="d3f66-113">Sets the UID property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3f66-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3f66-114">Requirements</span></span>



| <span data-ttu-id="d3f66-115">需求</span><span class="sxs-lookup"><span data-stu-id="d3f66-115">Requirement</span></span> | <span data-ttu-id="d3f66-116">值</span><span class="sxs-lookup"><span data-stu-id="d3f66-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f66-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3f66-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3f66-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3f66-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="d3f66-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3f66-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3f66-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3f66-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d3f66-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d3f66-121">Redistributable</span></span><br/>          | <span data-ttu-id="d3f66-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="d3f66-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="d3f66-123">標頭</span><span class="sxs-lookup"><span data-stu-id="d3f66-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3f66-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="d3f66-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





