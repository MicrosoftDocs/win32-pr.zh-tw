---
description: AcceptParentalLevelChange 方法會接受或拒絕新的暫時家長管理層級。
ms.assetid: b3d58069-16dc-4598-90ea-6136c2f62ac7
title: AcceptParentalLevelChange 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b2e81d1d82c4ede14580ed65d88566738dac1b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106985382"
---
# <a name="acceptparentallevelchange-method"></a><span data-ttu-id="75ceb-103">AcceptParentalLevelChange 方法</span><span class="sxs-lookup"><span data-stu-id="75ceb-103">AcceptParentalLevelChange Method</span></span>

> [!Note]  
> <span data-ttu-id="75ceb-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="75ceb-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="75ceb-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="75ceb-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="75ceb-106">AcceptParentalLevelChange 方法會接受或拒絕新的暫時家長管理層級。</span><span class="sxs-lookup"><span data-stu-id="75ceb-106">The AcceptParentalLevelChange method accepts or rejects the new temporary parental management level.</span></span>

``` syntax
        MSWebDVD.AcceptParentalLevelChange(bAccept)
```

## <a name="parameters"></a><span data-ttu-id="75ceb-107">參數</span><span class="sxs-lookup"><span data-stu-id="75ceb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75ceb-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*</span><span class="sxs-lookup"><span data-stu-id="75ceb-108"><span id="bAccept"></span><span id="baccept"></span><span id="BACCEPT"></span>*bAccept*</span></span>
</dt> <dd>

<span data-ttu-id="75ceb-109">將新的父層級指定為布林值。</span><span class="sxs-lookup"><span data-stu-id="75ceb-109">Specifies the new parental level as a Boolean value.</span></span>



| <span data-ttu-id="75ceb-110">值</span><span class="sxs-lookup"><span data-stu-id="75ceb-110">Value</span></span> | <span data-ttu-id="75ceb-111">描述</span><span class="sxs-lookup"><span data-stu-id="75ceb-111">Description</span></span>                               |
|-------|-------------------------------------------|
| <span data-ttu-id="75ceb-112">true</span><span class="sxs-lookup"><span data-stu-id="75ceb-112">true</span></span>  | <span data-ttu-id="75ceb-113">接受新的家長管理層級。</span><span class="sxs-lookup"><span data-stu-id="75ceb-113">Accept the new parental management level.</span></span> |
| <span data-ttu-id="75ceb-114">false</span><span class="sxs-lookup"><span data-stu-id="75ceb-114">false</span></span> | <span data-ttu-id="75ceb-115">拒絕新的家長管理層級。</span><span class="sxs-lookup"><span data-stu-id="75ceb-115">Reject the new parental management level.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75ceb-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="75ceb-116">Return Value</span></span>

<span data-ttu-id="75ceb-117">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="75ceb-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="75ceb-118">備註</span><span class="sxs-lookup"><span data-stu-id="75ceb-118">Remarks</span></span>

<span data-ttu-id="75ceb-119">呼叫這個方法以回應 [EC \_ DVD 家長監護] \_ \_ \_ 變更事件通知，以指定 DVD 導覽器是否應該播放具有新家長監護的內容，或在新的層級遭到拒絕時，將分支新增到光碟指定的位置。</span><span class="sxs-lookup"><span data-stu-id="75ceb-119">Call this method in response to an EC\_DVD\_PARENTAL\_LEVEL\_CHANGE event notification to specify whether the DVD Navigator should play the content with the new parental level, or branch to where the disc specifies if the new level is rejected.</span></span>

## <a name="see-also"></a><span data-ttu-id="75ceb-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75ceb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75ceb-121">強制執行家長管理層級</span><span class="sxs-lookup"><span data-stu-id="75ceb-121">Enforcing Parental Management Levels</span></span>](enforcing-parental-management-levels.md)
</dt> <dt>

[<span data-ttu-id="75ceb-122">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="75ceb-122">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="75ceb-123">**GetPlayerParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="75ceb-123">**GetPlayerParentalLevel**</span></span>](getplayerparentallevel-method.md)
</dt> <dt>

[<span data-ttu-id="75ceb-124">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="75ceb-124">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="75ceb-125">**NotifyParentalLevelChange**</span><span class="sxs-lookup"><span data-stu-id="75ceb-125">**NotifyParentalLevelChange**</span></span>](notifyparentallevelchange-method.md)
</dt> <dt>

[<span data-ttu-id="75ceb-126">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="75ceb-126">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="75ceb-127">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="75ceb-127">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



