---
description: Reset 方法會重設為列舉序列的開頭。
ms.assetid: 338e0614-8f18-4ee2-8697-66ff3898f813
title: IEnumMedia：： Reset 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14624d5a048df2f5bc80205f34f262068c53da74
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106988099"
---
# <a name="ienummediareset-method"></a><span data-ttu-id="921ef-103">IEnumMedia：： Reset 方法</span><span class="sxs-lookup"><span data-stu-id="921ef-103">IEnumMedia::Reset method</span></span>

<span data-ttu-id="921ef-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="921ef-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="921ef-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="921ef-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="921ef-106">**Reset** 方法會重設為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="921ef-106">The **Reset** method resets to the beginning of enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="921ef-107">語法</span><span class="sxs-lookup"><span data-stu-id="921ef-107">Syntax</span></span>


```C++
HRESULT Reset();
```

## <a name="parameters"></a><span data-ttu-id="921ef-108">參數</span><span class="sxs-lookup"><span data-stu-id="921ef-108">Parameters</span></span>
<span data-ttu-id="921ef-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="921ef-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="921ef-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="921ef-110">Return value</span></span>
<span data-ttu-id="921ef-111">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="921ef-111">This method can return one of these values.</span></span>

| <span data-ttu-id="921ef-112">值</span><span class="sxs-lookup"><span data-stu-id="921ef-112">Value</span></span> | <span data-ttu-id="921ef-113">意義</span><span class="sxs-lookup"><span data-stu-id="921ef-113">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="921ef-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="921ef-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="921ef-115">方法成功。</span><span class="sxs-lookup"><span data-stu-id="921ef-115">Method succeeded.</span></span> <br/>         |
