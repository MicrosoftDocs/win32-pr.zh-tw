---
title: 'IResultVerb Name 屬性 (WdsSharedIDL .h) '
description: 這個屬性會傳回動詞的 cononical 名稱指標，例如 print、open 等等。
ms.assetid: e911ef1c-0ac9-4b70-a3af-c05e42bd1f0f
keywords:
- 名稱屬性舊版 Windows 環境功能
- Name 屬性舊版 Windows 環境功能，IResultVerb 介面
- IResultVerb 介面舊版 Windows 環境功能，名稱屬性
topic_type:
- apiref
api_name:
- IResultVerb.Name
- IResultVerb.get_Name
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2c831ea0dad36f733995062d8a76fc27d4cc837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933971"
---
# <a name="iresultverbname-property"></a><span data-ttu-id="9a7be-106">IResultVerb：： Name 屬性</span><span class="sxs-lookup"><span data-stu-id="9a7be-106">IResultVerb::Name property</span></span>

> [!NOTE]
> <span data-ttu-id="9a7be-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="9a7be-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="9a7be-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="9a7be-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="9a7be-109">這個屬性會傳回動詞的 cononical 名稱指標，例如 print、open 等等。</span><span class="sxs-lookup"><span data-stu-id="9a7be-109">This property returns a pointer to the cononical name for the verb such as print, open, etc.</span></span>

<span data-ttu-id="9a7be-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9a7be-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7be-111">語法</span><span class="sxs-lookup"><span data-stu-id="9a7be-111">Syntax</span></span>


```C++
HRESULT get_Name(
  [out, retval] BSTR *name
);
```



## <a name="property-value"></a><span data-ttu-id="9a7be-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="9a7be-112">Property value</span></span>

<span data-ttu-id="9a7be-113">名稱是動詞 cononical 名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="9a7be-113">name is a pointer to the cononical name for the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a7be-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9a7be-114">Requirements</span></span>



| <span data-ttu-id="9a7be-115">需求</span><span class="sxs-lookup"><span data-stu-id="9a7be-115">Requirement</span></span> | <span data-ttu-id="9a7be-116">值</span><span class="sxs-lookup"><span data-stu-id="9a7be-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7be-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9a7be-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9a7be-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a7be-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9a7be-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9a7be-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9a7be-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9a7be-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9a7be-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9a7be-121">Redistributable</span></span><br/>          | <span data-ttu-id="9a7be-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="9a7be-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="9a7be-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9a7be-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a7be-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="9a7be-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





