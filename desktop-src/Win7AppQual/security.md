---
description: .
ms.assetid: 87331C1D-F468-4CA4-92BD-D4E5D4E930BC
title: Windows 7 和 Windows Server 2008 R2 應用程式品質逐步指南) 的安全性 (
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bbaaa6b34463e04f5870082e5c693462f4e19fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195570"
---
# <a name="security-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Windows 7 和 Windows Server 2008 R2 應用程式品質逐步指南) 的安全性 (

從 Windows Internet Explorer 7 開始，當使用者在 Windows Vista 作業系統或更新版本上執行時，Windows Internet Explorer 就會在稱為 *受保護模式* 的安全性內容中執行。 這種模式會以比標準使用者應用程式低的許可權設定來執行 Internet Explorer，因此某些功能會受到限制，尤其是 ActiveX 控制項和特定類型的外掛程式。如需 Internet Explorer 中受保護模式的詳細資訊及其對相容性的影響，請參閱 MSDN Library 中的 [瞭解和使用受保護模式 Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/) 。

Windows Internet Explorer 8 預設也會啟用資料執行防止 (DEP) ，以協助應用程式避免在線上攻擊中執行任意程式碼。 不過，某些附加元件可能不會使用這項安全性功能 (例如，任何未設計為只執行記憶體中已明確標示為可執行檔的程式碼的附加元件，例如使用舊版 ActiveX 範本程式庫所建立的應用程式， (ATL) framework) 。

Internet Explorer 8 也可保護使用者免于使用腳本的潛在安全性漏洞。 例如，除非透過明確的使用者互動，否則您無法從較不受信任區域中的 URL 流覽至更受信任區域中的 URL。 您也無法隱藏瀏覽器使用者介面的特定元素 (例如，在不受信任的 (網際網路) 區域中的 [網址列]) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設計影響瀏覽器相容性的更新](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 
