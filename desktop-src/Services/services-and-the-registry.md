---
description: 服務不應該存取 HKEY \_ CURRENT \_ USER 或 HKEY \_ 類別 \_ ROOT，尤其是在模擬使用者時。 請改用 RegOpenCurrentUser 或 RegOpenUserClassesRoot 函數。
ms.assetid: 8ad6c081-7ac0-4557-88dc-d8f1ec139926
title: 服務和登錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 669da912d5eb2a76981ff6e08293acccb1e313fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994507"
---
# <a name="services-and-the-registry"></a>服務和登錄

服務不應該存取 **HKEY \_ CURRENT \_ user** 或 **HKEY \_ 類別 \_ ROOT**，尤其是在模擬使用者時。 請改用 [**RegOpenCurrentUser**](/windows/desktop/api/winreg/nf-winreg-regopencurrentuser) 或 [**RegOpenUserClassesRoot**](/windows/desktop/api/winreg/nf-winreg-regopenuserclassesroot) 函數。

如果您嘗試從服務存取 **HKEY \_ CURRENT \_ USER** 或 **HKEY \_ 類別 \_ ROOT** ，它可能會失敗，或似乎運作正常，但有可能導致載入或卸載使用者設定檔時發生問題的根本洩漏。

 

 
