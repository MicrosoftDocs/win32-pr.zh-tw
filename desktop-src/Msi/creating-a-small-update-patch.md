---
description: 建立 Windows Installer small update 的修補程式時，請遵循下列指導方針。
ms.assetid: 0e57c2aa-e86a-4161-9749-c7963182a6d5
title: 建立小型更新修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d948c871baed7fbc15545ed9669c9864ce954799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999940"
---
# <a name="creating-a-small-update-patch"></a>建立小型更新修補程式

建立 [小型更新](small-updates.md)的修補程式時，作者應遵循下列指導方針：

-   小型更新修補程式必須針對單一的目標安裝設計。
-   小型更新修補程式應該使用最早的版本做為目標安裝。
-   小型更新修補程式應取代，並將任何先前的小型更新修補程式淘汰。

下列案例說明何時最適合小型更新修補程式。

您的公司發行了1.0 版的 Myproduct.msi。 不久之後，您就會針對名為 QFE1 的 Myproduct.msi 送出 [小型更新](small-updates.md) 修補程式。 這不會變更 [ [**ProductCode**](productcode.md) ] 屬性或 [**ProductVersion**](productversion.md) 屬性。

稍後，您會撰寫 Myproduct.msi 的第二個 [小型更新](small-updates.md) 修補程式，稱為 QFE2。 第二個修補程式必須以 Myproduct.msi 版本1.0 為目標。 第二個修補程式不得以 Myproduct.msi 1.0 版和 Myproduct.msi 1.0 + QFE1 版本為目標。 套用 QFE2 時，應移除 QFE1。

 

 



