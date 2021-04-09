---
title: 'IResultVerb Enabled 屬性 (WdsSharedIDL .h) '
description: 如果已啟用動詞，這個屬性會傳回 TRUE。
ms.assetid: 27e3dbb8-678e-46c7-82e5-40b86cb157a7
keywords:
- 已啟用屬性舊版 Windows 環境功能
- 已啟用屬性舊版 Windows 環境功能，IResultVerb 介面
- IResultVerb 介面舊版 Windows 環境功能，Enabled 屬性
topic_type:
- apiref
api_name:
- IResultVerb.Enabled
- IResultVerb.get_Enabled
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8570e7bbb06843467080dd0dd748391234f259d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934648"
---
# <a name="iresultverbenabled-property"></a><span data-ttu-id="9e28f-106">IResultVerb：： Enabled 屬性</span><span class="sxs-lookup"><span data-stu-id="9e28f-106">IResultVerb::Enabled property</span></span>

> [!NOTE]
> <span data-ttu-id="9e28f-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="9e28f-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="9e28f-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="9e28f-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="9e28f-109">如果已啟用動詞，這個屬性會傳回 TRUE。</span><span class="sxs-lookup"><span data-stu-id="9e28f-109">This property returns TRUE if the verb is enabled.</span></span>

<span data-ttu-id="9e28f-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9e28f-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e28f-111">語法</span><span class="sxs-lookup"><span data-stu-id="9e28f-111">Syntax</span></span>


```C++
HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *flag
);
```



## <a name="property-value"></a><span data-ttu-id="9e28f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="9e28f-112">Property value</span></span>

<span data-ttu-id="9e28f-113">如果已啟用動詞，這個屬性會傳回 True，否則會傳回 False。</span><span class="sxs-lookup"><span data-stu-id="9e28f-113">This property returns True if the verb is enabled or False if not.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e28f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9e28f-114">Requirements</span></span>



| <span data-ttu-id="9e28f-115">需求</span><span class="sxs-lookup"><span data-stu-id="9e28f-115">Requirement</span></span> | <span data-ttu-id="9e28f-116">值</span><span class="sxs-lookup"><span data-stu-id="9e28f-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e28f-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9e28f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9e28f-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e28f-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9e28f-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9e28f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9e28f-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9e28f-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9e28f-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9e28f-121">Redistributable</span></span><br/>          | <span data-ttu-id="9e28f-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="9e28f-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="9e28f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="9e28f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e28f-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="9e28f-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





