---
description: 當套件包含隔離的元件時，Windows Installer 在重新安裝應用程式期間執行下列動作。 通常， \_ 共用元件是元件 \_ 應用程式和其他用戶端可執行檔共用的 DLL。
ms.assetid: 65909b47-dc09-4e9a-920a-9cb3f55b2e67
title: 重新安裝隔離的元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ad1c7fb53eb09e96882209f7738e95be9b4a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849146"
---
# <a name="reinstallation-of-isolated-components"></a><span data-ttu-id="6dbdb-104">重新安裝隔離的元件</span><span class="sxs-lookup"><span data-stu-id="6dbdb-104">Reinstallation of Isolated Components</span></span>

<span data-ttu-id="6dbdb-105">當套件包含隔離的元件時，Windows Installer 在重新安裝應用程式期間執行下列動作。</span><span class="sxs-lookup"><span data-stu-id="6dbdb-105">Windows Installer performs the following actions during reinstallation of an application when the package contains isolated components.</span></span> <span data-ttu-id="6dbdb-106">通常， \_ 共用元件是元件 \_ 應用程式和其他用戶端可執行檔共用的 DLL。</span><span class="sxs-lookup"><span data-stu-id="6dbdb-106">Typically, Component\_Shared is a DLL that is shared by Component\_Application and other client executables.</span></span>

## <a name="reinstallation"></a><span data-ttu-id="6dbdb-107">重新安裝</span><span class="sxs-lookup"><span data-stu-id="6dbdb-107">Reinstallation</span></span>

-   <span data-ttu-id="6dbdb-108">\_ \_ 只有在 \_ 同時重新安裝元件應用程式時，才將與元件應用程式共用的元件檔案重新安裝在同一個資料夾中。</span><span class="sxs-lookup"><span data-stu-id="6dbdb-108">Reinstall of the files of Component\_Shared into the same folder as Component\_Application only if Component\_Application is also being reinstalled.</span></span>
-   <span data-ttu-id="6dbdb-109">請勿遞增共用元件的用戶端清單 \_ ，也不會遞增 SharedDLL 計數。</span><span class="sxs-lookup"><span data-stu-id="6dbdb-109">Do not increment the client list of Component\_Shared and do not increment the SharedDLL count.</span></span>
-   <span data-ttu-id="6dbdb-110">使用元件應用程式金鑰檔的簡短檔案名來重新建立零位元組檔案 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6dbdb-110">Recreate the zero-byte file with the short file name of the key file of Component\_Application.</span></span> <span data-ttu-id="6dbdb-111">這個檔案必須位於與元件應用程式相同的資料夾中 \_ ，而且副檔名為。當地。</span><span class="sxs-lookup"><span data-stu-id="6dbdb-111">This file must be located in the same folder as Component\_Application and have the extension .LOCAL.</span></span>
-   <span data-ttu-id="6dbdb-112">照常重新安裝元件應用程式的所有資源 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6dbdb-112">Reinstall all of the resources of Component\_Application as usual.</span></span>

<span data-ttu-id="6dbdb-113">如果共用元件的 SharedDLL refcount \_ 超過1，或其他產品仍在共用的元件用戶端清單上 \_ ：</span><span class="sxs-lookup"><span data-stu-id="6dbdb-113">If the SharedDLL refcount for Component\_Shared is more than 1, or if other products remain on the client list of Component\_Shared:</span></span>

-   <span data-ttu-id="6dbdb-114">將任何檔案重新安裝至共用的元件共用位置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6dbdb-114">Reinstall no files to the shared location of Component\_Shared.</span></span>

<span data-ttu-id="6dbdb-115">如果共用之元件的 SharedDLL refcount \_ 等於1，或沒有其他剩餘的元件共用用戶端 \_ ：</span><span class="sxs-lookup"><span data-stu-id="6dbdb-115">If the SharedDLL refcount for Component\_Shared equals 1, or if there are no other remaining clients of Component\_Shared:</span></span>

-   <span data-ttu-id="6dbdb-116">\_使用檔案[版本控制規則](file-versioning-rules.md)，重新安裝共用位置中共用的元件檔案。</span><span class="sxs-lookup"><span data-stu-id="6dbdb-116">Reinstall of the files of Component\_Shared into the shared location using the [File Versioning Rules](file-versioning-rules.md).</span></span>
-   <span data-ttu-id="6dbdb-117">處理元件共用的所有重新安裝動作 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6dbdb-117">Process all reinstall actions for Component\_Shared.</span></span>
-   <span data-ttu-id="6dbdb-118">如果元件 \_ 共用是 com 元件，請註冊完整的 com 路徑，讓安裝程式語法 \[ $Component \] 和 \[ \# FileKey \] 指向共用的元件共用位置 \_ 。</span><span class="sxs-lookup"><span data-stu-id="6dbdb-118">If Component\_Shared is a COM component, register the full COM path such that the installer syntaxes \[$Component\] and \[\#FileKey\] point to the shared location of Component\_Shared.</span></span>

 

 



