---
description: INF 檔案的 [安裝] 區段會定義安裝程式的步驟。
ms.assetid: 24d40dc6-ac09-4cf8-9229-f81da2925576
title: INF 安裝區段範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39c8162dbf06b87faf8a1ce432c361a28befca0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975804"
---
# <a name="inf-install-section-example"></a>INF 安裝區段範例

INF 檔案的 [ **安裝** ] 區段會定義安裝程式的步驟。 **安裝** 區段的每一行都有兩個部分。 在等號 (=) 的左邊是索引鍵。 右側是一個或多個區段標題的清單。 索引鍵會指定右側所列的區段類型。 如需本節格式的說明，請參閱 Microsoft Windows 2000 驅動程式開發工具組的「INF 檔案區段和指示詞」。

以下是 **安裝** 區段的範例。

``` syntax
[MyInstallSection]
Copyfiles=DataFiles, ProgramFiles
Delfiles=OldFiles
UpdateInis=NewIniInfo
AddReg=NewRegistryInfo, MoreNewRegistryInfo
DelReg=OldRegistryInfo, MoreOldRegistryInfo
```

在此範例中， **CopyFiles** 索引鍵會設定為 "資料檔案" 和 "ProgramFiles" 值。 這會指定 INF 檔案中的兩個 [ **複製** 檔案] 區段，其中包含複製作業所使用的原始程式檔名稱。 複製之檔案的目的地會在 INF 檔案的 **DestinationDirs** 區段中指定。

**Delfiles** 索引鍵的值為 "OldFiles"。 這會指定 [ **刪除** 檔案] 區段，其中包含與檔案刪除作業相關的資訊。

**UpdateInis** 索引鍵會指定 **更新 ini** 檔案區段，其中包含有關在 INI 檔案中更新專案的資訊。

**AddReg** 和 **DelReg** 金鑰指定 [**新增** 登錄] 和 [**刪除** 登錄] 區段，其中包含新增或刪除登錄資訊的相關資訊。

 

 



