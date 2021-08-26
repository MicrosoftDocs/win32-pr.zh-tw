---
description: 此範例說明如何建立修補程式套件，以將小型更新套用至安裝範例中所討論的範例安裝套件。
ms.assetid: 17dadd64-6e81-444a-985e-1b340e4f2ee5
title: 小型更新修補範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0670693e9f5c6bf1c6b48c72e4b05b0f06703d69c08f46f6a2209b3d5046ea7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082968"
---
# <a name="a-small-update-patching-example"></a>小型更新修補範例

此範例說明如何建立 [修補程式套件](patch-packages.md) ，以將 [小型更新](small-updates.md) 套用至 [安裝範例](an-installation-example.md)中所討論的範例安裝套件。 小規模的更新會變更一個或多個應用程式檔，而這些應用程式檔會被判定為太小而無法保證變更產品代碼。 如需詳細資訊，請參閱 [修補和升級](patching-and-upgrades.md)。

此範例說明如何建立 Windows Installer 修補程式套件，以更新假設產品 MNP2000 的協同功能，以修正原始產品中的錯誤。 範例修補套件會將小型更新套用至不需要變更產品代碼的產品。 如需有關主要升級的詳細資訊，請參閱[修補和升級](patching-and-upgrades.md)一節中的[重大升級](major-upgrades.md)主題。

範例升級套件具有下列規格：

-   它會更正協同功能所顯示的協同排程中的次要錯誤。
-   它會更新套件程式碼，以反映安裝套件已變更。
-   您可以修補產品的本機安裝，以套用 small update。

[繼續](planning-a-small-update-patch.md)

 

 



