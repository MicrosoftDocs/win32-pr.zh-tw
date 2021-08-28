---
description: 如果每一電腦的系統原則設定為 1 (一) ，Windows Installer 不會與重新開機管理員互動，但它會使用 FilesInUse 對話方塊。如果每一電腦的系統原則設定為 2 (兩個) ，Windows Installer 會使用 FilesInUse 對話方塊。
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: DisableAutomaticApplicationShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6484d6a03568017e4778f9c21cb8818f9c651a40f5e8f9d4a4fc52a97c14522f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692758"
---
# <a name="disableautomaticapplicationshutdown"></a>DisableAutomaticApplicationShutdown

如果每一電腦的系統原則設定為 1 (一) ，Windows Installer 不會與[重新開機管理員](/windows/desktop/RstMgr/restart-manager-portal)互動，但是會使用[FilesInUse 對話方塊](filesinuse-dialog.md)。

如果每一電腦的系統原則設定為 2 (兩個) ，Windows Installer 會使用 [ [FilesInUse] 對話方塊](filesinuse-dialog.md)。 這項設定會在安裝未撰寫為使用重新開機管理員的 Windows Installer 套件時，停用[重新開機管理員](/windows/desktop/RstMgr/restart-manager-portal)可減輕重新開機的嘗試。 安裝程式仍會使用重新開機管理員來偵測應用程式所使用的檔案。

從 Windows Vista Windows Installer 4.0 版開始提供 DisableAutomaticApplicationShutdown 原則。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **安裝程式**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
</dt> <dt>

[Windows Installer 3.1 及更早版本不支援](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
