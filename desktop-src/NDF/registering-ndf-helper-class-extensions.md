---
title: 註冊 NDF Helper 類別延伸模組
description: 每個 helper 類別延伸都有許多與其相關聯的登錄機碼。 COM 需要一些金鑰，而 NDF 需要一些金鑰。
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f211517a975bdef61db7937fffa95f13beddc156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675980"
---
# <a name="registering-ndf-helper-class-extensions"></a><span data-ttu-id="9ffa4-104">註冊 NDF Helper 類別延伸模組</span><span class="sxs-lookup"><span data-stu-id="9ffa4-104">Registering NDF Helper Class Extensions</span></span>

<span data-ttu-id="9ffa4-105">每個 helper 類別延伸都有許多與其相關聯的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-105">Each helper class extension has a number of registry keys associated with it.</span></span> <span data-ttu-id="9ffa4-106">COM 需要一些金鑰，而 NDF 需要一些金鑰。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-106">Some keys are required by COM, and some keys are required by NDF.</span></span>

## <a name="com-registry-keys"></a><span data-ttu-id="9ffa4-107">COM 登錄機碼</span><span class="sxs-lookup"><span data-stu-id="9ffa4-107">COM Registry Keys</span></span>

<span data-ttu-id="9ffa4-108">Helper 類別延伸模組必須實作為 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-108">Helper class extensions must be implemented as COM servers.</span></span> <span data-ttu-id="9ffa4-109">必須針對每個 helper 類別延伸模組完成 COM 註冊。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-109">COM registration must be completed for each helper class extension.</span></span> <span data-ttu-id="9ffa4-110">物件的 CLSID、 [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) 介面和 [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) 介面必須註冊。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-110">The object's CLSID, the [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) interface, and the [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) interface must be registered.</span></span> <span data-ttu-id="9ffa4-111">註冊會為 NDF 協助程式類別延伸建立許多與 COM 相關的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-111">Registration creates a number of COM-related registry keys for the NDF helper class extension.</span></span>

## <a name="ndf-registry-keys"></a><span data-ttu-id="9ffa4-112">NDF 登錄機碼</span><span class="sxs-lookup"><span data-stu-id="9ffa4-112">NDF Registry Keys</span></span>

<span data-ttu-id="9ffa4-113">協助程式類別延伸必須先註冊，才能與網路診斷架構和其他相關的 helper 類別互動。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-113">Helper class extensions must be registered before interacting with the Network Diagnostics Framework and with other related helper classes.</span></span> <span data-ttu-id="9ffa4-114">這可透過擴展登錄來完成。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-114">This is accomplished by populating the registry.</span></span>

<span data-ttu-id="9ffa4-115">下列程式示範如何將 helper 類別延伸新增至登錄。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-115">The following procedure shows how to add helper class extensions to the registry.</span></span>

1.  <span data-ttu-id="9ffa4-116">藉由在底下建立 DLL 的索引鍵，以發佈由 DLL 和其相依性所執行之 helper 類別的名稱</span><span class="sxs-lookup"><span data-stu-id="9ffa4-116">Publish the names of helper classes implemented by the DLL and their dependencies by creating a key for the DLL under</span></span>

    <span data-ttu-id="9ffa4-117">**HKLM \\System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper class DLL* \\ **HelperClasses** \\ *helper class Name*</span><span class="sxs-lookup"><span data-stu-id="9ffa4-117">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*</span></span>

    <span data-ttu-id="9ffa4-118">以使用者定義的值取代 *VendorName*、 *helper 類別 DLL* 和 *Helper 類別名稱* ，如下所述。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-118">Replace *VendorName*, *Helper Class DLL*, and *Helper Class Name* with user-defined values as described below.</span></span>

    | <span data-ttu-id="9ffa4-119">值</span><span class="sxs-lookup"><span data-stu-id="9ffa4-119">Value</span></span>               | <span data-ttu-id="9ffa4-120">類型</span><span class="sxs-lookup"><span data-stu-id="9ffa4-120">Type</span></span>    | <span data-ttu-id="9ffa4-121">意義</span><span class="sxs-lookup"><span data-stu-id="9ffa4-121">Meaning</span></span>                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | <span data-ttu-id="9ffa4-122">*VendorName*</span><span class="sxs-lookup"><span data-stu-id="9ffa4-122">*VendorName*</span></span>        | <span data-ttu-id="9ffa4-123">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="9ffa4-123">REG\_SZ</span></span> | <span data-ttu-id="9ffa4-124">廠商的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-124">The name of the vendor.</span></span>                                                      |
    | <span data-ttu-id="9ffa4-125">*Helper 類別 DLL*</span><span class="sxs-lookup"><span data-stu-id="9ffa4-125">*Helper Class DLL*</span></span>  | <span data-ttu-id="9ffa4-126">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="9ffa4-126">REG\_SZ</span></span> | <span data-ttu-id="9ffa4-127">DLL 的名稱，不含副檔名。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-127">Name of the DLL, without extension.</span></span>                                          |
    | <span data-ttu-id="9ffa4-128">*Helper 類別名稱*</span><span class="sxs-lookup"><span data-stu-id="9ffa4-128">*Helper Class Name*</span></span> | <span data-ttu-id="9ffa4-129">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="9ffa4-129">REG\_SZ</span></span> | <span data-ttu-id="9ffa4-130">目前 helper 類別相依的 helper 類別名稱。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-130">The name of the helper class on which the current helper class is dependent.</span></span> |

    

     

2.  <span data-ttu-id="9ffa4-131">在每個協助程式 *類別名稱* 索引鍵下，發佈下列資訊。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-131">Under each *Helper Class Name* key, publish the following information.</span></span>

    

    | <span data-ttu-id="9ffa4-132">值</span><span class="sxs-lookup"><span data-stu-id="9ffa4-132">Value</span></span>         | <span data-ttu-id="9ffa4-133">類型</span><span class="sxs-lookup"><span data-stu-id="9ffa4-133">Type</span></span>       | <span data-ttu-id="9ffa4-134">意義</span><span class="sxs-lookup"><span data-stu-id="9ffa4-134">Meaning</span></span>                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="9ffa4-135">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="9ffa4-135">**CLSID**</span></span>     | <span data-ttu-id="9ffa4-136">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="9ffa4-136">REG\_SZ</span></span>    | <span data-ttu-id="9ffa4-137">包含 helper 類別之 COM 類別識別碼的字串。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-137">A string that contains the COM class ID of the helper class.</span></span>                                                                                                            |
    | <span data-ttu-id="9ffa4-138">**版本**</span><span class="sxs-lookup"><span data-stu-id="9ffa4-138">**Version**</span></span>   | <span data-ttu-id="9ffa4-139">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="9ffa4-139">REG\_SZ</span></span>    | <span data-ttu-id="9ffa4-140">字串，其中包含格式的 helper 類別的主要和次要版本 <major> <minor> 。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-140">A string the contains the major and minor versions of the helper class in the format <major><minor>.</span></span>                                                        |
    | <span data-ttu-id="9ffa4-141">**已發行**</span><span class="sxs-lookup"><span data-stu-id="9ffa4-141">**Published**</span></span> | <span data-ttu-id="9ffa4-142">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="9ffa4-142">REG\_DWORD</span></span> | <span data-ttu-id="9ffa4-143">值為1表示應該直接從診斷用戶端叫用此 helper 類別。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-143">A value of 1 means that this helper class is expected to be directly invoked from the Diagnostics client.</span></span> <span data-ttu-id="9ffa4-144">0表示只能從另一個 helper 類別呼叫它。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-144">0 means that it can be called only from another helper class.</span></span> |
    | <span data-ttu-id="9ffa4-145">**父系**</span><span class="sxs-lookup"><span data-stu-id="9ffa4-145">**Parent**</span></span>    | <span data-ttu-id="9ffa4-146">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="9ffa4-146">REG\_SZ</span></span>    | <span data-ttu-id="9ffa4-147">字串，這個字串會為擴充的 Microsoft 可延伸 helper 類別命名。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-147">A string that names the Microsoft extensible helper class that is being extended.</span></span>                                                                                       |

    

     

3.  <span data-ttu-id="9ffa4-148">針對每個協助程式類別，在底下建立索引鍵以發佈相符屬性的清單</span><span class="sxs-lookup"><span data-stu-id="9ffa4-148">For each helper class, publish the list of matching attributes by creating a key under</span></span>

    <span data-ttu-id="9ffa4-149">**HKLM \\System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper class DLL* \\ **HelperClasses** \\ *Helper class Name* \\ **MatchAttributes**</span><span class="sxs-lookup"><span data-stu-id="9ffa4-149">**HKLM\\System\\CurrentControlSet\\Control\\NetDiagFx**\\*VendorName*\\**HostDLLs**\\*Helper Class DLL*\\**HelperClasses**\\*Helper Class Name*\\**MatchAttributes**</span></span>

    <span data-ttu-id="9ffa4-150">這些索引鍵必須包含一或多個值 (下列類型的每個屬性) 一個以上。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-150">They key must contain one or more values (one per attribute) of the following type.</span></span>

    | <span data-ttu-id="9ffa4-151">值</span><span class="sxs-lookup"><span data-stu-id="9ffa4-151">Value</span></span>             | <span data-ttu-id="9ffa4-152">類型</span><span class="sxs-lookup"><span data-stu-id="9ffa4-152">Type</span></span>                             | <span data-ttu-id="9ffa4-153">意義</span><span class="sxs-lookup"><span data-stu-id="9ffa4-153">Meaning</span></span>                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | <span data-ttu-id="9ffa4-154">**AttributeName**</span><span class="sxs-lookup"><span data-stu-id="9ffa4-154">**AttributeName**</span></span> | <span data-ttu-id="9ffa4-155">REG \_ SZ \| REG \_ DWORD \| REG \_ 二進位檔</span><span class="sxs-lookup"><span data-stu-id="9ffa4-155">REG\_SZ\|REG\_DWORD\|REG\_BINARY</span></span> | <span data-ttu-id="9ffa4-156">值，這個值會完成特定屬性的名稱和值組。</span><span class="sxs-lookup"><span data-stu-id="9ffa4-156">A value that completes the name and value pair for a particular attribute.</span></span> |

    

     

 

 




