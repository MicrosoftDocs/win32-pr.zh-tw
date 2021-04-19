---
description: 下圖說明與 TAPI 3 彙集目錄控制項相關的主要物件。 顯示的介面會以超連結的形式出現在相關的參考頁面中。
ms.assetid: f5ca1d61-5266-4406-8199-338e6a712db8
title: 目錄的控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c87a7b9c0b11c76aac6067e1a3f67c3899552f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973648"
---
# <a name="directory-controls"></a><span data-ttu-id="0784e-104">目錄的控制項</span><span class="sxs-lookup"><span data-stu-id="0784e-104">Directory Controls</span></span>

<span data-ttu-id="0784e-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="0784e-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0784e-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="0784e-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0784e-107">下圖說明與 TAPI 3 彙集目錄控制項相關的主要物件。</span><span class="sxs-lookup"><span data-stu-id="0784e-107">The following diagram illustrates the main objects involved in TAPI 3 Rendezvous directory controls.</span></span> <span data-ttu-id="0784e-108">顯示的介面會以超連結的形式出現在相關的參考頁面中。</span><span class="sxs-lookup"><span data-stu-id="0784e-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![彙集目錄控制項物件和介面](images/renddir.png)

<span data-ttu-id="0784e-110">主要目錄控制介面是 [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous)，必須藉由呼叫 **CoCreateInstance** 來建立。</span><span class="sxs-lookup"><span data-stu-id="0784e-110">The main directory control interface is [**ITRendezvous**](/windows/desktop/api/Rend/nn-rend-itrendezvous), which must be created by calling **CoCreateInstance**.</span></span> <span data-ttu-id="0784e-111">會合物件會公開方法，以取得可用目錄的清單，以及建立新的目錄或目錄物件。</span><span class="sxs-lookup"><span data-stu-id="0784e-111">The Rendezvous object exposes methods to get lists of available directories and to create new directories or directory objects.</span></span>

<span data-ttu-id="0784e-112">目錄位於伺服器上，而且是目錄物件清單以及描述性資訊。</span><span class="sxs-lookup"><span data-stu-id="0784e-112">A directory resides on a server and is a list of directory objects along with descriptive information.</span></span> <span data-ttu-id="0784e-113">與 [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) 相關聯的方法可以取得整個目錄的相關資訊，例如它是否為 ILS 目錄。</span><span class="sxs-lookup"><span data-stu-id="0784e-113">Methods associated with [**ITDirectory**](/windows/desktop/api/Rend/nn-rend-itdirectory) can get information associated with the directory as a whole, such as whether it is an ILS directory.</span></span>

<span data-ttu-id="0784e-114">目錄物件可以代表會議或使用者。</span><span class="sxs-lookup"><span data-stu-id="0784e-114">A directory object can represent a conference or a user.</span></span> <span data-ttu-id="0784e-115">[**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)介面提供的方法，可讓您取得或修改目錄物件的一般資訊，例如可撥撥的位址。</span><span class="sxs-lookup"><span data-stu-id="0784e-115">The [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject) interface supplies methods that can retrieve or modify information generic to a directory object, such as the dialable address.</span></span>

<span data-ttu-id="0784e-116">會議和使用者資訊（例如會議的 URL 或使用者的主要 IP 電話）是由 [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) 和 [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) 介面中提供的方法操作。</span><span class="sxs-lookup"><span data-stu-id="0784e-116">Conference and user information, such as the URL of a conference or the primary IP phone of a user, is manipulated by methods provided in the [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference) and [**ITDirectoryObjectUser**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectuser) interfaces.</span></span>

 

 



