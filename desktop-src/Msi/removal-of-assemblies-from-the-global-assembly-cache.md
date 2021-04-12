---
description: Windows Installer 會根據用戶端清單，決定是否允許移除通用語言執行時間元件，它會獨立于元件之外。
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: 從全域組件快取移除元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192777"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a>從全域組件快取移除元件

Windows Installer 會根據用戶端清單，決定是否允許移除通用語言執行時間元件，它會獨立于元件之外。 Windows Installer 會保留一個 pin 位來代表元件 Windows Installer 的用戶端。 安裝程式會釘選第一個 Windows Installer 用戶端的元件，並在移除最後一個 Windows Installer 用戶端時取消固定它。 元件會為元件的每個用戶端維護一個 pin 位。

Windows Installer 不會直接負責從電腦實際移除 common language runtime 元件。 移除最後一個 Windows Installer 用戶端時，安裝程式會取消固定元件。 如果 Windows Installer 是元件的最後一個用戶端，則 common language runtime 會提供強制同步清除元件的選項。 清除程式是不可部分完成的，此時不會提供「復原」。 當使用者有機會取消安裝或移除時，所有的 common language runtime 元件解除釘選都必須執行。

 

 



