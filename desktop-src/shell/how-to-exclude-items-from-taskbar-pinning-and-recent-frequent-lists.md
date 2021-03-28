---
description: 應用程式、處理常式和 windows 可以選擇使其無法釘選到工作列，或包含在 [開始] 功能表最常使用的 (MFU) 清單中。
title: 如何從工作列釘選和最近/頻繁清單中排除專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7f32ad641832703804f94b8cc28f47ea9cabb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973153"
---
# <a name="how-to-exclude-items-from-taskbar-pinning-and-recentfrequent-lists"></a>如何從工作列釘選和最近/頻繁清單中排除專案

應用程式、處理常式和 windows 可以選擇讓自己無法釘選到工作列，也可以包含在 [ **開始** ] 功能表最常使用的 (MFU) 清單中。

## <a name="instructions"></a>指示


有三種機制可以完成從工作列釘選和最近/頻繁清單中排除專案的機制：

-   將 NoStartPage 專案新增至應用程式的註冊，如下列範例所示：

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    與 NoStartPage 專案相關聯的資料會被忽略。 只需要存在專案。 因此，NoStartPage 的理想型別為 **REG \_ NONE**。

    請注意，任何使用明確應用程式使用者模型識別碼 (AppUserModelID) 都會覆寫 NoStartPage 專案。 如果已將明確的 AppUserModelID 套用至快捷方式、程式或視窗，它就會變成可釘選，而且符合 [ **開始** ] 功能表的 最常使用清單的資格。

-   在 windows 和快捷方式上設定 [AppUserModel PreventPinning](../properties/props-system-appusermodel-preventpinning.md) 屬性。 在設定 [PKEY \_ AppUserModel \_ ID](../properties/props-system-appusermodel-id.md) 屬性之前，必須先在視窗上設定這個屬性。
-   將明確的 AppUserModelID 新增為下列登錄子機碼底下的值，如下列範例所示：

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    每個專案都是具有 AppUserModelID 名稱的 **REG \_ Null** 值。 在此清單中找到的任何 AppUserModelID 都不會可釘選，也不適合包含在 [ **開始** ] 功能表的 最常使用清單中。

## <a name="remarks"></a>備註

請注意，某些可執行檔，以及包含其名稱中特定字串的快捷方式，會自動排除在 最常使用清單中的固定和包含。

> [!Note]  
> 您可以套用明確的 AppUserModelID 來覆寫此自動排除。

 

如果下列任何一個字串（不論大小寫）都包含在快捷方式名稱中，則不會可釘選程式，也不會顯示在最常使用的清單中 (不適用於 Windows 10) ：

-   文件
-   Help
-   安裝
-   其他資訊
-   自述
-   先閱讀
-   讀我檔案
-   移除
-   設定
-   支援
-   新功能

下列程式清單不是可釘選，而且會從最常使用的清單中排除：

-   Applaunch.exe
-   Control.exe
-   Dfsvc.exe
-   Dllhost.exe
-   Guestmodemsg.exe
-   Hh.exe
-   Install.exe
-   Isuninst.exe
-   Lnkstub.exe
-   Mmc.exe
-   Mshta.exe
-   Msiexec.exe
-   Msoobe.exe
-   Rundll32.exe
-   Setup.exe
-   St5unst.exe
-   Unwise.exe
-   Unwise32.exe
-   Werfault.exe
-   Winhlp32.exe
-   Wlrmdr.exe
-   Wuapp.exe

上述的清單會儲存在下列登錄值中。

> [!Note]  
> 應用程式不應修改這些清單。 請使用本主題稍早所述的其中一個排除清單方法，以獲得相同的體驗。

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作列](taskbar.md)
</dt> <dt>

[工作列擴充功能](taskbar-extensions.md)
</dt> </dl>

 

 
