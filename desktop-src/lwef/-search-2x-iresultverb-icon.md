---
title: 'IResultVerb 圖示屬性 (WdsSharedIDL .h) '
description: 這個屬性會傳回與動詞相關聯之選擇性圖示的控制碼指標。
ms.assetid: 19de0e36-b453-48a4-8ac0-f26432e088ae
keywords:
- Icon 屬性舊版 Windows 環境功能
- Icon 屬性舊版 Windows 環境功能，IResultVerb 介面
- IResultVerb 介面舊版 Windows 環境功能，Icon 屬性
topic_type:
- apiref
api_name:
- IResultVerb.Icon
- IResultVerb.get_Icon
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2babd2a9e45f1d038d5f7ce567eeaaf37e1f29f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465941"
---
# <a name="iresultverbicon-property"></a><span data-ttu-id="6bab5-106">IResultVerb：： Icon 屬性</span><span class="sxs-lookup"><span data-stu-id="6bab5-106">IResultVerb::Icon property</span></span>

> [!NOTE]
> <span data-ttu-id="6bab5-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="6bab5-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="6bab5-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="6bab5-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="6bab5-109">這個屬性會傳回與動詞相關聯之選擇性圖示的控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="6bab5-109">This property returns a pointer to handle of the optional icon associated with the verb.</span></span>

<span data-ttu-id="6bab5-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6bab5-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bab5-111">語法</span><span class="sxs-lookup"><span data-stu-id="6bab5-111">Syntax</span></span>


```C++
HRESULT get_Icon(
  [out, retval] SHANDLE_PTR *hicon
);
```



## <a name="property-value"></a><span data-ttu-id="6bab5-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="6bab5-112">Property value</span></span>

<span data-ttu-id="6bab5-113">hicon 是以動詞命令 assocuated 之選擇性圖示的控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="6bab5-113">hicon is a pointer to the handle of the optional icon assocuated with the verb.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bab5-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bab5-114">Requirements</span></span>



| <span data-ttu-id="6bab5-115">需求</span><span class="sxs-lookup"><span data-stu-id="6bab5-115">Requirement</span></span> | <span data-ttu-id="6bab5-116">值</span><span class="sxs-lookup"><span data-stu-id="6bab5-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6bab5-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6bab5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6bab5-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bab5-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6bab5-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6bab5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6bab5-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bab5-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6bab5-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6bab5-121">Redistributable</span></span><br/>          | <span data-ttu-id="6bab5-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="6bab5-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="6bab5-123">標頭</span><span class="sxs-lookup"><span data-stu-id="6bab5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6bab5-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="6bab5-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





