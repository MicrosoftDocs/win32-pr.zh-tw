---
description: 設定或取得預設配額限制。
title: DiskQuotaControl. DefaultQuotaLimit 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7d123bff-5dae-4430-be22-a822e231e43e
ms.openlocfilehash: fdfea60e58659b483a6b17c2dc89d313e3c81305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971972"
---
# <a name="diskquotacontroldefaultquotalimit-property"></a><span data-ttu-id="610ab-103">DiskQuotaControl. DefaultQuotaLimit 屬性</span><span class="sxs-lookup"><span data-stu-id="610ab-103">DiskQuotaControl.DefaultQuotaLimit property</span></span>

<span data-ttu-id="610ab-104">設定或取得預設配額限制。</span><span class="sxs-lookup"><span data-stu-id="610ab-104">Sets or gets the default quota limit.</span></span>

<span data-ttu-id="610ab-105">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="610ab-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="610ab-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="610ab-106">Syntax</span></span>


```JScript
iDefaultQuotaLimit = DiskQuotaControl.DefaultQuotaLimit
DiskQuotaControl.DefaultQuotaLimit = iDefaultQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="610ab-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="610ab-107">Property value</span></span>

<span data-ttu-id="610ab-108">指定或接收新使用者之預設配額限制的 **整數** 值（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="610ab-108">An **Integer** value that specifies or receives the default quota limit for new users, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="610ab-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="610ab-109">Requirements</span></span>



| <span data-ttu-id="610ab-110">需求</span><span class="sxs-lookup"><span data-stu-id="610ab-110">Requirement</span></span> | <span data-ttu-id="610ab-111">值</span><span class="sxs-lookup"><span data-stu-id="610ab-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="610ab-112">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="610ab-112">Minimum supported client</span></span><br/> | <span data-ttu-id="610ab-113">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="610ab-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="610ab-114">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="610ab-114">Minimum supported server</span></span><br/> | <span data-ttu-id="610ab-115">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="610ab-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="610ab-116">DLL</span><span class="sxs-lookup"><span data-stu-id="610ab-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="610ab-117"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="610ab-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="610ab-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="610ab-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="610ab-119">**DefaultQuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="610ab-119">**DefaultQuotaLimitText**</span></span>](diskquotacontrol-defaultquotalimittext.md)
</dt> <dt>

[<span data-ttu-id="610ab-120">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="610ab-120">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




