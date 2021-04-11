---
title: 'IResultType PreceivedType 屬性 (WdsSharedIDL .h) '
description: 這個屬性包含用來識別索引中之類型的字串。
ms.assetid: 26d5f14c-162a-4ded-ac72-875561b8c977
keywords:
- PreceivedType 屬性舊版 Windows 環境功能
- PreceivedType 屬性舊版 Windows 環境功能，IResultType 介面
- IResultType 介面舊版 Windows 環境功能，PreceivedType 屬性
topic_type:
- apiref
api_name:
- IResultType.PreceivedType
- IResultType.get_PreceivedType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b058105af254403c3b733f484d7c49a9ac5a0da3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843372"
---
# <a name="iresulttypepreceivedtype-property"></a><span data-ttu-id="fb3bd-106">IResultType：:P receivedType 屬性</span><span class="sxs-lookup"><span data-stu-id="fb3bd-106">IResultType::PreceivedType property</span></span>

> [!NOTE]
> <span data-ttu-id="fb3bd-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="fb3bd-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="fb3bd-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="fb3bd-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="fb3bd-109">這個屬性包含用來識別索引中之類型的字串。</span><span class="sxs-lookup"><span data-stu-id="fb3bd-109">This property contains the string used to identify the type in the index.</span></span>

<span data-ttu-id="fb3bd-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="fb3bd-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3bd-111">語法</span><span class="sxs-lookup"><span data-stu-id="fb3bd-111">Syntax</span></span>


```C++
HRESULT get_PreceivedType(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="fb3bd-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="fb3bd-112">Property value</span></span>

<span data-ttu-id="fb3bd-113">傳回在索引中 identifyint 類型之字串的位址。</span><span class="sxs-lookup"><span data-stu-id="fb3bd-113">returns the address of the string identifyint the type in the index.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb3bd-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb3bd-114">Requirements</span></span>



| <span data-ttu-id="fb3bd-115">需求</span><span class="sxs-lookup"><span data-stu-id="fb3bd-115">Requirement</span></span> | <span data-ttu-id="fb3bd-116">值</span><span class="sxs-lookup"><span data-stu-id="fb3bd-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3bd-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb3bd-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fb3bd-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb3bd-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fb3bd-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb3bd-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fb3bd-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb3bd-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fb3bd-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="fb3bd-121">Redistributable</span></span><br/>          | <span data-ttu-id="fb3bd-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="fb3bd-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="fb3bd-123">標頭</span><span class="sxs-lookup"><span data-stu-id="fb3bd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb3bd-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="fb3bd-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





