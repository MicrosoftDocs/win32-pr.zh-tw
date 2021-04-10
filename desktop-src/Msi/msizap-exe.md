---
description: Msizap.exe 是一種命令列公用程式，可移除產品的所有 Windows Installer 資訊，或電腦上安裝的所有產品。 使用 Msizap 之後，安裝程式所安裝的產品可能無法運作。
ms.assetid: 0debb8ab-3ae7-447e-84fc-0466ec1b2f26
title: Msizap.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a89f2287443bc442ee767b01e975d6bcc118c1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026560"
---
# <a name="msizapexe"></a>Msizap.exe

Msizap.exe 是一種命令列公用程式，可移除產品的所有 Windows Installer 資訊，或電腦上安裝的所有產品。 使用 Msizap 之後，安裝程式所安裝的產品可能無法運作。

在 Windows 2000 和 Windows XP 上，需要有系統管理許可權才能使用 Msizap.exe。

此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md) ，不應轉散發。 使用適用于 Windows Vista 或更新版本的 Windows Installer 開發人員 Windows SDK 元件中提供的 Msizap.exe (版本3.1.4000.2726 或更高版本) 。 較低版本的 Msizap.exe 可以移除已套用至使用者電腦上其他應用程式之所有更新的相關資訊。 如果移除此資訊，可能需要移除並重新安裝這些其他應用程式才能接收其他更新。

## <a name="syntax"></a>Syntax

**msizap T** _\[ WA！ \]{產品代碼}_

**msizap T** _\[ WA！ \] <msi package>_

**\* *** msizap \[WA！ \]***ALLPRODUCTS**

**msizap PWSA？！**

## <a name="command-line-options"></a>命令列選項

Msizap.exe 使用下表所示的不區分大小寫命令列選項。



| 選項 | Description                                                                                                                                                                                                                                                   |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*     | 移除所有 Windows Installer 資料夾和登錄機碼、調整共用的 DLL 計數，並停止 Windows Installer 服務。 也會移除 In-Progress 金鑰和復原資訊。                                                                           |
| a      | 只會針對任何指定的移除，將 Acl 變更為系統管理員的完全控制。                                                                                                                                                                                            |
| g      | 針對所有使用者，移除任何已孤立的快取 Windows Installer 資料檔案。                                                                                                                                                                       |
| p      | 移除 In-Progress 索引鍵。                                                                                                                                                                                                                                  |
| s      | 移除復原資訊。                                                                                                                                                                                                                                 |
| t      | 移除指定產品代碼的所有資訊。 使用這個選項時，請將產品代碼放在大括弧中。 此選項可搭配 .msi 檔案的完整路徑或產品代碼使用。                                        |
| w      | 移除所有使用者的 Windows Installer 資訊。 如果未設定此選項，則只會移除目前使用者的資訊。 使用這個選項需要載入使用者的設定檔，才能使用使用者的每個使用者登錄 hive。 |
| ?      | 詳細資訊說明。                                                                                                                                                                                                                                                 |
| !      | 強制對任何提示輸入「是」回應。                                                                                                                                                                                                                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



