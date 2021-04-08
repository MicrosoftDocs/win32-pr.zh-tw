---
description: EnableResetOnStop 屬性會設定或抓取值，決定當篩選圖形從停止狀態轉換時，播放將如何繼續。
ms.assetid: ff2e2756-e3f3-4ddb-b99d-5fa65ec67f6b
title: EnableResetOnStop 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9449d8dd3e2e5ab0e1f008cba3e4cb2aabaa78c8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688000"
---
# <a name="enableresetonstop-property"></a><span data-ttu-id="86355-103">EnableResetOnStop 屬性</span><span class="sxs-lookup"><span data-stu-id="86355-103">EnableResetOnStop Property</span></span>

> [!Note]  
> <span data-ttu-id="86355-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="86355-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="86355-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="86355-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="86355-106">`EnableResetOnStop`屬性會設定或抓取值，決定當篩選圖形從停止狀態轉換時，播放將如何繼續。</span><span class="sxs-lookup"><span data-stu-id="86355-106">The `EnableResetOnStop` property sets or retrieves a value that determines how play will resume when the filter graph makes a transition from a stopped state.</span></span>

``` syntax
[ bEnableReset = ] MSWebDVD.EnableResetOnStop
```

## <a name="return-value"></a><span data-ttu-id="86355-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="86355-107">Return Value</span></span>

<span data-ttu-id="86355-108">傳回布林值，表示 MSWebDVD 物件在篩選圖形停止之後，會在何處開始播放。</span><span class="sxs-lookup"><span data-stu-id="86355-108">Returns a Boolean value indicating where the MSWebDVD object will start playing again after the filter graph is stopped.</span></span>

## <a name="remarks"></a><span data-ttu-id="86355-109">備註</span><span class="sxs-lookup"><span data-stu-id="86355-109">Remarks</span></span>

<span data-ttu-id="86355-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="86355-110">This property is read/write.</span></span>

<span data-ttu-id="86355-111">這個屬性的可能值為：，預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="86355-111">The possible values of this property are: with a default value of true.</span></span>



| <span data-ttu-id="86355-112">值</span><span class="sxs-lookup"><span data-stu-id="86355-112">Value</span></span> | <span data-ttu-id="86355-113">描述</span><span class="sxs-lookup"><span data-stu-id="86355-113">Description</span></span>                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86355-114">true</span><span class="sxs-lookup"><span data-stu-id="86355-114">true</span></span>  | <span data-ttu-id="86355-115">DVD Navigator 將會重設，並開始從光碟的開頭播放。這是預設值</span><span class="sxs-lookup"><span data-stu-id="86355-115">DVD Navigator will reset and start play from the beginning of the disc. This is the default value</span></span> |
| <span data-ttu-id="86355-116">false</span><span class="sxs-lookup"><span data-stu-id="86355-116">false</span></span> | <span data-ttu-id="86355-117">DVD 導覽器將會從停止的地方繼續播放。</span><span class="sxs-lookup"><span data-stu-id="86355-117">DVD Navigator will resume play where it left off.</span></span>                                                 |



 

 

 



