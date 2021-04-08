---
description: 在64位作業系統上，Windows Installer 可能會呼叫已針對32位或64位系統編譯的自訂動作。
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: 64位自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fcd804152abd010f985aab3b92c0de73a2744f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692815"
---
# <a name="64-bit-custom-actions"></a>64位自訂動作

在64位作業系統上，Windows Installer 可能會呼叫已針對32位或64位系統編譯的自訂動作。

以 [腳本](scripts.md)為基礎的64位自訂動作必須明確標記為64位自訂動作，方法是在 [CustomAction 資料表](customaction-table.md)的類型資料行中，將 **msidbCustomActionType64BitScript** 位新增至自訂動作數數值型別。



| 常數                             | 十六進位 | Decimal | 意義                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| **msidbCustomActionType64BitScript** | 0x0001000   | 4096    | 這是以 [腳本](scripts.md)撰寫的64位自訂動作。 |



 

以 [可執行檔](executable-files.md) 為基礎的自訂動作或針對64位作業系統所遵守的 [動態連結程式庫](dynamic-link-libraries.md) ，不需要在 CustomAction 資料表的 Type 資料行中包含這個額外的位。

 

 



