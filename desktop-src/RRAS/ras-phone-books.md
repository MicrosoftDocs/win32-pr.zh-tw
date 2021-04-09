---
title: RAS 電話書籍
description: 電話簿提供一種標準方式來收集和指定遠端存取連線管理員建立遠端連線所需的資訊。
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- 電話書籍，RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021547"
---
# <a name="ras-phone-books"></a><span data-ttu-id="7151c-104">RAS 電話書籍</span><span class="sxs-lookup"><span data-stu-id="7151c-104">RAS Phone Books</span></span>

<span data-ttu-id="7151c-105">電話簿提供一種標準方式來收集和指定遠端存取連線管理員建立遠端連線所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="7151c-105">Phone books provide a standard way to collect and specify the information that the Remote Access Connection Manager needs to establish a remote connection.</span></span> <span data-ttu-id="7151c-106">電話簿將專案名稱與電話號碼、COM 埠和數據機設定等資訊相關聯。</span><span class="sxs-lookup"><span data-stu-id="7151c-106">Phone books associate entry names with information such as phone numbers, COM ports, and modem settings.</span></span> <span data-ttu-id="7151c-107">每個電話簿專案都包含建立 RAS 連線所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="7151c-107">Each phone-book entry contains the information needed to establish a RAS connection.</span></span>

<span data-ttu-id="7151c-108">電話簿儲存在電話簿檔案中，也就是包含專案名稱和相關資訊的文字檔。</span><span class="sxs-lookup"><span data-stu-id="7151c-108">Phone books are stored in phone-book files, which are text files that contain the entry names and associated information.</span></span> <span data-ttu-id="7151c-109">RAS 會建立名為 RASPHONE 的電話簿檔案。.PBK.</span><span class="sxs-lookup"><span data-stu-id="7151c-109">RAS creates a phone-book file called RASPHONE.PBK.</span></span> <span data-ttu-id="7151c-110">使用者可以使用 [主要 **撥號網路 (DUN)** ] 對話方塊來建立個人的電話簿檔案。</span><span class="sxs-lookup"><span data-stu-id="7151c-110">The user can use the main **Dial-Up Networking** dialog box to create personal phone-book files.</span></span> <span data-ttu-id="7151c-111">RAS API 目前不提供建立電話簿檔案的支援。</span><span class="sxs-lookup"><span data-stu-id="7151c-111">The RAS API does not currently provide support for creating a phone-book file.</span></span> <span data-ttu-id="7151c-112">某些 RAS 函式（例如 [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) 函式）有指定電話簿檔案的參數。</span><span class="sxs-lookup"><span data-stu-id="7151c-112">Some RAS functions, such as the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function, have a parameter that specifies a phone-book file.</span></span> <span data-ttu-id="7151c-113">如果呼叫者未指定電話簿檔案，則該函式會使用預設的電話簿檔案，也就是使用者在 [**撥號網路 (DUN)** ] 對話方塊的 [**使用者喜好** 設定] 屬性工作表中選取的檔案。</span><span class="sxs-lookup"><span data-stu-id="7151c-113">If the caller does not specify a phone-book file, the function uses the default phone-book file, which is the one selected by the user in the **User Preferences** property sheet of the **Dial-Up Networking** dialog box.</span></span>

<span data-ttu-id="7151c-114">Windows NT 4.0 提供的 [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) 和 [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) 函式會顯示內建的 RAS 使用者介面，讓使用者可以使用電話簿和電話簿專案。</span><span class="sxs-lookup"><span data-stu-id="7151c-114">Windows NT 4.0 provides the [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) and [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) functions that display the built-in RAS user interface that enable users to work with phone books and phone-book entries.</span></span>

<span data-ttu-id="7151c-115">**Windows 95：** 撥號網路會將電話簿專案儲存在登錄中，而不是在電話簿檔案中。</span><span class="sxs-lookup"><span data-stu-id="7151c-115">**Windows 95:** Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.</span></span> <span data-ttu-id="7151c-116">Windows 95 不支援顯示內建 RAS 對話方塊的個人電話簿檔案或功能。</span><span class="sxs-lookup"><span data-stu-id="7151c-116">Windows 95 does not support personal phone-book files or functions that display the built-in RAS dialog boxes.</span></span>

 

 




