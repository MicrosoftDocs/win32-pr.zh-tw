---
title: 'IResultType PropertyCount 屬性 (WdsSharedIDL .h) '
description: 這個屬性包含型別所公開的屬性數目。
ms.assetid: 4ca4b18c-d228-4275-b00d-06c6f227e0ae
keywords:
- PropertyCount 屬性舊版 Windows 環境功能
- PropertyCount 屬性舊版 Windows 環境功能，IResultType 介面
- IResultType 介面舊版 Windows 環境功能，PropertyCount 屬性
topic_type:
- apiref
api_name:
- IResultType.PropertyCount
- IResultType.get_PropertyCount
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1804c0abd249d93470cb2570f5bd58c600e8d3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508316"
---
# <a name="iresulttypepropertycount-property"></a><span data-ttu-id="53d71-106">IResultType：:P ropertyCount 屬性</span><span class="sxs-lookup"><span data-stu-id="53d71-106">IResultType::PropertyCount property</span></span>

> [!NOTE]
> <span data-ttu-id="53d71-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="53d71-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="53d71-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="53d71-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="53d71-109">這個屬性包含型別所公開的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="53d71-109">This property contains the number of properties exposed by the type.</span></span>

<span data-ttu-id="53d71-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="53d71-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d71-111">語法</span><span class="sxs-lookup"><span data-stu-id="53d71-111">Syntax</span></span>


```C++
HRESULT get_PropertyCount(
  [out, retval] long *count
);
```



## <a name="property-value"></a><span data-ttu-id="53d71-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="53d71-112">Property value</span></span>

<span data-ttu-id="53d71-113">傳回公開的屬性數目的位址。</span><span class="sxs-lookup"><span data-stu-id="53d71-113">returns the address of the number of properties exposed.</span></span>

## <a name="requirements"></a><span data-ttu-id="53d71-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="53d71-114">Requirements</span></span>



| <span data-ttu-id="53d71-115">需求</span><span class="sxs-lookup"><span data-stu-id="53d71-115">Requirement</span></span> | <span data-ttu-id="53d71-116">值</span><span class="sxs-lookup"><span data-stu-id="53d71-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="53d71-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="53d71-117">Minimum supported client</span></span><br/> | <span data-ttu-id="53d71-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53d71-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="53d71-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="53d71-119">Minimum supported server</span></span><br/> | <span data-ttu-id="53d71-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="53d71-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="53d71-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="53d71-121">Redistributable</span></span><br/>          | <span data-ttu-id="53d71-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="53d71-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="53d71-123">標頭</span><span class="sxs-lookup"><span data-stu-id="53d71-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="53d71-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="53d71-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





