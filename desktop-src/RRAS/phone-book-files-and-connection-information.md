---
title: Phone-Book 檔案和連接資訊
description: RasDial 呼叫必須指定遠端存取連線管理員建立連接所需的資訊。
ms.assetid: bc3885a4-3c1e-47bc-b622-072b33ac3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d352772eec057edd6ab8c9f53640c50ea0fc73
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093095"
---
# <a name="phone-book-files-and-connection-information"></a><span data-ttu-id="79eb6-103">Phone-Book 檔案和連接資訊</span><span class="sxs-lookup"><span data-stu-id="79eb6-103">Phone-Book Files and Connection Information</span></span>

<span data-ttu-id="79eb6-104">[**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)呼叫必須指定遠端存取連線管理員建立連接所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="79eb6-104">A [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call must specify the information that the Remote Access Connection Manager needs to establish the connection.</span></span> <span data-ttu-id="79eb6-105">一般而言， **RasDial** 呼叫會藉由指定電話簿專案來提供連接資訊。</span><span class="sxs-lookup"><span data-stu-id="79eb6-105">Typically, the **RasDial** call provides the connection information by specifying a phone-book entry.</span></span> <span data-ttu-id="79eb6-106">電話簿專案中的連接資訊包括電話號碼、bps 費率、 [使用者驗證資訊](user-authentication-information.md)，以及 [其他連線資訊](other-connection-information.md)。</span><span class="sxs-lookup"><span data-stu-id="79eb6-106">The connection information in a phone-book entry includes phone numbers, bps rates, [user authentication information](user-authentication-information.md), and [other connection information](other-connection-information.md).</span></span>

<span data-ttu-id="79eb6-107">RAS 用戶端會使用 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式的參數來指定電話簿檔案，以及該檔案中的專案。</span><span class="sxs-lookup"><span data-stu-id="79eb6-107">A RAS client uses the parameters of the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function to specify a phone-book file and an entry in that file.</span></span> <span data-ttu-id="79eb6-108">*LpszPhonebookPath* 參數可以指定電話簿檔案的名稱，也可以是 **Null** ，表示應使用預設的電話簿檔案。</span><span class="sxs-lookup"><span data-stu-id="79eb6-108">The *lpszPhonebookPath* parameter can specify the name of a phone-book file, or it can be **NULL** to indicate that the default phone-book file should be used.</span></span> <span data-ttu-id="79eb6-109">*LpRasDialParams* 參數會指向 [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85))結構，以指定要使用的電話簿專案名稱。</span><span class="sxs-lookup"><span data-stu-id="79eb6-109">The *lpRasDialParams* parameter points to a [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure that specifies the name of the phone-book entry to use.</span></span>

<span data-ttu-id="79eb6-110">若要顯示使用者可以從中選取連線的電話簿專案清單，RAS 用戶端可以呼叫 [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) 函式來列舉電話簿檔案中的專案。</span><span class="sxs-lookup"><span data-stu-id="79eb6-110">To display a list of phone-book entries from which the user can select a connection, a RAS client can call the [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) function to enumerate the entries in a phone-book file.</span></span>

<span data-ttu-id="79eb6-111">若要在不使用電話簿專案的情況下建立連接， [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala)呼叫可以為 [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85))結構的 **szEntryName** 成員指定空字串。</span><span class="sxs-lookup"><span data-stu-id="79eb6-111">To make a connection without using a phone-book entry, the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) call can specify an empty string for the **szEntryName** member of the [**RASDIALPARAMS**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) structure.</span></span> <span data-ttu-id="79eb6-112">**RASDIALPARAMS. szPhoneNumber** 成員必須包含要呼叫的數位。</span><span class="sxs-lookup"><span data-stu-id="79eb6-112">The **RASDIALPARAMS.szPhoneNumber** member must contain the number to call.</span></span> <span data-ttu-id="79eb6-113">在此情況下，遠端存取連線管理員會使用第一個可用的數據機埠，以及所有其他設定的預設值。</span><span class="sxs-lookup"><span data-stu-id="79eb6-113">In this case, the Remote Access Connection Manager uses the first available modem port and default values for all other settings.</span></span>

 

 