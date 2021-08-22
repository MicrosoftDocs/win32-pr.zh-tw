---
description: 將 Win32 元件設為 Microsoft Windows Installer 套件的元件，以安裝或更新您的應用程式。
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Win32 元件的安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c680d53e1c4702bab3b9a24920b18a2fdb644a86c41207712ec3726a310a8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633838"
---
# <a name="installation-of-win32-assemblies"></a>Win32 元件的安裝

將 Win32 元件設為 Microsoft Windows Installer 套件的元件，以安裝或更新您的應用程式。 當您撰寫 [MsiAssembly 資料表](msiassembly-table.md) 和 [MsiAssemblyName 資料表](msiassemblyname-table.md)時，這會將元件資料行中的元件識別 \_ 為元件。 安裝程式會將 [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) 屬性設定為可支援 Win32 元件的作業系統上 Sxs.dll 的檔案版本，否則不會設定此屬性。

在 Windows Vista 和 Windows XP 中，Windows Installer 不會將元件資訊寫入登錄中。 此外，也可以使用共用元件、私用元件和並存元件。 如需詳細資訊，請參閱 [共用元件](shared-assemblies.md)、 [私用元件](private-assemblies.md)和 [並存元件](side-by-side-assemblies.md)。

下列章節說明如何撰寫 Windows Installer 套件，以在不同的 Windows 作業系統上，將 Win32 元件安裝為共用、私用或並存。

-   [在 Windows XP 上安裝適用于並存共用的 Win32 元件](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [在 Windows XP 上安裝 Win32 元件以私用應用程式](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



