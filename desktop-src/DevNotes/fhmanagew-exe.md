---
description: FhManagew.exe 程式會從目前指派的檔案歷程記錄目標裝置刪除超過指定年齡的檔案版本。
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2570da9b2b874b723b28917028fab3c58ecdf772
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481514"
---
# <a name="fhmanagewexe"></a>FhManagew.exe

FhManagew.exe 程式會從目前指派的檔案歷程記錄目標裝置刪除超過指定年齡的檔案版本。

此程式可在 Windows 8 和 Windows Server 2012 和更新版本中使用。

若要執行此程式，請移至 [ **開始** ] 功能表，按一下 [ **執行**]，然後輸入下列命令。

**FhManagew.exe-清理***存留期*




| 參數 | Description | 
|-----------|-------------|
| <span id="age"></span><span id="AGE"></span><em>年齡</em><br /> | 此參數會指定可刪除之檔案版本的最小存留期（以天為單位）。 如果下列兩個條件都成立，則會刪除檔案版本：<br /><ul><li>檔案版本比指定的存留期還舊。</li><li>檔案已不再包含于保護範圍內，或目標裝置上有較新版本的相同檔案。</li></ul>如果 <em>age</em> 參數設定為零，則會刪除所有檔案版本，但目前存在於保護範圍內的每個檔案的最新版本除外。<br /> | 




 

若要隱藏此程式的所有輸出，請使用 **-quiet** 命令列選項，如下所示。

**FhManagew.exe-清理***存留期* **-安靜**

## <a name="examples"></a>範例



| 範例                                                                                                                                                                                                      | 描述                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe-清除30**<br/>                                 | 刪除所有早于一個月的檔案版本。<br/>                        |
| <span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe-清除 365-quiet**<br/> | 刪除早于一年的所有檔案版本，並隱藏所有輸出。<br/> |



 

 

 




