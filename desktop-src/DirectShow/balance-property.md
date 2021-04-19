---
description: 餘額屬性會設定或抓取音訊串流輸出的喇叭餘額。
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: 餘額屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106971943"
---
# <a name="balance-property"></a><span data-ttu-id="c1765-103">餘額屬性</span><span class="sxs-lookup"><span data-stu-id="c1765-103">Balance Property</span></span>

> [!Note]  
> <span data-ttu-id="c1765-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="c1765-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="c1765-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="c1765-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="c1765-106">`Balance`屬性會設定或抓取音訊串流輸出的喇叭餘額。</span><span class="sxs-lookup"><span data-stu-id="c1765-106">The `Balance` property sets or retrieves the speaker balance for the audio stream output.</span></span>

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a><span data-ttu-id="c1765-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="c1765-107">Return Value</span></span>

<span data-ttu-id="c1765-108">傳回代表餘額層級的整數值。</span><span class="sxs-lookup"><span data-stu-id="c1765-108">Returns an integer value representing the balance levels.</span></span> <span data-ttu-id="c1765-109">允許的輸入範圍為-10000 到10000。</span><span class="sxs-lookup"><span data-stu-id="c1765-109">The allowable input range is -10,000 to 10,000.</span></span> <span data-ttu-id="c1765-110">值為0會設定中性餘額，也就是左和右喇叭都有相同的波幅音訊信號。</span><span class="sxs-lookup"><span data-stu-id="c1765-110">A value of 0 sets a neutral balance, that is both left and right speakers are given the same amplitude audio signal.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1765-111">備註</span><span class="sxs-lookup"><span data-stu-id="c1765-111">Remarks</span></span>

<span data-ttu-id="c1765-112">此屬性是讀取/寫入，預設值為0，表示兩個喇叭都會收到相等的音訊信號。</span><span class="sxs-lookup"><span data-stu-id="c1765-112">This property is read/write with a default value of 0, meaning that both speakers receive equivalent audio signals.</span></span> <span data-ttu-id="c1765-113">如同 [**Volume**](volume-property.md) 屬性，單位會對應到 .01 分貝 (乘以-1</span><span class="sxs-lookup"><span data-stu-id="c1765-113">As with the [**Volume**](volume-property.md) property, units correspond to .01 decibels (multiplied by -1 when</span></span>


```
iBalance
```



<span data-ttu-id="c1765-114">這是) 的正值。</span><span class="sxs-lookup"><span data-stu-id="c1765-114">is a positive value).</span></span> <span data-ttu-id="c1765-115">例如，值1000表示右邊通道的10個 dB 和左邊通道上的 90 dB。</span><span class="sxs-lookup"><span data-stu-id="c1765-115">For example, a value of 1000 indicates 10 dB on the right channel and 90 dB on the left channel.</span></span>

 

 



