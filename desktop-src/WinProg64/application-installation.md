---
title: 64位系統上的應用程式安裝
description: 64位 Windows Installer 可以在64位 Windows 上順暢地安裝32位的 MSI 應用程式。
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- 應用程式安裝 64-位 Windows 程式設計
- 安裝64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26f06eaa527142145791e4ed29e2420d16b1d7a2f4fbe9a77801857a844ed7b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643598"
---
# <a name="application-installation-on-64-bit-systems"></a>64位系統上的應用程式安裝

[64 位 Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems)可以在64位 Windows 上順暢地安裝32位的 MSI 應用程式。 針對使用16位存根來啟動32位安裝引擎的繼承應用程式，64位 Windows 可辨識特定的16位安裝程式，並替代已移植的32位版本。

16位 DOS、Windows 或 OS/2 應用程式通常會使用16位的存根來檢查電腦類型，然後啟動32位安裝引擎以實際執行安裝。 若要啟用使用這項技術的應用程式安裝，64位 Windows 取代下列16位安裝程式的32位版本：

* 適用于 Windows 1.2 的 Microsoft 安裝程式  
* 適用于 Windows 2.6 的 Microsoft 安裝程式  
* 適用于 Windows 3.0 的 Microsoft 安裝程式  
* 適用于 Windows 3.01 的 Microsoft 安裝程式  
* InstallShield 5。x  

替代清單儲存在登錄中的下列機碼底下： **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ NtVdm64**。

> [!Note]  
> 這項機制只是為了與使用本主題中所列之16位 Microsoft 安裝程式的32位應用程式相容。 不支援新增協力廠商安裝程式。

 

> [!Note]  
> ARM 上的 Windows 10 不包含這項機制。

 

 

 