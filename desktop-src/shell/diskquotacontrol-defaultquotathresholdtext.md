---
description: 取得預設配額閾值做為文字字串。
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: DiskQuotaControl. DefaultQuotaThresholdText 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112324"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a><span data-ttu-id="1e49c-103">DiskQuotaControl. DefaultQuotaThresholdText 屬性</span><span class="sxs-lookup"><span data-stu-id="1e49c-103">DiskQuotaControl.DefaultQuotaThresholdText property</span></span>

<span data-ttu-id="1e49c-104">取得預設配額閾值做為文字字串。</span><span class="sxs-lookup"><span data-stu-id="1e49c-104">Gets the default quota threshold as a text string.</span></span>

<span data-ttu-id="1e49c-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1e49c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e49c-106">語法</span><span class="sxs-lookup"><span data-stu-id="1e49c-106">Syntax</span></span>


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="1e49c-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="1e49c-107">Property value</span></span>

<span data-ttu-id="1e49c-108">包含磁片區預設配額閾值的字串值。</span><span class="sxs-lookup"><span data-stu-id="1e49c-108">A string value that contains the default quota threshold for the volume.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e49c-109">備註</span><span class="sxs-lookup"><span data-stu-id="1e49c-109">Remarks</span></span>

<span data-ttu-id="1e49c-110">預設配額閾值會自動套用到磁片區的新使用者。</span><span class="sxs-lookup"><span data-stu-id="1e49c-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="1e49c-111">如果使用者的磁片使用量超過此值，且 [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) 屬性設定為 **TRUE**，則系統會產生事件記錄檔專案。</span><span class="sxs-lookup"><span data-stu-id="1e49c-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="1e49c-112">例如，如果預設閾值為 10.0 MB，則屬性的值為 "10.0 MB"。</span><span class="sxs-lookup"><span data-stu-id="1e49c-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="1e49c-113">如果磁片區沒有預設閾值，屬性會設定為「沒有限制」或當地語系化的對等專案。</span><span class="sxs-lookup"><span data-stu-id="1e49c-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e49c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e49c-114">Requirements</span></span>



| <span data-ttu-id="1e49c-115">需求</span><span class="sxs-lookup"><span data-stu-id="1e49c-115">Requirement</span></span> | <span data-ttu-id="1e49c-116">值</span><span class="sxs-lookup"><span data-stu-id="1e49c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e49c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e49c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1e49c-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e49c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e49c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e49c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1e49c-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e49c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1e49c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="1e49c-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e49c-122"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="1e49c-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e49c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1e49c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e49c-124">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="1e49c-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




