---
description: 近端分享存放區
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: 近端分享存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850579"
---
# <a name="people-near-me-stores"></a><span data-ttu-id="bf336-103">近端分享存放區</span><span class="sxs-lookup"><span data-stu-id="bf336-103">People Near Me Stores</span></span>

<span data-ttu-id="bf336-104">能夠 [近端分享](about-people-near-me.md) (PNM) 的應用程式可以使用下列資料存放區：</span><span class="sxs-lookup"><span data-stu-id="bf336-104">Applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following data stores:</span></span>

### <a name="windows-address-book"></a><span data-ttu-id="bf336-105">Windows 通訊錄</span><span class="sxs-lookup"><span data-stu-id="bf336-105">Windows Address Book</span></span>

<span data-ttu-id="bf336-106">Windows 通訊錄會儲存連絡人及其數位憑證的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bf336-106">The Windows Address Book stores information on contacts and their digital certificates.</span></span> <span data-ttu-id="bf336-107">代表目前登入使用者的 '**Me**' 連絡人也儲存在 Windows 通訊錄中。</span><span class="sxs-lookup"><span data-stu-id="bf336-107">The '**Me**' contact, representing the currently logged in user, is also stored in the Windows Address Book.</span></span>

### <a name="certificate-store"></a><span data-ttu-id="bf336-108">憑證存放區</span><span class="sxs-lookup"><span data-stu-id="bf336-108">Certificate Store</span></span>

<span data-ttu-id="bf336-109">憑證存放區包含 '**Me**' 連絡人的自我簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="bf336-109">The Certificate Store contains the self-signed certificate for the '**Me**' contact.</span></span>

### <a name="application-store"></a><span data-ttu-id="bf336-110">應用程式市集</span><span class="sxs-lookup"><span data-stu-id="bf336-110">Application Store</span></span>

<span data-ttu-id="bf336-111">應用程式安裝程式會在安裝過程中使用 PNM 註冊應用程式。</span><span class="sxs-lookup"><span data-stu-id="bf336-111">An application installer registers an application with PNM during the installation process.</span></span> <span data-ttu-id="bf336-112">這些物件是在嘗試使用一般應用程式（例如電腦遊戲）連接到使用者時，可供其他使用者搜尋的物件。</span><span class="sxs-lookup"><span data-stu-id="bf336-112">These are the objects that can be searched for by other users when attempting to connect to a user with a common application, such as a computer game.</span></span> <span data-ttu-id="bf336-113">針對每個應用程式，應用程式存放區包含應用程式的名稱、全域唯一識別碼 (GUID) 、應用程式範圍、描述，以及程式可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="bf336-113">For each application, the Application Store contains the name of the application, a globally unique identifier (GUID), a scope of the application, a description, and a path to the executable file of the program.</span></span> <span data-ttu-id="bf336-114">應用程式的範圍可以設定為 [無] (未公告) 、近端分享 (在本機子網上公告) 、[連絡人] (僅針對連絡人進行公告，或在本機子網上公告的所有) 或 [連絡人] (。</span><span class="sxs-lookup"><span data-stu-id="bf336-114">The scope of an application can be set to None (not advertised), People Near Me (advertised on the local subnet), Contacts (advertised just for contacts), or All (advertised on the local subnet and for contacts).</span></span> <span data-ttu-id="bf336-115">應用程式存放區位於 Windows Vista 登錄中。</span><span class="sxs-lookup"><span data-stu-id="bf336-115">The Application Store is located in the Windows Vista registry.</span></span>

 

 



