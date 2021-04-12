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
# <a name="setting-up-the-wmi-snmp-environment"></a>設定 WMI SNMP 環境

使用 WMI SNMP 介面與網路裝置通訊，需要設定裝置、SNMP 和 WMI 服務。 本主題中的資訊說明如何設定 WMI SNMP 環境。

本主題將討論下列各節：

## <a name="installing-the-snmp-provider"></a>安裝 SNMP 提供者

SNMP 服務預設不會啟用。 您可以透過主控台啟用 SNMP 服務和 WMI SNMP 提供者。 請注意，必須啟用並執行 SNMP 服務，WMI SNMP 提供者才能運作。

從 Windows Vista 開始，請使用下列程式來安裝 SNMP 提供者。

**安裝 SNMP 提供者**

1.  從 **主控台** 選取 [ **程式**]。
2.  在 [ **程式和功能**] 下，選取 [ **開啟或關閉 Windows 功能**]。
3.  在 [Windows 功能] 清單中，向下滾動至 **SNMP 功能** 並展開清單，讓您可以看到 **WMI SNMP 提供者**。
4.  選取 [ **WMI SNMP 提供者**] 的核取方塊。 系統會自動選取 [ **snmp] 功能** 的核取方塊，因為提供者需要 SNMP。
5.  按一下 [確定]  。
6.  從命令提示字元或 [ **開始** ] 功能表，執行 services.msc，並確認 SNMP 服務已啟動。

## <a name="creating-an-snmp-namespace"></a>建立 SNMP 命名空間

SNMP 命名空間會定義網路裝置的觀點。

> [!Note]  
> 如需有關在特定作業系統上支援和安裝此元件的詳細資訊，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。

 

下列程式說明如何建立 SNMP WMI [*命名空間*](gloss-n.md)。

**建立 SNMP 命名空間**

1.  藉由編譯 [*受控物件格式*](gloss-m.md)的 mof 檔案或使用 [適用于 WMI 的 COM API](com-api-for-wmi.md)，建立 [**\_ \_ 命名空間**](--namespace.md)系統類別的實例。

    如需詳細資訊，請參閱 [在 WMI 中建立](creating-hierarchies-within-wmi.md)階層。

2.  將 SNMP 提供者 [*限定詞*](gloss-q.md) 與命名空間定義產生關聯。

    SNMP 提供者限定詞包含執行特定的內容資訊和傳輸屬性，可定義 SNMP 提供者存取 SNMP 裝置的方式。 如需詳細資訊，請參閱 [**SNMP 提供者專用的限定詞**](qualifiers-specific-to-the-snmp-provider.md)。

3.  使用 [mofcomp.exe](mofcomp.md) 命令列工具，將 MOF 程式碼載入至 WMI 存放庫。

    如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。

下列 MOF 程式碼範例 \\ 會使用可與 snmp 命名空間相關聯的限定詞子集來定義 snmp 命名空間。

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

## <a name="inserting-snmp-mib-data-into-wmi"></a>將 SNMP MIB 資料插入 WMI

作為提供者，SNMP 提供者可做為 SNMP 資料與 WMI 類別之間的橋樑。 因此，您的 WMI 中必須有類別，代表啟用 SNMP 的裝置的不同層面。 若要這樣做，您必須使用 SNMP 資訊模組編譯器 ([smi2smir](smi2smir.md)) ，將 snmp 管理資訊從 snmp 格式編譯成相等的 CIM 架構定義。 然後，您可以將資訊編譯器的輸出導向至稱為「SNMP 模組資訊存放庫 (SMIR) 」的 SNMP 架構資料庫，或指向數種不同的 MOF 檔案。

編譯器會以命令列模式執行，並使用一個 MIB 檔案作為輸入。 下列命令會將指定的 MIB 檔案載入 SMIR 中。

**smi2smir/a***<MIB file>*

## <a name="setting-up-snmp-communities"></a>設定 SNMP 團體

作為安全性措施，預設不會建立 SNMP 「公用」群組。 您可以建立如「 [社區登錄設定](/previous-versions/windows/embedded/ms907028(v=msdn.10))」中所述的「社區」。 如果您沒有任何社區，請建立「公用」群體來存取 SNMP 提供者。

## <a name="generating-mof-files-from-mib-files"></a>從 MIB 檔案產生 MOF 檔案

下列命令是一個範例，說明如何從安裝 SNMP 提供者時所安裝的 MIB 檔案產生 MOF 檔案。

**cd** *% windir% \\ system32 \\ wbem \\ SNMP*

**Smi2smir/g** *... \\ . \\hostmib mib* **>** *hostmib mof*

**Smi2smir/g** *... \\ . \\ipforwd mib* **>** *ipforwd mof*

**Smi2smir/g** *... \\ . \\nipx mib* **>** *nipx mof*

**Smi2smir/g** *... \\ . \\mib \_ ii. mib* **>** *mib （ \_ mof* ）

**Smi2smir/g** *... \\ . \\lmmib2 mib* **>** *lmmib2 mof*

**Smi2smir/g** *... \\ . \\mcastmib mib* **>** *mcastmib mof*

**Smi2smir/g** *... \\ . \\rfc2571 mib* **>** *rfc2571 mof*

**Smi2smir/g** *... \\ . \\wfospf mib* **>** *wfospf mof*

**Smi2smir/g** *... \\ . \\dhcp \\ ... \\ 。msft. mib* **>** *dhcp*

**Smi2smir/g** *... \\ . \\wins .... \\ \\msft.* **>**  。

**Smi2smir/g** *... \\ . \\mipx .... \\ \\msft. mib* **>** *mipx. mof*

**Smi2smir/g** *... \\ . \\mripsap .... \\ \\msft. mib* **>** *mripsap. mof*

**Smi2smir/g** *... \\ . \\msipbtp .... \\ \\msft. mib* **>** *msipbtp. mof*

**Smi2smir/g** *... \\ . \\msiprip2 .... \\ \\msft. mib* **>** *msiprip2. mof*

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a>將 SNMP MOF 檔案新增至 WMI 儲存機制

下列命令是一個範例，說明如何將從 MIB 檔案產生的 MOF 檔案新增至 WMI 存放庫。 如果您想要將 MOF 檔案新增至 [*WMI 儲存*](gloss-w.md) 機制復原中要自動還原的檔案清單，請在每個命令的結尾新增 **-自動** 復原旗標。 如需 WMI Mofcomp.exe 命令列工具的詳細資訊，請參閱 [**mofcomp.exe**](mofcomp.md)。

**mofcomp.exe** *hostmib*

**mofcomp.exe** *ipforwd*

**mofcomp.exe** *nipx*

**mofcomp.exe** *mib \_ ii. mof*

**mofcomp.exe** *lmmib2*

**mofcomp.exe** *mcastmib*

**mofcomp.exe** *rfc2571*

**mofcomp.exe** *wfospf*

**mofcomp.exe** *dhcp mof*

**mofcomp.exe** *mipx*

**mofcomp.exe** *mripsap*

**mofcomp.exe** *msipbtp*

**mofcomp.exe** *msiprip2*

## <a name="related-topics"></a>相關主題

<dl> <dt>

[存取 SNMP 裝置](accessing-snmp-devices.md)
</dt> </dl>

 

 
