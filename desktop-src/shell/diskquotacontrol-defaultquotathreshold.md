---
description: 設定或取得預設配額閾值。
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: DiskQuotaControl. DefaultQuotaThreshold 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a4ce4205ee8bcc73c78bd1aabe7d8659ac3f5489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971969"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a><span data-ttu-id="2f11d-103">DiskQuotaControl. DefaultQuotaThreshold 屬性</span><span class="sxs-lookup"><span data-stu-id="2f11d-103">DiskQuotaControl.DefaultQuotaThreshold property</span></span>

<span data-ttu-id="2f11d-104">設定或取得預設配額閾值。</span><span class="sxs-lookup"><span data-stu-id="2f11d-104">Sets or gets the default quota threshold.</span></span>

<span data-ttu-id="2f11d-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f11d-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f11d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f11d-106">Syntax</span></span>


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="2f11d-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="2f11d-107">Property value</span></span>

<span data-ttu-id="2f11d-108">設定為新使用者預設警告臨界值的 **整數** 值（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="2f11d-108">An **Integer** value that is set to the default warning threshold for new users, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f11d-109">備註</span><span class="sxs-lookup"><span data-stu-id="2f11d-109">Remarks</span></span>

<span data-ttu-id="2f11d-110">預設配額閾值會自動套用到磁片區的新使用者。</span><span class="sxs-lookup"><span data-stu-id="2f11d-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="2f11d-111">如果使用者的磁片使用量超過此值，且 [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) 屬性設定為 **TRUE**，則系統會產生事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="2f11d-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="2f11d-112">例如，如果預設閾值為 10.0 MB，則屬性的值為 "10.0 MB"。</span><span class="sxs-lookup"><span data-stu-id="2f11d-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="2f11d-113">如果磁片區沒有預設閾值，屬性會設定為「沒有限制」或當地語系化的對等專案。</span><span class="sxs-lookup"><span data-stu-id="2f11d-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f11d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f11d-114">Requirements</span></span>



| <span data-ttu-id="2f11d-115">需求</span><span class="sxs-lookup"><span data-stu-id="2f11d-115">Requirement</span></span> | <span data-ttu-id="2f11d-116">值</span><span class="sxs-lookup"><span data-stu-id="2f11d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f11d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f11d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2f11d-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f11d-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2f11d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f11d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2f11d-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f11d-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2f11d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2f11d-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f11d-122"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="2f11d-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f11d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f11d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f11d-124">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="2f11d-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




