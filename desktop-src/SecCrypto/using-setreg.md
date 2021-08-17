---
description: SetReg 工具會設定登錄機碼的值，以控制 Authenticode 憑證驗證程式的行為。
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: 使用 SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0de37d236b978217d8c2a713e9595fbaad70afb69beb32cd0f5200738d2d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896735"
---
# <a name="using-setreg"></a>使用 SetReg

SetReg 工具會設定登錄機碼的值，以控制 Authenticode 憑證驗證程式的行為。 這些金鑰稱為軟體發佈狀態金鑰，可控制是否要信任測試根目錄、允許離線核准憑證、測試憑證到期日，以及執行撤銷檢查。

下列命令會列出使用 SetReg 的語法和選項。

**setreg-？**

下列命令會將測試根目錄信任。 根據預設，測試根目錄不受信任。 在索引鍵值的任何變更之後，就會顯示所有索引鍵值的目前值清單。 如果使用 **-q** 選項，則不會顯示金鑰值。

**setreg 1 TRUE**

下列命令會讓測試根目錄不受信任，並導致所有驗證檢查撤銷。 使用 **-q** 選項，因此不會顯示金鑰值清單

**setreg-q 1 FALSE 3 TRUE**

> [!Note]  
> 命令、選項和引數不區分大小寫。

 

 

 



