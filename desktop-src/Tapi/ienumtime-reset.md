---
description: Reset 方法會重設為列舉序列的開頭。
ms.assetid: a9131da1-051d-493c-939d-07801fda2d49
title: IEnumTime：： Reset 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9615fbc07edfb93c2377a7455d94b5fcd8ccd698
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113605"
---
# <a name="ienumtimereset-method"></a><span data-ttu-id="4b0a9-103">IEnumTime：： Reset 方法</span><span class="sxs-lookup"><span data-stu-id="4b0a9-103">IEnumTime::Reset method</span></span>

<span data-ttu-id="4b0a9-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="4b0a9-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="4b0a9-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="4b0a9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="4b0a9-106">**Reset** 方法會重設為列舉序列的開頭。</span><span class="sxs-lookup"><span data-stu-id="4b0a9-106">The **Reset** method resets to the beginning of the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b0a9-107">語法</span><span class="sxs-lookup"><span data-stu-id="4b0a9-107">Syntax</span></span>


```C++
HRESULT Reset();
```

## <a name="parameters"></a><span data-ttu-id="4b0a9-108">參數</span><span class="sxs-lookup"><span data-stu-id="4b0a9-108">Parameters</span></span>
<span data-ttu-id="4b0a9-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4b0a9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b0a9-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b0a9-110">Return value</span></span>
<span data-ttu-id="4b0a9-111">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="4b0a9-111">This method can return one of these values.</span></span>

| <span data-ttu-id="4b0a9-112">值</span><span class="sxs-lookup"><span data-stu-id="4b0a9-112">Value</span></span> | <span data-ttu-id="4b0a9-113">意義</span><span class="sxs-lookup"><span data-stu-id="4b0a9-113">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="4b0a9-114"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4b0a9-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="4b0a9-115">方法成功。</span><span class="sxs-lookup"><span data-stu-id="4b0a9-115">Method succeeded.</span></span> <br/>         |
