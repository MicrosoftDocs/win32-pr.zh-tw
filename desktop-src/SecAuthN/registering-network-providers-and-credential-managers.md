---
description: 建立網路提供者或認證管理員之後，您必須向系統註冊。
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: 註冊網路提供者和認證管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de34c97b61f685c3e779bd487fbc2c5b21fa7af2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193081"
---
# <a name="registering-network-providers-and-credential-managers"></a><span data-ttu-id="c396d-103">註冊網路提供者和認證管理員</span><span class="sxs-lookup"><span data-stu-id="c396d-103">Registering Network Providers and Credential Managers</span></span>

<span data-ttu-id="c396d-104">建立網路提供者或認證管理員之後，您必須向系統註冊。</span><span class="sxs-lookup"><span data-stu-id="c396d-104">After you have created your network provider or credential manager, you must register it with the system.</span></span> <span data-ttu-id="c396d-105">這是必要的，因此 MPR 會知道安裝了哪些網路提供者。</span><span class="sxs-lookup"><span data-stu-id="c396d-105">This is necessary so the MPR will know what network providers are installed.</span></span> <span data-ttu-id="c396d-106">當 MPR 啟動時，它會檢查登錄，並載入其找到的任何網路提供者或認證管理員。</span><span class="sxs-lookup"><span data-stu-id="c396d-106">When the MPR starts, it checks the registry and loads any network providers or credential managers it finds.</span></span>

<span data-ttu-id="c396d-107">由於網路提供者和認證管理員是相關的，因此它們會在登錄的相同子機碼中進行註冊。</span><span class="sxs-lookup"><span data-stu-id="c396d-107">Because network providers and credential managers are related, they are registered in the same subkeys of the registry.</span></span> <span data-ttu-id="c396d-108">事實上，網路提供者 Dll 也可以是認證管理員。</span><span class="sxs-lookup"><span data-stu-id="c396d-108">In fact, network provider DLLs can also be credential managers.</span></span>

<span data-ttu-id="c396d-109">如需有關您應該為網路提供者或認證管理員建立之登錄機碼的詳細資訊，請參閱驗證登錄機 [碼](authentication-registry-keys.md)。</span><span class="sxs-lookup"><span data-stu-id="c396d-109">For detailed information about the registry keys you should create for your network provider or credential manager, see [Authentication Registry Keys](authentication-registry-keys.md).</span></span>

 

 



