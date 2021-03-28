---
description: 取得資料夾的識別碼一節討論了兩種取得命名空間物件指標的方法， (PIDL) 的專案識別碼清單。
ms.assetid: c99a2f6c-3144-41ec-ad97-59a30bfec9ab
title: 取得資料夾內容的相關資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7eb26e9df28af4811e74f2878eebb7af9d5c92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991066"
---
# <a name="getting-information-about-the-contents-of-a-folder"></a>取得資料夾內容的相關資訊

[取得資料夾的](folder-id.md)識別碼一節討論了兩種取得命名空間物件指標的方法， (PIDL) 的專案識別碼清單。 其中一個明顯的問題是： PIDL 之後，您可以用它來做什麼？ 相關的問題是：如果兩種方法都可行，或適用于您的應用程式，該怎麼辦？ 這兩個問題的答案都需要進一步瞭解命名空間的執行方式。 索引鍵是 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。

-   [使用 IShellFolder 介面](#using-the-ishellfolder-interface)
-   [列舉資料夾的內容](#enumerating-the-contents-of-a-folder)
-   [判斷顯示名稱和其他屬性](#determining-display-names-and-other-properties)
-   [取得子資料夾 IShellFolder 介面的指標](#getting-a-pointer-to-a-subfolders-ishellfolder-interface)
-   [判斷物件的父資料夾](#determining-an-objects-parent-folder)

## <a name="using-the-ishellfolder-interface"></a>使用 IShellFolder 介面

稍早在本檔中，命名空間資料夾稱為物件。 雖然在該時間點使用的是很好用的詞彙，但其實也是絕對的意義。 每個命名空間資料夾都是由元件物件模型代表 (COM) 物件。 每個資料夾物件都會公開一些介面，這些介面可用於各種不同的工作。 某些選用介面可能無法由所有資料夾公開。 不過，所有資料夾都必須公開 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)的基本介面。

使用資料夾物件的第一個步驟是取得其 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面的指標。 除了提供物件其他介面的存取權之外， **IShellFolder** 也會公開一組方法來處理許多常見的工作，本節會討論其中的幾個。

若要取得命名空間物件之 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面的指標，您必須先呼叫 [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder)。 此函式會傳回命名空間根目錄（即桌面） **IShellFolder** 介面的指標。 當您擁有桌面的 **IShellFolder** 介面之後，有各種不同的方式可繼續進行。

如果您已經有感興趣的資料夾 PIDL （例如，藉由呼叫 [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation)），您可以藉由呼叫桌面的 [**IShellFolder：： BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject)方法來取出其 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)介面。 如果您有檔案系統物件的路徑，您必須先呼叫桌面的 [**IShellFolder：:P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) 方法，然後呼叫 **IShellFolder：： BindToObject**，以取得其 PIDL。 如果這兩種方法都不適用，您可以使用其他 **IShellFolder** 方法來流覽命名空間。 如需詳細資訊，請參閱 [流覽命名空間](navigate.md)。

## <a name="enumerating-the-contents-of-a-folder"></a>列舉資料夾的內容

您通常會想要對資料夾執行的第一件事，就是了解它所包含的內容。 您必須先呼叫資料夾的 [**IShellFolder：： EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) 方法。 此資料夾會建立標準的 OLE 列舉物件，並傳回其 [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) 介面。 此介面會公開四個標準方法（[**Clone**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone)、 [**Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next)、 [**Reset**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset)和 [**Skip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)），可用來列舉資料夾的內容。

列舉資料夾內容的基本程式如下：

1.  呼叫 [**IShellFolder：： EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) 方法資料夾，以取得列舉物件之 [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) 介面的指標。
2.  將未配置的 PIDL 傳遞至 [**IEnumIDList：： Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next)。 **接下來** 會負責配置 PIDL，但應用程式必須在不再需要時將其解除配置。 當 **下一次** 傳回時，PIDL 只會包含物件的專案識別碼和終止的 **Null** 字元。 換句話說，它是相對於資料夾的單一層級 PIDL，而不是完整的 PIDL。
3.  重複步驟2，直到 [**[下一步]**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) 傳回 \_ FALSE，表示所有專案都已列舉。
4.  呼叫 **IEnumIDList：： release** 以釋放列舉物件。

> [!Note]  
> 請務必追蹤您是否正在使用完整或相對 PIDL。 某些函式和方法會接受，但其他函式和方法只會接受其中一種。

 

如果您需要對資料夾進行重複的列舉，則其餘三個 [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) 方法 ([**重設**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset)、 [**略過**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)和 [**複製**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone)) 會很有用。 它們可讓您重設列舉、略過一或多個物件，以及建立列舉物件的複本以保留其狀態。

## <a name="determining-display-names-and-other-properties"></a>判斷顯示名稱和其他屬性

列舉出資料夾所包含的所有 Pidl 之後，您就可以找到它們所代表的物件類型。 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder)介面提供許多有用的方法，這裡有兩個討論。 其他的 **IShellFolder** 方法和其他 Shell 資料夾介面稍後會討論。

其中一個最有用的屬性是物件的顯示名稱。 若要取得物件的顯示名稱，請將其 PIDL 傳遞至 [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)。 雖然物件可以位於命名空間中父資料夾的任何位置，但其 PIDL 必須是資料夾的相對路徑。

[**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 會傳回 [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) 結構一部分的顯示名稱。 由於從 **STRRET** 結構中解壓縮顯示名稱可能有點複雜，因此 Shell 會提供兩個函式來為您 [**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra) 和 [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)作業。 這兩個函式會採用 **STRRET** 結構，並以一般字串的形式傳回顯示名稱。 它們的差異只在於字串的配置方式。

除了其顯示名稱之外，物件可以有數個屬性，例如，它是資料夾或是否可以移動。 您可以藉由將物件的 PIDL 傳遞至 [**IShellFolder：： GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)，來取得物件的屬性。 屬性的完整清單相當大，因此您應該會看到詳細資料的參考。 請注意，您傳遞至 **GetAttributesOf** 的 PIDL 必須是單一層級。 尤其是， **IShellFolder：： GetAttributesOf** 會接受 [**IEnumIDList：： Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next)所傳回的 pidl。 您可以傳入 Pidl 的陣列，而 **GetAttributesOf** 會傳回陣列中的所有物件都有共同的屬性。

如果您有物件的完整路徑或 PIDL， [**SHGetFileInfo**](/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa) 會提供簡單的方法，讓您取得足以滿足許多用途之物件的相關資訊。 **SHGetFileInfo** 採用完整路徑或 PIDL，並傳回物件的各種資訊，包括：

-   物件的顯示名稱
-   物件的屬性
-   物件圖示的控制碼
-   系統映射清單的控制碼
-   包含物件圖示的檔案路徑

## <a name="getting-a-pointer-to-a-subfolders-ishellfolder-interface"></a>取得子資料夾 IShellFolder 介面的指標

您可以藉由呼叫 [**IShellFolder：： GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) ，並檢查是否 \_ 已設定 SFGAO 資料夾旗標，來判斷您的資料夾是否包含任何子資料夾。 如果物件是資料夾，您可以系結至它，它會為您提供其 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面的指標。

若要系結至子資料夾，請呼叫父資料夾的 [**IShellFolder：： BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) 方法。 這個方法會使用子資料夾的 PIDL，並將指標傳回至其 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。 有了這個指標之後，您就可以使用 **IShellFolder** 方法來列舉子資料夾內容、判斷它們的屬性等等。

## <a name="determining-an-objects-parent-folder"></a>判斷物件的父資料夾

如果您有物件的 PIDL，您可能需要其父資料夾所公開的其中一個介面的控制碼。 例如，如果您想要使用 [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)來判斷與 PIDL 相關聯的顯示名稱，就必須先取得物件父系的 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面。 您可以使用前幾節所討論的技術來完成這項作業。 不過，更簡單的方法是使用 Shell 函數 [**SHBindToParent**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent)。 此函式會採用物件的完整 PIDL，並傳回父資料夾上的指定介面指標。 此外，它也會傳回專案的單一層級 PIDL，以便在 [**IShellFolder：： GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)之類的方法中使用。

下列範例主控台應用程式會抓取 System 特殊資料夾的 PIDL，並傳回其顯示名稱。


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>
#include <objbase.h>

int main()
{
    IShellFolder *psfParent = NULL;
    LPITEMIDLIST pidlSystem = NULL;
    LPCITEMIDLIST pidlRelative = NULL;
    STRRET strDispName;
    TCHAR szDisplayName[MAX_PATH];
    HRESULT hr;

    hr = SHGetFolderLocation(NULL, CSIDL_SYSTEM, NULL, NULL, &pidlSystem);

    hr = SHBindToParent(pidlSystem, IID_IShellFolder, (void **) &psfParent, &pidlRelative);

    if(SUCCEEDED(hr))
    {
        hr = psfParent->GetDisplayNameOf(pidlRelative, SHGDN_NORMAL, &strDispName);
        hr = StrRetToBuf(&strDispName, pidlSystem, szDisplayName, sizeof(szDisplayName));
        cout << "SHGDN_NORMAL - " <<szDisplayName << '\n';
    }

    psfParent->Release();
    CoTaskMemFree(pidlSystem);

    return 0;
}
```



應用程式會先使用 [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) 來取出系統資料夾的 PIDL。 然後，它會呼叫 [**SHBindToParent**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent)，它會傳回父資料夾的 [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 介面的指標，以及相對於其父系的系統資料夾 PIDL。 然後，它會使用上層資料夾的 [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) 方法來取出系統資料夾的顯示名稱。 由於 **GetDisplayNameOf** 會傳回 [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) 結構，因此會使用 [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa) 將顯示名稱轉換成一般字串。 顯示名稱之後，會釋放介面指標並釋放系統 PIDL。 請注意，您不能釋放 **SHBindToParent** 所傳回的相對 PIDL。

 

 
