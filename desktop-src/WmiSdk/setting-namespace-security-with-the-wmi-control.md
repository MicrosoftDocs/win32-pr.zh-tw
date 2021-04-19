---
description: WMI 控制項是位於主控台的 MMC 嵌入式管理單元，可用來在本機電腦上手動設定 WMI 命名空間安全性。 您也可以設定腳本的預設命名空間。
ms.assetid: 87c23919-c482-4278-b005-894a8ac21da4
ms.tgt_platform: multiple
title: 使用 WMI 控制項設定命名空間安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e8b6ed7c45b6b0d107f7f4e4b92f31f504900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981041"
---
# <a name="setting-namespace-security-with-the-wmi-control"></a><span data-ttu-id="d0f79-104">使用 WMI 控制項設定命名空間安全性</span><span class="sxs-lookup"><span data-stu-id="d0f79-104">Setting Namespace Security with the WMI Control</span></span>

<span data-ttu-id="d0f79-105">WMI 控制項是位於 **主控台** 的 MMC 嵌入式管理單元，可用來在本機電腦上手動設定 WMI 命名空間安全性。</span><span class="sxs-lookup"><span data-stu-id="d0f79-105">The WMI Control is an MMC snap-in located in the **Control Panel** and is used to set WMI namespace security manually on a local computer.</span></span> <span data-ttu-id="d0f79-106">您也可以設定腳本的預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="d0f79-106">You can also set the default namespace for scripting.</span></span>


<span data-ttu-id="d0f79-107">下列程式說明如何找出 WMI 控制項。</span><span class="sxs-lookup"><span data-stu-id="d0f79-107">The following procedure describes how to locate the WMI Control.</span></span>

<span data-ttu-id="d0f79-108">**找出 WMI 控制項**</span><span class="sxs-lookup"><span data-stu-id="d0f79-108">**To locate the WMI control**</span></span>

1.  <span data-ttu-id="d0f79-109">在 [ **主控台** 中，按兩下 [系統 **管理工具**]。</span><span class="sxs-lookup"><span data-stu-id="d0f79-109">In the **Control Panel**, double-click **Administrative Tools**.</span></span>
2.  <span data-ttu-id="d0f79-110">在 [系統管理工具] 視窗中，按兩下 [電腦管理]。</span><span class="sxs-lookup"><span data-stu-id="d0f79-110">In the **Administrative Tools** window, double-click **Computer Management**.</span></span>
3.  <span data-ttu-id="d0f79-111">在 [ **電腦管理** ] 視窗中，展開 [ **服務和應用程式** ] 樹狀結構，然後按兩下 [ **WMI] 控制項**。</span><span class="sxs-lookup"><span data-stu-id="d0f79-111">In the **Computer Management** window, expand the **Services and Applications** tree and double-click the **WMI Control**.</span></span>
4.  <span data-ttu-id="d0f79-112">以滑鼠右鍵按一下 [ **WMI 控制** ] 圖示，然後選取 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="d0f79-112">Right-click the **WMI Control** icon and select **Properties**.</span></span>

<span data-ttu-id="d0f79-113">下列程式說明如何使用 WMI 控制項，將命名空間的安全性設定為範本，然後以程式設計方式取得安全性設定，以設定其他命名空間的安全性。</span><span class="sxs-lookup"><span data-stu-id="d0f79-113">The following procedure describes how to use the WMI control to set up the security for a namespace as a template, then programmatically obtain the security settings to set security for other namespaces.</span></span>

<span data-ttu-id="d0f79-114">**使用 WMI 控制項設定命名空間安全性**</span><span class="sxs-lookup"><span data-stu-id="d0f79-114">**To set namespace security with the WMI control**</span></span>

1.  <span data-ttu-id="d0f79-115">使用受控物件格式 (MOF) 程式碼來建立新的命名空間。</span><span class="sxs-lookup"><span data-stu-id="d0f79-115">Create a new namespace by using Managed Object Format (MOF) code.</span></span>
2.  <span data-ttu-id="d0f79-116">執行 WMI 控制項，在新的命名空間上設定安全性。</span><span class="sxs-lookup"><span data-stu-id="d0f79-116">Run the WMI Control to set the security on the new namespace.</span></span> <span data-ttu-id="d0f79-117">在 [ **開始** ] 功能表上，按一下 [ **執行** ]，然後輸入 **wmimgmt.msc** ，或查看 [找出 WMI 控制項](#)。</span><span class="sxs-lookup"><span data-stu-id="d0f79-117">On the **Start** menu, click **Run** and type **wmimgmt.msc** or see [Locating the WMI Control](#).</span></span>
3.  <span data-ttu-id="d0f79-118">在 [ **Wmi 控制** ] 窗格中，以滑鼠右鍵按一下 [ **wmi 控制**]，選擇 [ **屬性**]，然後選取 [ **安全性** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="d0f79-118">In the **WMI Control** pane, right-click **WMI Control**, choose **Properties**, and then select the **Security** tab.</span></span>
4.  <span data-ttu-id="d0f79-119">流覽至新的命名空間，按一下 [ **安全性**]，然後設定命名空間的群組和許可權。</span><span class="sxs-lookup"><span data-stu-id="d0f79-119">Navigate to the new namespace, click **Security**, and then configure groups and permissions for the namespace.</span></span>

<span data-ttu-id="d0f79-120">您也可以使用 Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) 來設定命名空間安全性。</span><span class="sxs-lookup"><span data-stu-id="d0f79-120">You can also use Windows Management Instrumentation Command-Line ([WMIC](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754534(v=ws.11))) to set namespace security.</span></span> <span data-ttu-id="d0f79-121">如需詳細資訊，請參閱 [**wmic**](wmic.md)。</span><span class="sxs-lookup"><span data-stu-id="d0f79-121">For more information, see [**wmic**](wmic.md).</span></span>

## <a name="setting-the-default-namespace-for-scripts"></a><span data-ttu-id="d0f79-122">設定腳本的預設命名空間</span><span class="sxs-lookup"><span data-stu-id="d0f79-122">Setting the Default Namespace for Scripts</span></span>

<span data-ttu-id="d0f79-123">如果腳本在連接至 WMI 時未明確連接到命名空間，則 WMI 會使用此控制項中指定的預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="d0f79-123">If a script does not connect explicitly to a namespace when connecting to WMI, then WMI uses the default namespace specified in this control.</span></span> <span data-ttu-id="d0f79-124">在登錄專案中也可以找到預設值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="d0f79-124">The default is also found in the registry entry as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         WBEM
            Scripting
               Default
                  Namespace
```

<span data-ttu-id="d0f79-125">由於預設的命名空間很容易變更，不論是使用此控制項，或是藉由呼叫 [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)的方法以程式設計方式進行，請在透過 [**wbemscripting.swbemlocator 或. ConnectServer**](swbemlocator-connectserver.md)[的呼叫](constructing-a-moniker-string.md)連接至 WMI 時，指定命名空間。</span><span class="sxs-lookup"><span data-stu-id="d0f79-125">Because the default namespace is easy to change, either with this control or programmatically by calling methods of [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), specify the namespace when connecting to WMI either through the [moniker](constructing-a-moniker-string.md) or calls to [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span> <span data-ttu-id="d0f79-126">如需詳細資訊，請參閱 [建立 WMI 腳本](creating-a-wmi-script.md)</span><span class="sxs-lookup"><span data-stu-id="d0f79-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md)</span></span>

<span data-ttu-id="d0f79-127">**設定腳本的預設命名空間**</span><span class="sxs-lookup"><span data-stu-id="d0f79-127">**To set the default namespace for scripts**</span></span>

1.  <span data-ttu-id="d0f79-128">在 [ **WMI 控制項屬性** ] 視窗中，選擇 [ **Advanced （Advanced** ）] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="d0f79-128">In the **WMI Control Properties** window, choose the **Advanced** tab.</span></span>
2.  <span data-ttu-id="d0f79-129">按一下 [ **變更** ] 按鈕，然後選取要做為預設值的命名空間。</span><span class="sxs-lookup"><span data-stu-id="d0f79-129">Click the **Change** button and select the namespace to make the default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0f79-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="d0f79-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0f79-131">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="d0f79-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> </dl>

 

 
