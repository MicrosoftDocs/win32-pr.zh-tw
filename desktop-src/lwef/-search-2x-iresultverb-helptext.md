---
title: 'IResultVerb HelpText 屬性 (WdsSharedIDL .h) '
description: 這個屬性會傳回動詞的當地語系化說明字串指標。
ms.assetid: 14e91101-5ee2-459a-97d7-35c76d3ba990
keywords:
- HelpText 屬性舊版 Windows 環境功能
- HelpText 屬性舊版 Windows 環境功能，IResultVerb 介面
- IResultVerb 介面舊版 Windows 環境功能，HelpText 屬性
topic_type:
- apiref
api_name:
- IResultVerb.HelpText
- IResultVerb.get_HelpText
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a0615ea9cc62f3a5f207e7be2c2c4e80987239c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685791"
---
# <a name="iresultverbhelptext-property"></a><span data-ttu-id="41b43-106">IResultVerb：： HelpText 屬性</span><span class="sxs-lookup"><span data-stu-id="41b43-106">IResultVerb::HelpText property</span></span>

> [!NOTE]
> <span data-ttu-id="41b43-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="41b43-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="41b43-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="41b43-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="41b43-109">這個屬性會傳回動詞的當地語系化說明字串指標。</span><span class="sxs-lookup"><span data-stu-id="41b43-109">This property returns a pointer to the localized help string for the verb.</span></span>

<span data-ttu-id="41b43-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="41b43-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="41b43-111">語法</span><span class="sxs-lookup"><span data-stu-id="41b43-111">Syntax</span></span>


```C++
HRESULT get_HelpText(
  [out, retval] BSTR *text
);
```



## <a name="property-value"></a><span data-ttu-id="41b43-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="41b43-112">Property value</span></span>

<span data-ttu-id="41b43-113">這個屬性的值是此動詞命令之當地語系化說明字串的指標。</span><span class="sxs-lookup"><span data-stu-id="41b43-113">The value of this property is a pointer to the localized help string for this verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="41b43-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="41b43-114">Requirements</span></span>



| <span data-ttu-id="41b43-115">需求</span><span class="sxs-lookup"><span data-stu-id="41b43-115">Requirement</span></span> | <span data-ttu-id="41b43-116">值</span><span class="sxs-lookup"><span data-stu-id="41b43-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b43-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41b43-117">Minimum supported client</span></span><br/> | <span data-ttu-id="41b43-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41b43-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="41b43-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41b43-119">Minimum supported server</span></span><br/> | <span data-ttu-id="41b43-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41b43-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="41b43-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="41b43-121">Redistributable</span></span><br/>          | <span data-ttu-id="41b43-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="41b43-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="41b43-123">標頭</span><span class="sxs-lookup"><span data-stu-id="41b43-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="41b43-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="41b43-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





