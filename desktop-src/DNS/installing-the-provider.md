---
title: 安裝提供者
description: 安裝 DNS WMI 提供者的程式，會根據安裝的 Windows 版本而有所不同。
ms.assetid: 5f2bd11a-bc1d-4a43-92d4-26392d2504e7
keywords:
- 網域名稱系統、WMI 提供者、安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9b4b976ccb1a600f56042cb75b500577335059966a82dbb1f9e77b04f7a4df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693038"
---
# <a name="installing-the-provider"></a>安裝提供者

安裝 DNS WMI 提供者的程式，會根據安裝的 Windows 版本而有所不同。 下列程式說明如何在 Windows 2000 上安裝和設定 DNS WMI 提供者。 若要取得 Windows 2000 的 DNS WMI 提供者，請下載下列檔案：

**警告：** DNS WMI 提供者檔案不可互換。 Windows 2000 dns 伺服器需要不同的檔案和與 Windows Server 2003 DNS 伺服器不同的程式。 提供每個的程式。

**在 Windows 2000 伺服器上安裝 DNS WMI 提供者**

1.  從 Windows 2000 伺服器資源套件取得 Windows 2000 的 DNS WMI 提供者，或從下列裝置下載檔案 Dnsprov.zip： ftp://ftp.microsoft.com/reskit/win2000/
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

-   針對 Windows Server 2003 作業系統，系統會自動安裝並註冊 dns WMI 提供者，並在安裝 dns 伺服器服務時，編譯其 MOF 檔案。

 

 




