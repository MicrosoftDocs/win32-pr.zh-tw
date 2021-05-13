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
ms.openlocfilehash: bf818bdcd22b734c6f4638a837af97bfecef1695
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843209"
---
# <a name="didiskquotauserquotausedtext-property"></a><span data-ttu-id="ec221-103">DIDiskQuotaUser. QuotaUsedText 屬性</span><span class="sxs-lookup"><span data-stu-id="ec221-103">DIDiskQuotaUser.QuotaUsedText property</span></span>

<span data-ttu-id="ec221-104">以文字字串形式取得使用者的目前磁片使用量。</span><span class="sxs-lookup"><span data-stu-id="ec221-104">Gets the user's current disk usage as a text string.</span></span>

<span data-ttu-id="ec221-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ec221-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec221-106">語法</span><span class="sxs-lookup"><span data-stu-id="ec221-106">Syntax</span></span>


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a><span data-ttu-id="ec221-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="ec221-107">Property value</span></span>

<span data-ttu-id="ec221-108">字串值，設定為目前使用中的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="ec221-108">A string value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="ec221-109">如果 NTFS 檔案壓縮已啟用，此屬性會反映資料在未壓縮狀態中所需的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="ec221-109">If NTFS file compression is enabled, this property reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec221-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec221-110">Requirements</span></span>



| <span data-ttu-id="ec221-111">需求</span><span class="sxs-lookup"><span data-stu-id="ec221-111">Requirement</span></span> | <span data-ttu-id="ec221-112">值</span><span class="sxs-lookup"><span data-stu-id="ec221-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec221-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec221-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ec221-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec221-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ec221-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec221-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ec221-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec221-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ec221-117">DLL</span><span class="sxs-lookup"><span data-stu-id="ec221-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec221-118"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="ec221-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec221-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec221-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec221-120">**DIDiskQuotaUser 物件**</span><span class="sxs-lookup"><span data-stu-id="ec221-120">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="ec221-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="ec221-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="ec221-122">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="ec221-122">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[<span data-ttu-id="ec221-123">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="ec221-123">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




