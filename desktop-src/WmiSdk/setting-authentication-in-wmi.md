---
description: 在呼叫進程以外或遠端 WMI 服務中進行呼叫時，WMI 會使用元件物件模型的分散式版本 (DCOM) 。
ms.assetid: 261b4f18-5de5-4e06-a887-f5afd9c45511
ms.tgt_platform: multiple
title: 在 WMI 中設定驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0293d74c528e7c1c0e77a1ffb9f5f9ee7dfd5f00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193634"
---
# <a name="setting-authentication-in-wmi"></a><span data-ttu-id="fb762-103">在 WMI 中設定驗證</span><span class="sxs-lookup"><span data-stu-id="fb762-103">Setting Authentication in WMI</span></span>

<span data-ttu-id="fb762-104">在呼叫進程以外或遠端 WMI 服務中進行呼叫時，WMI 會使用元件物件模型的分散式版本 (DCOM) 。</span><span class="sxs-lookup"><span data-stu-id="fb762-104">When making calls outside of the calling process or to a remote WMI service, WMI uses the distributed version of the Component Object Model (DCOM).</span></span> <span data-ttu-id="fb762-105">跨進程和遠端呼叫是透過 proxy 進行，需要驗證呼叫進程的認證。</span><span class="sxs-lookup"><span data-stu-id="fb762-105">Out-of-process and remote calls are made through proxies, which require authentication of the credentials of the calling process.</span></span>

<span data-ttu-id="fb762-106">連接到電腦和 WMI 命名空間時，您可以設定驗證等級。</span><span class="sxs-lookup"><span data-stu-id="fb762-106">You set the authentication level when connecting to a computer and WMI namespace.</span></span> <span data-ttu-id="fb762-107">若要連接至 WMI，請在 c + + 中呼叫 [**IWbemLocator：： ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) 。</span><span class="sxs-lookup"><span data-stu-id="fb762-107">To connect to WMI, call [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) in C++.</span></span> <span data-ttu-id="fb762-108">在腳本或 Visual Basic 中，您可以使用 Wbemscripting.swbemlocator ConnectServer 或透過 [標記](constructing-a-moniker-string.md) 字串連接至 WMI。</span><span class="sxs-lookup"><span data-stu-id="fb762-108">In scripting or Visual Basic, you connect to WMI using SWbemLocator.ConnectServer or through the [moniker](constructing-a-moniker-string.md) string.</span></span> <span data-ttu-id="fb762-109">DCOM 安全性和 WMI 在電腦之間連接時都需要某些驗證等級。</span><span class="sxs-lookup"><span data-stu-id="fb762-109">DCOM security and WMI both require certain authentication levels when connecting between computers.</span></span> <span data-ttu-id="fb762-110">必要層級會根據您所連接的作業系統而有所不同。</span><span class="sxs-lookup"><span data-stu-id="fb762-110">The required level differs according to which operating system you are connecting.</span></span> <span data-ttu-id="fb762-111">如需詳細資訊，請參閱 [連接到遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)。</span><span class="sxs-lookup"><span data-stu-id="fb762-111">For more information, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span>

<span data-ttu-id="fb762-112">WMI 通常會在共用服務主機中執行，並與主機中的其他進程共用相同的驗證。</span><span class="sxs-lookup"><span data-stu-id="fb762-112">WMI normally runs in a shared service host and shares the same authentication as other processes in the host.</span></span> <span data-ttu-id="fb762-113">若要以不同層級的驗證執行 WMI 進程，請使用 [**winmgmt**](winmgmt.md) 命令搭配 **/standalonehost** 參數來執行 wmi，並一般設定 wmi 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="fb762-113">To run the WMI process with a different level of authentication, run WMI with the [**winmgmt**](winmgmt.md) command with the **/standalonehost** switch and set the authentication level for WMI generally.</span></span> <span data-ttu-id="fb762-114">如需詳細資訊，請參閱 [維護 WMI 安全性](maintaining-wmi-security.md)。</span><span class="sxs-lookup"><span data-stu-id="fb762-114">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

<span data-ttu-id="fb762-115">如需如何為 WMI 連接設定驗證的詳細資訊和程式碼範例，請參閱 [使用 VBScript 設定驗證服務](setting-the-authentication-service-using-vbscript.md) 和 [使用 c + + 設定驗證](setting-authentication-using-c-.md)。</span><span class="sxs-lookup"><span data-stu-id="fb762-115">For more information and code examples of how to set authentication for WMI connections, see [Setting the Authentication Service using VBScript](setting-the-authentication-service-using-vbscript.md) and [Setting Authentication Using C++](setting-authentication-using-c-.md).</span></span> <span data-ttu-id="fb762-116">這些主題也包含列出 c + + 和腳本之驗證常數的資料表。</span><span class="sxs-lookup"><span data-stu-id="fb762-116">These topics also contain tables that list the authentication constants for C++ and scripting.</span></span>

## <a name="using-proxies-in-wmi"></a><span data-ttu-id="fb762-117">在 WMI 中使用 proxy</span><span class="sxs-lookup"><span data-stu-id="fb762-117">Using Proxies in WMI</span></span>

<span data-ttu-id="fb762-118">若要設定 proxy 的驗證，請呼叫 [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) 函數。</span><span class="sxs-lookup"><span data-stu-id="fb762-118">To set authentication for a proxy, call the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) function.</span></span> <span data-ttu-id="fb762-119">如需詳細資訊和程式碼範例，請參閱 [設定 IWbemServices 和其他 proxy 的安全性](setting-the-security-on-iwbemservices-and-other-proxies.md)。</span><span class="sxs-lookup"><span data-stu-id="fb762-119">For more information and a code example, see [Setting the Security on IWbemServices and Other Proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).</span></span>

<span data-ttu-id="fb762-120">下列 [適用于 WMI 物件的 COM API](com-api-for-wmi.md) 會直接在 c + + 或 c # 中使用 proxy，以呼叫進程外或遠端 WMI 服務：</span><span class="sxs-lookup"><span data-stu-id="fb762-120">The following [COM API for WMI](com-api-for-wmi.md) objects use proxies directly in C++ or C# to call out of process or to a remote WMI service:</span></span>

-   [<span data-ttu-id="fb762-121">**IWbemServices**</span><span class="sxs-lookup"><span data-stu-id="fb762-121">**IWbemServices**</span></span>](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)
-   [<span data-ttu-id="fb762-122">**IEnumWbemClassObject**</span><span class="sxs-lookup"><span data-stu-id="fb762-122">**IEnumWbemClassObject**</span></span>](/windows/desktop/api/Wbemcli/nn-wbemcli-ienumwbemclassobject)
-   [<span data-ttu-id="fb762-123">**IWbemCallResult**</span><span class="sxs-lookup"><span data-stu-id="fb762-123">**IWbemCallResult**</span></span>](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult)
-   [<span data-ttu-id="fb762-124">**IWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="fb762-124">**IWbemRefresher**</span></span>](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher)

<span data-ttu-id="fb762-125">腳本物件（例如 [**SWbemObject**](swbemobject.md)、 [**SWbemServices**](swbemservices.md)和 [**SWbemRefresher**](swbemrefresher.md) ）不會直接使用 proxy。</span><span class="sxs-lookup"><span data-stu-id="fb762-125">The scripting objects, such as [**SWbemObject**](swbemobject.md), [**SWbemServices**](swbemservices.md), and [**SWbemRefresher**](swbemrefresher.md) do not use proxies directly.</span></span> <span data-ttu-id="fb762-126">相反地，腳本物件代表包裝函式或圖層，可針對上面所列的 WMI 物件呼叫 [COM API](com-api-for-wmi.md) 。</span><span class="sxs-lookup"><span data-stu-id="fb762-126">Instead, the scripting objects represent a wrapper or layer that calls into the [COM API for WMI](com-api-for-wmi.md) objects listed above.</span></span> <span data-ttu-id="fb762-127">如需在腳本中設定驗證的詳細資訊和程式碼範例，請參閱 [使用 VBScript 設定預設進程安全性層級](setting-the-default-process-security-level-using-vbscript.md)。</span><span class="sxs-lookup"><span data-stu-id="fb762-127">For more information and a code example of setting authentication in scripting, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

 

 
