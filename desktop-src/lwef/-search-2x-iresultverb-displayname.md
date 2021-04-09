---
title: 'IResultVerb DisplayName 屬性 (WdsSharedIDL .h) '
description: 這個屬性會傳回動詞之當地語系化顯示名稱的指標。
ms.assetid: f1f4a30e-ecfb-4091-b9cd-312e427d0eb4
keywords:
- DisplayName 屬性舊版 Windows 環境功能
- DisplayName 屬性舊版 Windows 環境功能，IResultVerb 介面
- IResultVerb 介面舊版 Windows 環境功能，DisplayName 屬性
topic_type:
- apiref
api_name:
- IResultVerb.DisplayName
- IResultVerb.get_DisplayName
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721831274fc87ee65c8ee1655fdb7b38f80e1114
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024949"
---
# <a name="iresultverbdisplayname-property"></a><span data-ttu-id="9d034-106">IResultVerb：:D isplayName 屬性</span><span class="sxs-lookup"><span data-stu-id="9d034-106">IResultVerb::DisplayName property</span></span>

> [!NOTE]
> <span data-ttu-id="9d034-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="9d034-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="9d034-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="9d034-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="9d034-109">這個屬性會傳回動詞之當地語系化顯示名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="9d034-109">This property returns a pointer to the localized display name for the verb.</span></span>

<span data-ttu-id="9d034-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9d034-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d034-111">語法</span><span class="sxs-lookup"><span data-stu-id="9d034-111">Syntax</span></span>


```C++
HRESULT get_DisplayName(
  [out, retval] BSTR *Verb
);
```



## <a name="property-value"></a><span data-ttu-id="9d034-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="9d034-112">Property value</span></span>

<span data-ttu-id="9d034-113">這個屬性會傳回動詞之當地語系化顯示名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="9d034-113">This property returns a pointer to the localized display name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d034-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d034-114">Requirements</span></span>



| <span data-ttu-id="9d034-115">需求</span><span class="sxs-lookup"><span data-stu-id="9d034-115">Requirement</span></span> | <span data-ttu-id="9d034-116">值</span><span class="sxs-lookup"><span data-stu-id="9d034-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d034-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d034-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9d034-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d034-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9d034-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d034-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9d034-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d034-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9d034-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9d034-121">Redistributable</span></span><br/>          | <span data-ttu-id="9d034-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="9d034-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="9d034-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9d034-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d034-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d034-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





