---
description: 註冊 MPEG2 編解碼器
ms.assetid: f730a7df-af8f-4dce-9bfe-6ee1eca8fd90
title: 註冊 MPEG2 編解碼器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6de007cebdd0a911f6b43f21003ed3ede0bc1723
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108924"
---
# <a name="registering-mpeg2-codecs"></a>註冊 MPEG2 編解碼器

本主題僅適用于 Windows XP Media Center Edition。

Windows XP Media Center Edition 會維護兩個登錄機碼，用來判斷要使用哪一個編解碼器來播放 MPEG2 影片和音訊檔案。 第一個登錄機碼會指定電腦製造商慣用的 MPEG2 編解碼器，而第二個登錄機碼會列出目前安裝在電腦上的所有 Media Center 相容編解碼器。 Media Center 必須播放 MPEG2 檔案時，會使用製造商慣用的編解碼器（如果有指定的話）。 如果沒有，則會使用登錄中列出的第一個 Media Center 相容編解碼器。 如果登錄未指定慣用或相容的編解碼器，Media Center 會使用標準的 DirectShow 篩選器來選擇編解碼器。

為了確保 Media Center 一律使用相容的 MPEG2 編解碼器，Media Center 電腦的製造商應該在下列登錄位置指定慣用的 MPEG2 編解碼器：


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Media Center\Service\Video
```



金鑰資料應該如下所示：


```C++
PreferredMPEG2VideoDecoder=REG_SZ "{MPEG2 Video CLSID GUID}"
PreferredMPEG2AudioDecoder=REG_SZ "{MPEG2 Audio CLSID GUID}"
```



Media Center 相容的 MPEG2 編解碼器安裝程式應藉由建立下列登錄機碼的兩個實例（一個用於視頻編碼器，另一個用於音訊編解碼器）來註冊編解碼器：


```C++
[HKEY_CLASSES_ROOT\CLSID\{083863F1-70DE-11d0-BD40-00A0C911CE86}\Instance\<Your Codec CLSID here>\Capabilities]
```



金鑰資料應該如下所示：


```C++
"{374ac4df-7c98-4257-b13d-36087dbee458}"=dword:00000001
```



 

 



