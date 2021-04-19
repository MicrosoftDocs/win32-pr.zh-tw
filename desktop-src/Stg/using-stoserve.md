---
title: 使用 StoServe
description: StoServe 是主要用於 COM 伺服器的 DLL。
ms.assetid: 32cb284a-de78-4953-9d8e-5bb87d6d5a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d46dfd4070e9951223e0a498184b8db814c7a43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969922"
---
# <a name="using-stoserve"></a>使用 StoServe

**StoServe** 是主要用於 COM 伺服器的 DLL。 雖然可以透過連結到其相關聯的方式隱含載入。LIB 檔案，通常是在明確的 LoadLibrary 呼叫之後使用，通常是從 COM 函數 [**CoGetClassObject**](/windows/win32/api/combaseapi/nf-combaseapi-cogetclassobject)內。 **StoServe** 是自我註冊的同進程伺服器。

若要使用 **StoServe**，用戶端程式不需要包含 StoServe。H 或 STOSERVE 的連結。自由。 **StoServe** 的 COM 用戶端只會透過其物件的 CLSID 和 COM 服務取得存取權。 若為 **StoServe**，該 clsid 是 \_ 在 [檔案 PAPGUIDS] 中定義的 clsid DllPaper (。H 在 \\ inc. 的) 。 [StoClien](structured-storage-client-sample--stoclien-.md)程式碼範例會顯示用戶端如何取得此存取權。

建立此範例的 makefile 會自動在登錄中註冊伺服器。 您可以在 **StoServe** 目錄中的命令提示字元發出下列命令，以手動起始自我註冊：

**nmake** **註冊**

這會假設您已設定編譯環境。 如果不是，您也可以在 **StoServe** 目錄中的命令提示字元，直接叫用 REGISTER.EXE 命令。

**..\\註冊 \\register.exe** **stoserve.dll**

這些註冊命令需要在此系列中有先前的註冊範例組建，以及先前的 STOSERVE.DLL 組建。

在此系列中，makefile 使用來自註冊範例的 REGISTER.EXE 公用程式。 最新版本的平臺軟體發展工具組 (SDK) 和 Visual C++ 包含公用程式 REGSVR32.EXE，可使用類似于註冊同進程伺服器和封送處理 Dll 的方式來使用。

**StoServe** 會使用 APPUTIL 所提供的許多公用程式類別和服務。 如需更多有關 APPUTIL 的詳細資訊，請研究 APPUTIL 程式庫在同輩 APPUTIL 目錄中的原始程式碼，並 APPUTIL.HTM 在主要教學課程目錄中。

 

 