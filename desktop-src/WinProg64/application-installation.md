---
title: 64位系統上的應用程式安裝
description: 64位的 Windows Installer 可以在64位的 Windows 上順暢地安裝32位的 MSI 應用程式。
ms.assetid: fb9c5720-9906-4827-9daf-d7caa453e818
keywords:
- 應用程式安裝 64-位 Windows 程式設計
- 安裝64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13a5f8f623776ffa637718fc0d565f2c71a7b8e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092864"
---
# <a name="application-installation-on-64-bit-systems"></a>64位系統上的應用程式安裝

64位的 [Windows Installer](/windows/desktop/Msi/windows-installer-on-64-bit-operating-systems) 可以在64位的 Windows 上順暢地安裝32位的 MSI 應用程式。 針對使用16位存根來啟動32位安裝引擎的繼承應用程式，64位 Windows 會辨識特定的16位安裝程式，並替代已移植的32位版本。

16位 DOS、Windows 或 OS/2 應用程式通常會使用16位的存根來檢查電腦類型，然後啟動32位安裝引擎以實際執行安裝。 為了讓您能夠安裝使用這項技術的應用程式，64位的 Windows 會將32位版本取代為下列16位安裝程式：

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

 

 

 