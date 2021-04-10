---
description: 所有安全物件都會使用下圖所示的存取遮罩格式來排列其存取權限。
ms.assetid: c7b97cd8-66b6-42dc-b75b-2c0adb87d020
title: 存取遮罩格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2f6c66c99ed93dca399825621dfbd0cc01c2ec6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849888"
---
# <a name="access-mask-format"></a>存取遮罩格式

所有安全物件都會使用下圖所示的 [*存取遮罩*](/windows/desktop/SecGloss/a-gly) 格式來排列其存取權限。

![存取遮罩格式](images/accctrl4.png)

以這種格式來說，低序位16位適用于特定物件的存取權限，下8個位適用于 [標準存取權限](standard-access-rights.md)，適用于大部分的物件類型，而4個高序位位可用來指定 [泛型存取權限](generic-access-rights.md) ，每個物件類型都可對應至一組標準和物件特定的許可權。 存取 \_ 系統 \_ 安全位會對應至 [存取物件之 SACL](sacl-access-right.md)的許可權。

 

 
