---
description: 您可以使用 InkPicture 控制項，在 Microsoft Windows 2000、Windows Server 2003 和非 Tablet PC 版本的 Windows XP 上呈現筆墨。 不過，您無法使用控制項在這些作業系統上輸入筆墨。
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: 在舊版 Windows 上使用 InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbd2bf8545524787c9e37f70c43d954ab440910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973255"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a>在舊版 Windows 上使用 InkPicture

您可以使用 [InkPicture 控制項](inkpicture-control.md) ，在 Microsoft windows 2000、windows Server 2003 和非 Tablet PC 版本的 windows XP 上呈現筆墨。 不過，您無法使用控制項在這些作業系統上輸入筆墨。

控制項的 [**InkEnabled**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) 屬性設定為 **FALSE**，而且嘗試變更屬性沒有任何作用。 您可以將值指派給其他屬性，並以程式設計方式操作筆墨，但是您無法使用控制項來收集筆跡。

 

 



