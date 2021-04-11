---
description: 當封裝包含隔離的元件時，Windows Installer 在安裝應用程式期間執行下列動作。 通常， \_ 共用元件是元件 \_ 應用程式和其他用戶端可執行檔共用的 DLL。
ms.assetid: fbc5dd86-5d38-4ce8-ab38-03c84cc77e80
title: 獨立元件的安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c1b9a7e21c212474701409e887d0afd5517774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691560"
---
# <a name="installation-of-isolated-components"></a><span data-ttu-id="f1768-104">獨立元件的安裝</span><span class="sxs-lookup"><span data-stu-id="f1768-104">Installation of Isolated Components</span></span>

<span data-ttu-id="f1768-105">當封裝包含隔離的元件時，Windows Installer 在安裝應用程式期間執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="f1768-105">Windows Installer performs the following actions during installation of an application when the package contains isolated components.</span></span> <span data-ttu-id="f1768-106">通常， \_ 共用元件是元件 \_ 應用程式和其他用戶端可執行檔共用的 DLL。</span><span class="sxs-lookup"><span data-stu-id="f1768-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="installation"></a><span data-ttu-id="f1768-107">安裝</span><span class="sxs-lookup"><span data-stu-id="f1768-107">Installation</span></span>

-   <span data-ttu-id="f1768-108">\_ \_ 只有在同時安裝元件應用程式時，才將共用的元件檔案複製到與元件應用程式相同的資料夾中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f1768-108">Copy the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being installed.</span></span>
-   <span data-ttu-id="f1768-109">使用元件應用程式金鑰檔的簡短檔案名來建立零位元組檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f1768-109">Create a zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="f1768-110">在與元件應用程式相同的資料夾中找到這個檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f1768-110">Locate this file in the same folder as Component\_Application.</span></span> <span data-ttu-id="f1768-111">附加延伸模組。這個檔案名的本機。</span><span class="sxs-lookup"><span data-stu-id="f1768-111">Append the extension .LOCAL to this file name.</span></span>
-   <span data-ttu-id="f1768-112">如果在 [元件資料表](component-table.md)的 [屬性] 資料行中設定了 msidbComponentAttributesSharedDllRefCount 位，則遞增 SharedDLL refcount。</span><span class="sxs-lookup"><span data-stu-id="f1768-112">Increment the SharedDLL refcount if the msidbComponentAttributesSharedDllRefCount bit is set in the Attributes column of the [Component table](component-table.md).</span></span>
-   <span data-ttu-id="f1768-113">將元件 \_ 應用程式註冊為共用元件的用戶端 \_ ，並註冊指向共用元件共用位置的金鑰路徑 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f1768-113">Register Component\_Application as a client of Component\_Shared and register a key path pointing to the shared location of Component\_Shared.</span></span>
-   <span data-ttu-id="f1768-114">照常安裝元件應用程式的所有資源 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f1768-114">Install all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="f1768-115">如果 \_ 電腦上已安裝元件共用或其金鑰檔，則不會將檔案複製到共用的元件共用位置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f1768-115">If Component\_Shared or its key file is already installed on the computer do not copy files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="f1768-116">如果 \_ 電腦上尚未安裝元件共用或其金鑰檔：</span><span class="sxs-lookup"><span data-stu-id="f1768-116">If Component\_Shared or its key file is not yet installed on the computer:</span></span>

-   <span data-ttu-id="f1768-117">將共用的元件檔案複製 \_ 到共用位置。</span><span class="sxs-lookup"><span data-stu-id="f1768-117">Copy the files of Component\_Shared to the shared location.</span></span>
-   <span data-ttu-id="f1768-118">處理元件共用的所有安裝動作 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f1768-118">Process all install actions for Component\_Shared.</span></span>
-   <span data-ttu-id="f1768-119">如果元件 \_ 共用是 com 元件，請註冊完整的 com 路徑，讓語法 \[ $Component \] 和 \[ \# FileKey \] 指向共用的元件共用位置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f1768-119">If Component\_Shared is a COM component, register the full COM path such that the syntax \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



