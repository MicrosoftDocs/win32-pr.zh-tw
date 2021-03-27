---
description: 設定或取得布林值，這個值會指出當使用者超過其指派的配額限制時，是否要建立系統事件記錄檔專案。
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: DiskQuotaControl. LogQuotaLimit 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3db64d7fb06ed8bfb7ba8c2483eb413f3f01a224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971957"
---
# <a name="diskquotacontrollogquotalimit-property"></a><span data-ttu-id="6b0d0-103">DiskQuotaControl. LogQuotaLimit 屬性</span><span class="sxs-lookup"><span data-stu-id="6b0d0-103">DiskQuotaControl.LogQuotaLimit property</span></span>

<span data-ttu-id="6b0d0-104">設定或取得布林值，這個值會指出當使用者超過其指派的配額限制時，是否要建立系統事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="6b0d0-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span>

<span data-ttu-id="6b0d0-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="6b0d0-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b0d0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b0d0-106">Syntax</span></span>


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="6b0d0-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="6b0d0-107">Property value</span></span>

<span data-ttu-id="6b0d0-108">如果使用者超過配額限制，則會將此屬性設定為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6b0d0-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota limit, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b0d0-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b0d0-109">Requirements</span></span>



| <span data-ttu-id="6b0d0-110">需求</span><span class="sxs-lookup"><span data-stu-id="6b0d0-110">Requirement</span></span> | <span data-ttu-id="6b0d0-111">值</span><span class="sxs-lookup"><span data-stu-id="6b0d0-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b0d0-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b0d0-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6b0d0-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b0d0-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b0d0-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b0d0-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6b0d0-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b0d0-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6b0d0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="6b0d0-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b0d0-117"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="6b0d0-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b0d0-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b0d0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b0d0-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="6b0d0-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="6b0d0-120">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="6b0d0-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="6b0d0-121">**LogQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="6b0d0-121">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




