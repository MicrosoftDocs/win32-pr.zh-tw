---
description: 取得使用者的警告臨界值做為文字字串。
ms.assetid: 55b53ad0-e7cd-4417-9087-297ac96e245f
title: DIDiskQuotaUser. QuotaThresholdText 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 511829233b93dbe164ce2feccd1247ccebf3ec3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971981"
---
# <a name="didiskquotauserquotathresholdtext-property"></a><span data-ttu-id="07c83-103">DIDiskQuotaUser. QuotaThresholdText 屬性</span><span class="sxs-lookup"><span data-stu-id="07c83-103">DIDiskQuotaUser.QuotaThresholdText property</span></span>

<span data-ttu-id="07c83-104">取得使用者的警告臨界值做為文字字串。</span><span class="sxs-lookup"><span data-stu-id="07c83-104">Gets the user's warning threshold as a text string.</span></span>

<span data-ttu-id="07c83-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="07c83-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c83-106">語法</span><span class="sxs-lookup"><span data-stu-id="07c83-106">Syntax</span></span>


```JScript
QuotaThresholdText = DIDiskQuotaUser.QuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="07c83-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="07c83-107">Property value</span></span>

<span data-ttu-id="07c83-108">包含使用者之警告臨界值的字串值。</span><span class="sxs-lookup"><span data-stu-id="07c83-108">The string value that contains the user's warning threshold.</span></span> <span data-ttu-id="07c83-109">如果使用者的磁片使用量超過此值，且 [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) 屬性設定為 **TRUE**，則系統會產生事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="07c83-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c83-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="07c83-110">Requirements</span></span>



| <span data-ttu-id="07c83-111">需求</span><span class="sxs-lookup"><span data-stu-id="07c83-111">Requirement</span></span> | <span data-ttu-id="07c83-112">值</span><span class="sxs-lookup"><span data-stu-id="07c83-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c83-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07c83-113">Minimum supported client</span></span><br/> | <span data-ttu-id="07c83-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07c83-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07c83-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07c83-115">Minimum supported server</span></span><br/> | <span data-ttu-id="07c83-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07c83-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="07c83-117">DLL</span><span class="sxs-lookup"><span data-stu-id="07c83-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07c83-118"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="07c83-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c83-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07c83-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c83-120">**IDiskQuotaUser 物件**</span><span class="sxs-lookup"><span data-stu-id="07c83-120">**IDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="07c83-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="07c83-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="07c83-122">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="07c83-122">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="07c83-123">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="07c83-123">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> </dl>

 

 




