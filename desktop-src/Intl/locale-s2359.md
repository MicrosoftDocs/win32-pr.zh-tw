---
description: 地區設定 \_ S2359 和地區設定 \_ SPM
ms.assetid: 8a97073e-84f6-47d9-98fb-65760e8a6cd8
title: LOCALE_S2359 和 LOCALE_SPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca0c22d541102fcdf0826778de591dc4100dda55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981191"
---
# <a name="locale_s2359-and-locale_spm"></a><span data-ttu-id="f7a52-103">地區設定 \_ S2359 和地區設定 \_ SPM</span><span class="sxs-lookup"><span data-stu-id="f7a52-103">LOCALE\_S2359 and LOCALE\_SPM</span></span>

<span data-ttu-id="f7a52-104">PM 指示項的字串 (第一天的12小時) 。</span><span class="sxs-lookup"><span data-stu-id="f7a52-104">String for the PM designator (second 12 hours of the day).</span></span> <span data-ttu-id="f7a52-105">針對不同版本的 Windows，此字串允許的最大字元數不同。</span><span class="sxs-lookup"><span data-stu-id="f7a52-105">The maximum number of characters allowed for this string is different for different releases of Windows.</span></span>

<span data-ttu-id="f7a52-106">**WINDOWS XP：** 十三包含 [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa)的終止 null 字元。</span><span class="sxs-lookup"><span data-stu-id="f7a52-106">**Windows XP:** Thirteen including a terminating null character for [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="f7a52-107">15包含 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)的終止 null 字元。</span><span class="sxs-lookup"><span data-stu-id="f7a52-107">Fifteen including a terminating null character for [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span></span>

<span data-ttu-id="f7a52-108">**Windows Me/98/95、Windows NT 4.0、Windows 2000：** 九個包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="f7a52-108">**Windows Me/98/95, Windows NT 4.0, Windows 2000:** Nine including a terminating null character.</span></span>

<span data-ttu-id="f7a52-109">**Windows Server 2003 和更新版本：** 15個包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="f7a52-109">**Windows Server 2003 and later:** Fifteen including a terminating null character.</span></span>

<span data-ttu-id="f7a52-110">Windows 10 新增了值 **地區設定 \_ SPM** ，作為 **地區設定 \_ S2359** 更容易閱讀的同義字。</span><span class="sxs-lookup"><span data-stu-id="f7a52-110">Windows 10 added the value **LOCALE\_SPM** as a more readable synonym for **LOCALE\_S2359**.</span></span>

 

 



