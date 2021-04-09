---
description: 將 TransformsSecure 原則設定為1，會通知安裝程式在使用者電腦上的本機電腦上，將轉換快取到使用者沒有寫入存取權的位置。
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: TransformsSecure 原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69180c797008f34755cfa415c7a76fb5f7721f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847683"
---
# <a name="transformssecure-policy"></a>TransformsSecure 原則

將 TransformsSecure 原則設定為1，會通知安裝程式在使用者電腦上的本機電腦上，將轉換快取到使用者沒有寫入存取權的位置。 設定此原則與設定 [TRANSFORMSSECURE 屬性](transformssecure.md) 相同，不同之處在于範圍不同。 設定 TransformsSecure 原則會套用至安裝至指定電腦的所有套件。 無論電腦為何，設定 TRANSFORMSSECURE 屬性都會套用至封裝。

此原則的目的是要為安全轉換儲存提供 Windows 2000 的旅遊使用者。 從 Windows Server 2003 開始，此原則的預設值為1。

設定此原則時， [維護安裝](maintenance-installation.md) 只能使用來自受保護快取的轉換。 當安裝程式發現本機電腦上缺少轉換時，安裝程式會嘗試還原轉換。 為了讓安裝程式還原轉換，安全轉換必須位於安裝套件來源清單中的授權來源。 如需詳細資訊，請參閱 [來源復原](source-resiliency.md)。 如果轉換無法使用或無法載入，維護安裝將會失敗。

在 Windows Server 2003 上，如果未設定此原則，預設行為是將轉換儲存在安全的位置。 在 Windows Server 2003 之前的所有版本上，如果未設定此原則，則預設行為是在使用者設定檔中儲存轉換。

如需詳細資訊，請參閱 [安全的轉換](secured-transforms.md) 。

Windows Installer 會將 [TransformsAtSource 原則](transformsatsource-policy.md) 解釋為與 TransformsSecure 原則相同的原則。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



