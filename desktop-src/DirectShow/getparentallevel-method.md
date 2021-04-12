---
description: DVDAdm. GetParentalLevel 方法會抓取上次儲存至登錄的父層級。
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: GetParentalLevel 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385565"
---
# <a name="getparentallevel-method"></a><span data-ttu-id="17f96-103">GetParentalLevel 方法</span><span class="sxs-lookup"><span data-stu-id="17f96-103">GetParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="17f96-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="17f96-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="17f96-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="17f96-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="17f96-106">`DVDAdm.GetParentalLevel`方法會抓取上次儲存至登錄的家長監護層級。</span><span class="sxs-lookup"><span data-stu-id="17f96-106">The `DVDAdm.GetParentalLevel` method retrieves the parental level that was last saved to the registry.</span></span>

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="17f96-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="17f96-107">Return Value</span></span>

<span data-ttu-id="17f96-108">傳回從1到8的整數，表示預設的父層級。</span><span class="sxs-lookup"><span data-stu-id="17f96-108">Returns an Integer from 1 through 8 indicating the default parental level.</span></span>

## <a name="remarks"></a><span data-ttu-id="17f96-109">備註</span><span class="sxs-lookup"><span data-stu-id="17f96-109">Remarks</span></span>

<span data-ttu-id="17f96-110">這個方法所抓取的父層級不一定是目前儲存在 MSWebDVD 控制項中的相同層級;若要取得目前儲存在控制項中的層級，請呼叫 [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="17f96-110">The parental level this method retrieves is not necessarily the same level currently stored in the MSWebDVD control; to get the level currently stored in the control, call the [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) method.</span></span> <span data-ttu-id="17f96-111">-1 的值表示已停用家長管理。</span><span class="sxs-lookup"><span data-stu-id="17f96-111">A value of -1 indicates that parental management is disabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="17f96-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17f96-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17f96-113">MSDVDAdm 物件</span><span class="sxs-lookup"><span data-stu-id="17f96-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



