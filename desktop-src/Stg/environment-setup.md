---
title: 環境設定
description: 已安裝的平臺軟體發展工具組 (SDK) 提供的 Setenv.bat 檔案位於 Platform SDK 的根目錄，您可以執行此檔案來設定您的環境，以建立使用 Platform SDK 的應用程式。
ms.assetid: 2dec3d7a-acac-4ff7-9d4a-d3540e6d441d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f752872b96e4b02cbfd1724d8a4a99ca1de13f0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969650"
---
# <a name="environment-setup"></a>環境設定

已安裝的平臺軟體發展工具組 (SDK) 提供的 Setenv.bat 檔案位於 Platform SDK 的根目錄，您可以執行此檔案來設定您的環境，以建立使用 Platform SDK 的應用程式。

## <a name="settings-and-variables"></a>設定和變數

您也可以手動設定您的環境，方法是在您的 Autoexec.bat 檔案中新增如下所示的內容。 您可以使用 Windows 來編輯 Autoexec.bat 檔案，以包含這些命令。 您可以使用 Windows Server 2003、Windows XP、Windows 2000 或 Windows NT，使用您可以從主控台執行的 [系統] 對話方塊來編輯這些設定，或將這些設定新增至環境變數。


```cmd
  SET INCLUDE=D:\MSSDK\INCLUDE;C:\MSDEV\INCLUDE;C:\MSDEV\ATL\INCLUDE
  SET LIB=D:\MSSDK\LIB;C:\MSDEV\LIB
  SET MSSDK=D:\MSSDK
  SET MSTOOLS=D:\MSSDK
  SET CPU=i386
  SET PATH=C:\WIN95;C:\WIN95\COMMAND;C:\DOS;D:\MSSDK\BIN;C:\MSDEV\BIN
```



這些設定適用于執行 Windows Me、Windows 98 或 Windows 95 且同時安裝 Microsoft Visual C++ 和 Platform SDK 的 Intel 80386 或更新版本平臺。 例如，在此系統上，Visual C++ 版本5.0 會安裝在 C： \\ MSDEV 目錄下。 Platform SDK 會安裝在 D： \\ MSSDK 目錄下。 您的磁片設定可能會不同。 此範例的 Platform SDK 目錄 (，其中的 D： \\ MSSDK) 在每個路徑順序中都是稍早的。 此順序假設命令列編譯是要在命令提示字元視窗中執行，而且 Platform SDK 中的 .h 包含和 .lib 程式庫檔案是這些編譯的慣用。

CPU 環境變數的定義是為了控制 Win32 組建，視平臺而定。 目前可能的值包括 i386、MIPS、ALPHA 和 PPC。 如需詳細資訊，請參閱 \\ MSSDK INCLUDE 目錄的 PLATFORM SDK 中提供的 Win32 檔案 \\ 。 所有的 COM 教學課程程式碼範例 makefile 都包含 Win32. mak。

 

 




