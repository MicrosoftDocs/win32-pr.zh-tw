---
description: 兩個步驟的程式會將 Windows Installer 的交易模型延伸至包含 common language runtime 元件的產品。 這可讓安裝程式復原失敗的安裝和元件的移除。
ms.assetid: 065a380c-4eb5-48a5-ab0a-7f1229b77898
title: 全域組件快取中的元件回復
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1379d8132e4a0789108bae4b26fc02c492f5ccb9a0ec7699bba3d9d4de04d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625823"
---
# <a name="rollback-of-assemblies-in-the-global-assembly-cache"></a>全域組件快取中的元件回復

兩個步驟的程式會將 Windows Installer 的交易模型延伸至包含 common language runtime 元件的產品。 這可讓安裝程式復原失敗的安裝和元件的移除。

在第一個步驟中，Windows Installer 會使用 Microsoft .NET Framework 為每個元件建立一個介面。 Windows Installer 使用的介面數目，與安裝的元件數目一樣。 使用其中一個介面認可元件，只表示元件已準備好使用相同名稱取代任何現有的元件，但它並不會取代它。 如果使用者取消安裝，或發生嚴重的安裝錯誤，則 Windows Installer 可以藉由釋放這些介面，將元件回復為先前的狀態。

在 Windows Installer 完成安裝所有元件和 Windows Installer 元件之後，安裝程式可能會起始安裝的第二個步驟。 第二個步驟會使用個別的函式來執行所有新的 common language runtime 元件的最終認可。 這會取代具有相同名稱的任何現有元件。

 

 



