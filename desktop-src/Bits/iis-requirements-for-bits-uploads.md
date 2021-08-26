---
title: BITS 上傳的 IIS 需求
description: 針對上傳，BITS 需要 Windows Server 2003 上的 iis 6.0，以及 Windows Server 2008 上的 iis 7.0;BITS 不支援 Windows XP 上的 IIS 5.1。
ms.assetid: 8ab07af5-3b59-4c98-8e57-f614deb8b594
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb09ec8c55cce592baf48b4b39faf031e5d6c98909927c0e597be6aaae8712e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004988"
---
# <a name="iis-requirements-for-bits-uploads"></a>BITS 上傳的 IIS 需求

針對上傳，BITS 需要 Windows Server 2003 上的 iis 6.0，以及 Windows Server 2008 上的 iis 7.0;BITS 不支援 Windows XP 上的 IIS 5.1。 您必須啟用 IIS 虛擬目錄的上傳功能，並設定 IIS 延伸模組的 BITS。

**Windows Server 的核心安裝：** 不支援 BITS IIS 延伸模組。

在 Windows Server 2008 上，使用 **伺服器管理員** 安裝 BITS 伺服器擴充功能。 在 **伺服器管理員** 中，按一下左窗格中的 [ **功能** ]。 在 [ **新增功能] 嚮導** 中，檢查 [BITS 伺服器擴充功能]。 請注意，必須安裝 IIS 6 管理相容性角色。

在 Windows Server 2003 上，請使用 **Windows 元件嚮導** 來安裝 BITS 伺服器擴充功能。 從 **主控台** 中，選取 [ **新增或移除程式**]。 然後，選取 [**新增/移除 Windows 元件**]，以顯示 [ **Windows 元件] Wizard**。 BITS 伺服器延伸是 Internet Information Services (IIS) 的子元件，這是 Web 應用程式伺服器的子元件。

> [!Note]  
> 如果重新開機 IISAdmin 服務，則必須先回收 IIS 背景工作進程，BITS 服務才能繼續上傳。 您可以使用 **IISReset.exe** 命令列公用程式，以手動方式回收 IIS 工作者進程。

 

如需有關為上傳設定 IIS 的詳細資訊，請參閱 [設定伺服器以進行上傳](setting-up-the-server-for-uploads.md)。

如需 bits 新增至 IIS 之屬性的詳細資訊，請參閱[Upload 作業的 bits 伺服器設定](bits-server-settings-for-upload-jobs.md)。

 

 




