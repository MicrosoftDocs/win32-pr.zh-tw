---
description: 公開方法，這些方法可用來初始化自動完成物件的最近使用 (MRU) 清單。
title: IACLCustomMRU 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU
api_type:
- COM
api_location: ''
ms.assetid: 6ebf64da-9eba-4ea7-91aa-242474097be1
ms.openlocfilehash: 54cda8d6cc3c7f1c46d6bce7736160b0da67a4c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991535"
---
# <a name="iaclcustommru-interface"></a><span data-ttu-id="01bb4-103">IACLCustomMRU 介面</span><span class="sxs-lookup"><span data-stu-id="01bb4-103">IACLCustomMRU interface</span></span>

<span data-ttu-id="01bb4-104">公開方法，這些方法可用來初始化自動完成物件的最近使用 (MRU) 清單。</span><span class="sxs-lookup"><span data-stu-id="01bb4-104">Exposes methods that are used to initialize a most recently used (MRU) list for an autocompletion object.</span></span>

## <a name="members"></a><span data-ttu-id="01bb4-105">成員</span><span class="sxs-lookup"><span data-stu-id="01bb4-105">Members</span></span>

<span data-ttu-id="01bb4-106">**IACLCustomMRU** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="01bb4-106">The **IACLCustomMRU** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="01bb4-107">**IACLCustomMRU** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="01bb4-107">**IACLCustomMRU** also has these types of members:</span></span>

-   [<span data-ttu-id="01bb4-108">方法</span><span class="sxs-lookup"><span data-stu-id="01bb4-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="01bb4-109">方法</span><span class="sxs-lookup"><span data-stu-id="01bb4-109">Methods</span></span>

<span data-ttu-id="01bb4-110">**IACLCustomMRU** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="01bb4-110">The **IACLCustomMRU** interface has these methods.</span></span>



| <span data-ttu-id="01bb4-111">方法</span><span class="sxs-lookup"><span data-stu-id="01bb4-111">Method</span></span>                                             | <span data-ttu-id="01bb4-112">描述</span><span class="sxs-lookup"><span data-stu-id="01bb4-112">Description</span></span>                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="01bb4-113">**AddMRUString**</span><span class="sxs-lookup"><span data-stu-id="01bb4-113">**AddMRUString**</span></span>](iaclcustommru-addmrustring.md) | <span data-ttu-id="01bb4-114">將專案加入至 MRU 清單。</span><span class="sxs-lookup"><span data-stu-id="01bb4-114">Adds an entry to the MRU list.</span></span><br/>                               |
| [<span data-ttu-id="01bb4-115">**初始化**</span><span class="sxs-lookup"><span data-stu-id="01bb4-115">**Initialize**</span></span>](iaclcustommru-initialize.md)     | <span data-ttu-id="01bb4-116">從登錄將字串清單載入至 MRU 清單。</span><span class="sxs-lookup"><span data-stu-id="01bb4-116">Loads a list of strings into the MRU list from the registry.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="01bb4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="01bb4-117">Requirements</span></span>



| <span data-ttu-id="01bb4-118">需求</span><span class="sxs-lookup"><span data-stu-id="01bb4-118">Requirement</span></span> | <span data-ttu-id="01bb4-119">值</span><span class="sxs-lookup"><span data-stu-id="01bb4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="01bb4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="01bb4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="01bb4-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01bb4-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="01bb4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="01bb4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="01bb4-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="01bb4-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
