---
description: 取得布林值，這個值會指出磁片區的配額檔案是否已完成。
ms.assetid: 25eb7df4-ba6c-4c6c-b611-e32b673a4d18
title: DiskQuotaControl. QuotaFileIncomplete 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileIncomplete
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: feb9365a6aa541ed8461bbe6d58c77ebc3684b91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991826"
---
# <a name="diskquotacontrolquotafileincomplete-property"></a><span data-ttu-id="8f47a-103">DiskQuotaControl. QuotaFileIncomplete 屬性</span><span class="sxs-lookup"><span data-stu-id="8f47a-103">DiskQuotaControl.QuotaFileIncomplete property</span></span>

<span data-ttu-id="8f47a-104">取得布林值，這個值會指出磁片區的配額檔案是否已完成。</span><span class="sxs-lookup"><span data-stu-id="8f47a-104">Gets a Boolean value that indicates whether the quota file for the volume is complete.</span></span>

<span data-ttu-id="8f47a-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="8f47a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f47a-106">語法</span><span class="sxs-lookup"><span data-stu-id="8f47a-106">Syntax</span></span>


```JScript
bQuotaFileIncomplete = DiskQuotaControl.QuotaFileIncomplete
```



## <a name="property-value"></a><span data-ttu-id="8f47a-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="8f47a-107">Property value</span></span>

<span data-ttu-id="8f47a-108">如果配額檔案不完整，這個屬性會設定為 **TRUE** ，否則會設為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8f47a-108">This property is set to **TRUE** if the quota file is incomplete, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f47a-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f47a-109">Requirements</span></span>



| <span data-ttu-id="8f47a-110">需求</span><span class="sxs-lookup"><span data-stu-id="8f47a-110">Requirement</span></span> | <span data-ttu-id="8f47a-111">值</span><span class="sxs-lookup"><span data-stu-id="8f47a-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f47a-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f47a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8f47a-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f47a-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8f47a-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f47a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8f47a-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f47a-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8f47a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="8f47a-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f47a-117"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="8f47a-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f47a-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f47a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f47a-119">**DiskQuotaControl 物件**</span><span class="sxs-lookup"><span data-stu-id="8f47a-119">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




