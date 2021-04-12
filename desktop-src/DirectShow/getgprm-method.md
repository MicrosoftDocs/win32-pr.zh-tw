---
description: GetGPRM 方法會抓取指定的一般參數 register。
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: GetGPRM 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510239"
---
# <a name="getgprm-method"></a><span data-ttu-id="ec197-103">GetGPRM 方法</span><span class="sxs-lookup"><span data-stu-id="ec197-103">GetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="ec197-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="ec197-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ec197-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="ec197-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ec197-106">方法會抓取 `GetGPRM` 指定的一般參數暫存器。</span><span class="sxs-lookup"><span data-stu-id="ec197-106">The `GetGPRM` method retrieves the specified general parameter register.</span></span>

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="ec197-107">參數</span><span class="sxs-lookup"><span data-stu-id="ec197-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec197-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="ec197-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="ec197-109">指定要取出為整數的暫存器。</span><span class="sxs-lookup"><span data-stu-id="ec197-109">Specifies the register to retrieve as an Integer.</span></span> <span data-ttu-id="ec197-110">值的範圍必須介於0到15之間。</span><span class="sxs-lookup"><span data-stu-id="ec197-110">The value must range from 0 through 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec197-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec197-111">Return Value</span></span>

<span data-ttu-id="ec197-112">傳回整數值，代表指定的暫存器。</span><span class="sxs-lookup"><span data-stu-id="ec197-112">Returns an integer value representing the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec197-113">備註</span><span class="sxs-lookup"><span data-stu-id="ec197-113">Remarks</span></span>

<span data-ttu-id="ec197-114">使用 **MSWebDVD** 物件的 DVD 流覽或播放功能不需要這個方法。</span><span class="sxs-lookup"><span data-stu-id="ec197-114">This method is not required for any DVD navigation or playback functionality using the **MSWebDVD** object.</span></span> <span data-ttu-id="ec197-115">這項功能的目的是為了讓您徹底瞭解想要執行 advanced 功能的 DVD 規格。</span><span class="sxs-lookup"><span data-stu-id="ec197-115">It is provided for those with a thorough understanding of the DVD specification who want to implement advanced features.</span></span> <span data-ttu-id="ec197-116">GPRMs 可以用來保存任何值，因此可以自由設定和讀取。</span><span class="sxs-lookup"><span data-stu-id="ec197-116">GPRMs can be used to hold any values, so they can be freely set and read.</span></span> <span data-ttu-id="ec197-117">但由於 GPRMs 也用來儲存光碟命令，因此使用 [**SetGPRM**](setgprm-method.md) 變更其值可能會導致無法預期的行為。</span><span class="sxs-lookup"><span data-stu-id="ec197-117">But since GPRMs are used to store disc commands as well, changing their values using [**SetGPRM**](setgprm-method.md) can result in unpredictable behavior.</span></span>

## <a name="see-also"></a><span data-ttu-id="ec197-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec197-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec197-119">**SetGPRM**</span><span class="sxs-lookup"><span data-stu-id="ec197-119">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



