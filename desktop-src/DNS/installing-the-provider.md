---
title: 安裝提供者
description: 安裝 DNS WMI 提供者的程式會根據其安裝所在的 Windows 版本而有所不同。
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- 網域名稱系統、WMI 提供者、安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b1c9dbdaf6d3ad55247d0b978c0a422361a2f04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671964"
---
# <a name="installing-the-provider"></a>安裝提供者

安裝 DNS WMI 提供者的程式會根據其安裝所在的 Windows 版本而有所不同。 下列程式說明如何在 Windows 2000 上安裝和設定 DNS WMI 提供者。 若要取得 Windows 2000 的 DNS WMI 提供者，請下載下列檔案：

**警告：** DNS WMI 提供者檔案不可互換。 Windows 2000 DNS 伺服器需要不同的檔案，以及與 Windows Server 2003 DNS 伺服器不同的程式。 提供每個的程式。

**在 Windows 2000 伺服器上安裝 DNS WMI 提供者**

1.  從 Windows 2000 伺服器資源套件取得適用于 Windows 2000 的 DNS WMI 提供者，或從 ftp://ftp.microsoft.com/reskit/win2000/下載檔案（Dnsprov.zip）。
2.  將 DNS WMI 提供者 (Dnsprov.dll) 和 Dnsschema mof 檔案複製到 <winntdir> \\ system32 \\ wbem 目錄。
3.  編譯 MOF 檔案。 這麼做會自訂符合伺服器的架構。

    **mofcomp.exe dnsschema**

4.  在 DNS 伺服器上註冊 DLL。

    **regsvr32 dnsprov.dll**

5.  接著，可以使用使用 DNS WMI 提供者來管理 DNS 伺服器的腳本或程式。 腳本或程式可以從 DNS 伺服器或從用戶端電腦執行。
    > [!Note]  
    > 執行 DNS WMI 提供者不需要 WMI SDK，但包含許多有用的工具。

     

DNS WMI 提供者必須安裝在要管理的任何 DNS 伺服器上;不過，您可以在 DNS 伺服器或遠端主機上執行 DNS 腳本。

**在 Windows Server 2003 上安裝 DNS WMI 提供者**

-   若為 Windows Server 2003 作業系統，系統會自動安裝並註冊 DNS WMI 提供者，並在安裝 DNS 伺服器服務時，編譯其 MOF 檔案。

 

 




