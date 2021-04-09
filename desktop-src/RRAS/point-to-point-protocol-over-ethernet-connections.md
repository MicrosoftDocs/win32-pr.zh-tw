---
title: '透過乙太網路連接的點對點通訊協定 (PPP) '
description: Windows Server 2003、Windows XP 及更新版本的作業系統透過乙太網路上的點對點通訊協定 (PPP) 提供支援 (PPPoE) 。 針對 PPPoE 連接，在 RASENTRY 結構中設定下列值。
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933539"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a><span data-ttu-id="1a478-104">透過乙太網路連接的點對點通訊協定 (PPP) </span><span class="sxs-lookup"><span data-stu-id="1a478-104">Point-to-Point Protocol over Ethernet Connections</span></span>

<span data-ttu-id="1a478-105">Windows Server 2003、Windows XP 及更新版本的作業系統透過乙太網路上的點對點通訊協定 (PPP) 提供支援 (PPPoE) 。</span><span class="sxs-lookup"><span data-stu-id="1a478-105">Windows Server 2003, Windows XP, and later operating systems provide support for Point-to-Point Protocol over Ethernet (PPPoE).</span></span> <span data-ttu-id="1a478-106">針對 PPPoE 連接，在 [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) 結構中設定下列值。</span><span class="sxs-lookup"><span data-stu-id="1a478-106">For a PPPoE connection, set the following values in the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure.</span></span>



| <span data-ttu-id="1a478-107">成員</span><span class="sxs-lookup"><span data-stu-id="1a478-107">Member</span></span>                      | <span data-ttu-id="1a478-108">值</span><span class="sxs-lookup"><span data-stu-id="1a478-108">Value</span></span>             |
|-----------------------------|-------------------|
| <span data-ttu-id="1a478-109">RASENTRY. dwType</span><span class="sxs-lookup"><span data-stu-id="1a478-109">RASENTRY.dwType</span></span>             | <span data-ttu-id="1a478-110">RASET \_ 寬頻</span><span class="sxs-lookup"><span data-stu-id="1a478-110">RASET\_Broadband</span></span>  |
| <span data-ttu-id="1a478-111">RAENTRY.szDeviceType</span><span class="sxs-lookup"><span data-stu-id="1a478-111">RAENTRY.szDeviceType</span></span>        | <span data-ttu-id="1a478-112">RASDT \_ PPPoE</span><span class="sxs-lookup"><span data-stu-id="1a478-112">RASDT\_PPPoE</span></span>      |
| <span data-ttu-id="1a478-113">RASENTRY.szLocalPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="1a478-113">RASENTRY.szLocalPhoneNumber</span></span> | <span data-ttu-id="1a478-114">服務名稱。</span><span class="sxs-lookup"><span data-stu-id="1a478-114">The service name.</span></span> |



 

<span data-ttu-id="1a478-115">您可以使用 [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) 函數來設定這些值。</span><span class="sxs-lookup"><span data-stu-id="1a478-115">Use the [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) function to set these values.</span></span>

<span data-ttu-id="1a478-116">您也可以使用 [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga)和 RASENTRYDLG 的 RASEDFLAG \_ NewBroadbandEntry 旗 [](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga)標，顯示建立 PPPoE 電話簿專案的 wizard。</span><span class="sxs-lookup"><span data-stu-id="1a478-116">You can also use [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) and the RASEDFLAG\_NewBroadbandEntry flag for [**RASENTRYDLG**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) to display a wizard for creating a PPPoE phonebook entry.</span></span>

 

 