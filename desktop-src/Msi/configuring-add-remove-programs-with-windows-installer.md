---
description: 您可以在應用程式的 Windows Installer 套件中設定特定安裝程式屬性的值，以提供在主控台中設定 [新增/移除程式] 所需的所有資訊。
ms.assetid: 2eb00fe5-e441-4fce-9623-81a089269a2b
title: 使用 Windows Installer 設定新增/移除程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d48ad8499d395ffc4a5aad5491883f9c3161b78a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465485"
---
# <a name="configuring-addremove-programs-with-windows-installer"></a>使用 Windows Installer 設定新增/移除程式

您可以在應用程式的 Windows Installer 套件中設定特定安裝程式屬性的值，以提供在主控台中設定 [新增/移除程式] 所需的所有資訊。 設定這些屬性會自動將對應的值寫入登錄中。 如果安裝程式偵測到產品已標示為完整移除，則會自動將作業新增至腳本，以移除產品主控台資訊中的 [新增/移除程式] 資料夾。

如果未註冊應用程式，則不會在主控台的 [新增/移除程式] 中列出。 如需詳細資訊，請參閱 [新增和移除應用程式，並在登錄中保留沒有追蹤](adding-and-removing-an-application-and-leaving-no-trace-in-the-registry.md)。

已安裝在每個使用者 [安裝內容](installation-context.md) 中的應用程式會顯示在目前使用者的 [新增/移除程式] 中。 安裝在每部電腦安裝內容中的應用程式會顯示在所有使用者的 [新增/移除程式] 中。 如果應用程式未安裝在每部電腦上，而且僅針對目前使用者以外的使用者安裝為每個使用者的應用程式，則不會出現在目前使用者的 [新增/移除程式] 中。

請注意，使用 [**LIMITUI**](limitui.md) 屬性的安裝套件也必須包含 [**ARPNOMODIFY**](arpnomodify.md)。 若要在嘗試設定產品時，讓使用者從主控台公用程式中的 [新增/移除程式] 取得正確的行為，這是必要的。

安裝程式會使用下列 [公用屬性](public-properties.md) 來管理主控台中的 [新增/移除程式]。


| 屬性名稱 | 屬性的簡短描述 | 
|---------------|-------------------------------|
| <a href="arpauthorizedcdfprefix.md"><strong>ARPAUTHORIZEDCDFPREFIX</strong></a> | 應用程式更新通道的 URL。 安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。 | 
| <a href="arpcomments.md"><strong>ARPCOMMENTS</strong></a> | 提供主控台中的 [新增/移除程式] 的批註。 安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。 | 
| <a href="arpcontact.md"><strong>ARPCONTACT</strong></a> | 提供主控台中的 [新增/移除程式] 的連絡人。 安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。 | 
| <a href="arpinstalllocation.md"><strong>ARPINSTALLLOCATION</strong></a> | 應用程式主要資料夾的完整路徑。 安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。 | 
| <a href="arphelplink.md"><strong>ARPHELPLINK</strong></a> | 技術支援的網際網路位址或 URL。 安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。 | 
| <a href="arphelptelephone.md"><strong>ARPHELPTELEPHONE</strong></a> | 技術支援電話號碼。 安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。 | 
| <a href="arpnomodify.md"><strong>ARPNOMODIFY</strong></a> | 防止在主控台的 [新增/移除程式] 中顯示產品的變更按鈕。<blockquote><b>注意：</b> 這只會影響 ARP 中的顯示。 Windows Installer 仍可以透過命令列或程式設計介面來修復、安裝隨選和卸載應用程式。</blockquote><br /> | 
| <a href="arpnoremove.md"><strong>ARPNOREMOVE</strong></a> | 防止在主控台的 [新增/移除程式] 中顯示產品的 [移除] 按鈕。 如果已使用可提供產品移除選項的使用者介面來撰寫安裝套件，仍然可以藉由選取 [變更] 按鈕來移除產品。<blockquote><b>注意：</b> 這只會影響 ARP 中的顯示。 Windows Installer 仍可以透過命令列或程式設計介面來修復、安裝隨選和卸載應用程式。</blockquote><br /> | 
| <a href="arpnorepair.md"><strong>ARPNOREPAIR</strong></a> | 在主控台中停用 [新增/移除程式] 中的 [修復] 按鈕。<blockquote><b>注意：</b> 這只會影響 ARP 中的顯示。 Windows Installer 仍可以透過命令列或程式設計介面來修復、安裝隨選和卸載應用程式。</blockquote><br /> | 
| <a href="arpproducticon.md"><strong>ARPPRODUCTICON</strong></a> | 識別 [新增/移除程式] 中顯示的圖示。 如果未定義此屬性，[新增/移除程式] 會指定顯示圖示。 | 
| <a href="arpreadme.md"><strong>ARPREADME</strong></a> | 提供主控台中的 [新增/移除程式] 的讀我檔案。 安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。 | 
| <a href="arpsize.md"><strong>ARPSIZE</strong></a> | 應用程式的估計大小（以 KB 為單位）。 | 
| <a href="arpsystemcomponent.md"><strong>ARPSYSTEMCOMPONENT</strong></a> | 防止在主控台的 [新增/移除程式] 的 [程式] 清單中顯示應用程式。<blockquote><b>注意：</b> 這只會影響 ARP 中的顯示。 Windows Installer 仍可以透過命令列或程式設計介面來修復、安裝隨選和卸載應用程式。</blockquote><br /> | 
| <a href="arpurlinfoabout.md"><strong>ARPURLINFOABOUT</strong></a> | 應用程式首頁的 URL。 安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。 | 
| <a href="arpurlupdateinfo.md"><strong>ARPURLUPDATEINFO</strong></a> | 應用程式更新資訊的 URL。 安裝程式在卸載登錄機 <a href="uninstall-registry-key.md">碼</a>下寫入的值。 | 


> [!Note]  
> 如需 [設定程式] 和 [預設值] 工具的相關資訊，請參閱 [使用設定程式存取和電腦預設值](/previous-versions//bb776877(v=vs.85))一節。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[卸載登錄機碼](uninstall-registry-key.md)
</dt> </dl>
