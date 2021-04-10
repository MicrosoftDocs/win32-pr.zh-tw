---
description: 地區設定 \_ S1159 和地區設定 \_ SAM
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 和 LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6b41f98ea5c07f1d88534c1e47acecfa81a4e62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850936"
---
# <a name="locale_s1159-and-locale_sam"></a><span data-ttu-id="cda35-103">地區設定 \_ S1159 和地區設定 \_ SAM</span><span class="sxs-lookup"><span data-stu-id="cda35-103">LOCALE\_S1159 and LOCALE\_SAM</span></span>

<span data-ttu-id="cda35-104">AM 指示項的字串 (一天中的前12小時) 。</span><span class="sxs-lookup"><span data-stu-id="cda35-104">String for the AM designator (first 12 hours of the day).</span></span> <span data-ttu-id="cda35-105">針對不同版本的 Windows，此字串允許的最大字元數（包括結束的 null 字元）會有所不同。</span><span class="sxs-lookup"><span data-stu-id="cda35-105">The maximum number of characters allowed for this string, including a terminating null character, is different for different releases of Windows.</span></span>

<span data-ttu-id="cda35-106">**WINDOWS XP：** 十三包含 [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa)的終止 null 字元。</span><span class="sxs-lookup"><span data-stu-id="cda35-106">**Windows XP:** Thirteen including a terminating null character for [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa).</span></span> <span data-ttu-id="cda35-107">15包含 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)的終止 null 字元。</span><span class="sxs-lookup"><span data-stu-id="cda35-107">Fifteen including a terminating null character for [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa).</span></span>

<span data-ttu-id="cda35-108">**Windows Me/98/95、Windows NT 4.0、Windows 2000：** 九個包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="cda35-108">**Windows Me/98/95, Windows NT 4.0, Windows 2000:** Nine including a terminating null character.</span></span>

<span data-ttu-id="cda35-109">**Windows Server 2003 和更新版本：** 15個包含終止的 null 字元。</span><span class="sxs-lookup"><span data-stu-id="cda35-109">**Windows Server 2003 and later:** Fifteen including a terminating null character.</span></span>

<span data-ttu-id="cda35-110">Windows 10 為 **地區設定 \_ S1159** 新增了值 **地區設定 \_ SAM** 作為更容易閱讀的同義字。</span><span class="sxs-lookup"><span data-stu-id="cda35-110">Windows 10 added the value **LOCALE\_SAM** as a more readable synonym for **LOCALE\_S1159**.</span></span>

 

 



