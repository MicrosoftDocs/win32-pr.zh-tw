---
description: GetAudioLanguage 方法會抓取字串，指出指定的音訊串流上有哪些語言可用。
ms.assetid: 5ff12058-eb00-4a2c-8d39-88282f68f001
title: GetAudioLanguage 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af71ad7943fe5442ded09f0b599c64c4b7215dac
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104509823"
---
# <a name="getaudiolanguage-method"></a><span data-ttu-id="88a2c-103">GetAudioLanguage 方法</span><span class="sxs-lookup"><span data-stu-id="88a2c-103">GetAudioLanguage Method</span></span>

> [!Note]  
> <span data-ttu-id="88a2c-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="88a2c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="88a2c-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="88a2c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="88a2c-106">`GetAudioLanguage`方法會抓取字串，指出指定的音訊資料流程上有哪些語言可用。</span><span class="sxs-lookup"><span data-stu-id="88a2c-106">The `GetAudioLanguage` method retrieves a string indicating which language is available on the specified audio stream.</span></span>

``` syntax
[ slang = ] MSWebDVD.GetAudioLanguage(iStream)
```

## <a name="parameters"></a><span data-ttu-id="88a2c-107">參數</span><span class="sxs-lookup"><span data-stu-id="88a2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88a2c-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="88a2c-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="88a2c-109">將目前標題中的音訊串流號碼指定為整數。</span><span class="sxs-lookup"><span data-stu-id="88a2c-109">Specifies the audio stream number in the current title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88a2c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="88a2c-110">Return Value</span></span>

<span data-ttu-id="88a2c-111">傳回人們可讀取的字串，識別目前標題中音訊資料流程的語言。</span><span class="sxs-lookup"><span data-stu-id="88a2c-111">Returns a human-readable string identifying the language of the audio stream in the current title.</span></span>

 

 



