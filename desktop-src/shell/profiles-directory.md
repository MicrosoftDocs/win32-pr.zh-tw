---
description: 系統會將使用者設定檔資訊儲存在不同 Windows 版本中具有不同名稱的特定目錄中： &\# 0034; 檔和設定&\# 0034; windows XP 和 &\# 0034;使用者&\# 0034; 在 Windows Vista 和更新版本中。
title: 設定檔目錄
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973348"
---
# <a name="profiles-directory"></a>設定檔目錄

系統會將使用者設定檔資訊儲存在不同 Windows 版本的特定目錄中： Windows XP 中的「檔和設定」和 Windows Vista 和更新版本中的「使用者」。 若要取得設定檔目錄的路徑，請使用 [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) 函數。

設定檔目錄包含下列使用者設定檔的子目錄。



| 目錄                                      | 描述                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ProgramData (Windows Vista 或更新版本) /All 使用者 | 適用于所有使用者的程式資訊。 在 Windows Vista 或更新版本中，[所有使用者] 目錄仍然存在，以提供回溯相容性。 |
| 預設                                        | 適用于預設使用者的設定檔資訊。                                                                                      |
| *使用者*                                         | 適用于指定使用者的設定檔資訊。 每個使用者都有自己的設定檔子目錄。                                      |



 

若要取得 ProgramData/All Users 目錄的位置，請呼叫 [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) 函數。 此目錄包含下列子目錄：



| 目錄  | 描述                          |
|------------|--------------------------------------|
| 桌面    | 要顯示在桌面上的快捷方式。 |
| 開始功能表 | [ **開始** ] 功能表的功能表項目。   |



 

若要取得預設使用者目錄的位置，請呼叫 [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) 函數。 若要取得特定使用者目錄的位置，請呼叫 [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) 函數。 預設的使用者和特定的使用者目錄都包含下列子目錄。 斜體的目錄表示預設會隱藏的目錄。 您可以選取 [**資料夾選項**] 控制台專案中的 [**顯示隱藏的檔案、資料夾和磁片磁碟機**] 選項來查看這些目錄。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>目錄</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>應用程式資料</td>
<td>應用程式特定資料。</td>
</tr>
<tr class="even">
<td>Cookie</td>
<td>Windows Internet Explorer cookies。</td>
</tr>
<tr class="odd">
<td>桌面</td>
<td>要顯示在桌面上的快捷方式。</td>
</tr>
<tr class="even">
<td>我的最愛</td>
<td>連結至我的最愛網站。</td>
</tr>
<tr class="odd">
<td>本機設定</td>
<td>未隨設定檔漫遊的應用程式設定和資料。 此目錄中的設定或資料通常是電腦特定的，或太大而無法有效漫遊。 此目錄包含下列子資料夾：
<ul>
<li>應用程式資料</li>
<li>記錄</li>
<li>Temp</li>
<li>Temporary Internet Files</li>
</ul></td>
</tr>
<tr class="even">
<td>我的文件</td>
<td>使用者所建立檔的預設位置。 根據預設，應用程式應該會將檔檔儲存到這個目錄。</td>
</tr>
<tr class="odd">
<td><em>NetHood</em></td>
<td>網路鄰近專案的快捷方式。</td>
</tr>
<tr class="even">
<td><em>PrintHood</em></td>
<td>印表機資料夾專案的快捷方式。</td>
</tr>
<tr class="odd">
<td><em>最近</em></td>
<td>最近使用之檔的快捷方式。</td>
</tr>
<tr class="even">
<td>SendTo</td>
<td>使用者通常傳送檔案之位置的快捷方式。</td>
</tr>
<tr class="odd">
<td>開始功能表</td>
<td>[ <strong>開始</strong> ] 功能表的功能表項目。</td>
</tr>
<tr class="even">
<td><em>範本</em></td>
<td>範本專案的快捷方式。</td>
</tr>
</tbody>
</table>



 

若要取得這些目錄之子目錄的位置，請使用 [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) 或 [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) 函式。

 

 



