---
title: 'IResultType GetProperty 屬性 (WdsSharedIDL .h) '
description: 此屬性包含指定的屬性資訊。
ms.assetid: 04c810f2-c781-4384-93ae-1060466e2bc4
keywords:
- GetProperty 屬性舊版 Windows 環境功能
- GetProperty 屬性舊版 Windows 環境功能，IResultType 介面
- IResultType 介面舊版 Windows 環境功能，GetProperty 屬性
topic_type:
- apiref
api_name:
- IResultType.GetProperty
- IResultType.get_GetProperty
- IResultType.put_GetProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd62517e7db9fdc15841c443ba9010903ddea697
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843375"
---
# <a name="iresulttypegetproperty-property"></a><span data-ttu-id="7b192-106">IResultType：： GetProperty 屬性</span><span class="sxs-lookup"><span data-stu-id="7b192-106">IResultType::GetProperty property</span></span>

> [!NOTE]
> <span data-ttu-id="7b192-107">Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。</span><span class="sxs-lookup"><span data-stu-id="7b192-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="7b192-108">在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。</span><span class="sxs-lookup"><span data-stu-id="7b192-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="7b192-109">此屬性包含指定的屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="7b192-109">This property contains specified property information.</span></span>

<span data-ttu-id="7b192-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="7b192-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b192-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b192-111">Syntax</span></span>


```C++
HRESULT put_GetProperty(
  [in]          VARIANT        index
);

HRESULT get_GetProperty(
  [out, retval] ISrsultPropery **prop
);
```



## <a name="property-value"></a><span data-ttu-id="7b192-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="7b192-112">Property value</span></span>

<span data-ttu-id="7b192-113">設定指定之屬性資訊的位址。</span><span class="sxs-lookup"><span data-stu-id="7b192-113">Sets the address of the specified property information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b192-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b192-114">Requirements</span></span>



| <span data-ttu-id="7b192-115">需求</span><span class="sxs-lookup"><span data-stu-id="7b192-115">Requirement</span></span> | <span data-ttu-id="7b192-116">值</span><span class="sxs-lookup"><span data-stu-id="7b192-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b192-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7b192-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7b192-118">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b192-118">Windows XP with SP2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="7b192-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7b192-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7b192-120">僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7b192-120">Windows Server 2003 with SP1 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7b192-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7b192-121">Redistributable</span></span><br/>          | <span data-ttu-id="7b192-122">Windows 桌面搜尋 (WDS) 2.6。5</span><span class="sxs-lookup"><span data-stu-id="7b192-122">Windows Desktop Search (WDS) 2.6.5</span></span><br/>                                             |
| <span data-ttu-id="7b192-123">標頭</span><span class="sxs-lookup"><span data-stu-id="7b192-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b192-124"><dt>WdsSharedIDL。h</dt></span><span class="sxs-lookup"><span data-stu-id="7b192-124"><dt>WdsSharedIDL.h</dt></span></span> </dl> |



 

 





