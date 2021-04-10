---
description: 並存私用元件可以用來建立可輕鬆更新的元件，而不需要更新裝載應用程式。
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: 更新應用程式元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba559323c3272db96f0cd106f0fc61624519b770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943342"
---
# <a name="updating-application-components"></a><span data-ttu-id="a63e0-103">更新應用程式元件</span><span class="sxs-lookup"><span data-stu-id="a63e0-103">Updating Application Components</span></span>

<span data-ttu-id="a63e0-104">並存私用元件可以用來建立可輕鬆更新的元件，而不需要更新裝載應用程式。</span><span class="sxs-lookup"><span data-stu-id="a63e0-104">Side-by-side private assemblies can be used to create components that can be easily updated without also updating the hosting application.</span></span> <span data-ttu-id="a63e0-105">這可讓更新服務安裝應用程式的更新元件、重新開機應用程式，並讓應用程式使用這些變更。</span><span class="sxs-lookup"><span data-stu-id="a63e0-105">This allows an updating service to install the application's updated components, restart the application, and have the application use the changes.</span></span> <span data-ttu-id="a63e0-106">使用應用程式資訊清單時，您可以更新應用程式所裝載之元件的功能，而不需要變更裝載應用程式的程式碼。</span><span class="sxs-lookup"><span data-stu-id="a63e0-106">When using application manifests, the functionality of components hosted by an application can be updated without having to change the hosting application's code.</span></span>

<span data-ttu-id="a63e0-107">這個方法可以用來更新應用程式資源的版本。</span><span class="sxs-lookup"><span data-stu-id="a63e0-107">This method can be used to update the version of an application's resources.</span></span> <span data-ttu-id="a63e0-108">例如，如果應用程式包含元件，則應用程式的資訊清單可以指定此元件的相依性。</span><span class="sxs-lookup"><span data-stu-id="a63e0-108">For example, if an application contains an assembly, the application's manifest can specify a dependency on this assembly.</span></span> <span data-ttu-id="a63e0-109">應用程式可以藉由呼叫 [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) 來尋找並載入所需的檔案，以取得元件。</span><span class="sxs-lookup"><span data-stu-id="a63e0-109">The application can get the assembly by calling [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) to find and load the files it requires.</span></span> <span data-ttu-id="a63e0-110">更新程式只需要關閉元件的最新位，它就可以與舊版元件並存存在。</span><span class="sxs-lookup"><span data-stu-id="a63e0-110">An updater simply has to bring down the newest bits for the assembly, which can exist side-by-side with an earlier version of the assembly.</span></span>

 

 
