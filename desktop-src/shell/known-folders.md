---
description: WindowsVista 引進了新的儲存案例和新的使用者設定檔命名空間。
title: 已知的資料夾
ms.topic: article
ms.date: 05/31/2018
ms.assetid: d0c25eef-53ac-4dad-805a-b9ba4cd86be9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3b5fbdaf0086f88fc4eed42ce47749a99ab07b40
ms.sourcegitcommit: 8bfe4f468ee5de7bbe096e5db81e427db53d977c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/26/2021
ms.locfileid: "114680311"
---
# <a name="known-folders"></a>已知的資料夾

WindowsVista 引進了新的儲存案例和新的使用者設定檔命名空間。 為了解決這些新的因素，已取代以 [**CSIDL**](csidl.md) 值參照標準資料夾的較舊系統。 從 Windows Vista 中，這些資料夾是由一組稱為已知資料夾識別碼的新 GUID 值所參考。

已知的資料夾系統提供下列優點：

-   獨立軟體廠商 (Isv) 可以自行擴充已知的資料夾識別碼集。 他們可以定義資料夾、提供其識別碼，並向系統註冊。 無法擴充 CSIDL 值。
-   系統上所有已知的資料夾都可以列舉。 沒有任何 API 提供這種 CSIDL 值的功能。 如需詳細資訊，請參閱 [**IKnownFolderManager：： GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids) 。
-   ISV 新增的已知資料夾可以新增自訂屬性，讓它解釋其用途和預定用途。
-   許多已知的資料夾都可以重新導向至新的位置，包括網路位置。 在 CSIDL 系統下，只能重新導向 **我的檔** 資料夾。
-   已知的資料夾可以有自訂處理常式，可在建立或刪除期間使用。

使用 CSIDL 值的 CSIDL 系統和 Api 仍支援相容性。 但是，不建議在任何新的開發中使用它們。


下列主題討論已知資料夾系統的詳細資訊。

-   [使用應用程式中的已知資料夾](working-with-known-folders.md)
-   [如何使用自訂資料夾擴充已知資料夾](how-to-extend-known-folders-with-custom-folders.md)
-   [**KNOWNFOLDERID**](knownfolderid.md)

下列參考頁面說明 Win32 已知資料夾函式，可用來取出已知資料夾的位置，或將其重新導向至新的位置。 這些函式會取代較舊的 Win32 函數。 系統會提供新的函式，將對等的行為提供給舊的函式，但元件物件模型也會複製每個新函數， (COM) API。



| New 函式                                             | 取代                                           | COM 對等專案                                            |
|----------------------------------------------------------|----------------------------------------------------|-----------------------------------------------------------|
| [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)     | [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)         | [**IKnownFolder：： GetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getpath)     |
| [**SHGetKnownFolderIDList**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist) | [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) | [**IKnownFolder::GetIDList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getidlist) |
| [**SHSetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetknownfolderpath)     | [**SHSetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shsetfolderpatha)         | [**IKnownFolder::SetPath**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfolder-setpath)     |



 

下列參考頁面說明 COM 已知的資料夾 Api，其提供上列 Win32 Api 的所有功能，並新增列舉所有已知資料夾的功能、存取已知的資料夾屬性，以及延伸標準的已知資料夾集。

-   [**IKnownFolder**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder)
-   [**IKnownFolderManager**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfoldermanager)

示範已知資料夾 api 的 c + + 範例包含在 Windows 軟體開發套件 (SDK) 中。 當您在電腦上安裝 Windows SDK 之後，就可以在% ProgramFiles% \\ Microsoft sdk \\ Windows \\ v 6.0 \\ 範例 \\ WinUI \\ Shell \\ AppPlatform \\ KnownFolders 中找到此範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[已知資料夾範例](/windows/win32/shell/samples-knownfolders)
</dt> </dl>
