---
description: 指定磁片磁碟機的自訂圖示和標籤。
ms.assetid: B6EF7F84-7747-4689-B740-A91CA8E394D7
title: 將自訂圖示和標籤指派給磁碟機號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848c076db443c502a667d67e0b7b49ce51db4ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973188"
---
# <a name="how-to-assign-a-custom-icon-and-label-to-a-drive-letter"></a>如何將自訂圖示和標籤指派給磁碟機號

指定磁片磁碟機的自訂圖示和標籤。

## <a name="instructions"></a>指示

### <a name="step-1-replacing-the-standard-drive-icon-with-a-custom-icon-in-windows-2000"></a>步驟1：以 Windows 2000 中的自訂圖示取代標準磁片磁碟機圖示

若要以 Windows 2000 中的自訂圖示取代標準磁片磁碟機圖示，請將磁碟機號命名的子機碼新增至下列機碼。

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
```

下列範例會指定 E：磁片磁碟機的自訂圖示和標籤。 此圖示位於 C： \\ MyDirMyDrive.exe 檔案中 \\ ，以零為基底的索引為三個。

若為 Windows 2000：

```
HKEY_CLASSES_ROOT
   Applications
      Explorer.exe
         Drives
            E
               DefaultIcon
                  (Default) = C:\MyDir\MyDrive.exe,3
               DefaultLabel
                  (Default) = MyDrive
```

### <a name="step-2-replacing-the-standard-drive-icon-with-a-custom-icon-in-all-other-versions-of-windows"></a>步驟2：以所有其他 Windows 版本的自訂圖示取代標準磁片磁碟機圖示

若要以 Windows 2000 以外的所有 Windows 版本中的自訂圖示取代標準磁片磁碟機圖示，請將磁碟機號命名的子機碼新增至下列機碼。

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
```

下列範例會指定 E：磁片磁碟機的自訂圖示和標籤。 此圖示位於 C： \\ MyDirMyDrive.exe 檔案中 \\ ，以零為基底的索引為三個。

針對所有其他版本的 Windows：

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  DriveIcons
                     E
                        DefaultIcon
                           (Default) = C:\MyDir\MyDrive.exe,3
                        DefaultLabel
                           (Default) = MyDrive
```

### <a name="step-3-calling-the-shupdateimage-event"></a>步驟3：呼叫 SHUpdateImage 事件

在所有版本的 Windows 中，如果您變更檔案類型或磁片磁碟機圖示，您也必須呼叫 SHUpdateImage 來通知 Shell 更新目前顯示的任何圖示。

## <a name="remarks"></a>備註

磁碟機號後面不能加上冒號 (： ) 。 將 **DefaultIcon** 子機碼新增至磁碟機號子機碼，並將其預設值設定為包含圖示位置的字串。 字串的第一個部分包含圖示檔案的完整路徑。 如果檔案中有一個以上的圖示，路徑後面會接著逗號，然後是以零為基底的圖示索引。

 

 



