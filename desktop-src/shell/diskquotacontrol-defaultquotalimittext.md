---
description: 取得做為文字字串的預設配額限制。
title: DiskQuotaControl. DefaultQuotaLimitText 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 14a5b5a0cc42bda17f922020a8485430797875e1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841539"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a><span data-ttu-id="6b901-103">DiskQuotaControl. DefaultQuotaLimitText 屬性</span><span class="sxs-lookup"><span data-stu-id="6b901-103">DiskQuotaControl.DefaultQuotaLimitText property</span></span>

<span data-ttu-id="6b901-104">取得做為文字字串的預設配額限制。</span><span class="sxs-lookup"><span data-stu-id="6b901-104">Gets the default quota limit as a text string.</span></span>

<span data-ttu-id="6b901-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6b901-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b901-106">語法</span><span class="sxs-lookup"><span data-stu-id="6b901-106">Syntax</span></span>


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a><span data-ttu-id="6b901-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="6b901-107">Property value</span></span>

<span data-ttu-id="6b901-108">字串值，包含磁片區新使用者的預設配額限制。</span><span class="sxs-lookup"><span data-stu-id="6b901-108">A string value that contains the default quota limit for new users of the volume.</span></span> <span data-ttu-id="6b901-109">例如，如果預設配額為 10.5 MB，則屬性的值為 "10.5 MB"。</span><span class="sxs-lookup"><span data-stu-id="6b901-109">For example, if the default quota is 10.5 MB, the value of the property is "10.5 MB".</span></span> <span data-ttu-id="6b901-110">如果磁片區沒有預設配額，屬性會設定為 [無限制] 或當地語系化的對等專案。</span><span class="sxs-lookup"><span data-stu-id="6b901-110">If the volume has no default quota, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b901-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b901-111">Requirements</span></span>



| <span data-ttu-id="6b901-112">需求</span><span class="sxs-lookup"><span data-stu-id="6b901-112">Requirement</span></span> | <span data-ttu-id="6b901-113">值</span><span class="sxs-lookup"><span data-stu-id="6b901-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b901-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b901-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6b901-115">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b901-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b901-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b901-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6b901-117">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b901-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6b901-118">DLL</span><span class="sxs-lookup"><span data-stu-id="6b901-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b901-119"><dt>Shell32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="6b901-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b901-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b901-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b901-121">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="6b901-121">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="6b901-122">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="6b901-122">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




