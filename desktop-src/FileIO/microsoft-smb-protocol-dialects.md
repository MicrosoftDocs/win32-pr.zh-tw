---
description: 若要使用 Microsoft SMB 通訊協定在用戶端與伺服器之間建立連線，您必須先使用用戶端和伺服器支援的最高層級功能來判斷方言。
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Microsoft SMB 通訊協定方言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468952"
---
# <a name="microsoft-smb-protocol-dialects"></a><span data-ttu-id="4ac86-103">Microsoft SMB 通訊協定方言</span><span class="sxs-lookup"><span data-stu-id="4ac86-103">Microsoft SMB Protocol Dialects</span></span>

<span data-ttu-id="4ac86-104">Microsoft SMB 通訊協定訊息封包的清單已成長多年，以配合 Microsoft SMB 通訊協定的增強功能，而現在是數百個數字。</span><span class="sxs-lookup"><span data-stu-id="4ac86-104">The list of Microsoft SMB Protocol message packets has grown over the years to accommodate the increasing functionality of Microsoft SMB Protocol, and now numbers in the hundreds.</span></span> <span data-ttu-id="4ac86-105">其成長的每個階段都是由標準的封包集或方言所標示。</span><span class="sxs-lookup"><span data-stu-id="4ac86-105">Each stage of its growth is marked by a standard packet set, or dialect.</span></span> <span data-ttu-id="4ac86-106">每個方言都會以標準字串來識別，例如「電腦網路程式1.0」、「MICROSOFT 網路3.0」、「DOS LANMAN 2.1」或「NT LM 0.12」。</span><span class="sxs-lookup"><span data-stu-id="4ac86-106">Each dialect is identified by a standard string such as "PC NETWORK PROGRAM 1.0", "MICROSOFT NETWORKS 3.0", "DOS LANMAN 2.1", or "NT LM 0.12".</span></span> <span data-ttu-id="4ac86-107">第一個字串會識別 SMB 的第一個方言，而最後一個字串會識別 CIFS，也就是 Microsoft SMB 通訊協定的第一個方言。</span><span class="sxs-lookup"><span data-stu-id="4ac86-107">The first string identifies the first dialect of SMB, and the last string identifies CIFS, the first dialect of Microsoft SMB Protocol.</span></span>

<span data-ttu-id="4ac86-108">大部分的 Windows 用戶端至少都支援六種不同的 Microsoft SMB 通訊協定方言，因此在用戶端與使用 Microsoft SMB 通訊協定的伺服器之間建立連線的第一個步驟，是使用用戶端和伺服器支援的最高層級功能來判斷方言。</span><span class="sxs-lookup"><span data-stu-id="4ac86-108">Most Windows clients support at least six different dialects of Microsoft SMB Protocol, so one of the first steps in establishing a connection between a client and a server using Microsoft SMB Protocol is to determine the dialect with the highest level of functionality that both the client and server support.</span></span> <span data-ttu-id="4ac86-109">此流程稱為「正在協商方言」。</span><span class="sxs-lookup"><span data-stu-id="4ac86-109">This process is known as "negotiating the dialect."</span></span> <span data-ttu-id="4ac86-110">上述的方言字串包含在方言協商要求和回應封包中，以供此用途之用。</span><span class="sxs-lookup"><span data-stu-id="4ac86-110">The dialect strings mentioned above are included in the dialect negotiation request and response packets for this purpose.</span></span>

 

 



