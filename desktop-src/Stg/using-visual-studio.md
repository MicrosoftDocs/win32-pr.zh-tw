---
title: 使用 Visual Studio
description: 為了方便起見，Microsoft Visual Studio 6.0 會提供每個範例的專案檔。
ms.assetid: 8da6affd-a881-4dc4-a2e6-d35f655c69fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee6edc1b19cb0e56495c8af6f96d28e4d255e40d53161671f52a1a7d27939f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796848"
---
# <a name="using-visual-studio"></a>使用 Visual Studio

為了方便起見，Microsoft Visual Studio 6.0 會提供每個範例的專案檔。 此檔案具有 DSP 延伸模組。 主要目錄中也提供 Allsamp dsw 工作區檔案，讓您可以從 Visual Studio 內一次編譯所有範例。

> [!Note]  
> 下列指示是針對 Microsoft Visual Studio 6.0 所撰寫。 在舊版和更新版本的 Visual Studio 中，這些命令可能會有所不同。

 

若要為範例載入適當的專案，您可以在範例目錄的命令提示字元中執行 Visual Studio，如下列範例所示。 您必須以的範例專案名稱取代 **<project name>** 。

**msdev <project name> dsp**

您也可以直接按兩下 Windows 檔案總管中的 dsp 檔案，將範例的工作區載入 Visual Studio。 在 Visual Studio 中，您接著可以流覽範例來源的 c + + 類別，並一般執行其他編輯-編譯-debug 作業。

作為平臺軟體發展工具組的一部分 (SDK) ，在 Visual Studio 中編譯這些範例需要 Visual Studio 中正確設定目錄路徑。 若要設定目錄路徑，請執行下列步驟：

-   執行 Microsoft Visual Studio (Visual C++) 。
-   選擇 [**工具**] 功能表上的 [**選項**]。
-   選擇 [**選項**] 對話方塊中的 [**目錄**] 索引標籤。
-   在 [ **顯示目錄** ] 下拉式清單中，選取 [ **可執行檔** ]，並輸入已安裝平臺 SDK 的 BIN 目錄路徑 (例如 C： \\ Program files \\ Microsoft SDK \\ BIN) 。 按一下向上箭號按鈕，將這個新輸入的路徑移到 [ **目錄** ] 清單中的第一個專案。
-   在 [ **顯示目錄** ] 下拉式清單中，選取 [ **包含** 檔案]，然後輸入已安裝之平臺 SDK 的包含目錄路徑 (例如，C： \\ Program files \\ Microsoft SDK \\ 包含) 。 按一下向上箭號按鈕，將這個新輸入的路徑移到 [ **目錄** ] 清單中的第一個專案。
-   在 [ **顯示目錄** ] 下拉式清單中，選取 [連結 **庫** 檔案]，然後輸入已安裝平臺 SDK 的 LIB 目錄路徑 (例如，C： \\ Program files \\ Microsoft SDK \\ LIB) 。 按一下向上箭號按鈕，將這個新輸入的路徑移到 [ **目錄** ] 清單中的第一個專案。
-   按一下 [ **選項** ] 對話方塊中的 [確定] 按鈕，以完成設定。

從該處，您可以使用編輯器、偵錯工具和專案功能來編輯、編譯、連結和偵錯工具。

如果有程式碼範例的現有原始程式檔，其他 visual Ide 也可以輕鬆地產生其中一個原生專案 makefile。 如果您使用這類的 IDE，產生這類原生專案 makefile 可能很值得，因為它提供了流覽程式 c + + 類別的方法。 如需使用外部 makefile 或使用一組現有原始程式檔建立原生專案 makefile 的詳細資訊，請參閱您的 IDE 檔。

除了相依于同輩 APPUTIL、INC. 和 LIB 目錄中的通用程式碼，許多程式碼範例都是獨立的。 建立任何其他程式碼範例之前的組建 APPUTIL。 序列中稍後的一些範例可能會使用先前範例的已編譯結果。 下列程式碼範例相互相關性如下所示：

-   任何：任何程式碼範例的組建都需要先前的 APPUTIL 組建。
-   DLLUSER：組建或執行需要先前的 DLLSKEL 組建。
-   COMUSER：組建或執行需要先前的 COMOBJ 組建。
-   DLLSERVE：組建需要註冊之前的組建。
-   DLLCLIEN： Run 需要 DLLSERVE 先前的組建。
-   LICSERVE：組建需要註冊之前的組建。
-   LICCLIEN： Run 必須有 LICSERVE 和 DLLSERVE 之前的組建。
-   封送處理：組建需要預先註冊的組建。
-   LOCSERVE：組建或執行需要先前的註冊和封送處理組建。
-   LOCCLIEN： Run 需要 LOCSERVE 先前的組建。
-   APTSERVE：組建或執行需要先前的註冊和封送處理組建。
-   APTCLIEN： Run 需要 APTSERVE 先前的組建。
-   REMCLIEN：組建或執行需要在本機 (用戶端) 電腦上註冊和封送處理之前的組建。 在遠端 (server) 的電腦上執行註冊、封送和 APTSERVE 之前的版本需要執行。
-   FRESERVE：組建需要註冊之前的組建。
-   FRECLIEN： Run 需要 FRESERVE 先前的組建。
-   節省：組建需要預先註冊的組建。
-   CONCLIEN：執行之前需要節省的版本。
-   STOSERVE：組建需要註冊之前的組建。
-   STOCLIEN： Run 需要 STOSERVE 先前的組建。
-   保留：組建需要註冊之前的組建。
-   PERTEXT：組建需要註冊之前的組建。
-   PERDRAW：組建需要註冊之前的組建。
-   PERCLIEN： Run 必須有保留、PERTEXT 和 PERDRAW 之前的組建。
-   DCDMARSH：組建需要註冊之前的組建。
-   DCDSERVE：組建或執行需要先前的 REGISTER 和 DCDMARSH 組建。
-   DCOMDRAW：組建或執行需要在本機 (用戶端) 電腦上進行登錄和 DCDMARSH 先前的組建。 執行需要在遠端 (server) 電腦上註冊、DCDMARSH 和 DCOMDRAW 之前的版本。

 

 




