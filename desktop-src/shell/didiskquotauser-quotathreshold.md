---
description: 設定或取得使用者的警告臨界值（以位元組為單位）。
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: DIDiskQuotaUser. QuotaThreshold 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7ce336c84d086c4e4be369278a77e40e59474bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847789"
---
# <a name="didiskquotauserquotathreshold-property"></a><span data-ttu-id="2b750-103">DIDiskQuotaUser. QuotaThreshold 屬性</span><span class="sxs-lookup"><span data-stu-id="2b750-103">DIDiskQuotaUser.QuotaThreshold property</span></span>

<span data-ttu-id="2b750-104">設定或取得使用者的警告臨界值（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2b750-104">Sets or gets the user's warning threshold, in bytes.</span></span>

<span data-ttu-id="2b750-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2b750-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b750-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2b750-106">Syntax</span></span>


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="2b750-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="2b750-107">Property value</span></span>

<span data-ttu-id="2b750-108">指定或接收使用者之警告臨界值的 **整數** 值。</span><span class="sxs-lookup"><span data-stu-id="2b750-108">An **Integer** value that specifies or receives the user's warning threshold.</span></span> <span data-ttu-id="2b750-109">如果使用者的磁片使用量超過此值，且 [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) 屬性設定為 **TRUE**，則系統會產生事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="2b750-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b750-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b750-110">Requirements</span></span>



| <span data-ttu-id="2b750-111">需求</span><span class="sxs-lookup"><span data-stu-id="2b750-111">Requirement</span></span> | <span data-ttu-id="2b750-112">值</span><span class="sxs-lookup"><span data-stu-id="2b750-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b750-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b750-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2b750-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b750-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2b750-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b750-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2b750-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b750-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2b750-117">DLL</span><span class="sxs-lookup"><span data-stu-id="2b750-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b750-118"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2b750-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b750-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b750-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b750-120">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="2b750-120">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="2b750-121">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="2b750-121">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="2b750-122">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="2b750-122">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="2b750-123">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="2b750-123">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




