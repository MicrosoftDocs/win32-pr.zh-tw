---
description: 使用 WMI SNMP 介面與網路裝置通訊，需要設定裝置、SNMP 和 WMI 服務。 本主題中的資訊說明如何設定 WMI SNMP 環境。
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: 設定 WMI SNMP 環境
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeed470b1e38bf853bd6b023fa0f07b01c5df47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320667"
---
# <a name="setting-up-the-wmi-snmp-environment"></a><span data-ttu-id="1aec8-104">設定 WMI SNMP 環境</span><span class="sxs-lookup"><span data-stu-id="1aec8-104">Setting up the WMI SNMP Environment</span></span>

<span data-ttu-id="1aec8-105">使用 WMI SNMP 介面與網路裝置通訊，需要設定裝置、SNMP 和 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="1aec8-105">Communicating with a network device using the WMI SNMP interface requires the configuration of the device, SNMP, and WMI services.</span></span> <span data-ttu-id="1aec8-106">本主題中的資訊說明如何設定 WMI SNMP 環境。</span><span class="sxs-lookup"><span data-stu-id="1aec8-106">The information in this topic explains how to set up the WMI SNMP environment.</span></span>

<span data-ttu-id="1aec8-107">本主題將討論下列各節：</span><span class="sxs-lookup"><span data-stu-id="1aec8-107">The following sections are discussed in this topic:</span></span>

## <a name="installing-the-snmp-provider"></a><span data-ttu-id="1aec8-108">安裝 SNMP 提供者</span><span class="sxs-lookup"><span data-stu-id="1aec8-108">Installing the SNMP Provider</span></span>

<span data-ttu-id="1aec8-109">SNMP 服務預設不會啟用。</span><span class="sxs-lookup"><span data-stu-id="1aec8-109">The SNMP service is not enabled by default.</span></span> <span data-ttu-id="1aec8-110">您可以透過主控台啟用 SNMP 服務和 WMI SNMP 提供者。</span><span class="sxs-lookup"><span data-stu-id="1aec8-110">You can enable the SNMP service and the WMI SNMP Provider through the Control Panel.</span></span> <span data-ttu-id="1aec8-111">請注意，必須啟用並執行 SNMP 服務，WMI SNMP 提供者才能運作。</span><span class="sxs-lookup"><span data-stu-id="1aec8-111">Be aware that the SNMP service must be enabled and running for the WMI SNMP provider to work.</span></span>

<span data-ttu-id="1aec8-112">從 Windows Vista 開始，請使用下列程式來安裝 SNMP 提供者。</span><span class="sxs-lookup"><span data-stu-id="1aec8-112">Starting with Windows Vista, use the following procedure to install the SNMP provider.</span></span>

<span data-ttu-id="1aec8-113">**安裝 SNMP 提供者**</span><span class="sxs-lookup"><span data-stu-id="1aec8-113">**To install the SNMP Provider**</span></span>

1.  <span data-ttu-id="1aec8-114">從 **主控台** 選取 [ **程式**]。</span><span class="sxs-lookup"><span data-stu-id="1aec8-114">From the **Control Panel**, select **Programs**.</span></span>
2.  <span data-ttu-id="1aec8-115">在 [ **程式和功能**] 下，選取 [ **開啟或關閉 Windows 功能**]。</span><span class="sxs-lookup"><span data-stu-id="1aec8-115">Under **Programs and Features**, select **Turn Windows features on or off**.</span></span>
3.  <span data-ttu-id="1aec8-116">在 [Windows 功能] 清單中，向下滾動至 **SNMP 功能** 並展開清單，讓您可以看到 **WMI SNMP 提供者**。</span><span class="sxs-lookup"><span data-stu-id="1aec8-116">In the Windows features list, scroll down to **SNMP feature** and expand the list so that you can see **WMI SNMP Provider**.</span></span>
4.  <span data-ttu-id="1aec8-117">選取 [ **WMI SNMP 提供者**] 的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="1aec8-117">Select the check box for **WMI SNMP Provider**.</span></span> <span data-ttu-id="1aec8-118">系統會自動選取 [ **snmp] 功能** 的核取方塊，因為提供者需要 SNMP。</span><span class="sxs-lookup"><span data-stu-id="1aec8-118">The check box for **SNMP feature** is selected automatically because the provider requires SNMP.</span></span>
5.  <span data-ttu-id="1aec8-119">按一下 [確定]  。</span><span class="sxs-lookup"><span data-stu-id="1aec8-119">Click **OK**.</span></span>
6.  <span data-ttu-id="1aec8-120">從命令提示字元或 [ **開始** ] 功能表，執行 services.msc，並確認 SNMP 服務已啟動。</span><span class="sxs-lookup"><span data-stu-id="1aec8-120">From a command prompt or the **Start** menu, run Services.msc and ensure that the SNMP service is started.</span></span>

## <a name="creating-an-snmp-namespace"></a><span data-ttu-id="1aec8-121">建立 SNMP 命名空間</span><span class="sxs-lookup"><span data-stu-id="1aec8-121">Creating an SNMP Namespace</span></span>

<span data-ttu-id="1aec8-122">SNMP 命名空間會定義網路裝置的觀點。</span><span class="sxs-lookup"><span data-stu-id="1aec8-122">An SNMP namespace defines a view of a network device.</span></span>

> [!Note]  
> <span data-ttu-id="1aec8-123">如需有關在特定作業系統上支援和安裝此元件的詳細資訊，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。</span><span class="sxs-lookup"><span data-stu-id="1aec8-123">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="1aec8-124">下列程式說明如何建立 SNMP WMI [*命名空間*](gloss-n.md)。</span><span class="sxs-lookup"><span data-stu-id="1aec8-124">The following procedure describes how to create an SNMP WMI [*namespace*](gloss-n.md).</span></span>

<span data-ttu-id="1aec8-125">**建立 SNMP 命名空間**</span><span class="sxs-lookup"><span data-stu-id="1aec8-125">**To create an SNMP namespace**</span></span>

1.  <span data-ttu-id="1aec8-126">藉由編譯 [*受控物件格式*](gloss-m.md)的 mof 檔案或使用 [適用于 WMI 的 COM API](com-api-for-wmi.md)，建立 [**\_ \_ 命名空間**](--namespace.md)系統類別的實例。</span><span class="sxs-lookup"><span data-stu-id="1aec8-126">Create an instance of the [**\_\_Namespace**](--namespace.md) system class either by compiling a [*Managed Object Format*](gloss-m.md) .mof file or by using the [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="1aec8-127">如需詳細資訊，請參閱 [在 WMI 中建立](creating-hierarchies-within-wmi.md)階層。</span><span class="sxs-lookup"><span data-stu-id="1aec8-127">For more information, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

2.  <span data-ttu-id="1aec8-128">將 SNMP 提供者 [*限定詞*](gloss-q.md) 與命名空間定義產生關聯。</span><span class="sxs-lookup"><span data-stu-id="1aec8-128">Associate SNMP provider [*qualifiers*](gloss-q.md) with the namespace definition.</span></span>

    <span data-ttu-id="1aec8-129">SNMP 提供者限定詞包含執行特定的內容資訊和傳輸屬性，可定義 SNMP 提供者存取 SNMP 裝置的方式。</span><span class="sxs-lookup"><span data-stu-id="1aec8-129">The SNMP provider qualifiers contain implementation-specific context information and transport properties that define how the SNMP provider accesses an SNMP device.</span></span> <span data-ttu-id="1aec8-130">如需詳細資訊，請參閱 [**SNMP 提供者專用的限定詞**](qualifiers-specific-to-the-snmp-provider.md)。</span><span class="sxs-lookup"><span data-stu-id="1aec8-130">For more information, see [**Qualifiers Specific to the SNMP Provider**](qualifiers-specific-to-the-snmp-provider.md).</span></span>

3.  <span data-ttu-id="1aec8-131">使用 [mofcomp.exe](mofcomp.md) 命令列工具，將 MOF 程式碼載入至 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="1aec8-131">Use the [mofcomp](mofcomp.md) command line tool to load the MOF code into the WMI repository.</span></span>

    <span data-ttu-id="1aec8-132">如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="1aec8-132">For more information, see [Compiling MOF files](compiling-mof-files.md).</span></span>

<span data-ttu-id="1aec8-133">下列 MOF 程式碼範例 \\ 會使用可與 snmp 命名空間相關聯的限定詞子集來定義 snmp 命名空間。</span><span class="sxs-lookup"><span data-stu-id="1aec8-133">The following MOF code example defines the \\snmp namespace with a subset of the qualifiers that can be associated with an SNMP namespace.</span></span>

``` syntax
// Load classes and instances into <\\.\root> namespace

#pragma namespace("\\\\.\\root")               

[ 
  AgentAddress( "localhost" ), 
  AgentReadCommunityName( "public"), 
  AgentWriteCommunityName( "private"), 
  AgentRetryCount( 1 ), 
  AgentRetryTimeout( 500 ), 
  AgentVarBindsPerPdu( 10 ),
  AgentFlowControlWindowSize ( 3 ) 
]

  instance of __Namespace
  {
      Name = "snmp" ;
  };
```

## <a name="inserting-snmp-mib-data-into-wmi"></a><span data-ttu-id="1aec8-134">將 SNMP MIB 資料插入 WMI</span><span class="sxs-lookup"><span data-stu-id="1aec8-134">Inserting SNMP MIB Data into WMI</span></span>

<span data-ttu-id="1aec8-135">作為提供者，SNMP 提供者可做為 SNMP 資料與 WMI 類別之間的橋樑。</span><span class="sxs-lookup"><span data-stu-id="1aec8-135">As a provider, the SNMP provider acts as a bridge between SNMP data and WMI classes.</span></span> <span data-ttu-id="1aec8-136">因此，您的 WMI 中必須有類別，代表啟用 SNMP 的裝置的不同層面。</span><span class="sxs-lookup"><span data-stu-id="1aec8-136">Therefore, you must have classes in WMI that represent different aspects of an SNMP-enabled device.</span></span> <span data-ttu-id="1aec8-137">若要這樣做，您必須使用 SNMP 資訊模組編譯器 ([smi2smir](smi2smir.md)) ，將 snmp 管理資訊從 snmp 格式編譯成相等的 CIM 架構定義。</span><span class="sxs-lookup"><span data-stu-id="1aec8-137">To do so, you must use the SNMP information module compiler ([smi2smir](smi2smir.md)) to compile SNMP management information from the SNMP format into the equivalent CIM schema definitions.</span></span> <span data-ttu-id="1aec8-138">然後，您可以將資訊編譯器的輸出導向至稱為「SNMP 模組資訊存放庫 (SMIR) 」的 SNMP 架構資料庫，或指向數種不同的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="1aec8-138">You can then direct the output of the information compiler into an SNMP schema database called the "SNMP Module Information Repository (SMIR)" or to several different kinds of MOF files.</span></span>

<span data-ttu-id="1aec8-139">編譯器會以命令列模式執行，並使用一個 MIB 檔案作為輸入。</span><span class="sxs-lookup"><span data-stu-id="1aec8-139">The compiler runs in the command-line mode, using one MIB file as input.</span></span> <span data-ttu-id="1aec8-140">下列命令會將指定的 MIB 檔案載入 SMIR 中。</span><span class="sxs-lookup"><span data-stu-id="1aec8-140">The following command loads the specified MIB file into the SMIR.</span></span>

<span data-ttu-id="1aec8-141">\**smi2smir/a\*\*\*<MIB file>*</span><span class="sxs-lookup"><span data-stu-id="1aec8-141">**smi2smir /a** *<MIB file>*</span></span>

## <a name="setting-up-snmp-communities"></a><span data-ttu-id="1aec8-142">設定 SNMP 團體</span><span class="sxs-lookup"><span data-stu-id="1aec8-142">Setting Up SNMP Communities</span></span>

<span data-ttu-id="1aec8-143">作為安全性措施，預設不會建立 SNMP 「公用」群組。</span><span class="sxs-lookup"><span data-stu-id="1aec8-143">As a security measure, the SNMP "public" community is not created by default.</span></span> <span data-ttu-id="1aec8-144">您可以建立如「 [社區登錄設定](/previous-versions/windows/embedded/ms907028(v=msdn.10))」中所述的「社區」。</span><span class="sxs-lookup"><span data-stu-id="1aec8-144">You can create the community as described in [Communities Registry Settings](/previous-versions/windows/embedded/ms907028(v=msdn.10)).</span></span> <span data-ttu-id="1aec8-145">如果您沒有任何社區，請建立「公用」群體來存取 SNMP 提供者。</span><span class="sxs-lookup"><span data-stu-id="1aec8-145">If you do not have any community, then create the "public" community to access the SNMP provider.</span></span>

## <a name="generating-mof-files-from-mib-files"></a><span data-ttu-id="1aec8-146">從 MIB 檔案產生 MOF 檔案</span><span class="sxs-lookup"><span data-stu-id="1aec8-146">Generating MOF Files from MIB Files</span></span>

<span data-ttu-id="1aec8-147">下列命令是一個範例，說明如何從安裝 SNMP 提供者時所安裝的 MIB 檔案產生 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="1aec8-147">The following commands are an example of how to generate MOF files from the MIB files that are installed when the SNMP provider is installed.</span></span>

<span data-ttu-id="1aec8-148">**cd** *% windir% \\ system32 \\ wbem \\ SNMP*</span><span class="sxs-lookup"><span data-stu-id="1aec8-148">**cd** *%windir%\\system32\\wbem\\SNMP*</span></span>

<span data-ttu-id="1aec8-149">**Smi2smir/g** *... \\ . \\hostmib mib* **>** *hostmib mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-149">**Smi2smir /g** *..\\..\\hostmib.mib* **>** *hostmib.mof*</span></span>

<span data-ttu-id="1aec8-150">**Smi2smir/g** *... \\ . \\ipforwd mib* **>** *ipforwd mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-150">**Smi2smir /g** *..\\..\\ipforwd.mib* **>** *ipforwd.mof*</span></span>

<span data-ttu-id="1aec8-151">**Smi2smir/g** *... \\ . \\nipx mib* **>** *nipx mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-151">**Smi2smir /g** *..\\..\\nipx.mib* **>** *nipx.mof*</span></span>

<span data-ttu-id="1aec8-152">**Smi2smir/g** *... \\ . \\mib \_ ii. mib* **>** *mib （ \_ mof* ）</span><span class="sxs-lookup"><span data-stu-id="1aec8-152">**Smi2smir /g** *..\\..\\mib\_ii.mib* **>** *mib\_ii.mof*</span></span>

<span data-ttu-id="1aec8-153">**Smi2smir/g** *... \\ . \\lmmib2 mib* **>** *lmmib2 mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-153">**Smi2smir /g** *..\\..\\lmmib2.mib* **>** *lmmib2.mof*</span></span>

<span data-ttu-id="1aec8-154">**Smi2smir/g** *... \\ . \\mcastmib mib* **>** *mcastmib mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-154">**Smi2smir /g** *..\\..\\mcastmib.mib* **>** *mcastmib.mof*</span></span>

<span data-ttu-id="1aec8-155">**Smi2smir/g** *... \\ . \\rfc2571 mib* **>** *rfc2571 mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-155">**Smi2smir /g** *..\\..\\rfc2571.mib* **>** *rfc2571.mof*</span></span>

<span data-ttu-id="1aec8-156">**Smi2smir/g** *... \\ . \\wfospf mib* **>** *wfospf mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-156">**Smi2smir /g** *..\\..\\wfospf.mib* **>** *wfospf.mof*</span></span>

<span data-ttu-id="1aec8-157">**Smi2smir/g** *... \\ . \\dhcp \\ ... \\ 。msft. mib* **>** *dhcp*</span><span class="sxs-lookup"><span data-stu-id="1aec8-157">**Smi2smir /g** *..\\..\\dhcp.mib..\\..\\msft.mib* **>** *dhcp.mof*</span></span>

<span data-ttu-id="1aec8-158">**Smi2smir/g** *... \\ . \\wins .... \\ \\msft.* **>**  。</span><span class="sxs-lookup"><span data-stu-id="1aec8-158">**Smi2smir /g** *..\\..\\wins.mib..\\..\\msft.mib* **>** *wins.mof*</span></span>

<span data-ttu-id="1aec8-159">**Smi2smir/g** *... \\ . \\mipx .... \\ \\msft. mib* **>** *mipx. mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-159">**Smi2smir /g** *..\\..\\mipx.mib..\\..\\msft.mib* **>** *mipx.mof*</span></span>

<span data-ttu-id="1aec8-160">**Smi2smir/g** *... \\ . \\mripsap .... \\ \\msft. mib* **>** *mripsap. mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-160">**Smi2smir /g** *..\\..\\mripsap.mib..\\..\\msft.mib* **>** *mripsap.mof*</span></span>

<span data-ttu-id="1aec8-161">**Smi2smir/g** *... \\ . \\msipbtp .... \\ \\msft. mib* **>** *msipbtp. mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-161">**Smi2smir /g** *..\\..\\msipbtp.mib..\\..\\msft.mib* **>** *msipbtp.mof*</span></span>

<span data-ttu-id="1aec8-162">**Smi2smir/g** *... \\ . \\msiprip2 .... \\ \\msft. mib* **>** *msiprip2. mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-162">**Smi2smir /g** *..\\..\\msiprip2.mib..\\..\\msft.mib* **>** *msiprip2.mof*</span></span>

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a><span data-ttu-id="1aec8-163">將 SNMP MOF 檔案新增至 WMI 儲存機制</span><span class="sxs-lookup"><span data-stu-id="1aec8-163">Adding SNMP MOF Files to the WMI Repository</span></span>

<span data-ttu-id="1aec8-164">下列命令是一個範例，說明如何將從 MIB 檔案產生的 MOF 檔案新增至 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="1aec8-164">The following commands are an example of how to add the MOF files that are generated from the MIB files to the WMI repository.</span></span> <span data-ttu-id="1aec8-165">如果您想要將 MOF 檔案新增至 [*WMI 儲存*](gloss-w.md) 機制復原中要自動還原的檔案清單，請在每個命令的結尾新增 **-自動** 復原旗標。</span><span class="sxs-lookup"><span data-stu-id="1aec8-165">If you want to add the MOF files to the list of files to be automatically restored in a [*WMI repository*](gloss-w.md) recovery, add the **-AUTORECOVER** flag to the end of each command.</span></span> <span data-ttu-id="1aec8-166">如需 WMI Mofcomp.exe 命令列工具的詳細資訊，請參閱 [**mofcomp.exe**](mofcomp.md)。</span><span class="sxs-lookup"><span data-stu-id="1aec8-166">For more information about the WMI Mofcomp.exe command-line tool, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="1aec8-167">**mofcomp.exe** *hostmib*</span><span class="sxs-lookup"><span data-stu-id="1aec8-167">**mofcomp** *hostmib.mof*</span></span>

<span data-ttu-id="1aec8-168">**mofcomp.exe** *ipforwd*</span><span class="sxs-lookup"><span data-stu-id="1aec8-168">**mofcomp** *ipforwd.mof*</span></span>

<span data-ttu-id="1aec8-169">**mofcomp.exe** *nipx*</span><span class="sxs-lookup"><span data-stu-id="1aec8-169">**mofcomp** *nipx.mof*</span></span>

<span data-ttu-id="1aec8-170">**mofcomp.exe** *mib \_ ii. mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-170">**mofcomp** *mib\_ii.mof*</span></span>

<span data-ttu-id="1aec8-171">**mofcomp.exe** *lmmib2*</span><span class="sxs-lookup"><span data-stu-id="1aec8-171">**mofcomp** *lmmib2.mof*</span></span>

<span data-ttu-id="1aec8-172">**mofcomp.exe** *mcastmib*</span><span class="sxs-lookup"><span data-stu-id="1aec8-172">**mofcomp** *mcastmib.mof*</span></span>

<span data-ttu-id="1aec8-173">**mofcomp.exe** *rfc2571*</span><span class="sxs-lookup"><span data-stu-id="1aec8-173">**mofcomp** *rfc2571.mof*</span></span>

<span data-ttu-id="1aec8-174">**mofcomp.exe** *wfospf*</span><span class="sxs-lookup"><span data-stu-id="1aec8-174">**mofcomp** *wfospf.mof*</span></span>

<span data-ttu-id="1aec8-175">**mofcomp.exe** *dhcp mof*</span><span class="sxs-lookup"><span data-stu-id="1aec8-175">**mofcomp** *dhcp.mof*</span></span>

<span data-ttu-id="1aec8-176">**mofcomp.exe** *mipx*</span><span class="sxs-lookup"><span data-stu-id="1aec8-176">**mofcomp** *mipx.mof*</span></span>

<span data-ttu-id="1aec8-177">**mofcomp.exe** *mripsap*</span><span class="sxs-lookup"><span data-stu-id="1aec8-177">**mofcomp** *mripsap.mof*</span></span>

<span data-ttu-id="1aec8-178">**mofcomp.exe** *msipbtp*</span><span class="sxs-lookup"><span data-stu-id="1aec8-178">**mofcomp** *msipbtp.mof*</span></span>

<span data-ttu-id="1aec8-179">**mofcomp.exe** *msiprip2*</span><span class="sxs-lookup"><span data-stu-id="1aec8-179">**mofcomp** *msiprip2.mof*</span></span>

## <a name="related-topics"></a><span data-ttu-id="1aec8-180">相關主題</span><span class="sxs-lookup"><span data-stu-id="1aec8-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1aec8-181">存取 SNMP 裝置</span><span class="sxs-lookup"><span data-stu-id="1aec8-181">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 
