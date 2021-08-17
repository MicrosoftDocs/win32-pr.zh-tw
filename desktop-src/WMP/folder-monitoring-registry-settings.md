---
title: 資料夾監控登錄設定
description: 資料夾監控登錄設定
ms.assetid: 563aeaec-0759-4b0c-a8e9-a9a2b3092515
keywords:
- Windows Media Player，資料夾監控登錄設定
- Windows Media Player，檔案資料夾監控登錄設定
- Windows Media Player，登錄
- 登錄，資料夾監控設定
- 登錄，檔案資料夾監控設定
- 登錄，Windows Media Player 的設定
- 資料夾監控登錄設定
- 檔案資料夾監控登錄設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac3e5e99c633c58a68b3579c55d38e6ad5b2415d9faac8d6c3438251c5a83459
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748439"
---
# <a name="folder-monitoring-registry-settings"></a>資料夾監控登錄設定

Windows Media Player 9 系列或更新版本可以監視新數位媒體檔案的檔案資料夾。 當播放玩家偵測到受監視資料夾中的新檔案時，它會自動將檔案新增至程式庫。 在 Windows Media Player 9 到 Windows Media Player 11 中，使用者可以在 [**選項**] 對話方塊的 [媒體櫃] 索引標籤上，按一下 [**監視資料夾**] 來變更受監視的資料夾清單。 針對 Windows Media Player 12，使用者可以依照主題[將專案新增至 Windows Media Player 程式庫](https://windows.microsoft.com/windows7/Add-items-to-the-Windows-Media-Player-Library)中的指示，來變更受監視資料夾的清單。 針對 Windows Media Player 9 到 Windows Media Player 11，您可以透過將值新增至登錄，以程式設計方式新增要監視的資料夾。 針對 Windows Media Player 12，您無法使用登錄，以程式設計方式新增或移除要監視的資料夾。

針對 Windows Media Player 9 到 Windows Media Player 11]，若要新增要監視的資料夾，您必須先在下列登錄機碼中建立或修改兩個值：

**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ 喜好設定\\**

新的值必須命名如下。



| 名稱                           | 類型           | 描述                                                                                                                                                                                                                                                                    |
|--------------------------------|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **TrackFoldersDirectories**    | **REG \_ DWORD** | **DWORD** 值，表示要監視的資料夾計數。 這必須符合 **TrackFoldersDirectories**_X_ 值的計數。                                                                                                                                         |
| **TrackFoldersDirectories**_X_ | **REG \_ SZ**    | 字串值，表示要監視的資料夾路徑。 要監視的每個資料夾都需要個別的值。 尾碼 *X* 是一個整數，應一律從0開始，然後以1遞增。 Windows Media Player 也會監視指定資料夾的子資料夾。 |



 

例如，若要新增第一個要監視的資料夾，請新增下列值：


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories0" = "c:\MyPath\MyFolder"

```



然後，建立計數值：


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000001

```



若要新增第二個要監視的資料夾，請新增下列值：


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories1" = "c:\MyPath\MyFolder2"

```



然後，將計數值遞增：


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Preferences]
"TrackFoldersDirectories" = dword:00000002

```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[**登錄設定**](registry-settings.md)
</dt> </dl>

 

 




