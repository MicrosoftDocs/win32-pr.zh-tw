---
title: 使用 COM 物件編寫腳本
description: 使用 COM 物件編寫腳本
ms.assetid: d99a561b-67dc-4fc9-adfa-cd7350eb16ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2b00380a14db2d254675a5826b61f262e8cfe8
ms.sourcegitcommit: 8c981a2f4149b4a9d605ffb71fefda8d82bc696e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/24/2019
ms.locfileid: "103677976"
---
# <a name="scripting-with-com-objects"></a>使用 COM 物件編寫腳本

*指令碼語言* 是一種程式設計語言，可在執行時間由 *腳本引擎* 進行剖析，這是將以該語言撰寫的腳本轉譯成機器碼的元件。 每個腳本引擎都會翻譯特定的指令碼語言。 *腳本主* 控制項是一種應用程式，例如網頁瀏覽器，它會裝載腳本引擎來執行腳本。 如果您的腳本主機支援 COM，您可以撰寫使用 COM 物件的腳本。 下列主題描述支援 COM 物件的腳本主機、通用指令碼語言，以及如何在指令碼語言之間轉譯。

指令碼語言與編譯的語言不同之處在于，它會在執行時間轉譯成機器碼。 這表示當您每次執行腳本時，腳本引擎會先剖析程式碼，然後執行它。 相反地，在編譯期間，編譯的語言（例如 c + +）會轉譯成機器碼一次。 當您執行已編譯的應用程式時，作業系統只會執行先行編譯的程式碼。

由於腳本引擎必須在每次執行腳本時重新剖析腳本，因此指令碼語言的速度通常會比先行編譯的對應專案更慢且更有效率。 不過，腳本的優點是容易撰寫和維護。 指令碼語言通常比先行編譯語言更簡單，而且當腳本變更時，就不需要重新編譯。 針對輕量且快速變更的應用程式（例如網頁），指令碼語言很理想。

您可以使用數個主機環境來撰寫使用 COM 物件的腳本，如下所述：

-   [在網頁中內嵌 COM 物件](embedding-com-objects-in-web-pages.md)
-   [使用 Active Server Pages 中的 COM 物件](using-com-objects-in-active-server-pages.md)
-   [在 Windows Script Host 中使用 COM 物件](using-com-objects-in-windows-script-host.md)
-   [在自訂應用程式中編寫 COM 物件的腳本](scripting-com-objects-in-custom-applications.md)

在前面提到的每個主機環境中，腳本引擎會剖析並執行腳本。 因為每個指令碼語言的引擎都是個別的元件，所以您可以藉由加入新的引擎，將新的指令碼語言新增至環境。

最常使用的指令碼語言為：

-   Microsoft Visual Basic Scripting Edition (VBScript) ，Visual Basic 的子集。
-   JavaScript 是 Netscape 指令碼語言，先前稱為 LiveScript。
-   Microsoft JScript 開發軟體，這是 Microsoft 在 ECMA 262 語言規格中的實作為。

Microsoft 提供適用于 JScript 和 VBScript 的腳本引擎。 其他軟體公司則提供 ActiveX 腳本引擎，適用于 PerlScript、PScript、Python 等語言。

如需詳細資訊，請參閱 [ECMA 262 語言規格](https://www.ecma-international.org/publications/standards/Ecma-262.htm)。

請注意，大部分的指令碼語言（如 VBScript 和 JScript）無法存取或修改檔案。 這無法防止腳本變更用戶端電腦上的資料。 不過，COM 物件沒有這類限制。 在用戶端電腦上下載並安裝這些電腦之後，就可以執行任何標準的應用程式動作。 因此，使用者只能從受信任的來源下載並執行 ActiveX 控制項。

如需在指令碼語言之間轉換的詳細資訊，請參閱下列主題：

-   [翻譯為 VBScript](translating-to-vbscript.md)
-   [翻譯為 JScript](translating-to-jscript.md)
-   [翻譯為 JavaScript](translating-to-javascript.md)

 

 




