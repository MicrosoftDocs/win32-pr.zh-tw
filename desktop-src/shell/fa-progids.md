---
description: Shell 會使用程式設計識別碼 (ProgID) 登錄子機碼，以將檔案類型與應用程式產生關聯，以及控制關聯的行為。
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: 程式設計識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67720fed1ad4b8401d11f6532cdc79836911e7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991078"
---
# <a name="programmatic-identifiers"></a>程式設計識別碼

Shell 會使用程式設計識別碼 (ProgID) 登錄子機碼，以將檔案類型與應用程式產生關聯，以及控制關聯的行為。 用於檔案關聯的 ProgID 專案位於登錄的 **HKEY \_ 類別 \_ 根目錄** 下。

本主題的組織方式如下：

-   [檔案關聯所使用的程式設計識別碼元素](#programmatic-identifier-elements-used-by-file-associations)
-   [使用已建立版本的程式設計識別碼](#using-versioned-programmatic-identifiers)
-   [相關主題](#related-topics)

如需詳細資訊，請參閱 [如何註冊新應用程式的檔案類型](how-to-register-a-file-type-for-a-new-application.md)

## <a name="programmatic-identifier-elements-used-by-file-associations"></a>檔案關聯所使用的程式設計識別碼元素

ProgID 金鑰名稱的正確格式為「 \[ *廠商」或「應用程式*」 \] 。 \[*元件* \] 。 \[*版本* \] ，以句號分隔，而且沒有空格，如 Word.Doc>ument 6。 *版本* 部分是選擇性的，但強烈建議使用。 如需詳細資訊，請參閱使用已建立版本的程式 [設計識別碼](#using-versioned-programmatic-identifiers)。

ProgID 子機碼應包含下列元素。 請注意，此機碼中的某些字串資料需要特定的格式。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>元素</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong> (預設) </strong></td>
<td>將 ProgID 子機碼的預設專案設定為該 ProgID 的易記名稱，適合顯示給使用者。 在執行 Windows 2000 或更新版本的系統上，FriendlyTypeName 專案會取代使用此專案來保存易記名稱。 不過，您應該將此值設定為回溯相容性。<br/></td>
</tr>
<tr class="even">
<td><strong>AllowSilentDefaultTakeOver</strong> (Windows 8) 引進</td>
<td>設定此選用專案，以指出當您決定公用檔案類型的預設處理常式時，Windows 應忽略此 ProgID。 不論是否已設定此值，ProgID 都會繼續出現在 OpenWith 快捷方式功能表和對話方塊中。 這是 REG_NONE 的值。</td>
</tr>
<tr class="odd">
<td> (在 Windows 7) 引進的<strong>AppUserModelID</strong></td>
<td>將此選擇性專案設定為應用程式的明確應用程式使用者模型識別碼 (AppUserModelID) 如果應用程式使用明確的 AppUserModelID，並使用系統自動產生的 <strong>最新</strong> 或 <strong>經常</strong> 跳躍的快捷方式清單，或提供自訂捷徑清單。 如果應用程式使用明確的 AppUserModelID 但未設定此值，則專案不會出現在該應用程式的快捷方式清單中。 這是 REG_SZ 字串。 如需詳細資訊，請參閱 <a href="appids.md">應用程式使用者模型識別碼 (AppUserModelIDs) </a>。<br/></td>
</tr>
<tr class="even">
<td><strong>EditFlags</strong></td>
<td>使用 <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> 列舉中的旗標設定此選擇性專案。 EditFlags 專案會控制 Shell 處理連結至此 ProgID 之檔案類型的某些層面。 您也可以使用 EditFlags 專案，限制使用者可以使用檔案的屬性工作表來修改這些檔案類型的特定部分。 用於 EditFlags 的 <strong>FILETYPEATTRIBUTEFLAGS</strong> 值是二進位值，可讓您將多個屬性結合成位 or 運算中的單一值。 這是 REG_DWORD 或 REG_BINARY 值。<br/></td>
</tr>
<tr class="odd">
<td><strong>FriendlyTypeName</strong></td>
<td>將此專案設定為 ProgID 的易記名稱，適合顯示給使用者。 為求一致，此字串應該包含與此 ProgID 索引鍵的預設專案相同的資料。 這個專案可以是 REG_SZ 或 REG_EXPAND_SZ 字串，但必須格式化為間接字串 (完整的檔案名和資源值，並在前面加上 @ 符號) ，例如 <em>@% SystemRoot% \shell32.dll，-154</em>。<br/></td>
</tr>
<tr class="even">
<td><strong>InfoTip</strong></td>
<td>將此專案設定為命令介面顯示此 ProgID 的簡短說明訊息。 [提示] 專案會顯示在滑鼠停留對話方塊中。 這個值可以是 REG_SZ 或 REG_EXPAND_SZ 字串，但就像 FriendlyTypeName 一樣，它必須格式化為間接字串。<br/></td>
</tr>
<tr class="odd">
<td><strong>CurVer</strong></td>
<td>將此子機碼 (預設) 專案設定為此 ProgID 的最新版本。<br/>
<blockquote>
[!Note]<br />
除非您有並存的應用程式版本，也就是在相同的系統上安裝多個版本，所以您應該避免使用 <strong>CurVer</strong>。
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>DefaultIcon</strong>。</td>
<td>將此子機碼的 (預設) 專案設定為您想要針對與此 ProgID 相關聯的檔案類型顯示的預設圖示。 此值可以是 REG_SZ 或 REG_EXPAND_SZ 字串，但必須以完整檔案名的形式提供，其具有其附隨的資源值，例如 <em>% SystemRoot% \shell32.dll，-154</em>。<br/></td>
</tr>
</tbody>
</table>



 

下列登錄機碼範例說明檔案關聯 ProgID 索引鍵節點：

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a>使用已建立版本的程式設計識別碼

版本設定的 ProgID 是在其名稱中表示版本的 ProgID。 您通常會將句點和版本號碼加入至名稱來完成這項作業。 例如：

-   Word.Doc>ument 6
-   Word.Doc>ument 8

這些是版本設定的 Progid，分別為6和8版。 如果您有並存的應用程式，也就是同時安裝了支援多個應用程式版本的應用程式，則請使用 CurVer 與獨立版本的 Progid。 否則，應該避免 CurVer 和版本獨立 Progid，因為它們會導致效率不好。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[如何註冊新應用程式的檔案類型](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[應用程式註冊](app-registration.md)
</dt> <dt>

[檔案類型](fa-file-types.md)
</dt> <dt>

[檔案關聯的運作方式](fa-how-work.md)
</dt> <dt>

[依檔案類型或種類的內容視圖](prophand-content-view.md)
</dt> <dt>

[檔案類型驗證器](file-type-verifier.md)
</dt> <dt>

[檔案類型處理常式](fa-file-extensions.md)
</dt> <dt>

[認知類型](fa-perceivedtypes.md)
</dt> <dt>

[關聯陣列](fa-associationarray.md)
</dt> </dl>

 

 




