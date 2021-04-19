---
title: 如何建立範例
description: 若要建立 COM 範例，必須設定電腦環境以建立 Microsoft Win32 c + + 應用程式。
ms.assetid: c62b8b4d-a9d2-4587-8bb6-7b2c30d1c00d
keywords:
- 如何建立範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593d3465d3ebcc32a6768dd8b2dffe1f0a653d07
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "106967881"
---
# <a name="how-to-build-samples"></a>如何建立範例

若要建立 COM 範例，必須設定電腦環境以建立 Microsoft Win32 c + + 應用程式。

## <a name="preparing-a-computer-to-create-com-samples"></a>準備電腦以建立 COM 範例

電腦環境必須設定正確安裝的32位 c + + 編譯器、連結器和資源編譯器，與 Microsoft Visual C++ 4.x 或更新版本，以及正確安裝的 Windows SDK 相容。 最好是最後安裝 Windows SDK。 Windows SDK 針對範例中編碼的 COM 功能，提供需要的 .h 包含和 .lib 程式庫檔案。

若要成功執行 Remclien、Freserve 和 Freclien 範例，需要可在 Windows 作業系統中使用的系統裝置： Windows Server 2003、Windows XP、Windows 2000 或 Windows NT 4.0。 Remclien、Freserve 和 Freclien 範例將會建立，但不會在 Windows Me、Windows 98 或 Windows 95 作業系統上執行，除非分散式 COM (DCOM) 和無限制執行緒 COM 是作業系統的一部分。 這項支援適用于 DCOM95.EXE add on 中的 Windows Me、Windows 98 和 Windows 95 作業系統。 您可以 [從 Microsoft 下載](https://www.microsoft.com/download/details.aspx?id=31661)dcom95.exe 來取得。

每個範例目錄都有必要的原始程式檔，可建立並執行範例。 父範例目錄具有 Makeall.bat 檔案，您可以從命令提示字元執行此檔案，以將所有的程式碼範例都設為下列分支中的所有程式碼範例。 如需詳細資訊，請參閱 Makeall.bat 檔案。 如果您的環境已設定為建立 Win32 c + + 應用程式，您可以直接從它所在的目錄執行 Makeall.bat，以建立下一個分支中的所有程式碼範例。 Makeall 可確保組建的正確順序，以滿足所有的程式碼範例相依性。

主要目錄也有 makefile，可使用類似 Makeall.bat 所支援的選項來建立所有教學課程程式碼範例。 如需詳細資訊，請參閱這個 makefile。 這個 makefile 假設整個程式碼範例分支會安裝為 Windows SDK 的一部分。 此位置目前的路徑類似 *d： \\ MSSDK \\ 範例 \\ COM \\ TUTSAMP*，其中 d：代表安裝磁片磁碟機。 如果您已將教學課程程式碼範例分支解壓縮 (例如，COM 目錄 COM 及其子目錄) 至 Windows SDK (以外的其他位置，或您從 Microsoft 網站) 取得範例集合作為個別下載，則請使用 Makeall.bat 來編譯分支中的所有範例。 一般情況下，建議使用 Makeall.bat。 也會提供 Logmall.bat 檔案。 它會與 Makeall 批次檔相同，不同之處在于它會將所有編譯輸出記錄至主要教學課程目錄中的檔案 Errorlog.txt。

主要目錄中也提供兩個批次檔 Regall.bat 和 Unregall.bat，可在教學課程程式碼範例系列中註冊及取消註冊所有的 COM 伺服器。 若要註冊所有伺服器，請從主要目錄執行 Regall.bat 檔案。 若要取消註冊所有伺服器，請以相同的方式執行 Unregall.bat。 這些批次檔需要註冊、封送、DLLSERVE、LICSERVE、LOCSERVE、APTSERVE、FRESERVE 的先前組建，以及節省程式碼範例。 如果您執行一般的程式碼範例組建，伺服器 makefile 將會自動註冊伺服器。 在此情況下，不需要執行 Regall 批次檔。

執行 Cleanall.bat 批次檔，以執行所有 COM 教學課程範例的完整 Cleanall。

> [!WARNING]
> 此批次檔會刪除範例中 Visual C++ 所建立的所有 Visual Studio 專案檔和其他暫存工作檔案。 教學課程程式碼範例中內建的所有 COM 伺服器都會從登錄中取消註冊。 所有可執行檔 exe 和 .dll 檔案都會刪除。 所有的 debug 符號檔都會刪除。 也會刪除各種組建環境中產生的檔案。

 

執行 ' Makeall Clean ' 以執行更快且更適度的程式碼範例清除。 這項清除作業不會嘗試像 Cleanall.bat 所執行的完整。 .Obj 檔案會遭到刪除，但會保留輸出二進位檔。 COM 伺服器不會從登錄中取消註冊。

此範例系列是 Windows SDK 的不可或缺部分產生，因此教學課程的敘述會假設已正確安裝 Windows SDK 的環境。

不過，版本4.0 和更新版本的 Microsoft Visual C++ 也可以提供編譯所需的 .h 和 .lib 程式庫檔案。 在這種情況下，可能不需要安裝 Windows SDK 來編譯範例。

如需詳細資訊及完整的範例組建詳細資料，請參閱：

[環境設定](environment-setup.md)

[生成](makefiles.md)

[使用 Visual Studio](using-visual-studio.md)

[解壓縮程式代碼範例](extracting-the-code-samples.md)

[編碼樣式慣例](coding-style-conventions.md)

 

 




