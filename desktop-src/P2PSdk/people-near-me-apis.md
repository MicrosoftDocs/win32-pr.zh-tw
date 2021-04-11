---
description: 近端分享 Api
ms.assetid: 3b142d23-a9b2-465c-9bdc-484afbde154e
title: 近端分享 Api
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132d358a7d51a1069f7a4d1dc1ddfe2752dbdd1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944278"
---
# <a name="people-near-me-apis"></a><span data-ttu-id="e86a9-103">近端分享 Api</span><span class="sxs-lookup"><span data-stu-id="e86a9-103">People Near Me APIs</span></span>

<span data-ttu-id="e86a9-104">任何能夠 [近端分享](about-people-near-me.md) (PNM) 的應用程式都可以使用下列 Win32 api：</span><span class="sxs-lookup"><span data-stu-id="e86a9-104">Any applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following Win32 APIs:</span></span>

### <a name="contacts-api"></a><span data-ttu-id="e86a9-105">連絡人 API</span><span class="sxs-lookup"><span data-stu-id="e86a9-105">Contacts API</span></span>

<span data-ttu-id="e86a9-106">連絡人 API 是用來存取已登入使用者的連絡人資訊、取出先前儲存之連絡人的相關資訊，或是儲存連絡人資訊和新連絡人的數位憑證。</span><span class="sxs-lookup"><span data-stu-id="e86a9-106">The Contacts API is used to access the contact information for the logged on user, retrieve information about previously stored contacts, or store the contact information and digital certificate of a new contact.</span></span>

### <a name="people-near-me-api"></a><span data-ttu-id="e86a9-107">近端分享 API</span><span class="sxs-lookup"><span data-stu-id="e86a9-107">People Near Me API</span></span>

<span data-ttu-id="e86a9-108">PNM API 可用來尋找附近的使用者、其公告的興趣、他們選擇要發佈的任意物件，以及公告的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e86a9-108">The PNM API is used to find users nearby, their advertised interests, any arbitrary objects they choose to publish, and advertised applications.</span></span>

### <a name="publication-api"></a><span data-ttu-id="e86a9-109">發行集 API</span><span class="sxs-lookup"><span data-stu-id="e86a9-109">Publication API</span></span>

<span data-ttu-id="e86a9-110">發行集 API 是用來與遠端連絡人互動。</span><span class="sxs-lookup"><span data-stu-id="e86a9-110">The Publication API is used to interact with remote contacts.</span></span> <span data-ttu-id="e86a9-111">PNM 模組也會使用發行集管理員所使用的 [對等信號](windows-peer-components-for-people-near-me.md) 層來建立連接。</span><span class="sxs-lookup"><span data-stu-id="e86a9-111">The [Peer Signaling](windows-peer-components-for-people-near-me.md) layer used by the Publication Manager is also used by the PNM module for establishing connections.</span></span>

### <a name="invitation-api"></a><span data-ttu-id="e86a9-112">邀請 API</span><span class="sxs-lookup"><span data-stu-id="e86a9-112">Invitation API</span></span>

<span data-ttu-id="e86a9-113">共同作業應用程式會使用邀請 API 來邀請特定的對等 () 到共同作業活動中。</span><span class="sxs-lookup"><span data-stu-id="e86a9-113">The Invitation API is used by a collaboration application to invite specific peer(s) into a collaboration activity.</span></span>

### <a name="application-registration-api"></a><span data-ttu-id="e86a9-114">應用程式註冊 API</span><span class="sxs-lookup"><span data-stu-id="e86a9-114">Application Registration API</span></span>

<span data-ttu-id="e86a9-115">共同作業應用程式的安裝程式會使用應用程式註冊 API 來註冊應用程式。</span><span class="sxs-lookup"><span data-stu-id="e86a9-115">The Application Registration API is used by the installer of a collaboration application to register the application.</span></span> <span data-ttu-id="e86a9-116">具有 PNM 功能的應用程式會在安裝過程中提示使用者，以判斷是否應該將應用程式提供給子網的使用者使用。</span><span class="sxs-lookup"><span data-stu-id="e86a9-116">A PNM-capable application will prompt the user during the installation process to determine whether the application should be made available to users on the subnet.</span></span>

 

 



