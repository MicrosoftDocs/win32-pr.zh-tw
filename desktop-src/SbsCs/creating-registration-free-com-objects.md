---
description: 啟用內容可讓您使用 COM 物件，而不需要註冊它們。
ms.assetid: e6ec7b8b-8032-4dff-8f96-07ae3ffc286d
title: 建立 Registration-Free COM 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70e377a04f44e6624294116b8274a8dcc1e82b8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106982490"
---
# <a name="creating-registration-free-com-objects"></a><span data-ttu-id="9fd8f-103">建立 Registration-Free COM 物件</span><span class="sxs-lookup"><span data-stu-id="9fd8f-103">Creating Registration-Free COM Objects</span></span>

<span data-ttu-id="9fd8f-104">啟用內容可讓您使用 COM 物件，而不需要註冊它們。</span><span class="sxs-lookup"><span data-stu-id="9fd8f-104">Activation contexts enable COM objects to be used without requiring that they be registered.</span></span> <span data-ttu-id="9fd8f-105">這可讓您的應用程式根據其版本而非其登錄資訊，讓多個元件具有不同的功能。</span><span class="sxs-lookup"><span data-stu-id="9fd8f-105">This enables your application to have multiple components with different functionality based upon their version rather than their registry information.</span></span> <span data-ttu-id="9fd8f-106">多個元件可以使用相同的 GUID 來公開相同的 COM 物件，但根據版本有不同的功能。</span><span class="sxs-lookup"><span data-stu-id="9fd8f-106">Multiple components can expose the same COM object with the same GUID but have different functionality based on the version.</span></span>

<span data-ttu-id="9fd8f-107">當應用程式從 [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid)要求 GUID 時，COM 會先在使用中的啟用內容中搜尋從 PROGID 到 CLSID 的對應。</span><span class="sxs-lookup"><span data-stu-id="9fd8f-107">When an application requests a GUID from [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid), COM first searches for the mapping from progid to CLSID in the active activation context.</span></span> <span data-ttu-id="9fd8f-108">當應用程式使用 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來取得實例介面指標時，COM 會在作用中的啟用內容中搜尋，以找出將裝載 CLSID 的 DLL。</span><span class="sxs-lookup"><span data-stu-id="9fd8f-108">When an application uses [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to obtain an instance interface pointer, COM searches in the active activation context to find which DLL will host the CLSID.</span></span> <span data-ttu-id="9fd8f-109">如果啟用內容不包含所需的資訊，COM 就會使用一般方法在登錄中搜尋資訊。</span><span class="sxs-lookup"><span data-stu-id="9fd8f-109">If the activation context does not contain the required information, COM then searches for the information in the registry using the usual method.</span></span>

<span data-ttu-id="9fd8f-110">請注意，由於啟用內容是個別執行緒的，COM 會將建立執行緒的啟用內容封送處理到主執行緒，並在主執行緒上呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 或 [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) 之前啟動它。</span><span class="sxs-lookup"><span data-stu-id="9fd8f-110">Note that because activation contexts are per-thread, COM marshals the activation context of the creating thread over to the host thread and activates it before calling [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) or [**DllGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) on the host thread.</span></span> <span data-ttu-id="9fd8f-111">Windows 中已經有這項功能，用戶端程式代碼不需要執行任何動作來執行此作業。</span><span class="sxs-lookup"><span data-stu-id="9fd8f-111">This functionality is already present in Windows, client code is not required to do anything to implement this.</span></span>

<span data-ttu-id="9fd8f-112">裝載的元件可以匯出 COM 類別，而不需要經過登錄。</span><span class="sxs-lookup"><span data-stu-id="9fd8f-112">COM classes can be exported by hosted components without going through the registry.</span></span> <span data-ttu-id="9fd8f-113">多個元件可以針對不同的 COM 物件公開相同的 ProgID，而您的裝載應用程式應該只尋找適當的啟用內容，然後使用 [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) 和 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 來取得主控物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="9fd8f-113">Multiple components can expose the same ProgID for different COM objects, and your hosting application should only find the proper activation context and then use [**CLSIDFromProgID**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) to get the hosted object's interface pointers.</span></span>

 

 
