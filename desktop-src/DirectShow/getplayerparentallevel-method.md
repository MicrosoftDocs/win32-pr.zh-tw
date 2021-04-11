---
description: GetPlayerParentalLevel 會捕獲 MSWebDVD 物件中所設定的家長管理層級。
ms.assetid: 451e0891-4e5d-4a01-94b8-290f5a804ff1
title: GetPlayerParentalLevel 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bac51e776a45e0d1fa748fc995240292474e902
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108500"
---
# <a name="getplayerparentallevel-method"></a><span data-ttu-id="788e9-103">GetPlayerParentalLevel 方法</span><span class="sxs-lookup"><span data-stu-id="788e9-103">GetPlayerParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="788e9-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="788e9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="788e9-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="788e9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="788e9-106">會抓取 `GetPlayerParentalLevel` **MSWebDVD** 物件中設定的家長管理層級。</span><span class="sxs-lookup"><span data-stu-id="788e9-106">The `GetPlayerParentalLevel` retrieves the parental management level set in the **MSWebDVD** object.</span></span>

``` syntax
[ iLevel = ] MSWebDVD.GetPlayerParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="788e9-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="788e9-107">Return Value</span></span>

<span data-ttu-id="788e9-108">傳回整數值，這個值會指定 DVD 導覽中的目前家長層級，如果停用家長管理，則傳回-1。</span><span class="sxs-lookup"><span data-stu-id="788e9-108">Returns an integer value specifying the current parental level in the DVD Navigator, or -1 if parental management is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="788e9-109">備註</span><span class="sxs-lookup"><span data-stu-id="788e9-109">Remarks</span></span>

<span data-ttu-id="788e9-110">播放機應用程式負責強制執行家長監護控制項。</span><span class="sxs-lookup"><span data-stu-id="788e9-110">A player application is responsible for enforcing parental controls.</span></span> <span data-ttu-id="788e9-111">Media player 家長監護是由應用程式所設定的值，其可用來指出目前使用者可查看的最高家長能等級。</span><span class="sxs-lookup"><span data-stu-id="788e9-111">The player parental level is a value set by an application than can be used to indicate the highest parental level the current user can view.</span></span> <span data-ttu-id="788e9-112">當 DVD 導覽器遇到新的家長監護時，請使用這個方法來判斷新的層級是否大於應用程式透過 [**SelectParentalLevel**](selectparentallevel-method.md)所設定的層級。</span><span class="sxs-lookup"><span data-stu-id="788e9-112">When the DVD Navigator encounters a new parental level, use this method to determine whether the new level is greater than the level that was set by the application through [**SelectParentalLevel**](selectparentallevel-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="788e9-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="788e9-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="788e9-114">**GetTitleParentalLevels**</span><span class="sxs-lookup"><span data-stu-id="788e9-114">**GetTitleParentalLevels**</span></span>](gettitleparentallevels-method.md)
</dt> <dt>

[<span data-ttu-id="788e9-115">**GetPlayerParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="788e9-115">**GetPlayerParentalCountry**</span></span>](getplayerparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="788e9-116">**SelectParentalCountry**</span><span class="sxs-lookup"><span data-stu-id="788e9-116">**SelectParentalCountry**</span></span>](selectparentalcountry-method.md)
</dt> <dt>

[<span data-ttu-id="788e9-117">**SelectParentalLevel**</span><span class="sxs-lookup"><span data-stu-id="788e9-117">**SelectParentalLevel**</span></span>](selectparentallevel-method.md)
</dt> </dl>

 

 



