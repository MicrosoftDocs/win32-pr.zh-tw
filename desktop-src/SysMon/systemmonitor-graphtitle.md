---
title: SystemMonitor. GraphTitle 屬性
description: 抓取或設定圖形的標題。
ms.assetid: 10a91b38-6963-4ef6-8b4f-9ecd1341f471
keywords:
- GraphTitle 屬性 SysMon
- GraphTitle 屬性 SysMon、SystemMonitor 類別
- SystemMonitor 類別 SysMon，GraphTitle 屬性
topic_type:
- apiref
api_name:
- SystemMonitor.GraphTitle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55918b67eb88b8c2c1aca99ce6e86f190ad1a395
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508587"
---
# <a name="systemmonitorgraphtitle-property"></a><span data-ttu-id="6d58a-106">SystemMonitor. GraphTitle 屬性</span><span class="sxs-lookup"><span data-stu-id="6d58a-106">SystemMonitor.GraphTitle property</span></span>

<span data-ttu-id="6d58a-107">抓取或設定圖形的標題。</span><span class="sxs-lookup"><span data-stu-id="6d58a-107">Retrieves or sets the title of the graph.</span></span>

<span data-ttu-id="6d58a-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6d58a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d58a-109">語法</span><span class="sxs-lookup"><span data-stu-id="6d58a-109">Syntax</span></span>


```VB
Property GraphTitle As String
```



## <a name="property-value"></a><span data-ttu-id="6d58a-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="6d58a-110">Property value</span></span>

<span data-ttu-id="6d58a-111">圖形的標題。</span><span class="sxs-lookup"><span data-stu-id="6d58a-111">Title of the graph.</span></span> <span data-ttu-id="6d58a-112">標題的長度上限為128個字元。</span><span class="sxs-lookup"><span data-stu-id="6d58a-112">The maximum length of the title is 128 characters.</span></span> <span data-ttu-id="6d58a-113">如果標題超過128個字元，則會截斷標題。</span><span class="sxs-lookup"><span data-stu-id="6d58a-113">If the title exceeds 128 characters, the title is truncated.</span></span>

<span data-ttu-id="6d58a-114">**WINDOWS XP 和 windows 2000：** 標題的長度沒有限制。</span><span class="sxs-lookup"><span data-stu-id="6d58a-114">**Windows XP and Windows 2000:** There is no limit to the length of the title.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d58a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d58a-115">Requirements</span></span>



| <span data-ttu-id="6d58a-116">需求</span><span class="sxs-lookup"><span data-stu-id="6d58a-116">Requirement</span></span> | <span data-ttu-id="6d58a-117">值</span><span class="sxs-lookup"><span data-stu-id="6d58a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6d58a-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6d58a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6d58a-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d58a-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="6d58a-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6d58a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6d58a-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6d58a-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6d58a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6d58a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d58a-123"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="6d58a-123"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d58a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d58a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d58a-125">**SystemMonitor**</span><span class="sxs-lookup"><span data-stu-id="6d58a-125">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





