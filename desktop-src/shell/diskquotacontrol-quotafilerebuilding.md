---
description: 取得布林值，指出目前是否正在重建磁片區的配額檔案。
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: DiskQuotaControl. QuotaFileRebuilding 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972124"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a><span data-ttu-id="eab87-103">DiskQuotaControl. QuotaFileRebuilding 屬性</span><span class="sxs-lookup"><span data-stu-id="eab87-103">DiskQuotaControl.QuotaFileRebuilding property</span></span>

<span data-ttu-id="eab87-104">取得布林值，指出目前是否正在重建磁片區的配額檔案。</span><span class="sxs-lookup"><span data-stu-id="eab87-104">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span>

<span data-ttu-id="eab87-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="eab87-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eab87-106">語法</span><span class="sxs-lookup"><span data-stu-id="eab87-106">Syntax</span></span>


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a><span data-ttu-id="eab87-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="eab87-107">Property value</span></span>

<span data-ttu-id="eab87-108">如果正在重建配額檔案，這個屬性會設定為 **TRUE** ，否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="eab87-108">This property is set to **TRUE** if the quota file is being rebuilt, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="eab87-109">備註</span><span class="sxs-lookup"><span data-stu-id="eab87-109">Remarks</span></span>

<span data-ttu-id="eab87-110">當系統上已啟用配額，或有一或多個使用者專案標記為刪除時，就會自動重建配額檔案。</span><span class="sxs-lookup"><span data-stu-id="eab87-110">The quota file is automatically rebuilt when quotas are enabled on the system or when one or more user entries are marked for deletion.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab87-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="eab87-111">Requirements</span></span>



| <span data-ttu-id="eab87-112">需求</span><span class="sxs-lookup"><span data-stu-id="eab87-112">Requirement</span></span> | <span data-ttu-id="eab87-113">值</span><span class="sxs-lookup"><span data-stu-id="eab87-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eab87-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eab87-114">Minimum supported client</span></span><br/> | <span data-ttu-id="eab87-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eab87-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="eab87-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eab87-116">Minimum supported server</span></span><br/> | <span data-ttu-id="eab87-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eab87-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="eab87-118">DLL</span><span class="sxs-lookup"><span data-stu-id="eab87-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eab87-119"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="eab87-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eab87-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eab87-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eab87-121">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="eab87-121">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




