---
description: 本主題說明 Tablet PC library 二進位版本之間的差異。
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: 要參考的程式庫版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 899866dd11bbe72f9476ee3b645ed4e5612fe7043dae38675bd206e81562ca68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589278"
---
# <a name="which-library-version-to-reference"></a>要參考的程式庫版本

本主題說明 Tablet PC library 二進位版本之間的差異。

## <a name="tablet-pc-library-versions"></a>Tablet PC Library 版本

Tablet PC library 二進位檔 (Microsoft.Ink.dll) 已在 Windows Vista 中更新。 這些二進位檔稱為 "version 6.0"，可與發行 Windows 的版本共同 incide。

最新版本的二進位檔與 Windows XP 相容，稱為「版本1.7」。

Windows SDK 可以安裝在 Vista 和 XP 電腦上，而 Windows SDK 包含兩種 Microsoft.Ink.dll 版本。

這些都安裝在：

1. % programfiles% \\ 參考元件 \\ MICROSOFT \\ Tablet PC \\ 1.7 版 \\Microsoft.Ink.dll

2. % programfiles% \\ 參考元件 \\ MICROSOFT \\ Tablet PC \\ 6.0 6.0 \\Microsoft.Ink.dll

版本6.0 二進位檔只與 Windows vista 相容，因此針對它們撰寫的應用程式應該只在 Windows Vista 上執行。

在 Windows Vista 上安裝時，不需修改就能執行針對1.7 版二進位檔所撰寫的應用程式。

 

 



