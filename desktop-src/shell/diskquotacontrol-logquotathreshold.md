---
description: 設定或取得布林值，這個值會指出當使用者超過其指派的配額閾值時，是否要建立系統事件記錄檔專案。
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: DiskQuotaControl. LogQuotaThreshold 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fbbf83ae978e46a3867d27c23e8b8f726ba0d7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971956"
---
# <a name="diskquotacontrollogquotathreshold-property"></a><span data-ttu-id="f6e6f-103">DiskQuotaControl. LogQuotaThreshold 屬性</span><span class="sxs-lookup"><span data-stu-id="f6e6f-103">DiskQuotaControl.LogQuotaThreshold property</span></span>

<span data-ttu-id="f6e6f-104">設定或取得布林值，這個值會指出當使用者超過其指派的配額閾值時，是否要建立系統事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="f6e6f-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span>

<span data-ttu-id="f6e6f-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="f6e6f-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e6f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6e6f-106">Syntax</span></span>


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="f6e6f-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="f6e6f-107">Property value</span></span>

<span data-ttu-id="f6e6f-108">如果使用者超過其配額警告臨界值，則此屬性會設定為 TRUE，否則會設為 **TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="f6e6f-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota warning threshold, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6e6f-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6e6f-109">Requirements</span></span>



| <span data-ttu-id="f6e6f-110">需求</span><span class="sxs-lookup"><span data-stu-id="f6e6f-110">Requirement</span></span> | <span data-ttu-id="f6e6f-111">值</span><span class="sxs-lookup"><span data-stu-id="f6e6f-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e6f-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6e6f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f6e6f-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6e6f-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6e6f-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6e6f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f6e6f-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6e6f-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f6e6f-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f6e6f-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6e6f-117"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="f6e6f-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6e6f-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6e6f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6e6f-119">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="f6e6f-119">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="f6e6f-120">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="f6e6f-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="f6e6f-121">**LogQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="f6e6f-121">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




