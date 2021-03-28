---
description: 以文字字串形式取得使用者的目前磁片使用量。
title: DIDiskQuotaUser. QuotaUsedText 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: 1091d7f2d75b264b085c09af1873ac7c8ebd1617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971976"
---
# <a name="didiskquotauserquotausedtext-property"></a><span data-ttu-id="15749-103">DIDiskQuotaUser. QuotaUsedText 屬性</span><span class="sxs-lookup"><span data-stu-id="15749-103">DIDiskQuotaUser.QuotaUsedText property</span></span>

<span data-ttu-id="15749-104">以文字字串形式取得使用者的目前磁片使用量。</span><span class="sxs-lookup"><span data-stu-id="15749-104">Gets the user's current disk usage as a text string.</span></span>

<span data-ttu-id="15749-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="15749-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="15749-106">語法</span><span class="sxs-lookup"><span data-stu-id="15749-106">Syntax</span></span>


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a><span data-ttu-id="15749-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="15749-107">Property value</span></span>

<span data-ttu-id="15749-108">字串值，設定為目前使用中的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="15749-108">A string value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="15749-109">如果 NTFS 檔案壓縮已啟用，此屬性會反映資料在未壓縮狀態中所需的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="15749-109">If NTFS file compression is enabled, this property reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="15749-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="15749-110">Requirements</span></span>



| <span data-ttu-id="15749-111">需求</span><span class="sxs-lookup"><span data-stu-id="15749-111">Requirement</span></span> | <span data-ttu-id="15749-112">值</span><span class="sxs-lookup"><span data-stu-id="15749-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15749-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="15749-113">Minimum supported client</span></span><br/> | <span data-ttu-id="15749-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15749-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15749-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="15749-115">Minimum supported server</span></span><br/> | <span data-ttu-id="15749-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="15749-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="15749-117">DLL</span><span class="sxs-lookup"><span data-stu-id="15749-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15749-118"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="15749-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15749-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="15749-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15749-120">**DIDiskQuotaUser 物件**</span><span class="sxs-lookup"><span data-stu-id="15749-120">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="15749-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="15749-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="15749-122">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="15749-122">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[<span data-ttu-id="15749-123">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="15749-123">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




