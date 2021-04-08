---
title: 在 WinSNMP 中支援 IPX 位址字串
description: WinSNMP 2.0 將 IPX 位址字串的使用正規化。
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc33c3ff3b589f9614b139260cef993e232f4343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671075"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a><span data-ttu-id="6b5f4-103">在 WinSNMP 中支援 IPX 位址字串</span><span class="sxs-lookup"><span data-stu-id="6b5f4-103">Support for IPX Address Strings in WinSNMP</span></span>

<span data-ttu-id="6b5f4-104">WinSNMP 2.0 將 IPX 位址字串的使用正規化。</span><span class="sxs-lookup"><span data-stu-id="6b5f4-104">WinSNMP 2.0 formalizes the use of IPX address strings.</span></span> <span data-ttu-id="6b5f4-105">如果您指定 IPX 位址字串做為 [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) 函數的輸入參數，您必須使用下列標準來格式化字串：</span><span class="sxs-lookup"><span data-stu-id="6b5f4-105">If you specify an IPX address string as an input parameter to the [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) function, you must format the string using the following standards:</span></span>

-   <span data-ttu-id="6b5f4-106">包含八個十六進位數位 (零填滿的網路編號（如有必要）) </span><span class="sxs-lookup"><span data-stu-id="6b5f4-106">A network number that consists of eight hexadecimal digits (zero-filled if necessary)</span></span>
-   <span data-ttu-id="6b5f4-107">分隔符號 ("："、"." 或 "–" ) </span><span class="sxs-lookup"><span data-stu-id="6b5f4-107">A separator (either ":", "." or " – ")</span></span>
-   <span data-ttu-id="6b5f4-108">包含12個十六進位數位 (零填滿的節點編號（如有必要）) </span><span class="sxs-lookup"><span data-stu-id="6b5f4-108">A node number that consists of 12 hexadecimal digits (zero-filled if necessary)</span></span>

<span data-ttu-id="6b5f4-109">例如，00000001：00081A0D01C2 或 00000001.00081 a0d01c2。</span><span class="sxs-lookup"><span data-stu-id="6b5f4-109">For example, 00000001:00081A0D01C2 or 00000001.00081a0d01c2.</span></span> <span data-ttu-id="6b5f4-110">十六進位數位可以是大寫或小寫。</span><span class="sxs-lookup"><span data-stu-id="6b5f4-110">Hexadecimal digits can be uppercase or lowercase.</span></span>

<span data-ttu-id="6b5f4-111">這是 [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) 函數用來傳回 IPX 位址字串的格式。</span><span class="sxs-lookup"><span data-stu-id="6b5f4-111">This is the format the [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) function uses to return an IPX address string.</span></span> <span data-ttu-id="6b5f4-112">當以其中一個 SNMPAPI 未轉譯模式運作的應用程式呼叫 SnmpEntityToStr 函式時，就會傳回字串 \_ 。 </span><span class="sxs-lookup"><span data-stu-id="6b5f4-112">The string is returned when an application that is operating in one of the SNMPAPI\_UNTRANSLATED modes calls the **SnmpEntityToStr** function.</span></span> <span data-ttu-id="6b5f4-113">當應用程式是以 SNMPAPI \_ 轉譯模式運作，而且沒有可供實體使用的使用者易記名稱時，也可以傳回字串。</span><span class="sxs-lookup"><span data-stu-id="6b5f4-113">The string can also be returned when the application is operating in SNMPAPI\_TRANSLATED mode and no user-friendly name is available for the entity.</span></span>

 

 




