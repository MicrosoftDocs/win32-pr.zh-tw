---
description: 將資料放入登錄之前，應用程式應該將資料分成兩個類別：電腦特定的資料和使用者特定的資料。
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: 資料類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a3c89d23f713bb2ed08a7f7c53790e08055db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982773"
---
# <a name="categories-of-data"></a><span data-ttu-id="b0bd6-103">資料類別</span><span class="sxs-lookup"><span data-stu-id="b0bd6-103">Categories of Data</span></span>

<span data-ttu-id="b0bd6-104">將資料放入登錄之前，應用程式應該將資料分成兩個類別：電腦特定的資料和使用者特定的資料。</span><span class="sxs-lookup"><span data-stu-id="b0bd6-104">Before putting data into the registry, an application should divide the data into two categories: computer-specific data and user-specific data.</span></span> <span data-ttu-id="b0bd6-105">藉由進行這項區別，應用程式可以支援多個使用者，還可以透過網路來尋找使用者專屬的資料，並在不同的位置使用該資料，以允許與位置無關的使用者設定檔資料。</span><span class="sxs-lookup"><span data-stu-id="b0bd6-105">By making this distinction, an application can support multiple users, and yet locate user-specific data over a network and use that data in different locations, allowing location-independent user profile data.</span></span> <span data-ttu-id="b0bd6-106"> (使用者設定檔是一組為每位使用者儲存的設定資料。 ) </span><span class="sxs-lookup"><span data-stu-id="b0bd6-106">(A user profile is a set of configuration data saved for every user.)</span></span>

<span data-ttu-id="b0bd6-107">安裝應用程式時，它應該會在 **HKEY \_ 本機 \_ 電腦** 金鑰下記錄電腦特定的資料。</span><span class="sxs-lookup"><span data-stu-id="b0bd6-107">When the application is installed, it should record the computer-specific data under the **HKEY\_LOCAL\_MACHINE** key.</span></span> <span data-ttu-id="b0bd6-108">尤其是，它應該建立公司名稱、產品名稱和版本號碼的金鑰，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="b0bd6-108">In particular, it should create keys for the company name, product name, and version number, as shown in the following example:</span></span>

<span data-ttu-id="b0bd6-109">**HKEY \_LOCAL \_ MACHINE \\ Software \\** _MyCompany \\ MyProduct \\ 1.0_</span><span class="sxs-lookup"><span data-stu-id="b0bd6-109">**HKEY\_LOCAL\_MACHINE\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

<span data-ttu-id="b0bd6-110">如果應用程式支援 COM，則應該將該資料記錄在 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別** 下。</span><span class="sxs-lookup"><span data-stu-id="b0bd6-110">If the application supports COM, it should record that data under **HKEY\_LOCAL\_MACHINE\\Software\\Classes**.</span></span>

<span data-ttu-id="b0bd6-111">應用程式應該在 **HKEY \_ 目前 \_ 使用者** 金鑰下記錄使用者特定的資料，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="b0bd6-111">An application should record user-specific data under the **HKEY\_CURRENT\_USER** key, as shown in the following example:</span></span>

<span data-ttu-id="b0bd6-112">**HKEY \_CURRENT \_ USER \\ Software \\** _MyCompany \\ MyProduct \\ 1.0_</span><span class="sxs-lookup"><span data-stu-id="b0bd6-112">**HKEY\_CURRENT\_USER\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

 

 



