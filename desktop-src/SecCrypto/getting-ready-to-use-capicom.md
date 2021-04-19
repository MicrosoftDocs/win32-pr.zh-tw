---
description: 使用 CAPICOM 物件的應用程式必須使用 CAPICOM.dll 建立。 CAPICOM.dll 也必須存在，並且在執行時間註冊以使用 CAPICOM 物件。
ms.assetid: 69de5232-e2f9-4aed-935d-5fbcd7998cc9
title: 準備開始使用 CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6fc1ad0dbfe3d4f8c4dae3286eb3ffa5e1ae03d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988930"
---
# <a name="getting-ready-to-use-capicom"></a>準備開始使用 CAPICOM

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 .NET Framework 來執行安全性功能。 如需詳細資訊，請參閱 [使用 CAPICOM 的替代方案](alternatives-to-using-capicom.md)。\]

使用 CAPICOM 物件的應用程式必須使用 CAPICOM.dll 建立。 CAPICOM.dll 也必須存在，並且在執行時間註冊以使用 CAPICOM 物件。 CAPICOM.dll 應新增至 Visual Basic 專案參考，才能使用 CAPICOM 物件。

您可以從可從 [PLATFORM SDK](https://www.microsoft.com/download/details.aspx?id=25281)可轉散發套件下載的可轉散發檔案取得 capicom： capicom。 如需有關 CAPICOM 版本的詳細資訊，請參閱 [Capicom 版本](capicom-versions.md)。

**註冊 CAPICOM.dll**

-   在命令提示字元中，將目錄變更為儲存 CAPICOM.dll 的目錄，然後輸入下列命令：

    **regsvr32 CAPICOM.dll**

## <a name="example-code-limitations"></a>範例程式碼限制

為了提供更簡潔、更容易閱讀的程式碼，在這些範例中，不一定會遵循良好程式設計實務的原則。 特別是，只會顯示有限的錯誤回應。 使用中的應用程式應該一律檢查傳回的錯誤碼，並在發生錯誤時執行適當的動作。

## <a name="necessary-key-containers-keys-and-certificates-in-capicom"></a>在 CAPICOM 中所需的金鑰容器、金鑰和憑證

雖然任何使用者都可以在任何電腦上執行具有 CAPICOM 物件的某些作業，但使用 CAPICOM 物件建立 [*數位簽章*](../secgloss/d-gly.md) 以及抓取封包訊息的純文字內容是以憑證為基礎的作業。 建立數位簽章的使用者，以及抓取封包訊息之加密內容的使用者，都必須具有具有可用相關私密金鑰的數位憑證。 如果沒有具有相關私密金鑰的憑證，密碼編譯作業將會失敗。 當應用程式正在執行時，CAPICOM 應用程式的使用者必須確保它們具有適當的憑證和可用的私密金鑰。

下列各節中的一些範例會執行需要可用 [*公開/私密金鑰*](../secgloss/p-gly.md) 組的作業，以加密和解密檔案、訊息和簽章。 其中許多程式會在執行時間進行編譯和執行，但不會有適當的 [*金鑰容器*](../secgloss/k-gly.md)、金鑰、憑證存放區和 [*憑證*](../secgloss/c-gly.md) 存在於這些存放區中。

**建立自我簽署憑證**

1.  安裝簽署工具。 這些會安裝為 Microsoft Windows 軟體開發套件 (SDK) 、平臺軟體發展工具組 (SDK) 或 .NET Framework SDK 的一部分。
2.  下載 Makecert.exe 之後，請在命令提示字元中執行下列命令、將使用者名稱 *取代為使用者* 名稱、 *OrganizationName* 的組織名稱，以及用於公司 *名稱的公司名稱：*

    **makecert-r-n "cn =**_UserName_*_，ou =_*_OrganizationName_*_，o =_*_公司名稱_*_"-ss my_*

3.  您可以將憑證放在目前使用者的 [我的存放區] 中。 將建立的憑證匯入至根存放區，使其成為受信任的憑證。

 

 
