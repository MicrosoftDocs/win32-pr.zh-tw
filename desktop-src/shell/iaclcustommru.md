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
ms.openlocfilehash: f47a9df320da5c710c21ddbab83ca87b49c28e12
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842009"
---
# <a name="iaclcustommru-interface"></a><span data-ttu-id="f3b11-103">IACLCustomMRU 介面</span><span class="sxs-lookup"><span data-stu-id="f3b11-103">IACLCustomMRU interface</span></span>

<span data-ttu-id="f3b11-104">公開方法，這些方法可用來初始化自動完成物件的最近使用 (MRU) 清單。</span><span class="sxs-lookup"><span data-stu-id="f3b11-104">Exposes methods that are used to initialize a most recently used (MRU) list for an autocompletion object.</span></span>

## <a name="members"></a><span data-ttu-id="f3b11-105">成員</span><span class="sxs-lookup"><span data-stu-id="f3b11-105">Members</span></span>

<span data-ttu-id="f3b11-106">**IACLCustomMRU** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="f3b11-106">The **IACLCustomMRU** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f3b11-107">**IACLCustomMRU** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f3b11-107">**IACLCustomMRU** also has these types of members:</span></span>

-   [<span data-ttu-id="f3b11-108">方法</span><span class="sxs-lookup"><span data-stu-id="f3b11-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f3b11-109">方法</span><span class="sxs-lookup"><span data-stu-id="f3b11-109">Methods</span></span>

<span data-ttu-id="f3b11-110">**IACLCustomMRU** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f3b11-110">The **IACLCustomMRU** interface has these methods.</span></span>



| <span data-ttu-id="f3b11-111">方法</span><span class="sxs-lookup"><span data-stu-id="f3b11-111">Method</span></span>                                             | <span data-ttu-id="f3b11-112">描述</span><span class="sxs-lookup"><span data-stu-id="f3b11-112">Description</span></span>                                                             |
|:---------------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="f3b11-113">**AddMRUString**</span><span class="sxs-lookup"><span data-stu-id="f3b11-113">**AddMRUString**</span></span>](iaclcustommru-addmrustring.md) | <span data-ttu-id="f3b11-114">將專案加入至 MRU 清單。</span><span class="sxs-lookup"><span data-stu-id="f3b11-114">Adds an entry to the MRU list.</span></span><br/>                               |
| [<span data-ttu-id="f3b11-115">**初始化**</span><span class="sxs-lookup"><span data-stu-id="f3b11-115">**Initialize**</span></span>](iaclcustommru-initialize.md)     | <span data-ttu-id="f3b11-116">從登錄將字串清單載入至 MRU 清單。</span><span class="sxs-lookup"><span data-stu-id="f3b11-116">Loads a list of strings into the MRU list from the registry.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f3b11-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3b11-117">Requirements</span></span>



| <span data-ttu-id="f3b11-118">需求</span><span class="sxs-lookup"><span data-stu-id="f3b11-118">Requirement</span></span> | <span data-ttu-id="f3b11-119">值</span><span class="sxs-lookup"><span data-stu-id="f3b11-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3b11-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3b11-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f3b11-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3b11-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f3b11-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3b11-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f3b11-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3b11-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
