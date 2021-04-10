---
description: UiCreatePatchPackage 函式會將套件建立檔案)  ( pcp 檔案，並產生 Windows Installer 修補套件 ( .msp 套件) 。
ms.assetid: 77fedb80-b664-417d-879b-846e74cc4c23
title: 'UiCreatePatchPackage (Patchwiz.dll) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bcda07d74ffc32c76809037d9ac90cf11ea25c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847682"
---
# <a name="uicreatepatchpackage-patchwizdll"></a>UiCreatePatchPackage (Patchwiz.dll) 

UiCreatePatchPackage 函式會將套件建立檔案)  ( pcp 檔案，並產生 Windows Installer 修補套件 ( .msp 套件) 。 呼叫 [Msimsp.exe](msimsp-exe.md) 是使用 [Patchwiz.dll](patchwiz-dll.md)的建議方法。 [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md)函式可在4.0 版的 Patchwiz.dll 中取得，並擴充 UiCreatePatchPackage 函式的功能。

``` syntax
UINT UiCreatePatchPackage(
  LPCTSTR szPcpPath,              
  LPCTSTR szPatchPath,            
  LPCTSTR szLogPath,             
  HWND hwndStatus,                
  LPCTSTR szTempFolder,           
  Bool fRemoveTempFolderContents  
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

暫存檔案的位置。 這個參數可以是 **Null** 或空字串，但可能不會省略。 預設位置為% TMP% \\ ~ pcw \_ tmp \\ .。

</dd> <dt>

<span id="fRemoveTempFolderContents"></span><span id="fremovetempfoldercontents"></span><span id="FREMOVETEMPFOLDERCONTENTS"></span>*fRemoveTempFolderContents*
</dt> <dd>

若 **為 TRUE**，則移除暫存資料夾及其所有內容（如果有的話）。 如果 **為 FALSE** 且資料夾存在，則函數會失敗。

</dd> </dl>

## <a name="return-values"></a>傳回值

請參閱 UiCreatePatchPackage 傳回 [值](return-values-for-uicreatepatchpackage.md)中的資料表。

## <a name="remarks"></a>備註

如需撰寫 pcp 檔案，以及使用 UiCreatePatchPackage 來產生 Windows Installer 修補程式套件的範例，請參閱一節 [小型更新修補範例](a-small-update-patching-example.md)。

建立修補程式需要未壓縮的安裝映射，例如從 CD-ROM 的系統管理映射或未壓縮的安裝映射。 UiCreatePatchPackage 不會為封包中的檔案產生二進位修補程式。

 

 



