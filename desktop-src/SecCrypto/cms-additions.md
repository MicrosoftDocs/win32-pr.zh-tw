---
description: 從 PKCS 7 1.5 版衍生的 CMS)  (的密碼編譯訊息語法， \# 是用來雜湊、數位簽署、驗證和加密任意訊息的語法。
ms.assetid: 4396d3e2-8e41-4864-a12a-a598fab82840
title: CMS 新增
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dcd8470cabb237e128e313fcafedab2dd819da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981499"
---
# <a name="cms-additions"></a><span data-ttu-id="9e3c7-103">CMS 新增</span><span class="sxs-lookup"><span data-stu-id="9e3c7-103">CMS Additions</span></span>

<span data-ttu-id="9e3c7-104">從 PKCS 7 1.5 版衍生的 CMS)  (的密碼編譯訊息語法， \# 是用來 [*雜湊*](../secgloss/h-gly.md)、 [*數位簽署*](../secgloss/d-gly.md)、驗證和加密任意訊息的語法。</span><span class="sxs-lookup"><span data-stu-id="9e3c7-104">Cryptographic Message Syntax (CMS), derived from PKCS \#7 version 1.5, is the syntax used to [*hash*](../secgloss/h-gly.md), [*digitally sign*](../secgloss/d-gly.md), authenticate, and encrypt arbitrary messages.</span></span> <span data-ttu-id="9e3c7-105">可能的話，會保留回溯相容性;不過，已進行變更以容納屬性憑證傳輸和金鑰管理的金鑰協定技術。</span><span class="sxs-lookup"><span data-stu-id="9e3c7-105">Where possible, backward compatibility is preserved; however, changes have been made to accommodate attribute certificate transfer and key agreement techniques for key management.</span></span> <span data-ttu-id="9e3c7-106">CMS 允許多個封裝，讓一個封裝信封可以嵌套在另一個。</span><span class="sxs-lookup"><span data-stu-id="9e3c7-106">CMS allows multiple encapsulation so that one encapsulation envelope can be nested inside another.</span></span> <span data-ttu-id="9e3c7-107">此外，另一方可以數位簽署先前封裝的資料;您可以使用訊息內容來簽署任意屬性，例如簽章時間。和屬性（例如 [*副署*](../secgloss/c-gly.md)）可以與簽章相關聯。</span><span class="sxs-lookup"><span data-stu-id="9e3c7-107">Also, one party can digitally sign previously encapsulated data; arbitrary attributes, such as signing time, can be signed along with the message content; and attributes, such as [*countersignatures*](../secgloss/c-gly.md), can be associated with a signature.</span></span> <span data-ttu-id="9e3c7-108">CMS 可以支援各種不同的架構來進行以憑證為基礎的金鑰管理。</span><span class="sxs-lookup"><span data-stu-id="9e3c7-108">CMS can support a variety of architectures for certificate-based key management.</span></span>

<span data-ttu-id="9e3c7-109">為了支援其他 CMS 功能，已為基礎資料結構提供了新的欄位。</span><span class="sxs-lookup"><span data-stu-id="9e3c7-109">To support additional CMS capabilities, underlying data structures have been given new fields.</span></span> <span data-ttu-id="9e3c7-110">也加入了新的旗標和參數值。</span><span class="sxs-lookup"><span data-stu-id="9e3c7-110">New flags and parameter values have also been added.</span></span> <span data-ttu-id="9e3c7-111">所有使用 CMS 的資料結構和所有 Api 都是與 PKCS 7 1.5 版回溯相容的 100% \# 。</span><span class="sxs-lookup"><span data-stu-id="9e3c7-111">All data structures and all APIs using CMS are 100 percent backward compatible with PKCS \#7 version 1.5.</span></span>

<span data-ttu-id="9e3c7-112">新增專案包含新增的 [封包資料](enveloped-data-additions.md) 和 [已簽署的資料](signed-data-additions.md)。</span><span class="sxs-lookup"><span data-stu-id="9e3c7-112">Additions include [Enveloped Data Additions](enveloped-data-additions.md) and [Signed Data Additions](signed-data-additions.md).</span></span>

 

 
