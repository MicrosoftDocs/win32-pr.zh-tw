---
description: 抓取裝置的連接狀態。 這個屬性只適用于) 的裝置 (根專案類型專案。 可能的值為 &\# 0034; 連接的&\# 0034;、&\# 0034; 中斷連接&\# 0034; 或 Null (如果這個屬性不會套用至專案) 。 唯讀。
ms.assetid: 44b1713a-5859-4973-8495-e8a67f2344b2
title: ConnectStatus 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ConnectStatus
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 48e12c35ad98746f5a263680e74a09c814bbc65a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971806"
---
# <a name="itemconnectstatus-property"></a><span data-ttu-id="8b628-106">ConnectStatus 屬性</span><span class="sxs-lookup"><span data-stu-id="8b628-106">Item.ConnectStatus property</span></span>

<span data-ttu-id="8b628-107">抓取裝置的連接狀態。</span><span class="sxs-lookup"><span data-stu-id="8b628-107">Retrieves the connection status of the device.</span></span> <span data-ttu-id="8b628-108">這個屬性只適用于) 的裝置 (根專案類型專案。</span><span class="sxs-lookup"><span data-stu-id="8b628-108">This property applies only to items of type device (root items).</span></span> <span data-ttu-id="8b628-109">如果這個屬性不會套用至專案) ，可能的值為「已連線」、「已中斷連線」或 **Null** (。</span><span class="sxs-lookup"><span data-stu-id="8b628-109">Possible values are "connected", "disconnected", or **NULL** (if this property does not apply to the item).</span></span> <span data-ttu-id="8b628-110">唯讀。</span><span class="sxs-lookup"><span data-stu-id="8b628-110">Read-only.</span></span>

<span data-ttu-id="8b628-111">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="8b628-111">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b628-112">語法</span><span class="sxs-lookup"><span data-stu-id="8b628-112">Syntax</span></span>


```JScript
propVal = Item.ConnectStatus
```



## <a name="property-value"></a><span data-ttu-id="8b628-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="8b628-113">Property value</span></span>

<span data-ttu-id="8b628-114">接收連接狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="8b628-114">String that receives the connection status.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b628-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="8b628-115">Requirements</span></span>



| <span data-ttu-id="8b628-116">需求</span><span class="sxs-lookup"><span data-stu-id="8b628-116">Requirement</span></span> | <span data-ttu-id="8b628-117">值</span><span class="sxs-lookup"><span data-stu-id="8b628-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b628-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8b628-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8b628-119">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b628-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b628-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8b628-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8b628-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8b628-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8b628-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8b628-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b628-123"><dt>Wiascr.dll (4.90 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="8b628-123"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




