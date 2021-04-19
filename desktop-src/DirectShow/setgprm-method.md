---
description: SetGPRM 方法會將指定的一般參數暫存器設定為指定的值。
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: SetGPRM 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e7492c599cde4c074c1a806f897edf3a8fe0a4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970075"
---
# <a name="setgprm-method"></a><span data-ttu-id="f776a-103">SetGPRM 方法</span><span class="sxs-lookup"><span data-stu-id="f776a-103">SetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="f776a-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="f776a-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f776a-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f776a-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f776a-106">`SetGPRM`方法會將指定的一般參數暫存器設定為指定的值。</span><span class="sxs-lookup"><span data-stu-id="f776a-106">The `SetGPRM` method sets the specified general parameter register to the specified value.</span></span>

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a><span data-ttu-id="f776a-107">參數</span><span class="sxs-lookup"><span data-stu-id="f776a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f776a-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="f776a-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="f776a-109">指定要設定為整數的一般參數暫存器。</span><span class="sxs-lookup"><span data-stu-id="f776a-109">Specifies the general parameter register to set as an Integer.</span></span> <span data-ttu-id="f776a-110">整數值的範圍必須介於0到15之間。</span><span class="sxs-lookup"><span data-stu-id="f776a-110">The Integer value must range from 0 through 15.</span></span>

</dd> <dt>

<span data-ttu-id="f776a-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*N 值*</span><span class="sxs-lookup"><span data-stu-id="f776a-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValue*</span></span>
</dt> <dd>

<span data-ttu-id="f776a-112">將註冊的新值指定為整數。</span><span class="sxs-lookup"><span data-stu-id="f776a-112">Specifies the new value for the register as an Integer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f776a-113">備註</span><span class="sxs-lookup"><span data-stu-id="f776a-113">Remarks</span></span>

<span data-ttu-id="f776a-114">一般參數暫存器（或 GPRMs）是16位的暫存器，每個光碟都能以獨特的方式用於暫存資料儲存。</span><span class="sxs-lookup"><span data-stu-id="f776a-114">General parameter registers, or GPRMs, are 16-bit registers that each disc can use in unique ways for temporary data storage.</span></span> <span data-ttu-id="f776a-115">播放機應用程式不需要使用 **MSWebDVD** 物件來存取任何標準播放或導覽控制項的這些暫存器。</span><span class="sxs-lookup"><span data-stu-id="f776a-115">A player application does not need to access these registers for any standard playback or navigation control using the **MSWebDVD** object.</span></span> <span data-ttu-id="f776a-116">這種方法是針對執行 advanced 功能的播放程式應用程式所提供。</span><span class="sxs-lookup"><span data-stu-id="f776a-116">This method is provided for player applications implementing advanced functionality.</span></span> <span data-ttu-id="f776a-117">除非您已徹底瞭解 DVD 規格，以及在播放特定光碟上使用 GPRMs 的方式，否則請勿嘗試直接修改 GPRMs。</span><span class="sxs-lookup"><span data-stu-id="f776a-117">Do not attempt to modify the GPRMs directly unless you have a thorough knowledge of the DVD specification and the ways in which the GPRMs are used on the particular disc to be played.</span></span> <span data-ttu-id="f776a-118">變更這些值可能會導致無法預期的行為。</span><span class="sxs-lookup"><span data-stu-id="f776a-118">Changing these values can result in unpredictable behavior.</span></span>

 

 



