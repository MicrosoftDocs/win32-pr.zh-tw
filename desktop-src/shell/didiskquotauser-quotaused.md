---
description: 取得使用者目前的磁片使用量（以位元組為單位）。
title: DIDiskQuotaUser. QuotaUsed 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsed
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3e3ade59-b925-4ff5-ae7e-ed97eff506c7
ms.openlocfilehash: 7d5068e6f80fd2b0b435d04583e99da929e17fce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112332"
---
# <a name="didiskquotauserquotaused-property"></a><span data-ttu-id="635c0-103">DIDiskQuotaUser. QuotaUsed 屬性</span><span class="sxs-lookup"><span data-stu-id="635c0-103">DIDiskQuotaUser.QuotaUsed property</span></span>

<span data-ttu-id="635c0-104">取得使用者目前的磁片使用量（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="635c0-104">Gets the user's current disk usage, in bytes.</span></span>

<span data-ttu-id="635c0-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="635c0-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="635c0-106">語法</span><span class="sxs-lookup"><span data-stu-id="635c0-106">Syntax</span></span>


```JScript
iQuotaUsed = DIDiskQuotaUser.QuotaUsed
```



## <a name="property-value"></a><span data-ttu-id="635c0-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="635c0-107">Property value</span></span>

<span data-ttu-id="635c0-108">**整數** 值，設定為目前使用中的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="635c0-108">The **Integer** value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="635c0-109">如果已啟用 NTFS 檔案壓縮， **QuotaUsed** 會反映資料在未壓縮狀態中所需的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="635c0-109">If NTFS file compression is enabled, **QuotaUsed** reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="635c0-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="635c0-110">Requirements</span></span>



| <span data-ttu-id="635c0-111">需求</span><span class="sxs-lookup"><span data-stu-id="635c0-111">Requirement</span></span> | <span data-ttu-id="635c0-112">值</span><span class="sxs-lookup"><span data-stu-id="635c0-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="635c0-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="635c0-113">Minimum supported client</span></span><br/> | <span data-ttu-id="635c0-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="635c0-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="635c0-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="635c0-115">Minimum supported server</span></span><br/> | <span data-ttu-id="635c0-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="635c0-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="635c0-117">DLL</span><span class="sxs-lookup"><span data-stu-id="635c0-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="635c0-118"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="635c0-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="635c0-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="635c0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="635c0-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="635c0-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="635c0-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="635c0-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="635c0-122">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="635c0-122">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> <dt>

[<span data-ttu-id="635c0-123">**QuotaUsedText**</span><span class="sxs-lookup"><span data-stu-id="635c0-123">**QuotaUsedText**</span></span>](didiskquotauser-quotausedtext.md)
</dt> </dl>

 

 




