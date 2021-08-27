---
title: 受 WOW64 影響的登錄機碼
description: 在 WOW64 下，會重新導向特定的登錄機碼。
ms.assetid: 7b3f4f11-24bc-44f7-837e-d61d853c7291
keywords:
- 登錄機碼64位 Windows 程式設計
- WOW64 64 位 Windows 程式設計，登錄機碼
- 重新導向的登錄機碼64位 Windows 程式設計
- 反映登錄機碼64位 Windows 程式設計
- 共用登錄機碼64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5193d4aa64848d132aca446c6d1e4a50777614725b69cae637da65aebfe94c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071608"
---
# <a name="registry-keys-affected-by-windows-installations-that-include-windows-on-windows-wow-support-for-multiple-processor-architectures"></a>受 Windows 安裝影響的登錄機碼，其中 Windows 包含 Windows (WOW) 支援多處理器架構

在64位 Windows 從 Windows XP 和 Windows Server 2003 開始的安裝，以及在32位 ARM 處理器 Windows 架構中，從 Windows RT (Windows 8)  (Windows) 的安裝將會重新 *導向***特定的** 登錄機碼。

在受影響的 Windows 安裝中，當處理器架構與作業系統的處理器架構不同時 (將其稱為 **WOW 應用程式**) 對重新導向的金鑰進行登錄呼叫，登錄重新導向器會攔截呼叫，並將其對應至金鑰的對應實體登錄位置。 例如， \[  \] 在 **AMD64** /Intel x86-x64 Windows 安裝上執行的32位 Intel IA-32 x86 應用程式會受到重新導向的登錄機碼影響; 當此 x86 應用程式呼叫重新導向的按鍵時，登錄重新導向程式會攔截應用程式的呼叫，並將其重新導向至金鑰的對應實體登錄位置。 如需詳細資訊，請參閱登錄 [重定向](registry-redirector.md)程式。

其他的登錄機碼是在受影響的 Windows 安裝上，由不同處理器架構的應用程式所 *共用*。 對共用金鑰的 WOW 應用程式登錄呼叫不會重新導向。 相反地，會將金鑰的一個實體複本對應到登錄的每個邏輯視圖。

**Windows server 2008、Windows Vista Windows server 2003 和 Windows XP：** 此外也會 *反映* 重新導向的登錄機碼子集，以保持登錄的32位和64位之間的索引鍵和值的同步。 從 Windows 7 和 Windows Server 2008 R2 開始，已移除登錄反映。 如需詳細資訊，請參閱登錄 [反映](registry-reflection.md)。

本主題列出重新導向、共用或重新導向的登錄機碼，並反映在 WOW 之下。 它也會列出可為現有應用程式提供相容性的符號連結，而這些應用程式可能會使用包含 **Wow6432Node** 的硬式編碼登錄機碼路徑、在 Windows AMD64 上執行之 x86 進程的重新導向登錄位置 如需詳細資訊，請參閱下列：

- [在 WOW 下重新導向、共用和反映的索引鍵](#redirected-shared-and-reflected-keys-under-wow)
- [Windows on Windows 64 (WOW64) 符號連結](#windows-on-windows-64-wow64-symbolic-links)

## <a name="redirected-shared-and-reflected-keys-under-wow"></a>在 WOW 下重新導向、共用和反映的索引鍵

針對受影響的 Windows 安裝上的 WOW 應用程式，下表列出重新導向、共用或重新導向並反映的登錄機碼。 除非另有指定，否則此資料表中的索引鍵子機碼會繼承父索引鍵的行為。 如果索引鍵沒有列在此資料表中，則會共用金鑰。

| 答案 | WindowsServer 2008 R2、Windows 7 和更新版本 | Windowsserver 2008、Windows Vista、Windows server 2003 和 Windows XP |
|-|-|-|
| **HKEY \_ 本機 \_ 電腦** | 共用 | 共用 |
| **HKEY \_ 本機 \_ MACHINE\SOFTWARE** | 已重新導向 | 已重新導向 |
| **HKEY \_本機 \_ MACHINE\SOFTWARE** \\ **類別** | 共用 | 重新導向並反映 |
| **HKEY \_本機 \_ MACHINE\SOFTWARE** \\ **類別** \\ **Appid** | 共用 | 重新導向並反映一個例外狀況：如果 [DllSurrogate](../com/dllsurrogate.md) 和 [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) 登錄值為空字串，則不會反映這些值。 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **類別** \\ **CLSID** | 已重新導向 | 重新導向，而且只會反映未指定 InprocServer32 或 InprocHandler32 的 Clsid。 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **類別** \\ **DirectShow** | 已重新導向 | 重新導向並反映 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **類別** \\ **HCP** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **類別** \\ **介面** | 已重新導向 | 重新導向並反映 |
| **HKEY \_本機 \_ MACHINE\SOFTWARE** \\ **類別** \\ **媒體類型** | 已重新導向 | 重新導向並反映 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **類別** \\ **MediaFoundation** | 已重新導向 | 重新導向並反映 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **用戶端** | 共用 | 已重新導向 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **COM3** | 共用 | 重新導向並反映 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **密碼** 編譯 \\ **Calais** \\ **目前** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **密碼** 編譯 \\ **Calais** \\ **讀取** 程式 | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **密碼** 編譯 \\ **服務** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **CTF** \\ **SystemShared** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **CTF** \\ **秘訣** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **DFS** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **驅動程式簽署** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **EnterpriseCertificates** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **EventSystem** | 共用 | 重新導向並反映 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **MSMQ** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **非驅動程式簽署** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **記事本** \\ **DefaultFonts** | 共用 | 已重新導向 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **OLE** | 共用 | 重新導向並反映 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **RAS** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **RPC** | 共用 | 重新導向並反映 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **microsoft** \\ **軟體** \\ **microsoft** \\ **共用工具** \\ **MSInfo** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **SystemCertificates** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **TermServLicensing** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **TransactionServer** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **應用程式路徑** | 共用 | 已重新導向 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **主控台** 資料 \\ **指標** \\ **架構** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **AutoplayHandlers** | 共用 | 已重新導向 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **DriveIcons** | 共用 | 已重新導向 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **KindMap** | 共用 | 已重新導向 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **群組原則** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **原則** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **PreviewHandlers** | 共用 | 已重新導向 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **安裝程式** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **電話語音** \\ **位置** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **主控台**| 共用 | 已重新導向 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontDpi** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontLink** | 共用 | 已重新導向 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontMapper** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ 字型 | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontSubstitutes** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Gre \_ Initialize** | 共用 | 已重新導向 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **影像檔執行選項** | 共用 | 已重新導向 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **語言套件** | 共用 | 已重新導向 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **NetworkCards** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Perflib** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **埠** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **列印** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProfileList** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** 的 \\ **時區** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** | 共用 | 共用 |
| **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **RegisteredApplications** | 共用 | 分享 **Windows Server 2003 和 Windows XP：** 這是 Windows Vista 中新增的金鑰。 |
| **HKEY \_ 目前的 \_ 使用者** | 共用 | 共用 |
| **HKEY \_目前的 \_ 使用者** \\ **軟體** | 共用 | 共用 |
| **HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **類別** | 共用 | 重新導向並反映 |
| **HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **類別** \\ **Appid** | 共用 | 重新導向並反映一個例外狀況：如果 [DllSurrogate](../com/dllsurrogate.md) 和 [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) 登錄值為空字串，則不會反映這些值。 |
| **HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **類別** \\ **CLSID** | 已重新導向 | 重新導向並反映 |
| **HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **類別** \\ **DirectShow** | 已重新導向 | 重新導向並反映 |
| **HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **類別** \\ **介面** | 已重新導向 | 重新導向並反映 |
| **HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **類別** \\ **媒體類型** | 已重新導向 | 重新導向並反映 |
| **HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **類別** \\ **MediaFoundation** | 已重新導向 | 重新導向並反映 |

**HKEY \_[目前 \_ 使用者**] 是 **HKEY \_ 使用者** sid \\ **\[ \]** 的符號連結，其中 \[ sid 表示與 \] 目前使用者的安全識別碼相符 (sid) 。 **HKEY \_使用者** \\ **\[ sid \]** \\ **軟體** \\ **類別** 是 **HKEY \_ 使用者** \\ **\[ sid \] \_ 類別** 的符號連結。

**HKEY \_類別 \_ 根目錄** 是 **HKEY \_ 本機 \_ 電腦** \\ **軟體** \\ **類別** 和 **HKEY \_ 目前 \_ 使用者** \\ **軟體** \\ **類別** 的合併觀點。 這些登錄路徑中重新導向的金鑰也會有效地重新導向至 **HKEY \_ 類別 \_ ROOT** 。 這也適用于在支援它們的系統上反映的索引鍵。

## <a name="windows-on-windows-64-wow64-symbolic-links"></a>Windows on Windows 64 (WOW64) 符號連結

WOW64 只會定義下列符號連結，以便與可能使用硬式編碼登錄機碼路徑（包含 Wow6432Node）的現有應用程式相容。 新的應用程式應該避免在登錄機碼路徑中使用 Wow6432Node。

- **HKEY \_本機 \_ 電腦 \\ 軟體 \\ Wow6432Node \\ 類別** 已連結至 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ Wow6432Node**
- **HKEY \_本機 \_ 電腦 \\ 軟體 \\ 類別 \\ Wow6432Node \\ appid** 已連結至 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ AppId**
- **HKEY \_本機 \_ 電腦 \\ 軟體 \\ 類別 \\ Wow6432Node \\ 通訊協定** 已連結至 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ 通訊協定**
- **HKEY \_本機 \_ 電腦 \\ 軟體 \\ 類別 \\ Wow6432Node \\ typelib** 已連結至 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ Typelib**

**Windows server 2008、Windows Vista、Windows Server 2003 和 Windows XP： HKEY \_本機 \_ 電腦 \\ 軟體 \\ Wow6432Node \\ 類別** 會連結至 **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ Wow6432Node**。 其他符號連結已新增至 Windows 7 和 Windows Server 2008 R2。
