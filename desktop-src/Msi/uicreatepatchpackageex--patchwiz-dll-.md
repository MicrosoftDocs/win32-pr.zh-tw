---
description: UiCreatePatchPackageEx 函式會將套件建立檔案)  ( pcp 檔案，並產生 Windows Installer 修補套件 ( .msp 套件) 。 呼叫 Msimsp.exe 是使用 Patchwiz.dll 的建議方法。
ms.assetid: 76d9a21d-73bc-41fc-8ed0-7d7d7deff815
title: 'UiCreatePatchPackageEx (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e9c610aa6b03990eb4bb9fb34ce84568c9164a88ff2455b9c649436b3d327c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039397"
---
# <a name="uicreatepatchpackageex-patchwizdll"></a>UiCreatePatchPackageEx (Patchwiz.dll) 

UiCreatePatchPackageEx 函式會將套件建立檔案)  ( pcp 檔案，並產生 Windows Installer 修補套件 ( .msp 套件) 。 呼叫 [Msimsp.exe](msimsp-exe.md) 是使用 [Patchwiz.dll](patchwiz-dll.md)的建議方法。

從 Patchwiz.dll 4.0 版開始可使用 UiCreatePatchPackageEx 函式，並擴充 [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) 函式的功能。

``` syntax
UINT UiCreatePatchPackageEx(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  BOOL fRemoveTempFolderContents,
  DWORD dwFlags,
  DWORD dwReserved    
);
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="szPcpPath"></span><span id="szpcppath"></span><span id="SZPCPPATH"></span>*szPcpPath*
</dt> <dd>

修補程式建立內容檔案的完整路徑 ( pcp 檔案) 。

</dd> <dt>

<span id="szPatchPath"></span><span id="szpatchpath"></span><span id="SZPATCHPATH"></span>*szPatchPath*
</dt> <dd>

要建立之 Windows Installer 修補套件 ( .msp 檔) 的完整路徑。 這個參數可以是 **Null** 或空字串，但可能不會省略。 如果它是 **Null** 或空字串，則函數會在 Properties 資料表中使用 PatchOutputPath 的值 [ (Patchwiz.dll)](properties-table-patchwiz-dll-.md)。

</dd> <dt>

<span id="szLogPath"></span><span id="szlogpath"></span><span id="SZLOGPATH"></span>*szLogPath*
</dt> <dd>

將附加之文字記錄檔的完整路徑。 這個參數可以是 **Null** 或空字串，但可能不會省略。

</dd> <dt>

<span id="hwndStatus"></span><span id="hwndstatus"></span><span id="HWNDSTATUS"></span>*hwndStatus*
</dt> <dd>

顯示狀態文字之視窗的控制碼。 這個參數可以是 **Null** 或空字串，但可能不會省略。

</dd> <dt>

<span id="szTempFolder"></span><span id="sztempfolder"></span><span id="SZTEMPFOLDER"></span>*szTempFolder*
</dt> <dd>

暫存檔案的位置。 這個參數可以是 **Null** 或空字串，但可能不會省略。 使用者必須有足夠的許可權，才能讀取和寫入此資料夾。 預設位置為% TMP% \\ ~ pcw \_ tmp \\ .。

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*
</dt> <dd>

若 **為 TRUE**，則移除暫存資料夾及其所有內容（如果有的話）。 如果 **為 FALSE** 且資料夾存在，則函數會失敗。

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

這個參數可以設定為下列值的其中一個或組合，以指定記錄或使用者介面選項。



| 旗標            | 值       | 意義                                  |
|-----------------|-------------|------------------------------------------|
| LOGNONE         | 0x00000000  | 不將任何訊息寫入記錄檔。            |
| LOGINFO         | 0x00000001  | 將參考用訊息寫入記錄檔。 |
| LOGWARN         | 0x00000002  | 將警告寫入至記錄檔。               |
| LOGERR          | 0x00000004  | 將錯誤訊息寫入至記錄檔。         |
| LOGPERFMESSAGES | 0x00000008  | 將效能訊息寫入至記錄檔。   |
| UINONE          | 0x00000000f | 不顯示使用者介面。       |
| UIALL           | 0x00000010  | 顯示使用者介面。              |



 

</dd> <dt>

<span id="dwReserved"></span><span id="dwreserved"></span><span id="DWRESERVED"></span>*>dwreserved*
</dt> <dd>

保留的。 此參數必須設定為零。

</dd> </dl>

## <a name="return-values"></a>傳回值

請參閱 UiCreatePatchPackage 傳回 [值](return-values-for-uicreatepatchpackage.md)中的資料表。

## <a name="remarks"></a>備註

如需撰寫 pcp 檔案，以及使用[UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md)來產生 Windows Installer 修補程式套件的範例，請參閱一節[小型更新修補範例](a-small-update-patching-example.md)。

建立修補程式需要未壓縮的安裝映射，例如從 CD-ROM 的系統管理映射或未壓縮的安裝映射。 [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) 不會為封包中的檔案產生二進位修補程式。

 

 



